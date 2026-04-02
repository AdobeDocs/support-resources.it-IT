---
title: Gestire i profili di prodotto in Global Admin Console
description: Scopri come gli amministratori globali possono aggiungere, modificare ed eliminare profili di prodotto in Global Admin Console.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2: id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
exl-id: 6a0b2d9f-9e02-428c-a2be-bc457230f7e0
source-git-commit: 976bfc44cdae61376e2da89019f7758518c6fadc
workflow-type: tm+mt
source-wordcount: 579
ht-degree: 1%

---

# Gestire i profili di prodotto in Global Admin Console

**Si applica a:** Enterprise

Gli amministratori globali possono aggiungere, modificare ed eliminare profili di prodotto in [Global Admin Console](https://global-admin-console.adobe.com/).

>[!NOTE]
>
>In [Global Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console), seleziona un&#39;organizzazione e passa a **[!UICONTROL Prodotti]**. Puoi attivare tutti o alcuni servizi per un prodotto utilizzando i Profili di prodotto.

Come nell’Admin Console standard, i profili di prodotto ti consentono di perfezionare l’utilizzo dei prodotti all’interno di un’organizzazione. È inoltre possibile assegnare gli amministratori, denominati **[!UICONTROL amministratori del profilo di prodotto]**, ai profili di prodotto. Questi amministratori possono aggiungere utenti finali ai profili di prodotto che gestiscono.

Per gestire i profili di prodotto, seleziona un prodotto. Verranno visualizzati i controlli per aggiungere, modificare ed eliminare i profili di prodotto.

>[!NOTE]
>
>Per alcuni prodotti, non è possibile creare o modificare i profili di prodotto in Global Admin Console. In questi casi, utilizza [Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview).

## Aggiungere un profilo di prodotto

1. In [Global Admin Console](https://global-admin-console.adobe.com/), seleziona un&#39;organizzazione da modificare, quindi passa alla scheda **[!UICONTROL Prodotti]**.
1. Seleziona un prodotto a cui aggiungere un profilo di prodotto.
1. Seleziona **[!UICONTROL Aggiungi profilo]**.
1. Nella finestra di dialogo **[!UICONTROL Aggiungi profilo]** immettere i dettagli seguenti:

   | Campo | Descrizione |
   |---|---|
   | **[!UICONTROL Nome]** | Un nome univoco per il profilo di prodotto all’interno dell’organizzazione, distinto da altri profili di prodotto e gruppi di utenti. |
   | **[!UICONTROL Quota]** | Il numero target di licenze assegnate per questo profilo. |
   | **[!UICONTROL Gruppi di utenti]** | Seleziona dal menu a discesa o digita il nome di un gruppo di utenti. Se il gruppo di utenti non esiste ancora, crearlo tramite la scheda [**[!UICONTROL Gruppi di utenti ]**](https://helpx.adobe.com/enterprise/global-admin-console/manage-user-groups.html). |
   | **[!UICONTROL Amministratori]** | Seleziona dal menu a discesa o immetti l’indirizzo e-mail di un amministratore. Se l&#39;amministratore non esiste ancora, crealo prima tramite la scheda [**[!UICONTROL Amministratori ]**](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators). |

   Ai [!UICONTROL gruppi di utenti] specificati è assegnato il profilo di prodotto. Gli amministratori specificati diventano gli **[!UICONTROL amministratori del profilo di prodotto]**, che possono gestire il profilo tramite Adobe Admin Console per l&#39;organizzazione pertinente.

   ![Aggiungi profilo](./assets/manage-product-profiles_add-profile.png)

1. Utilizza l&#39;interruttore **[!UICONTROL Notifiche]** per abilitare o disabilitare le notifiche e-mail. Quando questa opzione è attivata, gli utenti ricevono una notifica tramite e-mail quando vengono aggiunti o rimossi dal profilo.
1. Utilizza i singoli **[!UICONTROL Servizi]** per attivare o disattivare servizi specifici per il profilo prodotto. Per ulteriori informazioni, vedere [Abilitare/disabilitare i servizi per un profilo di prodotto](https://helpx.adobe.com/enterprise/using/enable-disable-services.html).
1. Seleziona **[!UICONTROL Salva]**.
1. Selezionare **[!UICONTROL Rivedi modifiche in sospeso]** dopo aver completato la modifica delle organizzazioni. Dopo la revisione, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Modificare un profilo di prodotto

1. Seleziona un&#39;organizzazione da modificare, passa alla scheda **[!UICONTROL Prodotti]** e seleziona un prodotto.
1. Seleziona l&#39;icona **[!UICONTROL Altre opzioni]** ![Altre opzioni](./assets/manage-product-profiles_more-options.png) per il profilo di prodotto pertinente, quindi seleziona **[!UICONTROL Modifica profilo]**.
1. Aggiorna i dettagli del profilo di prodotto in base alle esigenze e seleziona **[!UICONTROL Salva]**.
1. Selezionare **[!UICONTROL Rivedi modifiche in sospeso]** dopo aver completato la modifica delle organizzazioni. Dopo la revisione, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Eliminare un profilo di prodotto

>[!WARNING]
>
> L’eliminazione di un profilo di prodotto rimuove l’accesso al prodotto per tutti gli utenti che erano membri di tale profilo o appartenevano a gruppi di utenti associati a tale profilo.

1. Seleziona un&#39;organizzazione da modificare, passa alla scheda **[!UICONTROL Prodotti]** e seleziona un prodotto.
1. Seleziona l&#39;icona **[!UICONTROL Altre opzioni]** ![Altre opzioni](./assets/manage-product-profiles_more-options.png) per il profilo di prodotto corrispondente, quindi seleziona **[!UICONTROL Elimina profilo]**.
1. Selezionare **[!UICONTROL OK]** nella finestra di dialogo di conferma.
1. Selezionare **[!UICONTROL Rivedi modifiche in sospeso]** dopo aver completato la modifica delle organizzazioni. Dopo la revisione, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).


## Lettura correlata

- [Adottare l&#39;amministrazione globale](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration)
- [Gestisci amministratori](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)
- [Gestione gruppi utenti](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-user-groups)
- [Alloca prodotti alle organizzazioni figlie](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/allocate-products)
- [Esegui processi in sospeso](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)
- [Attiva/disattiva servizi](https://helpx.adobe.com/enterprise/using/enable-disable-services.html)
- [Panoramica di Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview)
