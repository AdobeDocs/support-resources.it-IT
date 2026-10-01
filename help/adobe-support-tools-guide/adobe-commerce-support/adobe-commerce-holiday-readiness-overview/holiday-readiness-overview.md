---
title: Panoramica sulla preparazione alle festività per Adobe Commerce
description: Linee guida a livello esecutivo per preparare Adobe Commerce sugli ambienti dell’infrastruttura cloud per eventi con traffico elevato, come le feste.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
TQID: 'https://experienceleague.adobe.com/63svzoaJbKTgiO3iJR3iCyr4-slOLmt4QaVT2Y--NYI'
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
source-git-commit: 7ffe3c23f94b67342f02ed655d0a1700dd8f5a02
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%
---

# Panoramica sulla preparazione alle festività per Adobe Commerce

Questo playbook fornisce indicazioni per preparare gli ambienti Adobe Commerce per eventi a traffico elevato, come le feste. Consolida le raccomandazioni tecniche in cinque aree strategiche:

- Ottimizzazione delle prestazioni
- Best practice e stabilità
- Monitoraggio e osservabilità
- Scalabilità e pianificazione della capacità
- Prontezza operativa

Queste aree di interesse garantiscono che la piattaforma rimanga stabile, sicura e performante durante i picchi di carico.

## Ottimizzazione delle prestazioni

Di seguito è riportata una panoramica dei passaggi consigliati per garantire prestazioni ottimizzate. Per ulteriori informazioni, consulta [Preparazione per le festività di Adobe Commerce > Ottimizzazione delle prestazioni](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/performance-optimization.md).

* Ottimizza il caching delle richieste Fastly: normalizza i parametri di tracciamento promozionali, verifica che le pagine di destinazione siano memorizzabili in cache e utilizza GraphQL GET per PWA o headless storefront per aumentare il rapporto di hit della cache Fastly.
* Abilita Fastly IO: attiva Fastly Image Optimization e Deep IO in modo che le trasformazioni immagine vengano eseguite al bordo della rete CDN invece che all’origine, riducendo il tempo di rendering della pagina sui vetrine con immagini pesanti.
* Abilita cache L2: archivia i dati della cache localmente su ciascun nodo web per tagliare la latenza e ridurre le chiamate di rete a Redis/Valkey, a seconda della versione di Adobe Commerce in uso. La cache Redis non è supportata per Adobe Commerce 2.4.9 o per versioni patch successive a 2.4.5-p16, 2.4.6-p14, 2.4.7-p9 e 2.4.8-p4.
* Abilita connessioni slave: instradare query di lettura-pesanti ai nodi di replica con `MYSQL_USE_SLAVE_CONNECTION` e `REDIS_USE_SLAVE_CONNECTION` o `VALKEY_USE_SLAVE_CONNECTION` in modo che i database master non siano il collo di bottiglia in fase di caricamento.
* Abilita l’elaborazione asincrona di e-mail e ordini: il posizionamento dell’ordine nella coda, gli aggiornamenti della griglia dei dati dell’ordine e le e-mail di pagamento vengono eseguiti in background in tre impostazioni separate, in modo che il pagamento rimanga veloce in caso di volume di ordine elevato.
* Cambia gli indicizzatori in Aggiorna in modalità pianificazione: consente di spostare gli indicizzatori da Aggiorna al salvataggio alla modalità Aggiornamento in modalità pianificazione basato su cron per evitare il blocco durante gli aggiornamenti frequenti del catalogo, ad eccezione dell&#39;indicizzatore customer_grid.
* Considera l’architettura scalata (divisa): se l’ottimizzazione e le correzioni a livello di codice lasciano ancora il limite massimo di CPU in fase di caricamento, passa a un’impostazione a sei nodi a livello diviso che ridimensiona i nodi web e di database in modo indipendente.

## Best practice e stabilità

Di seguito è riportata una panoramica delle best practice per garantire la stabilità dell’istanza. Per i passaggi dettagliati per ciascuno di questi, consulta [Preparazione alle feste di Adobe Commerce > Best practice e stabilità](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/best-practices-stability.md).

