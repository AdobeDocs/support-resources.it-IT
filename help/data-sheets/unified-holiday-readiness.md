---
title: Guida di preparazione alle festività unificate per le soluzioni Adobe DX
description: Preparazione di Adobe DX per AEP, AJO, CJA, Commerce, AEM, Marketo, Workfront, Campaign, Analytics e Target per aiutarti a pianificare, scalare, proteggere e ottimizzare.
feature-set: Experience Cloud
feature: Support
solution: Experience Cloud, Experience Platform, Journey Optimizer, Customer Journey Analytics, Commerce, Experience Manager, Workfront, Campaign, Analytics, Target, Marketo Engage
role: Developer, Admin, Leader, User
index: true
source-git-commit: 542f9696ed2cc71b23cfc3cc4fd410af5c8f7f73
workflow-type: tm+mt
source-wordcount: '3827'
ht-degree: 1%

---

# Guida di preparazione alle festività unificate per le soluzioni Adobe DX


La guida Unified Holiday Readiness Guide di Adobe DX Solutions consente di prepararsi per le feste concentrandosi sulla pianificazione proattiva anziché sulla risoluzione reattiva dei problemi. Fornisce passaggi pratici per garantire che le istanze siano pronte, riducendo al minimo potenziali problemi prima che sorgano. Il team Adobe offre competenze tecniche, un&#39;ampia gamma di funzionalità e metodi collaudati per fornire il giusto livello di supporto e guida, sia tecnica che strategica, in modo da garantire la buona preparazione dell&#39;azienda.

Segui queste best practice per garantire che le soluzioni Adobe Digital Experience siano resilienti, sicure e pronte per il traffico di picco durante le feste:

