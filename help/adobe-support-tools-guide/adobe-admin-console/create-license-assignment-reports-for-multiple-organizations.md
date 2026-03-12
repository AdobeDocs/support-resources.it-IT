---
title: Creazione di report di assegnazione licenze per più organizzazioni e prodotti
description: Genera, visualizza e scarica rapporti sull’assegnazione delle licenze da più organizzazioni e prodotti da Global Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: e3380a89-8529-473f-bd17-efb05466eab9
source-git-commit: dbbd971e57265e1651f44f834e56d461159ab4fc
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 1%

---

# Creazione di report di assegnazione licenze per più organizzazioni e prodotti

Scopri come gli amministratori globali possono generare e scaricare rapporti dettagliati sulle licenze per più organizzazioni e prodotti per intervalli di date specifici per facilitare il tracciamento preciso del provisioning delle licenze.

>[!NOTE]
>
>Per creare, visualizzare ed esportare un report di assegnazione licenze, accedere a [Global Admin Console](https://global-admin-console.adobe.com/) e passare a **[!UICONTROL Insights]** > **[!UICONTROL Report]** > **[!UICONTROL Assegnazione licenza]**.

## Creare un rapporto

I rapporti sull’assegnazione delle licenze consentono di monitorare in modo proattivo il provisioning delle licenze e ridurre il tracciamento manuale. Gli amministratori globali possono creare un rapporto di assegnazione delle licenze per determinati prodotti per un numero qualsiasi di organizzazioni figlio, al fine di monitorare i dati di provisioning delle licenze software in tutti i reparti.

1. Vai alla scheda **[[!UICONTROL Approfondimenti]](https://global-admin-console.adobe.com/insights)** in Global Admin Console.
1. Nella pagina **[!UICONTROL Assegnazione licenza]**, selezionare **[!UICONTROL Crea report]**.
1. Seleziona le organizzazioni e seleziona **[!UICONTROL Avanti]**. È possibile scegliere singolarmente ogni organizzazione o selezionare tutte le organizzazioni figlio all&#39;interno di un padre utilizzando il pulsante **[!UICONTROL Seleziona tutto]**.

>[!NOTE]
>
>**Impossibile selezionare alcune organizzazioni**:
>Se un&#39;organizzazione figlio non dispone di un contratto o dispone di un contratto aziendale separato con lo stesso prodotto dell&#39;organizzazione padre, non è in grado di creare un rapporto di assegnazione delle licenze. Ad esempio, se il contratto dell’organizzazione principale ha Adobe Acrobat e l’organizzazione secondaria ha lo stesso valore come parte di un altro contratto, l’allocazione del prodotto è limitata. Di conseguenza, è anche limitato per la creazione di rapporti in Global Admin Console. [Scopri come tenere traccia del provisioning per tali organizzazioni utilizzando i rispettivi Admin Console](https://helpx.adobe.com/it/enterprise/using/assignment-reports.html).
>
>[!NOTE]
>
>È possibile creare rapporti sulle assegnazioni solo per le organizzazioni con un contratto attivo.

1. Selezionare i prodotti da includere nel report e selezionare **[!UICONTROL Avanti]**.

>[!NOTE]
>
>**Impossibile selezionare alcuni prodotti**:
>I prodotti che non sono allocabili in Global Admin Console non sono inclusi per la creazione di rapporti. Attualmente sono inclusi alcuni prodotti Digital Experience come [!DNL Workfront], [!DNL Adobe Experience Manager] e [!DNL Adobe Experience Platform] e anche prodotti come [!DNL Adobe Firefly Services], [!DNL Acrobat Sign] e [!DNL Adobe Stock]. [Utilizzare Adobe Admin Console per trovare i dati di provisioning licenze per questi prodotti](https://helpx.adobe.com/it/enterprise/using/assignment-reports.html).

1. Seleziona se aggregare il rapporto per mese o anno.
1. Seleziona un intervallo di date personalizzato o scegli tra le opzioni predefinite. Puoi scegliere una data di inizio qualsiasi dal 18 giugno 2020 fino al giorno precedente, purché non preceda la data di inizio del contratto.
1. Seleziona **[!UICONTROL Scarica]** per esportare il rapporto come file CSV.

Il report inizia l&#39;elaborazione e viene visualizzato nella pagina **[!UICONTROL Assegnazione licenza]** con dettagli quali nome, creatore, ora di creazione, intervallo di date e stato. Quando è pronto, ricevi una notifica e-mail e il rapporto viene scaricato automaticamente.

Qualsiasi amministratore globale può scaricare il report in qualsiasi momento dopo che è pronto, utilizzando l&#39;icona **[!UICONTROL Scarica]** accanto al nome del report.

>[!NOTE]
>
>- Per garantire che vengano rispecchiati i dati più recenti, genera rapporti 48 ore dopo qualsiasi allocazione.
>- I rapporti vengono conservati per 90 giorni dopo la loro generazione.

## Visualizzare e scaricare i rapporti generati in precedenza

Gli amministratori globali possono visualizzare e scaricare i rapporti sull’assegnazione delle licenze generati da qualsiasi altro amministratore globale dell’organizzazione. Tuttavia, i visualizzatori globali possono solo visualizzare l’elenco dei rapporti sulle assegnazioni delle licenze.

1. Vai alla scheda **[[!UICONTROL Approfondimenti]](https://global-admin-console.adobe.com/insights)** in Global Admin Console.
1. Nella pagina **[!UICONTROL Assegnazione licenza]**, tutti i report sono elencati con i dettagli seguenti:

   | Campo | Descrizione |
   | ------------- | ------------------------------------------------------------------------------------------------- |
   | Nome | Generato automaticamente e non può essere modificato. |
   | Creatore | L’amministratore globale che ha generato il rapporto. |
   | Ora di creazione | L’ora di sistema in cui è stato creato il rapporto. |
   | Intervallo date | L’intervallo di date selezionato per il rapporto. |
   | Stato | **Operazione completata** se il report è pronto per il download o **Elaborazione** se è ancora in fase di generazione. |

1. Per esportare il report come file CSV, seleziona l&#39;icona **[!UICONTROL Scarica]** accanto al report.

## Conoscere il rapporto di assegnazione delle licenze

Il rapporto scaricato contiene le seguenti informazioni per ogni evento:

| Campo | Descrizione |
| -------------------------------- | -------------------------------------------------------- |
| ID organizzazione | ID univoco associato all’organizzazione principale |
| Nome organizzazione | Nome dell’organizzazione principale |
| ID organizzazione figlio | Identificatore univoco dell’organizzazione figlio selezionata |
| Nome organizzazione figlio | Nome dell’organizzazione figlio |
| ID licenza | ID univoco della licenza del prodotto |
| Nome del prodotto | Nome del prodotto selezionato |
| Data | Selezione data |
| Qtà licenza totale | Numero totale di licenze a livello di organizzazione principale |
| Licenze figlio | Numero di licenze allocato all’organizzazione figlio |
| Qtà assegnata di picco mensile/annuale | Valore aggregato del provisioning delle licenze (mensile/annuale) |
