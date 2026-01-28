---
title: Configurazione dei diritti per l’assistenza clienti Adobe
description: In che modo i clienti Adobe possono configurare le adesioni al supporto per abilitare l’invio dei casi.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 009be3353a4bd690a7cf395e7e95540808058b39
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---


# Assistenza clienti per Adobe

Per configurare i diritti di supporto per la tua organizzazione, aggiungi o invita l’utente tramite Admin Console.

## Aggiunta di ruoli di supporto per l’adesione a un’organizzazione

Il ruolo amministratore del supporto è un ruolo non amministrativo che ha accesso alle informazioni relative al supporto. Gli amministratori del supporto possono visualizzare, creare e gestire i rapporti sui problemi.

Per aggiungere o invitare un amministratore:

1. In Admin Console scegliere **[!UICONTROL Utenti]** > **[!UICONTROL Amministratori]**.
1. Fai clic su **[!UICONTROL Aggiungi amministratore]**.
1. Immetti un nome o un indirizzo e-mail.

   Puoi cercare utenti esistenti o aggiungere un nuovo utente specificando un indirizzo e-mail valido e compilando le informazioni sullo schermo.

   ![Aggiungi amministratore](assets/admin-console-add-admin.png)

1. Fai clic su **[!UICONTROL Avanti]**. Viene visualizzato un elenco di ruoli di amministratore.

Per assegnare un ruolo di amministratore del supporto a un utente (consentire a un utente di contattare il supporto):

1. Selezionare l&#39;opzione **[!UICONTROL Amministratore supporto]**.

   ![Modifica diritti amministratore](assets/edit-admin-rights.png)

1. Scegliete una delle due opzioni seguenti:

   * Opzione 1: **[!UICONTROL Amministratore del supporto di base]**. Seleziona questa opzione se desideri consentire all’assistenza utente di accedere a tutte le soluzioni (ad eccezione di Marketo Engage).
   * Opzione 2: **[!UICONTROL Amministratore del supporto tecnico]**: selezionare questa opzione per il supporto tecnico Marketo Engage. Seleziona le istanze di Marketo Engage a cui concedere l’accesso al supporto utente.

   ![Modifica diritti amministratore Marketo](assets/edit-admin-rights-advanced.png)

1. Dopo aver effettuato le selezioni, fare clic su **[!UICONTROL Salva]**.

L&#39;utente riceve un invito e-mail relativo ai nuovi privilegi di amministratore da `message@adobe.com`.

Gli utenti devono fare clic su **[!UICONTROL Inizia]** nell&#39;e-mail per partecipare all&#39;organizzazione. Se i nuovi amministratori non utilizzano il collegamento **[!UICONTROL Inizia]** nell&#39;invito e-mail, non potranno accedere ad Admin Console.

Come parte del processo di accesso, agli utenti può essere richiesto di impostare un profilo Adobe se non ne hanno già uno. Se gli utenti hanno più profili associati al loro indirizzo e-mail, devono scegliere **[!UICONTROL Unisciti al team]** (se richiesto) e quindi selezionare il profilo associato alla nuova organizzazione.

![Conferma diritti amministratore](assets/admin-rights-confirmation.png)

Per ulteriori dettagli fare riferimento alle istruzioni [modifica ruolo amministratore organizzazione](admin-roles.md#add-enterprise-role) nella documentazione dei ruoli amministrativi. Solo un amministratore di sistema dell’organizzazione può assegnare questo ruolo. Per ulteriori informazioni sulla gerarchia amministrativa, consulta la documentazione di [ruoli amministrativi](admin-roles.md).
