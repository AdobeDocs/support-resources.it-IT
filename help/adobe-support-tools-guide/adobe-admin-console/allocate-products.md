---
title: Allocare prodotti alle organizzazioni figlio tramite Global Admin Console
description: Scopri come gli amministratori globali possono distribuire le risorse alle organizzazioni figlie, consentendo una gestione efficace delle risorse e l’assegnazione degli utenti all’interno di ogni organizzazione.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: de6e785d-8965-40d5-ac78-7fbb2cd7afc7
source-git-commit: d5f0473b100cda574b4980e6c871a9c275f9f95a
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# Allocare prodotti alle organizzazioni figlio tramite Global Admin Console

Applicabile all&#39;azienda.

Scopri come gli amministratori globali possono distribuire le risorse alle organizzazioni figlie, consentendo una gestione efficace delle risorse e l’assegnazione degli utenti all’interno di ogni organizzazione.

In [Global Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration), vai alla scheda **[!UICONTROL Allocazione prodotto]**, quindi seleziona un prodotto da allocare alle organizzazioni figlio.

Accedi a [Global Admin Console](https://global-admin-console.adobe.com).

>[!NOTE]
>
>**[!UICONTROL Allocazione prodotto]** è disponibile solo per i contratti Enterprise Term License Agreement (ETLA).

La distribuzione e l’amministrazione dei prodotti Adobe tra le organizzazioni prevede anche la suddivisione delle risorse acquistate in allocazioni di risorse tra le organizzazioni da gestire. Puoi distribuire l’amministrazione delle risorse dei prodotti ad altre organizzazioni assegnando tutte o parte delle risorse. Non è possibile allocare tutte le risorse di tutti i prodotti; alcuni prodotti non sono distribuibili ad altre organizzazioni. Tali prodotti vengono visualizzati nella scheda **[!UICONTROL Allocazione prodotto]** ma non dispongono di controlli per aggiungerli ad altre organizzazioni.

>[!WARNING]
>
>Non puoi allocare prodotti a un&#39;organizzazione figlio da un contratto con **scaduto** o se l&#39;organizzazione si trova in uno stato **inattivo**. Scopri di più sulla [scadenza del contratto](https://helpx.adobe.com/enterprise/using/contract-expiry.html) oppure contatta l&#39;amministratore della tua azienda per assistenza al fine di evitare che gli utenti dell&#39;organizzazione figlio perdano l&#39;accesso alle loro app e ai loro servizi Adobe.

## Archiviazione in pool

Questo vale per i clienti che hanno una scheda Storage nel proprio Admin Console. Se non viene visualizzata una scheda Storage (Archiviazione), Admin Console non è ancora stato aggiornato all&#39;Enterprise Storage Model (Modello di archiviazione aziendale). Dopo la migrazione dell’organizzazione, verranno visualizzate le seguenti modifiche:

- Gli amministratori globali possono accedere alla quota e all&#39;utilizzo dello spazio di archiviazione nella gerarchia e allocare spazio di archiviazione alle organizzazioni utilizzando la scheda **[!UICONTROL Allocazione prodotto]** in [Global Admin Console](https://adminconsole.adobe.com/).
- Gli amministratori di sistema e gli amministratori di storage hanno il pieno controllo e la completa visibilità dello storage all&#39;interno dell&#39;organizzazione. Possono tenere traccia e gestire l&#39;archiviazione utilizzando la scheda **[!UICONTROL Archiviazione]** in [Adobe Admin Console](https://adminconsole.adobe.com/).

Con gli aggiornamenti allo storage Adobe Creative Cloud, le quote di storage sono flessibili per gli utenti finali, fino alla quantità di storage acquistata dall&#39;organizzazione. [Ulteriori informazioni](https://helpx.adobe.com/enterprise/using/manage-adobe-storage.html).

## Allocare prodotti

La scheda **[!UICONTROL Allocazione prodotti]** in Global Admin Console mostra le unità di allocazione per i prodotti acquistati nella gerarchia dell&#39;organizzazione. In qualità di [amministratore globale](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins), puoi allocare queste risorse prodotto a un&#39;altra organizzazione nella struttura organizzativa e specificare la quantità di allocazione. In qualità di [visualizzatore globale](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins), puoi visualizzare ed esportare i dati ma non puoi apportare aggiornamenti.

Per allocare i prodotti a un&#39;organizzazione, eseguire la procedura seguente:

1. Accedi a [Global Admin Console](https://global-admin-console.adobe.com) e passa a **[!UICONTROL Allocazione prodotto]**.
1. Seleziona un prodotto dall’elenco a discesa per verificarne l’allocazione a organizzazioni diverse.\
   Se un&#39;organizzazione non dispone attualmente del prodotto, viene visualizzata l&#39;icona **[!UICONTROL Aggiungi +]**.

   >[!Note]
   >
   >Se l&#39;organizzazione figlio dispone già di un contratto di acquisto, l&#39;allocazione del prodotto dall&#39;organizzazione padre a quella organizzazione figlio può essere limitata. [Ulteriori informazioni](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html#limited-product-allocation).

1. Per allocare il prodotto, seleziona l&#39;icona **[!UICONTROL Aggiungi +]** per l&#39;organizzazione pertinente.\
   Alcuni prodotti includono più risorse allocabili. In tal caso, nella finestra di dialogo sono elencate più risorse e dovete fornire i valori per ciascuna risorsa. Ad esempio, Adobe Stock può includere crediti immagine Adobe Stock e crediti premium.
   ![Immagini Adobe Stock](/help/adobe-support-tools-guide/assets/adobe-stock-images.png)
1. Nella finestra di dialogo visualizzata, specifica la quantità di prodotto.
1. Seleziona **[!UICONTROL Salva]**.
1. Per consentire o non consentire la sovrassegnazione di una risorsa, seleziona l’opzione appropriata.
   ![Sovrassegnazione](/help/adobe-support-tools-guide/assets/overallocation.png)
1. Selezionare **[!UICONTROL Rivedi modifiche in sospeso]** dopo aver allocato le risorse. Dopo la revisione, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Allocazione e distribuzione di licenze utente o transazioni Adobe Acrobat Sign

Global Admin Console consente di allocare e distribuire le licenze utente o le transazioni di Acrobat Sign nella gerarchia organizzativa. Ogni organizzazione nella gerarchia a cui sono assegnate licenze o transazioni Acrobat Sign crea un proprio account Acrobat Sign separato.

- Ogni account Acrobat Sign creato è indipendente e isolato in termini di amministrazione e contenuto.
- Ogni account Acrobat Sign non è a conoscenza degli altri account Acrobat Sign (ad esempio, nelle organizzazioni principali o secondarie).

Ulteriori informazioni sulla [gestione di Adobe Acrobat Sign in Admin Console](https://helpx.adobe.com/enterprise/using/adobe-sign-for-enterprise.html).

Per gestire i componenti aggiuntivi di autenticazione, ad esempio KBA (Knowledge-based Authentication) e PA (Phone Authentication), contatta il rappresentante Adobe o il Customer Success Manager.


## Limitazioni all’allocazione dei prodotti

L&#39;allocazione da un&#39;organizzazione padre a un&#39;organizzazione figlio è limitata in questi casi:

- Se entrambe le organizzazioni hanno contratti diversi e il prodotto che stai tentando di allocare esiste in entrambi, non è consentito combinare la stessa offerta tra i contratti.
- Se entrambe le organizzazioni hanno lo stesso contratto, puoi richiedere l&#39;autorizzazione per allocare il prodotto contattando il tuo rappresentante Adobe o [inviando un caso di supporto](https://helpx.adobe.com/enterprise/using/support-for-enterprise.html) in cui si specifica che **[!UICONTROL Allocazione prodotti]** in Global Admin Console è bloccata.

## Sovrassegnazione

In qualità di [amministratore globale](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins), puoi consentire la sovrassegnazione delle risorse.

Un [criterio](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html#update-policies) di allocazione associato al prodotto e all&#39;organizzazione indica se è consentita la sovrassegnazione.

L’allocazione eccessiva consente di concedere a un’organizzazione figlio più risorse di prodotto di quante siano disponibili nell’organizzazione padre. È utile quando le allocazioni sono approssimative e l’amministratore non vuole essere costretto a mantenere la somma delle allocazioni delle risorse.
Se la sovrassegnazione è disabilitata per una risorsa prodotto in un&#39;organizzazione, la somma delle sovvenzioni figlio non può superare la sovvenzione padre. Le richieste di sovrassegnazione di una risorsa contrassegnata con sovrassegnazione disabilitata non vengono eseguite.
Quando si cambia l&#39;opzione di sovrassegnazione da abilitata a disabilitata, i valori di concessione devono essere adeguati per eliminare la sovrassegnazione prima di poter eseguire gli aggiornamenti delle sovvenzioni, se è presente una situazione di sovrassegnazione nelle quantità di concessione di una risorsa.

![Sovrassegnazione](/help/adobe-support-tools-guide/assets/overallocation.png)

## Contratti scaduti nella gerarchia

Non è possibile allocare prodotti a un&#39;organizzazione figlio da un contratto ETLA scaduto. I banner e le notifiche in-app, come quelli di seguito, nelle pagine **[!UICONTROL Panoramica]** e **[!UICONTROL Allocazione prodotto]** indicano chiaramente la scadenza, la scadenza o l&#39;inattività del contratto per una o più organizzazioni figlie.

![Allocazione prodotti](/help/adobe-support-tools-guide/assets/product-allocation.png)

>[!IImportante]
>
>Quando un contratto ETLA che fa parte della gerarchia è inattivo, i prodotti vengono rimossi dalle pagine **[!UICONTROL Panoramica]** e **[!UICONTROL Allocazione prodotti]**.

[Ulteriori informazioni sulla scadenza del contratto](https://helpx.adobe.com/enterprise/using/contract-expiry.html) o contatta l&#39;amministratore della tua azienda per assistenza al fine di evitare che gli utenti dell&#39;organizzazione figlio perdano l&#39;accesso alle loro app e ai loro servizi Adobe.
