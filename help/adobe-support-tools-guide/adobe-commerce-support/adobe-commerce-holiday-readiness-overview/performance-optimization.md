---
title: Ottimizzazione delle prestazioni
description: Raccomandazioni sull’ottimizzazione delle prestazioni per aiutare i commercianti di Adobe Commerce a preparare i loro ambienti per eventi a traffico elevato, ad esempio le feste.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: b2220ea4cb5a301cbee6cea5fb90d6dc8a05eeff
workflow-type: tm+mt
source-wordcount: '1698'
ht-degree: 0%
---

# Ottimizzazione delle prestazioni

Questa sezione fornisce consigli tecnici per preparare gli ambienti Adobe Commerce, sia Commerce su infrastrutture cloud che on-premise, per eventi a traffico elevato come le feste.

>[!NOTE]
>
>I passaggi contrassegnati come **(solo cloud)** si applicano a Commerce sull&#39;infrastruttura cloud. La maggior parte delle altre raccomandazioni si applica anche alle distribuzioni locali.

## Ottimizzare il caching rapido delle richieste (solo cloud) {#optimize-fastly-request-caching}

[!DNL Fastly] memorizza nella cache le risposte al server perimetrale per ridurre il carico sul server di origine. Durante la stagione di picco, alcuni controlli di configurazione ti aiutano a ottenere il massimo da quella cache, soprattutto quando esegui promozioni con parametri di tracciamento o una vetrina headless. Per il riferimento completo alla configurazione, vedere [Personalizzare la configurazione della cache](https://experienceleague.adobe.com/it/docs/commerce-on-cloud/user-guide/cdn/setup-fastly/fastly-custom-cache-configuration).

* Normalize tracking parameters: durante le feste, è probabile che tu esegua campagne social e a pagamento, come Google Ads, Facebook e X, che aggiungono stringhe di tracciamento univoche a ogni URL. Ogni stringa univoca crea una voce cache separata per quella che altrimenti sarebbe la stessa pagina, riducendo il rapporto di hit della cache. Aggiungi questi parametri all&#39;elenco **[!UICONTROL Parametri URL ignorati]** nella configurazione [!DNL Fastly] in Adobe Commerce Admin in modo che [!DNL Fastly] li consideri equivalenti.
* Conferma che le pagine di destinazione siano memorizzabili in cache: controlla l&#39;intestazione di risposta `x-cache` su ogni pagina di destinazione della promozione. Una pagina memorizzabile in cache restituisce `HIT` o una coppia `HIT`/`MISS` nei caricamenti successivi. Se l&#39;intestazione restituisce `MISS, MISS`, la pagina non viene memorizzata in cache e richiede un&#39;analisi.
* Utilizzare le richieste GET per le query GraphQL: se si esegue una vetrina PWA o headless, inviare le query GraphQL come `GET` richieste con la query inclusa nell&#39;URL, anziché come `POST` richieste. [!DNL Fastly] memorizza nella cache solo `GET` richieste in cui la query fa parte dell&#39;URL. Una richiesta `GET` con la query inviata nel corpo non è memorizzata nella cache.

>[!NOTE]
>
>La schermatura dell&#39;origine [!DNL Fastly] influisce anche sulle prestazioni della cache. Per informazioni sulla configurazione, vedere [Schermatura origine rapida](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md#fastly-origin-shielding).

## Abilita I/O veloce (solo cloud) {#enable-fastly-io}

L&#39;I/O [!DNL Fastly] esegue l&#39;offload del ridimensionamento delle immagini e della conversione del formato nella rete Edge [!DNL Fastly] anziché nell&#39;origine Adobe Commerce. Questo riduce il carico del server e migliora la velocità di rendering delle pagine per i vetrine con un numero elevato di immagini, un collo di bottiglia comune durante i periodi di vendita con traffico elevato. Per le opzioni di configurazione, vedi [Ottimizzazione immagine rapida](https://experienceleague.adobe.com/it/docs/commerce-on-cloud/user-guide/cdn/fastly-image-optimization).

Prima di iniziare, verifica che la schermatura dell’origine sia configurata. [!DNL Fastly] IO richiede come prerequisito la protezione dell&#39;origine. Per informazioni sulla configurazione, vedere [Schermatura origine rapida](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md#fastly-origin-shielding).

Per abilitare [!DNL Fastly] I/O:

1. Nell&#39;amministratore, passare alla pagina **[!UICONTROL Configurazione rapida]** e selezionare **[!UICONTROL Configura]** accanto a **[!UICONTROL Opzioni di configurazione I/O predefinite]**.
1. Verificare che lo snippet di I/O [!DNL Fastly] sia abilitato.
1. Nella configurazione di **[!UICONTROL Ottimizzazione immagine]**, impostare **[!UICONTROL Abilita ottimizzazione immagine approfondita]** su *[!UICONTROL Sì]*. Questa impostazione disabilita il ridimensionamento dell&#39;immagine incorporato di Adobe Commerce e trasferisce l&#39;attività a [!DNL Fastly].
1. Verificare che la posizione dello schermo sia impostata correttamente. Per informazioni sulla configurazione, vedere [Schermatura origine rapida](#fastly-origin-shielding).

>[!NOTE]
>
>L&#39;ottimizzazione deep image (immagini profonde) ridimensiona solo le immagini del prodotto. Le immagini CMS, come banner e blocchi di contenuto, non vengono influenzate e continuano a utilizzare il ridimensionamento integrato di Adobe Commerce.

Per verificare che l&#39;I/O [!DNL Fastly] funzioni, controllare le intestazioni di risposta in una richiesta di immagine del prodotto:

* L&#39;intestazione `x-cache` restituisce `HIT`.
* Le intestazioni `fastly-io-info` e `fastly-stats` sono compilate.
* L&#39;URL immagine non include una directory `/cache/` nel percorso.

## Implementazione della cache L2 Redis {#implement-redis-l2-cache}

Implementa procedure di caching efficaci in modo che il tuo archivio funzioni in modo affidabile durante le stagioni di traffico di picco. [!DNL Redis] La cache L2 riduce la larghezza di banda di rete a [!DNL Redis] memorizzando i dati della cache in locale su ogni nodo Web. Per informazioni generali sul funzionamento della cache L2, vedere [Cache di livello 2](https://experienceleague.adobe.com/it/docs/commerce-operations/configuration-guide/cache/level-two-cache).

In Commerce sull&#39;infrastruttura cloud, abilitarlo impostando la variabile di distribuzione `REDIS_BACKEND`. Per i passaggi di configurazione, consulta [REDIS_BACKEND](https://experienceleague.adobe.com/it/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#redis_backend) nella Guida all&#39;infrastruttura cloud di Commerce. In locale, configurarlo direttamente in `app/etc/env.php`.

>[!NOTE]
>
>[!DNL Redis] non è supportato come back-end della cache L2 in Adobe Commerce 2.4.9 o versione successiva oppure in versioni patch successive a 2.4.5-p16, 2.4.6-p14, 2.4.7-p9 o 2.4.8-p4. In queste versioni utilizzare `VALKEY_BACKEND`.

## Abilita connessioni slave MySQL e Redis (solo cloud) {#enable-mysql-and-redis-slave-connections}

[!DNL Redis] e [!DNL MySQL] connessioni slave scaricano il traffico di lettura sui nodi di replica, riducendo il carico sulla connessione master durante i periodi di traffico elevato. Per i passaggi di configurazione, vedi [MYSQL_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/it/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#mysql_use_slave_connection) e [REDIS_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/it/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#redis_use_slave_connection) o [VALKEY_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/it/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#valkey_use_slave_connection), a seconda della versione di Adobe Commerce in uso.

### Connessioni slave Redis

Una connessione slave [!DNL Redis] è una connessione di sola lettura a un&#39;istanza [!DNL Redis], che consente di gestire il traffico di lettura da un nodo non principale. Senza l&#39;abilitazione di [!DNL MySQL], potrebbe verificarsi un collo di bottiglia con carico elevato. Controllare il grafico Panoramica APM di [!DNL New Relic] per verificare l&#39;aumento dei tempi di risposta come segno di inizio, quindi confermare nella scheda **[!UICONTROL Database]** ordinando in base alla transazione più dispendiosa in termini di tempo per identificare le query [!DNL MySQL] `SELECT` lente. Abilitare questa operazione impostando la variabile di distribuzione `REDIS_USE_SLAVE_CONNECTION` su `true`.

>[!NOTE]
>
>`REDIS_USE_SLAVE_CONNECTION` è supportato solo negli ambienti cluster di Staging e Production Pro. Non è supportato nei progetti con architettura Starter o Scaled (split). L&#39;abilitazione di questa proprietà nell&#39;architettura scalata causa [!DNL Redis] errori di connessione. Utilizzare la cache L2 di [!DNL Redis] invece di tale architettura. Vedi [Implementare la cache L2 Redis](#implement-redis-l2-cache-implement-redis-l2-cache) sopra.

### Connessioni slave MySQL

Abilitare il flag `MYSQL_USE_SLAVE_CONNECTION` negli ambienti cluster Pro per indirizzare specifiche query di database di sola lettura a una connessione slave, scaricando l&#39;esecuzione delle query dalla connessione master.

>[!CAUTION]
>
>Prova di carico prima di abilitare entrambe le impostazioni in produzione. Negli ambienti con carico normale, le connessioni slave possono rallentare le prestazioni del 10-15%. In ambienti con un carico pesante e prolungato, possono migliorare le prestazioni con un margine simile. Valuta in base al traffico previsto nella stagione di picco prima di abilitare.

## Abilitare l’elaborazione asincrona di e-mail e ordini {#enable-asynchronous-order-and-email-processing}

Utilizza l’elaborazione asincrona per mettere in coda ed eseguire in background operazioni correlate a ordini di volumi elevati, riducendo la latenza front-end durante il traffico di picco. In questo modo vengono illustrate tre impostazioni correlate ma distinte. Per una panoramica, vedere [Best practice di configurazione](https://experienceleague.adobe.com/it/docs/commerce-operations/performance-best-practices/configuration).

* Posizionamento asincrono dell’ordine: il modulo Ordine asincrono contrassegna un ordine come ricevuto, lo inserisce in una coda ed elabora gli ordini al primo ingresso. Per impostazione predefinita, è disabilitata. Abilitalo dalla riga di comando:

  ```
  bin/magento setup:config:set --checkout-async 1
  ```

  Una volta abilitati, i dettagli dell&#39;ordine non sono immediatamente disponibili. L&#39;ordine rimane in coda fino a quando il consumatore `placeOrderProcess` non lo verifica in base al magazzino (abilitato per impostazione predefinita) e lo aggiorna. Prima di disabilitare questo modulo, verifica che l’elaborazione di tutti gli ordini asincroni in-flight sia stata completata. Per informazioni dettagliate, vedere [Best practice per le prestazioni di estrazione](https://experienceleague.adobe.com/it/docs/commerce-operations/performance-best-practices/high-throughput-order-processing).

* Elaborazione asincrona dei dati dell&#39;ordine: le vendite in vetrina e l&#39;elaborazione intensiva degli ordini possono creare conflitti a livello di database. Abilitando questa impostazione si distinguono i due pattern di traffico, in modo che gli ordini vengano inseriti in un archivio temporaneo e spostati in blocco nella griglia di Order Management senza conflitti. Questo programma viene aggiornato, in base alla cron, alle griglie Ordini, Fatture, Spedizioni e Note di credito, evitando blocchi e riducendo i tempi di elaborazione. Per ottenere risultati ottimali, configura cron in modo che venga eseguito una volta al minuto.

  >[!NOTE]
  > 
  >La modalità di attivazione dipende dalla modalità di distribuzione. Adobe Commerce sugli ambienti di staging e produzione dell’infrastruttura cloud viene eseguito in modalità di produzione per impostazione predefinita, dove questa impostazione non è disponibile tramite l’amministratore. In modalità di produzione, eseguire `bin/magento config:set dev/grid/async_indexing 1`. In modalità predefinita, vai a **[!UICONTROL Archivi]** > **[!UICONTROL Configurazione]** > **[!UICONTROL Avanzate]** > **[!UICONTROL Sviluppatore]** > **[!UICONTROL Impostazioni griglia]** e imposta **[!UICONTROL Indicizzazione asincrona]** su *[!UICONTROL Abilita]*.

  Per ulteriori dettagli, vedere [Operazioni ordini pianificate](https://experienceleague.adobe.com/it/docs/commerce-admin/stores-sales/order-management/orders/order-scheduled-operations).

* Notifiche e-mail asincrone: questa impostazione sposta in background le notifiche e-mail di pagamento e di elaborazione dell’ordine. Abilitala presso **[!UICONTROL Archivi]** > **[!UICONTROL Configurazione]** > **[!UICONTROL Vendite]** > **[!UICONTROL E-mail vendite]** > **[!UICONTROL Impostazioni generali]** > **[!UICONTROL Invio asincrono]**.

## Configura gli indicizzatori per l&#39;aggiornamento in base alla pianificazione {#configure-indexers-for-update-on-schedule}

Imposta gli indicizzatori in modo che vengano eseguiti in modalità pianificata per evitare il blocco del database e migliorare la reattività durante i frequenti aggiornamenti del catalogo. Per informazioni dettagliate, vedere [Best practice per la configurazione dell&#39;indicizzatore](https://experienceleague.adobe.com/it/docs/commerce-operations/implementation-playbook/best-practices/maintenance/indexer-configuration).

Un indicizzatore può essere eseguito in modalità **[!UICONTROL Aggiorna al salvataggio]** o **[!UICONTROL Aggiorna alla pianificazione]**.

* **[!UICONTROL Aggiorna al salvataggio]** indici immediatamente ogni volta che il catalogo o altri dati cambiano. Si presuppone un aggiornamento ridotto e un&#39;intensità di navigazione ridotta, e può causare ritardi significativi e la mancata disponibilità dei dati con un carico elevato.
* **[!UICONTROL È consigliabile eseguire l&#39;aggiornamento in base alla pianificazione]** per la produzione. Memorizza informazioni sugli aggiornamenti dei dati e sulle reindicizzazioni in background tramite un processo cron dedicato.

Imposta in modo indipendente la modalità di aggiornamento di ogni indicizzatore in **[!UICONTROL Sistema]** > **[!UICONTROL Strumenti]** > **[!UICONTROL Gestione indice]**.

>[!IMPORTANT]
>
>Le modalità supportate dell&#39;indicizzatore `customer_grid` dipendono dalla versione di Adobe Commerce. Nelle versioni precedenti alla 2.4.8, Customer Grid supporta **[!UICONTROL Update on Save]** only—non impostarlo su **[!UICONTROL Update on Schedule]**. In Adobe Commerce 2.4.8 e versioni successive, Customer Grid supporta entrambe le modalità e ora utilizza come impostazione predefinita **[!UICONTROL Aggiorna secondo pianificazione]**.

## Disattiva e valuta la tabella a pagina singola del catalogo {#disable-and-evaluate-catalog-flat-table}

Non è raccomandato l’uso di tabelle piatte per prodotti e categorie. Questa funzione obsoleta può causare il deterioramento delle prestazioni e problemi di indicizzazione. Per ulteriori dettagli, vedere [Cataloghi flat](https://experienceleague.adobe.com/it/docs/commerce-admin/catalog/catalog/catalog-flat).

Per disabilitare il catalogo flat, vai a **[!UICONTROL Archivi]** > **[!UICONTROL Configurazione]** > **[!UICONTROL Catalogo]** > **[!UICONTROL Catalogo]** > **[!UICONTROL Storefront]**, imposta **[!UICONTROL Usa categoria catalogo flat]** su *[!UICONTROL No]*, imposta **[!UICONTROL Usa prodotto catalogo flat]** su *[!UICONTROL No]*, quindi fai clic su **[!UICONTROL Salva configurazione]**.

Alcuni moduli e personalizzazioni di terze parti richiedono il corretto funzionamento delle tabelle semplici. Valuta l’impatto e il rischio di continuare a utilizzare tali estensioni prima di disabilitare le tabelle flat.

## Considera l’architettura ridimensionata (divisa) (solo cloud) {#consider-scaled-split-architecture}

Se, dopo aver applicato la configurazione precedente e le ottimizzazioni a livello di codice, i test di carico o le prestazioni dell’infrastruttura live mostrano ancora un CPU e altre risorse raggiunte il limite massimo, puoi passare a un’architettura scalata (divisa). Per ulteriori dettagli, vedere [Architettura ridimensionata](https://experienceleague.adobe.com/it/docs/commerce-on-cloud/user-guide/architecture/scaled-architecture).

>[!NOTE]
>
>L&#39;architettura scalata è disponibile solo per gli account con un cluster Pro 48 o superiore.

L&#39;architettura di split-tier utilizza almeno sei nodi: tre nodi di servizio che eseguono [!DNL OpenSearch] o [!DNL Elasticsearch], [!DNL MariaDB] e [!DNL Redis] o [!DNL Valkey] e tre nodi web che eseguono `php-fpm` e `NGINX`.

* I nodi di servizio possono essere scalati solo verticalmente, aumentando le dimensioni del server (CPU e memoria). Poiché il cluster di database è stato creato per garantire un&#39;elevata disponibilità, i nodi di servizio non possono scalare orizzontalmente in modo affidabile.
* I nodi web possono essere scalati sia verticalmente che orizzontalmente, aggiungendo server web per gestire un aumento del volume di richieste.

Questo consente di espandere l&#39;infrastruttura su richiesta per periodi di carico elevato, scalando ogni livello in modo indipendente. Per passare all’architettura a più livelli in anticipo rispetto a un periodo di carico pesante previsto, contatta il team del tuo account Adobe.
