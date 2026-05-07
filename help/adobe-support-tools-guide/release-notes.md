---
title: Note sulla versione del supporto Experience League
description: Informazioni aggiornate sulla versione del supporto Experience League.
feature: Release Notes
exl-id: 875ad82e-56b5-4d58-9237-bb7aa0d9ffaf
source-git-commit: eb474379539945e0bbfca35e9f83f1ece61a16b6
workflow-type: tm+mt
source-wordcount: '973'
ht-degree: 1%

---

# Note sulla versione del supporto Experience League

Queste note sulla versione contengono aggiornamenti al supporto Experience League e includono:

![Nuove](../adobe-support-tools-guide/assets/new.svg) nuove funzionalità
![Correzioni](../adobe-support-tools-guide/assets/fix.svg) correzioni e miglioramenti
![Bug](../adobe-support-tools-guide/assets/bug.svg) problemi noti

## 7 maggio 2026 - Espansione della funzione Richiedi richiamata

La funzione Richiedi callback è ora disponibile sia per Adobe Commerce che per Adobe GenStudio. I clienti di Adobe Commerce possono pianificare un callback in un momento che funziona meglio per loro, mentre i clienti di Adobe GenStudio possono richiedere un callback immediato o pianificato.

## 27 aprile 2026 - Miglioramenti alla gestione dell’escalation e a System Insights per Adobe Commerce

### Gestione delle escalation

1. La gestione delle escalation con il supporto Experience League offre una nuova serie di funzionalità self-service per offrire maggiore visibilità ai casi di supporto grazie a un flusso di lavoro semplificato e basato su sistemi, basato sulle tue esigenze.

1. Ottieni istantaneamente un’istantanea basata sull’intelligenza artificiale del tuo caso di supporto, con informazioni sullo stato corrente, sui passaggi successivi, sugli aggiornamenti principali e un riepilogo completo del caso, senza dover leggere l’intera cronologia del caso.

1. Una nuova opzione **[!UICONTROL Ottieni assistenza]** offre ai clienti un&#39;esperienza centralizzata per collaborare senza problemi con i team di supporto, fornendo informazioni sulla risoluzione dei problemi, le richieste di richiamata, gli aggiornamenti self-service per l&#39;urgenza dei problemi e le richieste di attenzione da parte della gestione.

1. **[!UICONTROL Richiedi chiamata immediata]** - Per i casi P1-critici, richiedi una chiamata immediata da un tecnico dell&#39;assistenza direttamente dall&#39;elenco dei casi. Fornisci semplicemente il tuo numero di telefono e una breve descrizione del problema; un tecnico dell’assistenza ti contatterà non appena sarà disponibile.

1. **[!UICONTROL Richiedi una chiamata pianificata]** - Per i casi P2-Urgente e P3-Importante, pianifica una riunione Web con un tecnico del supporto tecnico in una data e in un orario adatti alle tue esigenze. Al momento della prenotazione verrà confermata una sessione di condivisione schermo Microsoft Teams con tutti i dettagli della riunione.

