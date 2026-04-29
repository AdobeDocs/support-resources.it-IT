---
title: Approfondimenti sistema
description: System Insights identifica in modo proattivo potenziali problemi negli ambienti Adobe Commerce. L’analisi delle informazioni durante la creazione dei casi riduce i tempi di risoluzione, aiuta a prevenire interruzioni e supporta una distribuzione stabile e sicura.
hide: true
source-git-commit: f9a38443243d230c76d968ca7a67c4ba29d07a26
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---

# Approfondimenti sistema

System Insights fornisce risultati proattivi che aiutano a identificare potenziali problemi di prestazioni, sicurezza e funzionalità in una configurazione di prodotto Adobe. Questi insights evidenziano rischi quali il degrado delle prestazioni, vulnerabilità di sicurezza o configurazioni non corrette basate sui dati di telemetria raccolti dagli strumenti di osservabilità, tra cui API, New Relic e [!DNL Splunk].

System Insights viene visualizzato durante il processo di creazione del caso e aiuta ad accelerare la diagnosi e la risoluzione.

## Creazione di System Insights

I team di Adobe analizzano continuamente i problemi di supporto comuni e le tendenze emergenti. Sulla base di questi risultati, Adobe aggiunge al sistema i controlli automatizzati.

Questi controlli analizzano la configurazione del prodotto per rilevare problemi quali configurazioni errate, processi bloccati o condizioni che potrebbero causare problemi funzionali o interruzioni del sistema.

Quando un controllo identifica un valore o uno stato al di fuori dell’intervallo sicuro definito dai team di prodotto e supporto di Adobe, il sistema lo fa emergere come Insight di sistema.

## Perché System Insights conta

La revisione regolare di System Insights aiuta a identificare i problemi in anticipo, prima che influiscano sulla stabilità del sistema o sulla customer experience. Questo approccio proattivo:

- Migliora l&#39;affidabilità della piattaforma
- Riduzione del downtime
- Consente di mantenere le best practice consigliate da Adobe

## Disponibilità e ambito

System Insights è attualmente disponibile solo per Adobe Commerce. Queste informazioni vengono visualizzate durante il processo di creazione del caso sul supporto Experience League e sono disponibili anche tramite [Site-Wide Analysis Tool (SWAT)](https://experienceleague.adobe.com/it/docs/commerce-operations/tools/site-wide-analysis-tool/intro).

>[ !Nota]
>
>System Insights visualizza i dati solo per gli ambienti di produzione.

## Accesso a System Insights

Le informazioni di sistema vengono visualizzate in tutto il flusso di lavoro di creazione del caso. Man mano che vengono immessi i dettagli del problema, il pannello **[!UICONTROL System Insights]** viene visualizzato sul lato destro della schermata, sotto la sezione dei consigli basati sull&#39;intelligenza artificiale. Per ulteriori informazioni sui consigli basati sull&#39;intelligenza artificiale, consulta [Compila il ticket di supporto](https://experienceleague.adobe.com/it/docs/support-resources/adobe-support-tools-guide/adobe-customer-support-experience#fill-out-the-support-ticket) nell&#39;articolo sull&#39;esperienza di supporto clienti di Adobe.

Il pannello visualizza un elenco scorrevole di approfondimenti con ambito per l’istanza di progetto specifica. L&#39;ambito si basa sulle informazioni immesse nel campo **[!UICONTROL URL progetto]**. Immetti l&#39;**[!UICONTROL URL progetto]** con precisione per garantire che le informazioni riflettano l&#39;ambiente corretto.

Una volta caricato, il pannello mostra un elenco scorrevole delle schede insight contrassegnate per il tuo ambiente. Ogni scheda di insight include:

- Titolo che riepiloga il problema
- Breve descrizione di insight

![Accedi alle risorse di supporto](/help/adobe-support-tools-guide/assets/access-support-resources.png)

Per visualizzare i dettagli completi di insight, seleziona una scheda insight dall’elenco. La vista dettagliata fornisce le seguenti informazioni:

- Nome Insight
- Prodotto Adobe in cui è segnalato insight
- Tipo di Insight, suddiviso in categorie:
   - [!UICONTROL Funzionalità]
   - [!UICONTROL Prestazioni]
   - [!UICONTROL Sicurezza]
- [!UICONTROL Livello di rischio] che indica la gravità
- [!UICONTROL Ultima esecuzione controllo] indica quando è stato rilevato il risultato.
- [!UICONTROL Insight Source], fornito dallo strumento di analisi a livello di sito (SWAT)
- Una spiegazione dettagliata del problema e del suo potenziale impatto, insieme a passaggi attuabili per indagare e affrontare il problema. La vista dettagliata illustra inoltre le cause tipiche di questo tipo di problema e include collegamenti alla documentazione pertinente di Adobe per riferimento aggiuntivo.

![Fai clic sulla scheda del caso](/help/adobe-support-tools-guide/assets/click-case-card.png)

Rivedi tutte le informazioni nel pannello prima di procedere, in quanto un insight può risolvere direttamente il problema che si sta riscontrando.

## Intervenire su un insight

Dopo aver esaminato un’insight, scegli una delle azioni seguenti.

### Continua la creazione del caso

Se il problema persiste o richiede ulteriore assistenza, selezionare **[!UICONTROL Continua creazione caso]**. Il sistema conserva tutte le informazioni sul caso precedentemente immesse.

### Contrassegna il problema come risolto

Se insight risolve il problema e non è più necessario un caso di supporto, selezionare **[!UICONTROL Problema risolto]**.

Quando questa opzione è selezionata:

- Viene visualizzata una finestra di dialogo di conferma.
- La finestra di dialogo indica che tutti i dati del caso immessi verranno cancellati definitivamente.

![Azione su un insight](/help/adobe-support-tools-guide/assets/issue-resolved.png)

Seleziona **[!UICONTROL Fine]** per confermare e tornare alla pagina **[!UICONTROL Casi personali]**. Seleziona **[!UICONTROL Annulla]** per tornare alla visualizzazione dettagli di insight.

![Cancella modulo caso](/help/adobe-support-tools-guide/assets/clear-case-form.png)

## Invio di feedback su un insight

Nella parte inferiore di ogni visualizzazione dei dettagli di insight è possibile fornire un feedback sull’utilità o meno dell’insight. Questo feedback aiuta Adobe a migliorare continuamente la pertinenza e l’accuratezza di System Insights.

![Fornisci feedback](/help/adobe-support-tools-guide/assets/submit-feedback.png)

Per fornire un feedback:

1. Apri una vista dei dettagli di insight.
2. Scorri fino alla parte inferiore del pannello.
3. Individuare il prompt **[!UICONTROL È stato utile? Invia feedback.]**
4. Selezionare una delle opzioni seguenti:
   - Icona **Miniatura** se insight è stato utile
   - Icona **Miniatura** se insight non è stato utile
5. (Facoltativo) Inserire commenti aggiuntivi.
6. Seleziona **[!UICONTROL Invia]** per inviare un feedback oppure **[!UICONTROL Ignora]** per chiudere la sezione del feedback senza inviarlo.
