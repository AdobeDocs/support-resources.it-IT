---
title: Gestione delle escalation
description: La gestione delle escalation fornisce opzioni self-service nel supporto Experience League per visualizzare i riepiloghi dei casi, richiedere callback, pianificare le sessioni di risoluzione dei problemi, aggiornare l’urgenza dei casi e gestire le escalation del supporto.
source-git-commit: d41e987c8778849311922d1b9438c2c74fb60138
workflow-type: tm+mt
source-wordcount: '1148'
ht-degree: 1%

---

# Gestione delle escalation

**Gestione escalation** è una funzionalità self-service del supporto Adobe Experience League. Consente ai clienti di intervenire direttamente sui casi di supporto, fornisce visibilità dei casi in tempo reale tramite riepiloghi generati dall’intelligenza artificiale e offre opzioni di escalation strutturate per supportare una risoluzione più rapida dei problemi critici.

## Riepilogo del caso

La funzionalità **[!UICONTROL Riepilogo casi]** fornisce una panoramica generata da IA di un caso di supporto. Vengono riepilogati i commenti, le azioni e le interazioni fino ad oggi in modo da poter esaminare lo stato più recente senza leggere l’intera cronologia del caso.

Per accedere al **[!UICONTROL Riepilogo del caso]**, effettua le seguenti operazioni:

1. Passa a **[!UICONTROL I miei casi]** nel supporto Adobe Experience League.
2. Trovare il caso da esaminare dall&#39;elenco dei casi.
3. Nella colonna **[!UICONTROL Riepilogo casi]** fare clic su **Riepilogo casi** per il caso.

![Riepilogo casi](/help/adobe-support-tools-guide/assets/case-summary.png)

Viene visualizzato il pannello Riepilogo caso e viene visualizzato il riepilogo generato dall&#39;intelligenza artificiale con le seguenti informazioni:

- Prodotto Adobe per il quale viene inviata la controversia
- Il numero di giorni in cui la controversia è stata aperta
- **Stato corrente** - Un&#39;istruzione concisa dell&#39;avanzamento corrente del caso
- **Passaggi successivi**: una descrizione delle azioni intraprese dal team di supporto o dal team di progettazione e dei passaggi successivi.
- **Riepilogo** - Dettagli sul problema, inclusa la descrizione del problema e l&#39;impatto aziendale
- **Aggiornamenti chiave** - Un elenco cronologico di azioni e aggiornamenti significativi per il caso fino ad oggi.

>[!NOTE]
>
>L&#39;indicatore dello stato del caso visualizza lo stato corrente del caso. Se il caso è aperto, viene visualizzato il numero di giorni in cui il caso è stato aperto, ad esempio **Apri per 6 giorni**. Se il caso è chiuso, viene visualizzato **[!UICONTROL Chiuso]**.

![Riepilogo casi IA](/help/adobe-support-tools-guide/assets/ai-case-summary.png)

## Ottieni aiuto

La funzionalità **[!UICONTROL Ottieni aiuto]** consente ai clienti di sollevare e gestire le richieste di assistenza direttamente dall&#39;elenco dei casi, senza contattare il supporto tramite e-mail o telefono. In base alla priorità del caso, il supporto Adobe Experience League visualizza le opzioni di escalation self-service pertinenti.

Per accedere a **[!UICONTROL Visualizza la Guida]**, eseguire la procedura seguente:

1. Passa a **[!UICONTROL I miei casi]** nel supporto Adobe Experience League.
1. Individuare il caso da inoltrare dall&#39;elenco dei casi.
1. Nella colonna **[!UICONTROL Guida aggiuntiva]**, fare clic su **[!UICONTROL Visualizza la Guida]** per il caso.

   >[!NOTE]
   >
   >L&#39;opzione **[!UICONTROL Ottieni aiuto]** è disponibile solo per i casi aperti e non viene visualizzata per i casi chiusi.