1. **[!UICONTROL Modifica nell&#39;urgenza del problema]** - Per i casi P3-importanti e P4-minori, self-service aumenta la priorità del caso da P4-minori a P2-urgenti fornendo una breve giustificazione. È possibile modificare la richiesta di priorità senza che il ticket comporti una riassegnazione.

1. **[!UICONTROL Ho un problema non elencato]** - Per tutte le priorità, genera un&#39;escalation per qualsiasi scenario non coperto dalle opzioni precedenti, ad esempio **[!UICONTROL Tempo alla risoluzione]**, **[!UICONTROL La risoluzione non ha soddisfatto le aspettative]**, **[!UICONTROL Abilità di comunicazione agente]** o **[!UICONTROL Conoscenza tecnica agente]**.

### Informazioni di sistema nel modulo per la creazione di casi per Adobe Commerce

1. System Insights rileva automaticamente i problemi rilevati nell’ambiente. Include rallentamenti delle prestazioni, rischi per la sicurezza e configurazioni errate utilizzando dati di telemetria da API, New Relic e [!DNL Splunk]. Questo consente di identificare e risolvere i problemi più rapidamente.

1. System Insights è attualmente disponibile esclusivamente per Adobe Commerce sul supporto Experience League durante il processo di creazione del caso.

1. Le informazioni vengono estese all’istanza di progetto specifica, per garantire che siano pertinenti per l’ambiente in uso.

1. Gli approfondimenti includono una descrizione dettagliata, i passaggi da risolvere, l’analisi della causa principale e i collegamenti alla documentazione Adobe pertinente.

1. Gli utenti possono inviare feedback su singole informazioni per aiutare Adobe a migliorare continuamente l’accuratezza e la rilevanza di System Insights.

## 23 aprile 2026 - Espansione della funzione Richiedi richiamata

La funzione di richiesta di callback è ora disponibile per gli utenti dei prodotti Analytics, Admin Console, Audience Manager e Target.

## 8 aprile 2026 - Espansione della funzione Richiedi richiamata

La funzione Richiedi richiamata è ora disponibile per gli utenti di prodotti Marketo.

## 30 marzo 2026 - Modulo per casi avanzati

![Nuovo](../adobe-support-tools-guide/assets/new.svg) Il modulo del caso è organizzato in un flusso guidato che aiuta gli utenti a capire quali informazioni sono necessarie in ogni fase:

- [!UICONTROL Selezione prodotti]
- [!UICONTROL Descrizione del problema]
- [!UICONTROL Informazioni di sistema]
- [!UICONTROL Priorità e impatto aziendale]
- [!UICONTROL Informazioni di contatto e elenco dei controllori]
- [!UICONTROL Rivedi e invia]

![Nuovo](../adobe-support-tools-guide/assets/new.svg) è stata aggiunta la generazione automatica del titolo in base alla **[!UICONTROL Descrizione problema]**, che consente la generazione automatica del titolo, lasciando agli utenti la possibilità di modificarlo prima di inviare il caso.

![Nuovo](../adobe-support-tools-guide/assets/new.svg) aggiunto un **[!UICONTROL &quot;Il problema è riproducibile?&quot;]** per migliorare la risoluzione dei problemi. Se gli utenti selezionano **[!UICONTROL Sì]**, verrà richiesto di fornire i passaggi necessari per riprodurre il problema. Se è selezionato *No*, gli utenti possono procedere con l&#39;invio del caso.

![New](../adobe-support-tools-guide/assets/new.svg) ha aggiunto un&#39;opzione per indicare se sono state apportate modifiche recenti all&#39;ambiente o all&#39;istanza. Se è selezionato **[!UICONTROL Sì]**, agli utenti verrà richiesto di fornire ulteriori dettagli sulle modifiche.

![Nuovo](../adobe-support-tools-guide/assets/new.svg) Aggiunto **Ulteriori [!UICONTROL Campi Contesto dell&#39;ambiente]** per i prodotti autorizzati per acquisire i dettagli critici:

- **Marketo**
   - ID Munchkin
- **Adobe Target**
   - Nome attività
   - URL sito (nome proprietà tag)
- **Adobe Analytics**
   - RSID
   - URL del sito (nome proprietà tag) / cURL
   - Collegamento Workspace
- **Adobe Journey Optimizer (AJO)**
   - ID percorso o URL/ID campagna o URL/ID canale o URL/ID Offer Decisioning o URL
   - Esempio di profilo
   - Nome sandbox
- **Real-Time Customer Data Platform (RTCDP)**
   - ID componente interessato (ID destinazione/ID pubblico/ID set di dati/ID flusso di dati/ID criterio di unione/ID schema/ID Source/ID batch)
   - Esempio di profilo
   - Nome sandbox
- **Adobe Experience Platform (AEP)**
   - ID componente interessato (ID destinazione/ID pubblico/ID set di dati/ID flusso di dati/ID criterio di unione/ID schema/ID Source/ID batch)
   - Esempio di profilo
   - Nome sandbox
- **Customer Journey Analytics (CJA)**
   - URL progetto Workspace
   - ID connessione / Messaggio di errore / Codice
   - ID visualizzazione dati

![New](../adobe-support-tools-guide/assets/new.svg) ha aggiunto un **pannello [!UICONTROL Recommendations]** basato sull&#39;intelligenza artificiale per visualizzare indicazioni utili senza interrompere il flusso di creazione dei casi.

![Nuovo](../adobe-support-tools-guide/assets/new.svg) Aggiunto **[!UICONTROL Riepilogo recensioni]** passaggio per fornire una visualizzazione consolidata di tutte le informazioni immesse e consentire agli utenti di:

- Rivedere i dettagli del caso in un&#39;unica posizione
- Torna ai passaggi precedenti per apportare modifiche
- Torna al riepilogo senza perdere l’avanzamento

![Correzione](../adobe-support-tools-guide/assets/fix.svg) del campo Descrizione caso rinominato in *[!UICONTROL &quot;Descrivere il problema&quot;]* per una maggiore chiarezza.

![Correzione](../adobe-support-tools-guide/assets/fix.svg) asterischi aggiunti (*) come indicatori di campo obbligatori per garantire la completezza e ridurre gli errori di invio.

## 18 marzo 2026 - Espansione della funzione Richiedi richiamata

Experience League ora offre l’opzione Richiedi richiamata, che consente la pianificazione self-service delle riunioni web con funzionalità di condivisione dello schermo per una risoluzione più rapida dei problemi.

- Questa funzione è disponibile per Adobe Experience Manager, Campaign e Workfront.
- I clienti possono programmare le riunioni secondo le proprie esigenze e ricevere inviti immediati.
- Per i casi Adobe Experience Manager P1, i callback immediati garantiscono un coinvolgimento più rapido durante i problemi critici, contribuendo a ridurre al minimo i tempi di inattività e l&#39;impatto aziendale.
