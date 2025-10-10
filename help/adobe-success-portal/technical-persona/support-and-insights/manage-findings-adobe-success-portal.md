---
title: 'Gestire risultati nel portale [!DNL Adobe Success] '
description: Questa guida spiega come accedere, interpretare e agire sui risultati nel portale [!DNL Adobe Success] per aiutarti a gestire in modo proattivo i rischi relativi a prestazioni, sicurezza e funzionalità dei prodotti.
exl-id: c787ce29-993c-498c-9e39-8a04c2eeedda
source-git-commit: f23f0debcd6a0e2962524de321d436b854001495
workflow-type: ht
source-wordcount: '864'
ht-degree: 100%

---

# Gestire risultati nel portale [!DNL Adobe Success]

Questa guida spiega come accedere, interpretare e agire sui risultati nel portale [!DNL Adobe Success] per aiutarti a gestire in modo proattivo i rischi relativi a prestazioni, sicurezza e funzionalità dei prodotti.

Nella pagina **[!UICONTROL Risultati]** del portale [!DNL Adobe Success] sono visualizzati problemi o rischi rilevati nell’istanza del prodotto Adobe. I risultati includono problemi di prestazioni, sicurezza e funzionalità, insieme al loro stato e livello di rischio. Il monitoraggio di questa pagina consente di risolvere i problemi in anticipo, prima che influiscano sugli ambienti.

**Che cosa sono i risultati?**

I risultati sono avvisi relativi a insight di assistenza visualizzati nel portale [!DNL Adobe Success]. Evidenziano potenziali problemi nella configurazione del prodotto Adobe, come rallentamenti delle prestazioni, rischi per la sicurezza o configurazioni non corrette. Questi avvisi si basano sui dati di telemetria raccolti da strumenti come API, [!DNL New Relic] e [!DNL Splunk].

**Come vengono creati i risultati?**

I team di Adobe studiano regolarmente i problemi e le tendenze di assistenza più comuni. In base agli insight raccolti, vengono aggiunti nuovi controlli al sistema. Una volta al giorno, il portale [!DNL Adobe Success] analizza i dati dei prodotti per rilevare eventuali problemi, ad esempio configurazioni errate, processi bloccati o qualsiasi cosa che possa causare un’interruzione del sistema. Se un controllo rileva qualcosa che non rientra nell’intervallo di sicurezza (come definito dai team di prodotto e assistenza di Adobe), viene visualizzato come un risultato.

**Perché i risultati sono importanti**

Rivedere i risultati regolarmente aiuta a individuare i problemi in anticipo, prima che influiscano sul sistema o sulla clientela. Questo approccio proattivo migliora la stabilità del sistema, riduce i tempi di inattività e supporta le best practice.

**Come correggere i risultati**

Ogni risultato include consigli e istruzioni chiare su come risolvere il problema, insieme a collegamenti alla documentazione pertinente, se disponibile. Condividi questi risultati con il team IT, ingegneristico o partner Adobe e collabora con loro per affrontarli. La risoluzione anticipata di questi problemi consente di evitare problemi più gravi e mantiene il corretto funzionamento del sistema.


## Accedere ai risultati

Per visualizzare insight su un prodotto:

1. Passa a **[!UICONTROL Assistenza e insight]**.
1. Seleziona la scheda prodotto pertinente. Seleziona la scheda **[!UICONTROL Risultati]**.

   ![Portale Adobe Success che evidenzia i risultati in AEM as Cloud Service - Sono elencate risorse con 3 elementi](../../assets/asp-support-inisghts-findings.png "Visualizza i risultati di AEM Assets in Cloud Service")


1. Viene visualizzato un elenco di tutti i risultati per il prodotto selezionato.

   ![Portale Adobe Success che mostra la scheda Risultati per AEM Cloud Service - Sono elencate risorse con problemi di memorizzazione in cache](../../assets/adobe-success-portal-findings.png "Visualizza i risultati relativi alla memorizzazione in cache di AEM Assets in Cloud Service")

