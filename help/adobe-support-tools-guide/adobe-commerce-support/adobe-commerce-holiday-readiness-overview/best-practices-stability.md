---
title: Best practice e stabilità
description: Best practice e raccomandazioni sulla stabilità per aiutare i commercianti di Adobe Commerce a preparare i loro ambienti per eventi a traffico elevato, come le feste.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
TQID: 'https://experienceleague.adobe.com/iA6ioGYYgQSotPrPqujDBdRcjBLUQXMGXfwlcSMGjkM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: 3c398179-d35a-51ba-b317-6c5b95feef5e
    internal-label: Logs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 71589dd124714805fbf844540fb2d272433631ee
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 4%
---

# Best practice e stabilità

Questa sezione fornisce consigli tecnici per preparare gli ambienti Adobe Commerce, sia Commerce su infrastrutture cloud che on-premise, per eventi a traffico elevato come le feste.

>[!NOTE]
>
>I passaggi contrassegnati come **(solo cloud)** si applicano a Commerce sull&#39;infrastruttura cloud. La maggior parte delle altre raccomandazioni si applica anche alle distribuzioni locali.

## Aggiornamento alla versione più recente di Adobe Commerce {#upgrade-to-latest-version-of-adobe-commerce}

Assicurati che il tuo sito non utilizzi una versione non supportata di Adobe Commerce, il che potrebbe influire sulle prestazioni del sito e aumentarne la vulnerabilità ai problemi di sicurezza. Effettua l’aggiornamento all’ultima versione di Adobe Commerce per sicurezza e preparazione per le feste.