1. Esaminare il pannello Riassegnazione. Visualizza il prodotto selezionato, la priorità del caso, l’ID del caso e le opzioni di riassegnazione disponibili. Le opzioni disponibili includono:

   - [!UICONTROL Richiedi chiamata immediata]
   - [!UICONTROL Richiedi una chiamata pianificata]
   - [!UICONTROL Modifica dell&#39;urgenza del problema]
   - [!UICONTROL Ho un problema non elencato]

![Guida](/help/adobe-support-tools-guide/assets/get-help.png)

### Richiedi chiamata immediata

L&#39;opzione **[!UICONTROL Richiedi chiamata immediata]** è disponibile per i casi **P1-Critical**. Utilizza questa opzione per richiedere un callback immediato sul telefono da un tecnico del supporto tecnico.

>[!NOTE]
>
>È possibile richiedere un solo callback alla volta. Puoi richiedere un altro callback al termine della prima chiamata.

>[!NOTE]
>
>Questa opzione è disponibile per tutti i prodotti eccetto Adobe Experience Platform (AEP), [!DNL Commerce] e [!DNL GenStudio].

Per richiedere un callback immediato, segui i passaggi descritti di seguito:

1. Nel pannello **[!UICONTROL Visualizza Guida]**, selezionare **[!UICONTROL Richiedi chiamata immediata]**, quindi fare clic su **[!UICONTROL Continua]**.
1. Viene visualizzato il modulo di richiesta di callback, precompilato con il prodotto, la priorità e l’ID caso selezionati. Compila i campi obbligatori nel modulo.
   - Immetti il numero di telefono per ricevere il callback.
   - Immettere una breve descrizione del problema o il motivo della richiesta di callback (fino a 1.000 caratteri).
1. Fai clic su **[!UICONTROL Richiedi callback]** per inviare la richiesta oppure fai clic su **[!UICONTROL Indietro]** per tornare alla schermata precedente.

Dopo aver inviato la richiesta, viene visualizzata la schermata di conferma:

- [!UICONTROL Adobe ID]
- Numero di telefono
- Prodotto
- ID caso
- Titolo caso
- Priorità

Un tecnico del supporto tecnico ti contatta non appena disponibile. Fai clic su **[!UICONTROL Chiudi]** per ignorare la conferma.

### Richiedi una chiamata pianificata

L&#39;opzione **[!UICONTROL Richiedi una chiamata pianificata]** è disponibile per **P2-Urgent** e **P3-Importante** casi. Utilizzare questa opzione per pianificare una riunione Web di condivisione dello schermo con un tecnico del supporto tecnico in una data e in un orario adatti alle proprie esigenze.

>[!NOTE]
>
>Puoi pianificare una sola chiamata alla volta. Al termine della riunione corrente, è possibile pianificare un&#39;altra chiamata.

>[!NOTE]
>
>Questa opzione è disponibile per tutti i prodotti eccetto Adobe Experience Platform (AEP), [!DNL Commerce] e [!DNL GenStudio].

Per richiedere una chiamata pianificata, segui i passaggi seguenti:

1. Nel pannello **[!UICONTROL Visualizza Guida]**, selezionare **[!UICONTROL Richiedi una chiamata pianificata]**, quindi fare clic su **[!UICONTROL Continua]**.
1. Viene visualizzato un modulo di pianificazione, precompilato con il prodotto, la priorità e l’ID del caso selezionati. Compila i campi obbligatori nel modulo.
   - **[!UICONTROL Di cosa vuoi parlare?]**: fornisci una breve descrizione per aiutare il tecnico del supporto a prepararsi (fino a 1.000 caratteri).
   - **[!UICONTROL Seleziona data]**: seleziona una data dal calendario.
   - **[!UICONTROL Seleziona la data e l&#39;ora]**: seleziona un&#39;ora disponibile per la data scelta.
1. Selezionare la casella di controllo di conferma per confermare che il contenuto personale o sensibile sia chiuso prima della condivisione dello schermo.
1. Fai clic su **[!UICONTROL Pianifica chiamata]** per confermare la prenotazione oppure fai clic su **[!UICONTROL Indietro]** per tornare alla schermata precedente.

Dopo aver pianificato la riunione, viene visualizzata la schermata di conferma:

- Adobe ID
- Collegamento riunione
- Data riunione
- Ora riunione
- Fuso orario
- Priorità
- ID caso
- Prodotto
- Ingegnere di supporto
- Titolo caso

È disponibile un ingegnere del supporto tecnico che assiste mediante la condivisione dello schermo all’orario pianificato. L&#39;invito alla riunione include un collegamento Microsoft Teams per partecipare. Seleziona **[!UICONTROL Chiudi]** per ignorare la conferma.

### Modifica dell’urgenza del problema

L&#39;opzione **[!UICONTROL Modifica dell&#39;urgenza del problema]** è disponibile per **Casi importanti** e **Casi minori** di tipo P3. Utilizzare questa opzione per modificare la priorità del caso fino a **P2-Urgent**.

>[!NOTE]
>
>È possibile modificare la priorità da **P4-Minor** a **P3-Importante** o da **P3-Importante** a **P2-Urgente** una volta ogni 24 ore.

Per modificare l’urgenza di un problema, effettua le seguenti operazioni:

1. Nel pannello **[!UICONTROL Visualizza Guida]**, seleziona **[!UICONTROL Modifica in urgenza problema]**.
1. Viene visualizzato un campo di testo in linea. Sul campo, descrivi chiaramente cosa è cambiato o perché il problema richiede un&#39;attenzione immediata.
1. Fai clic su **[!UICONTROL Aggiorna urgenza problema]** per inviare la richiesta oppure fai clic su **[!UICONTROL Annulla]** per uscire senza apportare modifiche.

   Dopo aver inviato la richiesta, viene visualizzata la schermata di conferma:

   - Prodotto selezionato
   - Priorità
   - ID caso

1. Fai clic su **[!UICONTROL Torna al modulo]** per tornare al caso.

### Si è verificato un problema non elencato

L&#39;opzione **[!UICONTROL Ho un problema non elencato]** è disponibile per tutte le priorità dei casi e consente l&#39;escalation quando altre opzioni disponibili non risolvono il problema. Questa opzione assicura che il caso riceva l&#39;attenzione diretta di un tecnico del supporto.

Segui i passaggi seguenti per effettuare l’escalation nel caso in cui i tuoi problemi non siano elencati:

1. Nel pannello **[!UICONTROL Visualizza Guida]**, seleziona **[!UICONTROL Un problema non è presente nell&#39;elenco]**. Vengono visualizzati due campi in linea.
1. Completa i campi in linea:
   - **[!UICONTROL Perché inoltrare il caso?]**
   - **[!UICONTROL Informazioni dettagliate sono utili.]**
1. Nel menu a discesa, seleziona un motivo di escalation:
   - [!UICONTROL Tempo alla risoluzione]
   - [!UICONTROL La risoluzione non ha soddisfatto le aspettative]
   - [!UICONTROL Abilità di comunicazione agente]
   - [!UICONTROL Informazioni tecniche sull&#39;agente]
1. Nel campo di testo libero, fornisci contesto aggiuntivo sull’escalation.
1. Fai clic su **[!UICONTROL Inoltra caso]** per inviare l&#39;inoltro oppure fai clic su **[!UICONTROL Annulla]** per uscire senza inviare.

   Dopo aver inviato l’escalation, viene visualizzata la schermata di conferma:

   - Prodotto selezionato
   - Priorità
   - ID caso

1. Fai clic su **[!UICONTROL Torna al modulo]** per tornare al caso.
