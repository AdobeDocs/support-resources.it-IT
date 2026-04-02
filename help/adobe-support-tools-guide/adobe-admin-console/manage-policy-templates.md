---
title: Gestire i modelli di policy in Global Admin Console
description: Scopri come gli amministratori globali possono applicare modelli di policy a qualsiasi organizzazione figlia, direttamente o indirettamente dall’organizzazione in cui sono memorizzati in Global Admin Console.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2:
  - id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: cf30f2a656ccb28b678ea6fcd8e4d56d7c8a8fb4
workflow-type: tm+mt
source-wordcount: 705
ht-degree: 0%

---

# Gestire i modelli di policy in Global Admin Console

**Si applica a:** Enterprise

Scopri come gli amministratori globali possono applicare modelli di policy a qualsiasi organizzazione figlia, direttamente o indirettamente dall’organizzazione in cui sono memorizzati in Global Admin Console.

>[!NOTE]
>
>In [Global Admin Console](https://helpx.adobe.com/it/enterprise/global-admin-console/adopt-global-administration.html), seleziona un&#39;organizzazione da modificare e passa alla scheda **Modelli di criteri** per semplificare la configurazione e facilitare la gestione coerente dei criteri tra le organizzazioni.
>
> [Accedi a Global Admin Console](https://global-admin-console.adobe.com/)

## Funzionamento dei modelli di criteri

I modelli di criteri sono archiviati in un&#39;organizzazione e sono visibili a tutti gli amministratori globali dell&#39;organizzazione. Una volta applicati, i dati del modello di criterio vengono impostati singolarmente in ogni organizzazione. Quando un modello di criterio viene applicato a un&#39;organizzazione, ogni voce del modello di criterio viene applicata ai criteri dell&#39;organizzazione, sostituendo i valori dei criteri esistenti.

### Comportamento criterio bloccato

Gli aggiornamenti ai criteri bloccati vengono eseguiti solo se l&#39;utente che applica l&#39;aggiornamento è un amministratore globale dell&#39;organizzazione indicato dall&#39;icona **[!UICONTROL Bloccato da]** del criterio da aggiornare.

Se l’utente che applica il modello dispone dell’autorizzazione per sbloccare il criterio, i blocchi di criterio prendono i valori dal modello applicato (bloccato o sbloccato). Se il modello indica che il blocco deve essere lasciato invariato, il valore del blocco nel criterio rimane invariato.

### Nota importante sul salvataggio

>[!NOTE]
>
>A differenza di altre modifiche apportate in Global Admin Console, le modifiche ai modelli dei criteri diventano effettive immediatamente senza dover passare attraverso il processo **[!UICONTROL Revisione delle modifiche in sospeso - Invia]**. Tuttavia, per implementare le modifiche in sospeso nelle organizzazioni in cui viene applicato il modello di criteri, è necessario [invio](https://helpx.adobe.com/it/enterprise/global-admin-console/execute-jobs.html).

## Creare un modello di criteri

1. In [Global Admin Console](https://global-admin-console.adobe.com/), seleziona un&#39;organizzazione da modificare, quindi passa alla scheda **[!UICONTROL Modelli di criteri]**.
1. Seleziona **[!UICONTROL Crea modello]**.<br>
   ![Pic1](./assets/DXSKB-3209-1-ga_14.png)
   <br>
1. Nella finestra di dialogo **[!UICONTROL Crea modello criteri]** immettere **nome** e **descrizione** per il modello criteri.<br>Il nome del modello di criteri può contenere un massimo di 100 caratteri.
1. Selezionare i criteri da includere nel modello.
1. Impostare i valori per i criteri selezionati (vedere [Impostazione dei valori dei criteri](#setting-policy-values) di seguito).
1. Seleziona **Salva**.

### Impostazione dei valori dei criteri {#setting-policy-values}

Per ogni criterio incluso nel modello, configura due impostazioni:

* **Consentito/Non consentito:** Impostare il dispositivo di scorrimento sul valore desiderato. Scopri i [dettagli dei criteri](https://helpx.adobe.com/it/enterprise/global-admin-console/update-policies.html#policy-details).
* **Valore di blocco:** Modificare lo stato di blocco del criterio utilizzando una delle opzioni seguenti:
   * **Blocca** - Il criterio verrà bloccato dopo l&#39;applicazione del modello.
   * **Sblocca** — il criterio verrà sbloccato dopo l&#39;applicazione del modello.
   * **Mantieni invariato** - Lo stato di blocco del criterio verrà lasciato invariato rispetto a prima dell&#39;applicazione del modello.<br>
     ![Pic2](./assets/DXSKB-3209-2-policy-template.png)
<br>

## Applicare un modello alle organizzazioni

1. In [Global Admin Console](https://global-admin-console.adobe.com/), seleziona un&#39;organizzazione da modificare, quindi passa alla scheda **[!UICONTROL Modelli di criteri]**.
1. Seleziona l&#39;icona **[!UICONTROL Altre opzioni]** ![Altre opzioni](./assets/manage-product-profiles_more-options.png) per il modello di criteri pertinente e seleziona **[!UICONTROL Applica modello all&#39;organizzazione]**.<br>
   ![Pic3](./assets/DXSKB-3209-3-ga_15.png)
   <br>
1. Selezionare le organizzazioni a cui si desidera applicare il modello. È possibile selezionare più organizzazioni.<br>
   ![Pic4](./assets/DXSKB-3209-4-bulk-apply-template.png)
   <br>
1. Selezionare **[!UICONTROL Applica modello]**.
1. Per implementare le modifiche in sospeso nelle organizzazioni in cui viene applicato il modello di criteri, selezionare **[!UICONTROL Rivedi modifiche in sospeso]**. Dopo la revisione, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/it/enterprise/global-admin-console/execute-jobs.html).

Se tutti i valori dei criteri nelle organizzazioni selezionate corrispondono già ai valori del modello, viene visualizzato un messaggio che informa che non sono state apportate modifiche. Inoltre, **[!UICONTROL Revisione modifiche in sospeso]** non è abilitato se non sono presenti altre modifiche in sospeso.

## Modificare un modello

1. In [Global Admin Console](https://global-admin-console.adobe.com/), seleziona un&#39;organizzazione da modificare, quindi passa alla scheda **[!UICONTROL Modelli di criteri]**.
1. Seleziona l&#39;icona **[!UICONTROL Altre opzioni]** ![Altre opzioni](./assets/manage-product-profiles_more-options.png) per il modello pertinente e seleziona **[!UICONTROL Modifica modello]**.<br>
   ![Pic5](./assets/DXSKB-3209-5-ga_15-1.png)
   <br>
1. Aggiornare il modello di criteri e selezionare **[!UICONTROL Aggiorna]**.
1. Per implementare le modifiche in sospeso nelle organizzazioni in cui viene applicato il modello di criteri, selezionare **[!UICONTROL Rivedi modifiche in sospeso]**. Dopo la revisione, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/it/enterprise/global-admin-console/execute-jobs.html).

## Eliminare un modello

1. In [Global Admin Console](https://global-admin-console.adobe.com/), seleziona un&#39;organizzazione da modificare, quindi passa alla scheda **[!UICONTROL Modelli di criteri]**.
1. Seleziona l&#39;icona **[!UICONTROL Altre opzioni]** ![Altre opzioni](./assets/manage-product-profiles_more-options.png) per il modello pertinente e seleziona **[!UICONTROL Elimina modello]**.<br>
   ![Pic6](./assets/DXSKB-3209-6-ga_15-2.png)
   <br>
1. Selezionare *Sì* nella finestra di dialogo visualizzata.