La [versione più recente](https://experienceleague.adobe.com/it/docs/commerce-operations/release/notes/overview) di Adobe Commerce include molte [correzioni di sicurezza importanti](https://experienceleague.adobe.com/en/docs/commerce-operations/release/notes/security-patches/overview), inclusi miglioramenti e problemi attenuati, che apporteranno vantaggi al progetto quando si esegue l&#39;aggiornamento da una versione precedente.

Per ulteriori informazioni sulle versioni non supportate di Adobe Commerce, consultare [Adobe Commerce Life Cycle Policy](https://experienceleague.adobe.com/it/docs/commerce-operations/release/planning/lifecycle-policy).

## Installare gli strumenti ECE più recenti e QPT (Quality Patch Tool) {#install-latest-ece-tools-and-quality-patch-tool-qpt}

Verificare che il modulo `ece-tools` più recente e i relativi moduli dipendenti siano installati utilizzando lo switch `--with-dependencies`, in modo che tutte le patch cloud richieste siano installate correttamente per la versione di Adobe Commerce in uso. Per i passaggi, vedere [Aggiornare il pacchetto ECE-Tools](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/dev-tools/ece-tools/update-package).

Esaminate l&#39;elenco di patch disponibile nello strumento Patch di qualità e verificate che siano state applicate le patch delle prestazioni compatibili con la versione di Adobe Commerce in uso. Vedere [Strumento Patch di qualità: Ricerca di patch](https://experienceleague.adobe.com/it/docs/commerce-operations/tools/quality-patches-tool/patches-available-in-qpt/patches-available-in-qpt-tool-overview).

>[!NOTE]
>
>QPT è disponibile sia per l’infrastruttura cloud di Adobe Commerce che per le installazioni on-premise. I comandi di installazione e utilizzo differiscono tra i due: per Cloud, QPT è incluso nel pacchetto ECE-Tools.

## Revisione e pulizia dei file di registro {#review-and-clean-log-files}

Esaminare i file di log nell&#39;ambiente cloud (ad esempio, i file di log dell&#39;applicazione in `~/var/log`) e identificare eventuali record registrati di frequente scritti nei file di log predefiniti o personalizzati. Per ulteriori dettagli, vedere [Visualizzare e gestire i registri](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/test/log-locations).

* Esaminare i seguenti file di log predefiniti e correggere gli errori ricorrenti: `~/var/log`, `~/var/log/exception.log`, `~/var/log/support_report.log`, `~/var/log/system.log`, `~/var/report`.
* Rimuovi i registri di debug precedentemente aggiunti per la risoluzione dei problemi passati.

Questi registri sono disponibili anche in [!DNL New Relic]. Vedere [Gestione dei registri di New Relic](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/monitor/new-relic/log-management).

## Monitorare l&#39;aumento delle dimensioni del disco {#monitor-disk-size-growth}

La tua infrastruttura Adobe Commerce su cloud dispone di due volumi di dischi principali. Monitorare questi volumi per assicurarsi che dispongano di spazio libero sufficiente in caso di traffico intenso. Adobe Commerce fornisce un avviso quando uno dei volumi raggiunge un utilizzo superiore al 70%.

* `/mnt/shared` (file condivisi, inclusi log e file multimediali)
* `/data/mysql` (volume database)

Per ulteriori dettagli, vedere [Gestire lo spazio su disco](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/storage/manage-disk-space).

## Rivedere le richieste di database più lente {#review-slowest-database-requests}

È importante monitorare ed esaminare regolarmente le transazioni di database più dispendiose in termini di tempo in [!DNL New Relic]. Analizza query e componenti notevolmente lenti.

* **Controlla le transazioni che richiedono più tempo:** Vai a **[!UICONTROL New Relic]** > **[!UICONTROL APM &amp; Services]** > seleziona l&#39;ambiente > **[!UICONTROL Database]**, quindi ordina in base alle transazioni che richiedono più tempo.

* **Controllare il log delle query lente di MySQL:** Esaminare `mysql-slow.log` per individuare le query lente registrate dal sistema. Questi registri sono disponibili anche in [!DNL New Relic]: vai a **[!UICONTROL New Relic]** > **[!UICONTROL Registri]** e filtra per `filePath:"/var/log/mysql/mysql-slow.log"`.

Esaminare regolarmente i registri di query lente [!DNL MySQL] per verificare che le query lente non vengano eseguite di frequente. Per i passaggi per la risoluzione delle query identificate come problematiche, vedere [Risoluzione dei problemi di prestazioni del database](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/maintenance/resolve-database-performance-issues).

## Configurare i processi cron {#configure-cron-jobs}

Tutte le operazioni asincrone in Commerce vengono eseguite utilizzando il comando cron di Linux.

Commerce dipende dalla corretta configurazione dei processi cron per importanti funzioni di sistema, tra cui l’indicizzazione e le operazioni consumer di coda. Se non viene configurato correttamente, Commerce non funzionerà come previsto.

È fondamentale che Commerce Cron sia configurato e configurato correttamente, utilizzando l’utente Unix appropriato nel file Unix Crontab. Ogni utente Unix ha il proprio file crontab, che è la configurazione utilizzata per eseguire i processi cron per quell&#39;utente. Per i passaggi, vedere [Configurare ed eseguire i processi cron](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs).

Impossibile eseguire lo script `dev/tools/cron.sh` perché è stato rimosso.

## Ottimizzare le impostazioni lato client {#optimize-client-side-settings}

Per migliorare la reattività storefront dell&#39;istanza di Commerce, configura le seguenti impostazioni in **[!UICONTROL Archivi]** > **[!UICONTROL Configurazione]** > **[!UICONTROL Avanzate]** > **[!UICONTROL Sviluppatore]**, disponibile solo in modalità Sviluppatore:

* **[!UICONTROL Impostazioni griglia]** > **[!UICONTROL Indicizzazione asincrona]**: *[!UICONTROL Abilita]*
* **[!UICONTROL Impostazioni CSS]** — **[!UICONTROL Minimizza file CSS]**: *[!UICONTROL Sì]*
* **[!UICONTROL Impostazioni JavaScript]** — **[!UICONTROL Minimizza file JavaScript]**: *[!UICONTROL Sì]*
* **[!UICONTROL Impostazioni JavaScript]** — **[!UICONTROL Abilita bundle JavaScript]**: *[!UICONTROL Sì]* (non abilitato per impostazione predefinita)
* **[!UICONTROL Impostazioni modello]** — **[!UICONTROL Minimizza HTML]**: *[!UICONTROL Sì]*

Poiché Adobe Commerce on Cloud viene sempre eseguito in modalità di produzione, impostare ogni opzione dalla riga di comando, ad esempio `bin/magento config:set --lock-config dev/css/minify_files 1`, quindi eseguire il commit della modifica `app/etc/config.php` risultante e ridistribuirla. Per l&#39;elenco completo dei percorsi CLI, vedere [Ottimizzare i file di risorse](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/development/optimize-css-js-files).