1. Da qui, puoi:

   ![L’interfaccia del portale Adobe Success che evidenzia la barra di ricerca, il pulsante di download e un risultato a rischio grave in AEM Sites](../../assets/adobe-success-portal-download.png "Cerca, scarica o visualizza i risultati di AEM Sites in Cloud Service")

   * Cerca voci specifiche.
   * Esporta l’elenco dei risultati selezionando **[!UICONTROL Scarica risultati]**. Per esportare un rapporto di un risultato, seleziona la casella di controllo accanto al risultato rilevante nella colonna **[!UICONTROL Nome risultato]**. Se non selezioni un risultato, per impostazione predefinita il PDF contiene un elenco di tutti i risultati.
   * Visualizza i dettagli di un risultato, inclusa una risoluzione consigliata, selezionando un risultato in **[!UICONTROL Nome risultato]**. Nella pagina dei dettagli del risultato viene visualizzato il risultato selezionato con contesto aggiuntivo e un consiglio. Per visualizzare questo rapporto, seleziona la freccia di download.


     ![Pulsante Scarica per esportare i dettagli dei risultati nel portale Adobe Success](../../assets/findings-details.png "Scarica il rapporto dei risultati")


## Intervenire in base ai risultati

Segui questi passaggi per verificare se ciascun risultato è ancora applicabile o può essere ignorato.

>[!NOTE]:
>
>Sulle istanze vengono eseguiti controlli standard. Se i controlli non rilevano la presenza del problema nella tua istanza, lo stato risulterà **[!UICONTROL Non rilevato]**.

1. Passa a **[!UICONTROL Assistenza e insight]**.
1. Seleziona la scheda prodotto pertinente.
1. Apri la scheda **[!UICONTROL Risultati]**. Puoi visualizzare tutti i risultati per il prodotto selezionato.
1. Seleziona una voce in **[!UICONTROL Nome risultato]**. Nella pagina dei dettagli del risultato:
   * Seleziona **[!UICONTROL Convalida]** per controllare se il problema è ancora presente (il pulsante **[!UICONTROL Convalida]** è progettato per confermare che il problema è stato risolto):

   ![Pulsante Convalida nel pannello Risultati per confermare la risoluzione dei problemi nel portale Adobe Success](../../assets/adobe-success-portal-validate.png "Pulsante Convalida")


   * Se il problema persiste, viene visualizzato il seguente messaggio: *[!UICONTROL Convalida completata. Risultato ancora rilevato]*. Utilizza le informazioni e i consigli nella pagina dei dettagli del risultato per indagare e risolvere.
   * Se il problema non è più presente, viene visualizzato il seguente messaggio: *[!UICONTROL Convalida completata. Risultato non più rilevato]*. Quando non viene più rilevato, il risultato viene visualizzato in grigio e lo stato diventa **[!UICONTROL Non rilevato]**. I risultati con stato **[!UICONTROL Non rilevato]** si trovano in fondo all’elenco dei risultati.
   * Se il problema non è applicabile o rilevante per te, puoi ignorarlo selezionando **[!UICONTROL Ignora]**. Quando viene ignorato, il risultato viene visualizzato in grigio e lo stato diventa **[!UICONTROL Ignorato]**.  I risultati con stato **[!UICONTROL Ignorato]** si trovano in fondo all’elenco dei risultati.

## Informazioni sui risultati

* **[!UICONTROL Nome risultato]**: seleziona per informazioni dettagliate e passaggi di risoluzione consigliati.
* **[!UICONTROL Tipo]**: categorizzato come *Funzionalità*, *Prestazioni* e *Sicurezza*.
* **[!UICONTROL Livello di rischio]**: indicatore di gravità, con indicatori visivi.
* **[!UICONTROL Stato]**: stato corrente del risultato (ad esempio *Rilevato*, *Non rilevato*, *Ignorato*).
* **[!UICONTROL Ultima esecuzione del controllo]**: marca temporale dell’ultimo controllo che ha aggiornato il risultato.


## Best practice

Nella pagina **[!UICONTROL Risultati]** sono elencati i consigli con i seguenti livelli di rischio: **[!UICONTROL Alto]**, **[!UICONTROL Elevato]** e **[!UICONTROL Medio]**. **[!UICONTROL Alto]** è critico, **[!UICONTROL Elevato]** è urgente e **[!UICONTROL Medio]** è non critico. Per mantenere l’integrità e le prestazioni del sito:

* Risolvi immediatamente i problemi ad **[!UICONTROL alto rischio]**, in quanto rappresentano minacce critiche.
* Risolvi i problemi a rischio **[!UICONTROL elevato]** per evitare un’aggravamento.
* Monitora regolarmente i risultati a rischio **[!UICONTROL medio]** e agisci come necessario.