* Pianifica un aumento del traffico.
* Evitare modifiche importanti durante le finestre di picco; pianificare gli aggiornamenti prima o dopo le festività.
* Utilizza dashboard e avvisi per monitorare le prestazioni e rilevare tempestivamente i colli di bottiglia.
* Assicurati che i contatti per il supporto autorizzato siano aggiornati.
* [Se possibile, contatta in anticipo il supporto Adobe](https://experienceleague.adobe.com/it/docs/learning-manager/using/faq/how-to-submit-support-ticket).

Per i consigli di Adobe sulla preparazione a festività specifiche per la soluzione, consulta le sezioni seguenti.

* [Adobe Experience Platform](#aep)
* [Adobe Journey Optimizer](#ajo)
* [Adobe Customer Journey Analytics](#cja)
* [Adobe Commerce](#commerce)
* [Adobe Experience Manager](#aem)
* [Adobe Marketo](#marketo)
* [Adobe Workfront](#workfront)
* [Adobe Campaign](#campaign)
* [Adobe Analytics](#analytics)
* [Adobe Target](#target)

>[!NOTE]
>
>Fai clic su ogni sezione per espanderla.


## Guida di preparazione alle festività per Adobe Experience Platform (AEP) {#aep}

+++**Fare clic per visualizzare i consigli di preparazione per le festività di Adobe Experience Platform (AEP).**

Adobe Experience Platform (AEP) svolge un ruolo fondamentale nel fornire ai clienti esperienze in tempo reale. Con l’avvicinarsi delle festività, è essenziale garantire che l’implementazione di AEP sia ottimizzata per un aumento del traffico, una gestione sicura dei dati e un’acquisizione scalabile.

### Previsione della domanda stagionale

In preparazione ai picchi di traffico stagionali, Adobe consiglia di pianificare la capacità e monitorare l’acquisizione del profilo di streaming. Ciò include la previsione dei volumi di dati e la garanzia che il sistema sia in grado di gestire un throughput maggiore. Consulta [Piano per la capacità e il traffico stagionale](https://experienceleague.adobe.com/it/docs/experience-platform/dataflows/ui/monitor-streaming-profile) per riferimento.

### Preparazione per la scalabilità

Adobe fornisce diverse strategie per garantire che l’ambiente sia pronto per il traffico delle feste:

* Aumenta la capacità allocata per le sandbox.
* Identifica i flussi di dati ad alta velocità nel [dashboard di monitoraggio](https://experienceleague.adobe.com/it/docs/experience-platform/dataflows/ui/monitor-streaming-profile) e applica limitazioni o filtri dove necessario.
* Utilizza l&#39;acquisizione batch per casi d&#39;uso a latenza ridotta per ottimizzare le prestazioni come descritto in [Utilizzo della licenza e capacità: best practice per la velocità di trasmissione in streaming](https://experienceleague.adobe.com/it/docs/experience-platform/landing/license/capacity#suggestions).

Queste pratiche consentono di mantenere l’affidabilità dell’acquisizione e di ridurre la latenza durante i periodi di picco.

### Best practice e guardrail

Per rimanere entro i limiti operativi ed evitare interruzioni del servizio, Adobe consiglia di seguire i seguenti guardrail di acquisizione e profilo:

* [Best practice per la velocità effettiva di streaming](https://experienceleague.adobe.com/it/docs/experience-platform/landing/license/capacity#suggestions)
* [Guardrail per l&#39;acquisizione dei dati](https://experienceleague.adobe.com/it/docs/experience-platform/ingestion/guardrails)
* [Guardrail predefiniti per dati e segmentazione del profilo cliente in tempo reale](https://experienceleague.adobe.com/it/docs/experience-platform/profile/guardrails)
* [Blueprint AEP: guardrail](https://experienceleague.adobe.com/it/docs/blueprints-learn/architecture/architecture-overview/guardrails)

### Sicurezza e governance

Adobe sottolinea le solide pratiche di sicurezza e governance, in particolare nelle stagioni di traffico elevato in cui la sensibilità dei dati è aumentata.

Consulta [Governance, privacy e sicurezza in Adobe Experience Platform: sicurezza](https://experienceleague.adobe.com/it/docs/experience-platform/landing/governance-privacy-security/overview#security) per raccomandazioni su come proteggere i dati dei clienti, applicare i controlli sulla privacy e mantenere la conformità in tutta l&#39;implementazione di AEP.

Seguendo queste linee guida e sfruttando la documentazione pubblica di Adobe, le organizzazioni possono garantire che il Adobe Experience Platform sia resiliente, sicuro e pronto a fornire ai clienti esperienze eccezionali durante le feste.

+++

## Guida di preparazione alle festività per Adobe Journey Optimizer (AJO) {#ajo}

+++**Fare clic per visualizzare i consigli di preparazione per le festività di Adobe Journey Optimizer (AJO).**


Per preparare Adobe Journey Optimizer per le festività natalizie, le organizzazioni devono anticipare i picchi di eventi e la complessità cross-channel, configurare le regole di percorso e frequenza e garantire l’igiene dei dati e la logica decisionale. Devono inoltre convalidare le prestazioni su larga scala, applicare protezioni di sicurezza e API e applicare informazioni post-picco per perfezionare le campagne future.

### Prevedere la domanda

* In base alle compressioni della stagione festiva e al volume più pesante della campagna, prevedi:
   * Un picco di eventi in tempo reale e percorsi attivati (abbandono del carrello, offerte dell’ultimo minuto)
   * Rischi di saturazione dei messaggi (rinuncia più elevata, stanchezza)
   * Maggiore complessità cross-channel (e-mail + push + SMS + in-app)
* Utilizza le metriche dell’anno precedente (tassi di apertura/clic/rinuncia, volumi di ingresso nel percorso) per modellare i carichi previsti e impostare soglie per i sistemi di messaggistica.
* Identificare le &quot;finestre silenziose&quot; o i periodi di prestazioni ridotte (ad esempio: fine settimana, giorni festivi) e pianificare di conseguenza i volumi di invio.

### Preparazione per la scalabilità

* Assicurati che tutte le configurazioni di canale in AJO siano configurate correttamente: e-mail, push, SMS, web, in-app. Consulta [Configurare le configurazioni del canale](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/configuration/channel-surfaces).
* Configura le regole di quota limite e quota limite per controllare i volumi dei messaggi. Consulta l&#39;articolo [Limitazione della frequenza](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/configuration/business-rules/configure-frequency-capping-rules).
* Configurare i set di regole di canale/percorso: fare riferimento a [Operazioni con i set di regole](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets).
* Prepara l’igiene dei dati/i flussi di eventi in tempo reale e i framework di segmentazione.
* Assicurati di aver definito i tipi di pubblico target per le campagne festive, ad esempio:
   * clienti di alto valore
   * segmenti fedeli
   * carrelli abbandonati
   * nuovi acquirenti
* Precarica o prepara modelli per i percorsi festivi, sfrutta la logica decisionale (offerte/vincoli) per adattarti in modo dinamico in base all’inventario, alle offerte sensibili al tempo e alle preferenze di canale. Vedi l&#39;esempio nell&#39;articolo [Aggiungere vincoli a un&#39;offerta](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/decisioning/offer-decisioning/managing-offers-in-the-offer-library/configure-offers/add-constraints).
* Preparazione tecnica: conferma la capacità di caricamento dell’API/endpoint, regole di limitazione/limite per azioni personalizzate e integrazioni esterne. Consulta [Guardrail e limitazioni](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/get-started/guardrails).

### Test e convalida

* Utilizza il framework di sperimentazione per testare le modifiche delle variabili chiave:
   * ora di invio
   * tipo di offerta
   * mix di canali
Consulta [Best practice per AJO Experimentation Accelerator](https://experienceleague.adobe.com/en/docs/experimentation-accelerator/using/get-started/experiment-accelerator-best-practices).
* Eseguire la convalida end-to-end del percorso:
   * trigger di evento
   * voce di segmentazione
   * Flussi del percorso del percorso
   * logica di personalizzazione
   * vincoli di offerta
   * criteri di uscita
* Verificare le regole di limitazione e conflitto. Consulta l&#39;articolo [Limitazione Percorsi e arbitrato](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/conflict-prioritization/journey-capping).
* Stress test dei volumi scalati per picchi di invio o picchi: simula volumi ad alto trigger per convalidare il comportamento del sistema sotto carico.
* Convalida del recapito messaggi: riscalda domini e mittenti e-mail, conferma le configurazioni push per dispositivi mobili e controlla i canali di fallback per la presenza di SMS e in-app.

### Best practice

* Utilizza l’orchestrazione omni-channel. Consulta l&#39;articolo del blog [percorsi di clienti omnichannel essenziali per coinvolgimento e crescita](https://business.adobe.com/blog/essential-customer-journeys-for-omnichannel-engagement) che mostra un esempio di stagione festiva con AJO.
* Se necessario, assegna la priorità ai trigger in tempo reale. Ad esempio: abbandono del carrello, abbandono della navigazione e avvisi sulle scorte, in quanto gli acquirenti delle feste sono più reattivi.
* Sfrutta segmentazione e personalizzazione: esegui il targeting di segmenti ad alte intenzioni, personalizza le offerte in base al comportamento di acquisto passato e alle preferenze.
* Minima fatica nella messaggistica: applica limiti e ore di silenzio per evitare di sollecitare eccessivamente. Consulta il post del blog [Elevate Customer Experience with Daily Frequency Capping in AJO](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/elevate-customer-experience-with-daily-frequency-capping-in-ajo/ba-p/761510).
* La tempistica è importante: il piano invia prima in una finestra festiva (data la stagione compressa) e allinea i canali al fuso orario e al comportamento del pubblico locale.
* Offri offerte dinamiche/a tempo limitato per creare un’urgenza, ma coordinati tra i canali per evitare duplicazioni e conflitti.
* Utilizza la logica di soppressione: elimina i tipi di pubblico che hanno appena acquistato o applica percorsi post-acquisto per evitare messaggi ridondanti.

### Sicurezza e governance

* Assicurati che il controllo degli accessi e le autorizzazioni siano configurati in modo che solo gli utenti necessari possano distribuire percorsi o modificare regole aziendali.
* Monitora e applica il limite di chiamata/connessione API: ad esempio, consulta l&#39;API [Limitazione | Articolo di Adobe Journey Optimizer](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/connect-systems/external-systems/capping).
* Utilizza dati di prime parti puliti e assicurati che l’unione delle identità sia corretta in modo che i messaggi siano incentrati sul cliente e non duplicati/non allineati.
* Assicurati che i domini di recapito messaggi siano riscaldati e che siano in atto misure anti-spam, in particolare per gli invii di vacanze a volume elevato.
* Esamina i registri di audit e le modifiche al percorso frequentemente durante la stagione di picco per rilevare in anticipo eventuali errori di esecuzione o percorsi errati.

### Apprendimenti post-picco

* Dopo i picchi di carico, esegui una revisione dei conteggi di immissione del percorso, dei conteggi di soppressione, dei tassi di rinuncia, delle metriche di recapito messaggi e delle prestazioni del canale.
* Pulisci i segmenti soppressi e sospendi o ritira i percorsi generati per le finestre delle festività per evitare l’eccesso di comunicazioni.
* Utilizza informazioni provenienti dalle prestazioni in tempo reale per perfezionare la pianificazione del prossimo anno (ad esempio: regolazioni del tempo di invio, mix di canali e volume dei messaggi).

Prevedendo in modo proattivo la domanda stagionale, configurando canali e regole, convalidando le prestazioni del percorso e applicando sicurezza e governance, le organizzazioni possono garantire che Adobe Journey Optimizer offra ai clienti esperienze fluide, personalizzate e resilienti durante e dopo le feste.

+++

## Guida di preparazione alle festività di Customer Journey Analytics (CJA) {#cja}

+++**Fare clic per visualizzare i consigli di preparazione per le festività di Customer Journey Analytics (CJA).**

Customer Journey Analytics utilizza i 5 punti per ottenere la disponibilità per le festività e la stagione di picco.

### Preparazione per la scalabilità

* Esaminare le connessioni CJA e le visualizzazioni dati; stabilire quali connessioni e visualizzazioni dati richiedono un monitoraggio e un provisioning migliorati.
* Conferma che il provisioning sia sufficiente per le festività; effettua l’upscale delle connessioni e delle visualizzazioni dati critiche in base alle esigenze. Per ulteriori informazioni, vedere [Gestione connessioni](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-connections/manage-connections).

### Monitorare le prestazioni

* Sfrutta la RAM ([[!UICONTROL Panoramica di Reporting Activity Manager]](https://experienceleague.adobe.com/it/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)) per monitorare in tempo reale le richieste di reporting attive e in coda, identificare connessioni a capacità e colli di bottiglia spot.
* Presta attenzione all&#39;aumento della latenza durante il caricamento di picco utilizzando gli articoli [Errori e risoluzione dei problemi](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages) e [Limitazioni note](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-workspace/workspace-faq/aw-limitations).
* Consentire agli amministratori di sospendere o annullare preventivamente le richieste con tempi di esecuzione lunghi o bloccate tramite RAM. Consulta l&#39;articolo [Annulla richieste di reporting in CJA](https://experienceleague.adobe.com/it/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-cancel-requests).

### Best practice

* Pianifica esportazioni/rapporti durante periodi di traffico ridotto per ridurre il carico e la latenza. Consulta l&#39;articolo [Report pianificati](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-components/scheduled-projects-manager).
* Distribuisci richieste: pianifica i rapporti a intervalli diversi nel corso della giornata.
* Riduci i pannelli, semplifica i segmenti, accorcia gli intervalli di date ed evita processi concorrenti in eccesso. Per informazioni dettagliate, consulta l&#39;articolo [Ottimizzazione delle prestazioni di CJA Workspace](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-workspace/workspace-faq/optimizing-performance).

### Risoluzione dei problemi

* Per la risoluzione dei problemi relativi agli errori dell&#39;area di lavoro, vedere i messaggi di errore relativi alla causa e le azioni consigliate. Utilizzare la RAM ([!UICONTROL Gestione attività di reporting]) per eliminare i colli di bottiglia e gestire la concorrenza in modo efficace. Per ulteriori dettagli, vedere [Gestione errori CJA Workspace](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages).
* Utilizzare la RAM ([[!UICONTROL Reporting Activity Manager] in CJA](https://experienceleague.adobe.com/it/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)) per individuare utenti, query o progetti problematici; assegnare priorità e terminare/annullare in base alle esigenze.

### Apprendimenti post-picco

* Dopo le festività/i periodi di picco, controlla i registri di prestazioni e incidenti per valutare l’impatto delle best practice fornite.
* Rivedi le query lente e le attività degli utenti per identificare pattern e tendenze che possono essere ottimizzati per la prossima stagione.
* Raccogli feedback da utenti e stakeholder: aggiorna i tuoi runbook e i piani di preparazione utilizzando le nuove informazioni acquisite.
* Fornisci feedback ai team di Adobe tramite il tuo account team.

+++

## Guida di preparazione alle festività per Adobe Commerce {#commerce}

+++**Fare clic per visualizzare i consigli di preparazione per le festività di Adobe Commerce.**

Per garantire una stagione di picco di successo per la tua organizzazione, è essenziale preparare il tuo negozio digitale Adobe Commerce per un traffico elevato.

### Prevedere la domanda

* Durante il periodo di picco delle vendite durante le festività (da metà novembre a metà gennaio), Adobe consiglia a tutti i commercianti Adobe Commerce ospitati nella nostra infrastruttura cloud di pianificare in modo proattivo un aumento dei visitatori inviando richieste di capacità di picco durante le festività. Per informazioni dettagliate, consulta [Richieste di capacità di crescita per le festività per Adobe Commerce nella nostra infrastruttura cloud](https://experienceleague.adobe.com/it/docs/commerce-knowledge-base/kb/announcements/commerce-announcements/holiday-surge-capacity-requests-for-magento-commerce-cloud).

### Preparazione per la scalabilità

Segui i consigli riportati nella guida [Pianificazione e pivot: un approccio strategico alla stagione di picco 2025](https://experienceleague.adobe.com/it/perspectives/planning-and-pivoting-a-strategic-approach-to-peak-season-2025), che fornisce strategie utilizzabili tramite Adobe Commerce (e strumenti Adobe Experience Cloud opzionali) per aiutarti a pianificare, eseguire il pivot e fornire esperienze cliente straordinarie durante il periodo dell’anno più impegnativo.

### Best practice

* Segui la guida di Adobe [Come preparare la tua infrastruttura per un traffico elevato: i 5 punti di prestazioni della stagione di punta](https://business.adobe.com/blog/how-to/the-5-ps-of-peak-season-performance-a-guide-to-preparing-your-infrastructure-for-high-traffic).
* Consulta [Suggerimenti tecnici per prepararsi alle festività di Commerce](https://experienceleague.adobe.com/it/docs/commerce-knowledge-base/kb/how-to/tech-tips-for-commerce-holiday-readiness) per suggerimenti su come preparare l&#39;infrastruttura per un traffico elevato, evitare tempi di inattività e ottimizzare le prestazioni durante le festività.

+++

## Guida di preparazione alle festività per Adobe Experience Manager (AEM) {#aem}

+++**Fare clic per visualizzare i consigli di preparazione per le festività di Adobe Experience Manager (AEM).**

La stagione delle vacanze si sta avvicinando rapidamente e per molti clienti Adobe ciò indica l’inizio dei periodi di picco delle vendite. Nel nostro impegno per il tuo successo, vogliamo assicurarci che tu sia pienamente preparato per l’imminente aumento del traffico.

### Servizi cloud Adobe Experience Manager (AEM)

Se l’organizzazione ha momenti di maggior traffico durante le feste, potresti pensare a come ottimizzare il sito Adobe Experience Manager per far fronte alle picchi di traffico. Fortunatamente, con Adobe Experience Manager Cloud Services, il tuo sito è già dotato della funzionalità di scalabilità automatica, che assicura un’esperienza fluida per i visitatori, indipendentemente da cambiamenti improvvisi nel traffico.

#### Preparazione per la scalabilità

* Per informazioni dettagliate e indicazioni sulla preparazione al traffico elevato con Adobe Experience Manager Cloud Services, consulta i seguenti collegamenti:

   * [CDN in AEM as a Cloud Service](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/content-delivery/cdn)
   * [Memorizzazione in cache di AEM as a Cloud Service](https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/caching/overview)

* Se sei un cliente di Ultimate Success e di recente hai condiviso le informazioni sulle previsioni dei volumi con il tuo Account Team di Adobe, non preoccuparti di inviarle di nuovo a noi, in quanto abbiamo già una visualizzazione.

Siamo qui per aiutarvi in ogni fase del vostro percorso. In caso di domande o dubbi, puoi [inviare un ticket di supporto](https://experienceleague.adobe.com/it/docs/learning-manager/using/faq/how-to-submit-support-ticket).

Per prepararsi a una campagna di marketing durante le feste, consulta la [Guida utente di AEMaaCS: Introduzione - Parametri della campagna di marketing](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/content-delivery/caching#marketing-parameters).

#### Sicurezza e governance

Per informazioni sulla protezione/protezione del traffico del sito Web AEM, consulta l&#39;articolo [Panoramica - Protezione dei siti Web AEM](https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/security/traffic-filter-and-waf-rules/overview) nelle esercitazioni di AEM as a Cloud Service.

#### Pianificazione manutenzione vacanze

Adobe ha pianificato periodi di esclusione dalla manutenzione per garantire un servizio ininterrotto durante le feste critiche:

* **Nessun aggiornamento automatico** si verificherà tra:
   * 24 novembre 2025 - 2 dicembre 2025
   * 15 dicembre 2025 - 2 gennaio 2026

Questo garantisce stabilità durante i periodi di traffico elevato. Per le pianificazioni complete delle versioni e le finestre di manutenzione, consulta la [roadmap delle versioni di AEM](https://experienceleague.adobe.com/it/docs/experience-manager-release-information/aem-release-updates/update-releases-roadmap).


### Adobe Experience Manager (AEM) con Adobe Managed Services (AMS)

I clienti di AEM che sfruttano Adobe Managed Services possono lavorare in modo proattivo con i loro CSE per pianificare le esigenze di copertura delle festività.

++++

## Guida di preparazione alle festività per Adobe Marketo {#marketo}

+++**Fare clic per visualizzare i consigli di preparazione alle festività per Adobe Marketo.**

Per garantire il successo delle campagne festive con Adobe Marketo, i team devono verificare le impostazioni di autenticazione e-mail, pulire e proteggere il database, ottimizzare la logica e la pianificazione delle campagne, testare accuratamente il rendering e il recapito delle e-mail e semplificare la preparazione del supporto per prestazioni e coinvolgimento di picco.

### Preparazione per la scalabilità

* Controllare le impostazioni SPF/DKIM e assicurarsi che tutto sia ancora configurato e funzioni correttamente. Per informazioni dettagliate, consulta l&#39;articolo [Configura SPF e DKIM per il recapito messaggi e-mail](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-spf-and-dkim-for-your-email-deliverability).
* Controllare e pulire il database Marketo eliminando i record inattivi o non validi. Questo aumenterà le possibilità che il tuo invio arrivi nelle caselle in entrata dei tuoi lead più pronti per le vendite. Per ulteriori informazioni, vedere l&#39;articolo [Verifica stato del database di Marketo e Come mantenerlo pulito](https://nation.marketo.com/t5/champion-program-blogs/marketo-database-health-check-up-amp-how-to-keep-it-clean/ba-p/323563).
* Conferma che i membri del gruppo dispongano delle autorizzazioni necessarie per eseguire attività e impedire l’accesso involontario o le modifiche alle e-mail. Che tu stia apportando modifiche tramite **[!UICONTROL Admin]** o tramite **[!UICONTROL Admin Console]**, il problema è risolto. Consulta l&#39;articolo [Gestione di ruoli utente e autorizzazioni](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions).
* Controlla le integrazioni Launchpad per garantire l’autenticazione corretta e risolvere eventuali errori prima che vengano utilizzate. Consulta l&#39;articolo [Guida per gli sviluppatori di Marketo: autenticazione](https://experienceleague.adobe.com/it/docs/marketo-developer/marketo/rest/authentication).

### Best practice

L’efficienza inizia con la comprensione esatta delle priorità e dell’elaborazione delle campagne da parte di Marketo. Dai alle campagne il dono della velocità con questi suggerimenti di ottimizzazione.

* È fondamentale comprendere in che modo Marketo dà priorità all’elaborazione dei passaggi del flusso di campagna per evitare di ritardare inavvertitamente eventuali e-mail urgenti o ad alta priorità. Consulta l&#39;articolo [Funzionamento dell&#39;elaborazione di Campaign](https://nation.marketo.com/t5/knowledgebase/how-campaign-processing-works/ta-p/248264).
* Presta attenzione alla logica di elenco intelligente per garantire che le campagne vengano eseguite rapidamente e al massimo delle prestazioni. Consulta l&#39;articolo [Best practice per elenchi avanzati](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/best-practices-for-smart-lists).
* **[!UICONTROL Inizio intestazione]** o **[!UICONTROL Fuso orario destinatario]** può iniziare a creare e-mail prima dell&#39;invio, riducendo i ritardi e fornendo tempo di preparazione aggiuntivo per i lead qualificati con logica ad alte risorse. Per ulteriori informazioni, vedere gli articoli [Inizio programmazione per i programmi e-mail](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/head-start-for-email-programs) e [Programmazione programmi e-mail con fuso orario destinatario](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/scheduling-with-recipient-time-zone/schedule-email-programs-with-recipient-time-zone).
* La campagna è attiva e i lead scorrono, quindi si nota un errore nel passaggio di flusso. È invitante correggere il problema con una regolazione rapida, ma essere consapevoli di ciò che accade quando si cambia un passaggio di attesa live o si riordinano i flussi può aiutarti a evitare un sacco di problemi e pulizia in seguito. Consulta l&#39;articolo [Modifica del flusso di una campagna con membri in passaggi di attesa](https://nation.marketo.com/t5/knowledgebase/editing-campaign-flow-with-members-in-wait-steps/ta-p/254294).

### Test e convalida

Prima di premere **[!UICONTROL Invia]**, assicurati che le e-mail abbiano l&#39;aspetto e le prestazioni desiderati.

* Marketo offre diversi modi per testare l’aspetto di un’e-mail per assicurarti che sia esattamente come previsto.
   * Utilizza la funzione **[!UICONTROL Anteprima]** per assicurarti che il contenuto dinamico e i token siano visualizzati correttamente visualizzando l&#39;anteprima per segmentazione o singoli lead. Consulta l&#39;articolo [Anteprima di un&#39;e-mail con contenuto dinamico](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/email-marketing/general/functions-in-the-editor/preview-an-email-with-dynamic-content).
   * Invia un’e-mail diretta ai record di test in modo rapido e semplice per vedere come appare il messaggio e-mail su client/dispositivi diversi. Vedi l&#39;articolo [Esegui un singolo passaggio di flusso da un elenco avanzato](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/using-smart-lists/run-a-single-flow-step-from-a-smart-list).
   * Per gli utenti di [!DNL Litmus], è ora più facile che mai integrare il tuo account e avviare il rendering dei test direttamente dall&#39;editor e-mail. Consulta l&#39;articolo [Test rendering e-mail con [!DNL Litmus]](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/email-marketing/email-designer/test-email-rendering).
* Controlla la funzionalità di report posta indesiderata di Email, che si integra con [!DNL SpamAssassin] per rivedere il contenuto dell&#39;e-mail e assegnare un punteggio sulla probabilità che arrivi nella casella in entrata o che venga contrassegnato come *posta indesiderata*. Consulta l&#39;articolo [Rapporto posta indesiderata](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/email-marketing/email-designer/spam-report).
* Tieni d&#39;occhio [!UICONTROL Coda campagne] per verificare che le campagne siano in elaborazione e che la priorità degli elementi ad alta urgenza sia corretta. Vedi [La mia campagna è in esecuzione?](https://nation.marketo.com/t5/knowledgebase/is-my-campaign-running/ta-p/248662) articolo.

### Semplificazione dell&#39;esperienza di supporto

Quando qualcosa va storto, la velocità conta e il supporto Marketo è qui per aiutarti! Includi questi dettagli nel tuo caso di supporto per evitare di andare avanti e indietro e aiutare il nostro team a lavorare per una risoluzione più rapida. Consulta l&#39;articolo [Best practice per l&#39;utilizzo del supporto Marketo](https://nation.marketo.com/t5/knowledgebase/best-practices-for-working-with-marketo-support/ta-p/253491).

Con questa guida, puoi riposare un po&#39; più facilmente sapendo che stai partendo da una posizione solida per stimolare coinvolgimento e conversioni durante questa finestra critica. La posta in gioco è alta, ma il vostro stress non deve essere. Inizia oggi stesso i preparativi e fai di questa stagione delle vacanze la tua stagione di maggior successo.

+++

## Guida di preparazione alle festività per Adobe Workfront {#workfront}

+++**Fare clic per visualizzare i consigli di preparazione per le festività di Adobe Workfront.**

Per preparare Adobe Workfront per le feste natalizie, i team devono aggiornare i contatti di supporto, allineare le pianificazioni interne con Adobe, evitare modifiche importanti durante le finestre di picco e monitorare in modo proattivo le automazioni e le integrazioni per garantire la fluidità delle operazioni.

### Preparazione per la scalabilità

Per garantire un’esperienza di supporto fluida durante le vacanze:

* Rivedi e aggiorna in anticipo i contatti del supporto autorizzato.
* Verifica che le principali parti interessate siano disponibili a collaborare con il supporto in caso di problemi critici.
* Se la pianificazione del prodotto o del flusso di lavoro cambia durante le feste, è consigliabile pianificarle prima di metà novembre o dopo l&#39;inizio di gennaio per ottenere i tempi di risposta migliori.
* Comunica le pianificazioni delle festività interne ai tuoi contatti di Adobe per assicurarti che siano allineate.

### Test e convalida

Rimani informato sulle versioni di Workfront e testa le nuove funzioni negli ambienti sandbox:

* [Prepararsi per una versione di Adobe Workfront](https://experienceleague.adobe.com/it/docs/workfront/using/product-announcements/product-releases/release-readiness)
* [Archivio note sulla versione di Workfront](https://experienceleague.adobe.com/it/docs/workfront/using/product-announcements/product-releases/product-releases)
* [Panoramica sulla versione del primo trimestre 2025](https://experienceleague.adobe.com/it/docs/workfront/using/product-announcements/product-releases/release-25-q1/25-q1-release-overview)
* [Registrazione webinar sulla versione di Workfront](https://experienceleague.adobe.com/it/docs/events/workfront-recordings/releases/25-1-release-webinar)

### Best practice

* Pianificazione proattiva: identifica tutte le dipendenze di sistema o le automatizzazioni pianificate che possono essere influenzate dalle programmazioni interne del tempo libero.
* Comunicazione continua: tieni informati i team interni e il supporto Adobe in merito a manutenzione pianificata o eventi chiave.
* Utilizzare le dashboard: monitora le integrazioni e le automazioni chiave per individuare i primi segnali di problemi di prestazioni.
* Escalate in anticipo: se prevedete o osservate il degrado del servizio, aprite immediatamente un ticket di supporto, non aspettate che diventi critico.

Grazie a una pianificazione anticipata, alla comunicazione chiara e all&#39;escalation tempestiva dei problemi, le organizzazioni possono ridurre al minimo le interruzioni e garantire che Workfront continui a supportare i flussi di lavoro critici per tutto il periodo delle vacanze.

+++

## Guida di preparazione alle festività per Adobe Campaign {#campaign}

+++**Fare clic per visualizzare i consigli di preparazione per le festività di Adobe Campaign.**


Per preparare Adobe Campaign per le festività, i team devono convalidare in modo proattivo le impostazioni di recapito messaggi, ottimizzare la segmentazione del pubblico e la frequenza dei messaggi, garantire la scalabilità dell’infrastruttura e testare l’orchestrazione delle campagne cross-channel per gestire in modo efficace i picchi di volume stagionale e di coinvolgimento.

### Suggerimenti degli esperti per dare risalto alle campagne per le vacanze

Proprio come non è mai troppo presto per iniziare a fare acquisti per le vacanze, non è mai troppo presto per iniziare a pianificare una campagna di marketing di successo le per vacanze. Con Adobe Campaign puoi progettare, pianificare ed eseguire campagne che concretizzeranno tutti i desideri per le feste della tua organizzazione. Ma conosci già tutti i suggerimenti per l’esecuzione di campagne per concludere l’anno col botto? Guarda questo video, [Suggerimenti degli esperti per dare risalto alle tue campagne per le feste](https://experienceleague.adobe.com/it/docs/events/experience-league-live-recordings/episodes/exl-live-episode-03), che illustra le best practice per il recapito dei messaggi e l&#39;esecuzione e illustra come eseguire tutte queste operazioni in Adobe Campaign.

### Considerazioni e preparativi per il periodo festivo

Questo video, [Adobe Campaign: Holiday Readiness - Considerazioni e preparativi per il periodo festivo](https://helpx.adobe.com/it/customer-care-office-hours/campaign/campaign-holiday-readiness.html), tratta:

* Coinvolgere la community di Campaign
* Recapito messaggi: considerazioni per le vacanze e oltre!
* Raccomandazioni tecniche per Adobe Campaign Classic (ACC) e Adobe Campaign Standard (ACS)

Affinché Adobe Campaign sia pronto per la stagione estiva di picco, le organizzazioni devono finalizzare i controlli di consegna, convalidare le configurazioni delle campagne e garantire l’esistenza di un’infrastruttura scalabile e di un’orchestrazione cross-channel che consentano di eseguire in tutta sicurezza campagne di volume elevato e sensibili al tempo nel corso delle festività.

+++

## Guida di preparazione alle festività per Adobe Analytics {#analytics}

+++**Fare clic per visualizzare i consigli di preparazione per le festività di Adobe Analytics.**

Con l’avvicinarsi delle festività natalizie, le organizzazioni che utilizzano Adobe Analytics devono adottare misure proattive per garantire l’accuratezza dei dati, le prestazioni della piattaforma e l’affidabilità dei rapporti durante i periodi di traffico di picco. Adobe fornisce diverse risorse e best practice per aiutare i team a prepararsi in modo efficace.

### Prevedere il traffico

Per garantire un&#39;adeguata allocazione dell&#39;hardware e tempi di risposta del sistema, Adobe consiglia di inviare in anticipo **volumi di hit/chiamate server orari e giornalieri di picco**.

* Controllare [I lead time di pianificazione dei picchi di traffico e di allocazione hardware](https://experienceleague.adobe.com/it/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/traffic-management/t-traffic-schedule-spike#hardware-allocation-lead-times), poiché la rapidità con cui i dati diventano disponibili è fondamentale per prendere decisioni in tempo reale durante periodi di grandi volumi.

* Scopri cosa influisce sulla disponibilità e sulla latenza dei dati in Adobe Analytics in [Panoramica sulla latenza dei dati di Adobe Analytics](https://experienceleague.adobe.com/it/docs/analytics/technotes/latency), compresi picchi di traffico imprevisti e problemi hardware, e scopri le strategie consigliate per ridurre i ritardi nei dati.

### Best practice

Per i team che utilizzano feed di dati per esportare dati di analisi non elaborati, Adobe fornisce indicazioni su come ottimizzare le configurazioni dei feed ed evitare insidie comuni.

* [Best practice per i feed dati di Adobe Analytics](https://experienceleague.adobe.com/it/docs/analytics/export/analytics-data-feed/data-feeds-best-practices)

Per mantenere un reporting rapido e affidabile durante le festività, Adobe consiglia di:

* [Ottimizzazione delle prestazioni di Analysis Workspace](https://experienceleague.adobe.com/it/docs/analytics/analyze/analysis-workspace/workspace-faq/optimizing-performance)
* [Risoluzione dei problemi e best practice per Report Builder: consigli per l&#39;ottimizzazione delle richieste](https://experienceleague.adobe.com/it/docs/analytics/analyze/legacy-report-builder/troubleshoot#section_33EF919255BF46CD97105D8ACB43573F)
* [Guida ai componenti di Analytics: coda dei report pianificati](https://experienceleague.adobe.com/it/docs/analytics/components/scheduled-reports-admin)

### Pianificazione manutenzione vacanze

Adobe in genere applica **finestre di esclusione dalla manutenzione** durante i periodi di picco delle festività per garantire la continuità del servizio. I clienti devono monitorare i programmi di rilascio e manutenzione di Adobe tramite Experience League e coordinarsi con il proprio team di account Adobe per la pianificazione del supporto.

Seguendo queste linee guida e sfruttando la documentazione pubblica di Adobe, le organizzazioni possono garantire che l’implementazione di Adobe Analytics sia solida, reattiva e pronta per le esigenze delle feste.

+++

## Guida di preparazione alle festività per Adobe Target {#target}

+++**Fare clic per visualizzare i consigli di preparazione per le festività di Adobe Target.**

La stagione delle feste offre interessanti opportunità di coinvolgimento, ma è anche accompagnata da sfide quali l’aumento del traffico e l’aumento della domanda di sistemi di personalizzazione. Per aiutarti a fornire esperienze fluide durante questo periodo critico, abbiamo compilato consigli chiave per garantire che la tua implementazione di Adobe Target sia pronta.

### Prevedere la domanda

Innanzitutto, si prevedono picchi di traffico del 20-50% o superiori e si verifica che l’infrastruttura sia in grado di gestire il carico. Prevedi le attività e i volumi di dati in Adobe Target, Analytics e AEP per evitare sorprese.

È inoltre importante identificare i percorsi mission-critical, come il pagamento, i consigli di prodotto e le offerte promozionali, in modo che le attività di personalizzazione si concentrino sui punti più importanti.

Consulta [Best practice per l&#39;ottimizzazione con Adobe Target](https://experienceleague.adobe.com/it/docs/target-learn/tutorials/administration/strategy/target-best-practices-for-optimization).

### Preparazione per la scalabilità

* Pianifica un aumento del traffico sul sito web e sui dispositivi mobili e informa il team di supporto di Target di aumentare la capacità del server per evitare il blocco delle chiamate.
* Per qualsiasi test di carico/penna, il team di supporto di Target deve essere informato in anticipo.
* Eseguire l&#39;aggiornamento alle versioni più recenti di `at.js`/Delivery API.
* Blocca le modifiche non critiche; preparati per le esperienze di fallback.
* Allinea il supporto e i processi di escalation e abilita gli avvisi proattivi.

### Test e convalida

Convalida la distribuzione del contenuto utilizzando [collegamenti QA](https://experienceleague.adobe.com/it/docs/target/using/activities/activity-qa/activity-qa) per verificare che tutto funzioni come previsto. Utilizza l&#39;interruttore **[!UICONTROL Corrispondenza regole pubblico per visualizzare le esperienze]** per garantire che il pubblico giusto sia idoneo per l&#39;attività da testare. Verifica che la configurazione della **[!UICONTROL metrica obiettivo]** sia allineata all&#39;**[!UICONTROL obiettivo]** dell&#39;attività. E avere sempre pronto un piano di riserva — giusto nel caso.

### Best practice

Mantieni l&#39;implementazione entro i [limiti Adobe Target](https://experienceleague.adobe.com/it/docs/target/using/troubleshoot/target-limits) e verifica in anticipo la [conformità ai requisiti RGPD e CCPA](https://experienceleague.adobe.com/it/docs/target-dev/developer/implementation/privacy/cmp-privacy-and-general-data-protection-regulation) prima di avviarla. Mantieni meno di 100 attività attive e archivia quelle meno recenti per semplificare il lavoro. Sfrutta **[!UICONTROL Allocazione automatica]**/**[!UICONTROL Targeting automatico]** per l&#39;ottimizzazione basata su IA. Stabilisci piani di ripristino e dashboard di monitoraggio in tempo reale.

### Sicurezza e governance

Prima di personalizzare le esperienze, conferma la conformità del consenso in base a RGPD e CCPA. Evita di memorizzare dati personali (PII, personally identifiable information) nei parametri del profilo e convalida la sicurezza API per proteggere i dati dei clienti.

+++