* Aggiornamento alla versione più recente di Adobe Commerce: utilizza una versione supportata per mantenere le correzioni di sicurezza e i miglioramenti delle prestazioni forniti da Adobe in ogni versione.
* Installare gli strumenti ECE-Tools e Quality Patch Tool (QPT) più recenti: Aggiornare gli strumenti ece con le relative dipendenze e verificare che siano applicate le correzioni dello strumento Quality Patch applicabili, sia per le installazioni cloud che per quelle on-premise.
* Revisione e pulizia dei file di registro: consente di rimuovere i registri di debug e monitorare gli errori ricorrenti per evitare l&#39;utilizzo eccessivo del disco e migliorare la visibilità dei registri.
* Monitorare la crescita delle dimensioni dei dischi: mantenere i file condivisi e i volumi del database sotto il 70% di utilizzo in modo che la crescita dello storage non provochi interruzioni.
* Revisione delle query lente del database: utilizzare gli strumenti APM e il log delle query lente di MySQL per trovare e correggere le query costose prima che si accumulino in condizioni di traffico di picco.
* Configurare correttamente i processi cron: confermare che cron venga eseguito ogni minuto sotto l’utente corretto, in quanto ogni operazione asincrona in Commerce dipende da esso.
* Ottimizzare le impostazioni lato client: attiva la minimizzazione e il bundling CSS, JavaScript e HTML per velocizzare i tempi di caricamento della vetrina.

## Monitoraggio e osservabilità

Di seguito sono riportati i modi consigliati per monitorare l’istanza di Adobe Commerce durante la stagione di picco. Per i passaggi dettagliati per ciascuna di queste raccomandazioni sul monitoraggio e sull&#39;osservabilità, consulta [Preparazione alle feste di Adobe Commerce > Monitoraggio e osservabilità](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/monitoring-observability.md).

* Monitorare il traffico con New Relic: utilizza lo streaming di registri Fastly in New Relic per individuare anomalie del traffico, IP abusivi, richieste dannose indirizzate a endpoint come il pagamento e tendenze di dispositivi/browser.
* Personalizzare gli avvisi di New Relic: puoi impostare avvisi personalizzati basati su NRQL per traffico insolito, query GraphQL lente o tassi di errore crescenti, oltre agli avvisi gestiti di Adobe.
* Tracciare il punteggio di Apdex: osserva il punteggio di Apdex (≥ target 0,85) per mantenere i tempi di risposta back-end e front-end in un intervallo ritenuto soddisfacente dagli utenti.
* Rivedi informazioni sul supporto (rapporto SWAT): esegui un rapporto SWAT prima e dopo i picchi di eventi per identificare i rischi a livello di sistema e le aree di miglioramento.

## Scalabilità e pianificazione della capacità

Per i passaggi dettagliati per ciascuno di questi consigli sulla scalabilità e la pianificazione della capacità, consulta [Preparazione alle feste di Adobe Commerce > Scalabilità e pianificazione della capacità](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md).

* Pianifica l’upsize del cluster in anticipo: richiede un upsize temporaneo del computer dal supporto Adobe almeno 10 giorni lavorativi prima di una promozione importante.
* Abilita schermatura Fastly dell’origine: indirizza le richieste non memorizzate in cache tramite uno Shield POP vicino all’origine, in modo che meno richieste arrivino direttamente al server di origine.
* Esecuzione di test di carico e failover: verifica gli scenari di carico e ripristino prima delle campagne principali per verificare che i piani di scalabilità e rollback siano effettivamente in ritardo.

## Prontezza operativa

* Applicare tutte le patch di sicurezza e prestazioni: terminare tutte le patch prima del blocco del codice in modo che le distribuzioni non vengano interrotte in un secondo momento.
* Eseguire controlli di integrità precedenti alle festività: verificare i backup, lo stato di integrità del cron e gli script di riscaldamento della cache in modo che le operazioni vengano eseguite senza problemi durante il caricamento.
* Stabilisci i playbook di monitoraggio: documenta le soglie di allarme, i percorsi di escalation e i contatti 24 ore su 24, 7 giorni su 7, in modo che il team possa rispondere rapidamente durante i picchi di attività.
* Documenta piani di rollback: tieni pronte le strategie di rollback con gestione delle versioni in modo da poter eseguire rapidamente il ripristino in caso di implementazione non corretta.