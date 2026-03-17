---
title: Gestione dei gruppi di utenti in Global Admin Console
description: Scopri come creare, condividere, modificare ed eliminare gruppi di utenti in Global Admin Console per semplificare la gestione degli utenti nelle diverse organizzazioni.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: f81a20fd6d9d64443f4708b3fc17de7240d1bc61
workflow-type: tm+mt
source-wordcount: '1330'
ht-degree: 0%

---


# Gestione dei gruppi di utenti in Global Admin Console

Crea, gestisci e condividi gruppi di utenti in Global Admin Console per semplificare la gestione degli utenti raggruppando gli utenti con le stesse autorizzazioni, risparmiando tempo e garantendo coerenza.

In [Global Admin Console](https://helpx.adobe.com/it/enterprise/global-admin-console/adopt-global-administration.html), seleziona un&#39;organizzazione e passa a **[!UICONTROL Gruppi utenti]**. Condividere gruppi tra più organizzazioni utilizzando un&#39;unica origine per la gestione degli utenti per sincronizzare utenti e gruppi.

[Accedi a Global Admin Console](https://global-admin-console.adobe.com)



## Creazione di gruppi di utenti

È possibile [creare gruppi di utenti](https://helpx.adobe.com/it/enterprise/using/user-groups.html) singolarmente, in blocco o [sincronizzarli direttamente da un Azure AD](https://helpx.adobe.com/it/enterprise/using/add-azure-sync.html) stabilito in una directory federata in Adobe Admin Console. In Global Admin Console, puoi definire gruppi di utenti a cui vengono assegnati profili di prodotto rilevanti, ai quali gli amministratori dei gruppi di utenti possono aggiungere utenti in un secondo momento utilizzando Admin Console.

1. Accedi a [Global Admin Console](https://global-admin-console.adobe.com/), seleziona un&#39;organizzazione da modificare, quindi passa alla scheda **[!UICONTROL Gruppi utenti]**.

2. Selezionare **[!UICONTROL Aggiungi gruppo utenti]**.

   ![Scheda Organizzazioni in Global Admin Console con la scheda Gruppi di utenti selezionata.](assets/add-user-group.png "Aggiungi gruppo utenti")

   _Aggiungere gruppi di utenti a un&#39;organizzazione per semplificare la gestione degli utenti._

3. Immettere quanto segue nella finestra di dialogo **[!UICONTROL Aggiungi gruppo utenti]** visualizzata:
   - **[!UICONTROL Nome]**: specificare un nome per il gruppo di utenti.
   - **[!UICONTROL Profili di prodotto]**: se si desidera concedere l&#39;accesso al prodotto ai membri correnti o futuri del gruppo di utenti, fare clic sulla freccia dell&#39;elenco a discesa per selezionare un profilo di prodotto dall&#39;elenco oppure immettere il nome del profilo di prodotto e selezionarlo dall&#39;elenco a discesa visualizzato. Se desideri aggiungere un profilo di prodotto non ancora creato, devi prima farlo utilizzando la scheda [Profili di prodotto](https://helpx.adobe.com/it/enterprise/using/global-admin-edit-organizations.html#profiles).
   - **[!UICONTROL Amministratori]**: fare clic sulla freccia dell&#39;elenco a discesa per selezionare un amministratore dall&#39;elenco oppure immettere l&#39;indirizzo di posta elettronica dell&#39;amministratore e selezionarlo dall&#39;elenco a discesa visualizzato. Se desideri aggiungere un nuovo amministratore che non è già stato creato, devi prima crearlo utilizzando la scheda [Amministratori](#share-user-groups).

   I profili di prodotto specificati vengono assegnati al gruppo di utenti e gli amministratori specificati diventano gli amministratori del gruppo di utenti. Gli amministratori dei gruppi di utenti possono utilizzare Adobe Admin Console per l’organizzazione pertinente per gestire il gruppo.

4. Seleziona **[!UICONTROL Salva]**.

5. Selezionare **[!UICONTROL Rivedi modifiche in sospeso]** per rivedere gli aggiornamenti. Quindi, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/it/enterprise/global-admin-console/set-up-organizations.html#execute-jobs).

   >[!NOTE]
   >
   >Gli amministratori globali possono [assegnare profili di prodotto e amministratori di gruppi di utenti](#review-user-groups) ai gruppi di utenti utilizzando Global Admin Console. Utilizzando Adobe Admin Console, gli amministratori di sistema e gli amministratori dei gruppi di utenti possono [aggiungere utenti e assegnare amministratori e profili di prodotto](https://helpx.adobe.com/it/enterprise/using/user-groups.html) al gruppo di utenti.



## Condividere gruppi di utenti

La proiezione di gruppo consente di sincronizzare i gruppi di utenti e gli utenti associati da un’unica origine di gestione a più istanze di Admin Console. Gli amministratori globali possono condividere gruppi di utenti con discendenti gerarchici dell’organizzazione di origine, lavorando verso il basso, non verso l’alto o l’uno accanto all’altro.

1. Accedi a [Global Admin Console](https://global-admin-console.adobe.com/), seleziona un&#39;organizzazione e passa alla scheda **[!UICONTROL Gruppi utenti]**.

2. Selezionare le caselle di controllo relative ai gruppi di utenti che si desidera condividere.

   I gruppi potrebbero essere disabilitati per la condivisione nei seguenti casi:
   - Il gruppo utenti è condiviso da un’altra organizzazione. Per condividere o modificare il gruppo, selezionare l&#39;organizzazione a cui appartiene dalla gerarchia organizzazione.
   - L&#39;organizzazione non utilizza l&#39;archiviazione [Adobe per le aziende](https://helpx.adobe.com/in/enterprise/using/storage-for-business.html), che viene implementata globalmente in più fasi.
   - Il criterio dell&#39;organizzazione è disabilitato. Vai alla scheda **[!UICONTROL Criteri]** per attivare il criterio **[!UICONTROL Gestisci gruppi di utenti condivisi]**.
   - L’organizzazione non dispone di organizzazioni figlio con cui condividere i gruppi di utenti.

3. Selezionare **[!UICONTROL Condividi gruppo utenti]**.

4. <a id="review-user-groups"></a>Esaminare i gruppi di utenti da condividere con altre organizzazioni. Se sei anche un amministratore di sistema nell&#39;organizzazione selezionata, seleziona **[!UICONTROL Apri in Admin Console]** Icona <img src="assets/icon-open-in-admin-console.png" alt="Icona Apri in Admin Console" width="14" height="14"> per rivedere l&#39;elenco dei membri del gruppo utenti in Adobe Admin Console.

   >[!NOTE]
   >
   >Per evitare conflitti, verificare che le organizzazioni con cui si intende condividere i gruppi di utenti non abbiano già gruppi con lo stesso nome.

5. Seleziona **[!UICONTROL Avanti]**.

6. Seleziona le organizzazioni con cui condividere i gruppi di utenti e seleziona **[!UICONTROL Avanti]**.

7. Se non sono presenti conflitti, selezionare **[!UICONTROL Condividi gruppi di utenti]**.

   In caso di conflitti (in cui nell&#39;organizzazione di destinazione esistono gruppi di utenti con lo stesso nome), scegliere una delle opzioni seguenti, quindi selezionare **[!UICONTROL Condividi gruppi di utenti]**:
   - **[!UICONTROL Ignora (impostazione predefinita)]**: ignora i gruppi nelle organizzazioni di destinazione con lo stesso nome.
   - **[!UICONTROL Aggiungi solo]**: unisci i gruppi di utenti aggiungendo nuovi utenti ai gruppi di utenti esistenti senza rimuovere alcun utente.
   - **[!UICONTROL Gruppo mirror]**: regola i gruppi dell&#39;organizzazione di destinazione in modo che corrispondano al gruppo condiviso aggiungendo o rimuovendo utenti.

8. Selezionare **[!UICONTROL Rivedi modifiche in sospeso]** per rivedere gli aggiornamenti. Quindi, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/it/enterprise/global-admin-console/set-up-organizations.html#execute-jobs).

   Gli eventi di proiezione di gruppo vengono registrati come riferimento. Scopri come [visualizzare e scaricare i registri di controllo](https://helpx.adobe.com/it/enterprise/global-admin-console/insights.html).


Quando condividi un gruppo di utenti, il gruppo e i relativi utenti vengono aggiunti all’organizzazione di destinazione. Tuttavia, il *gruppo di utenti di origine controlla* i gruppi di utenti condivisi e i relativi utenti. Le assegnazioni dell&#39;amministratore e del profilo di prodotto sono *non* sincronizzate tra le organizzazioni.

Le modifiche al nome del gruppo di utenti previsto o degli utenti associati nel gruppo di utenti di origine vengono aggiornate automaticamente nell&#39;organizzazione di destinazione. Anche se il gruppo di utenti condiviso non può essere gestito direttamente, un amministratore dell’organizzazione di destinazione può assegnare profili di prodotto a un gruppo condiviso, fornendo l’accesso con licenza agli utenti del gruppo.



## Revoca dell&#39;accesso ai gruppi condivisi

1. Accedi a [Global Admin Console](https://global-admin-console.adobe.com/), seleziona un&#39;organizzazione e passa alla scheda **[!UICONTROL Gruppi utenti]**.

2. Seleziona **[!UICONTROL Gestisci accesso condiviso]** per il gruppo di utenti pertinente.

3. Seleziona le organizzazioni da cui desideri revocare l’accesso.

4. Seleziona **[!UICONTROL Revoca accesso]**.

5. Durante la revoca dell’accesso, puoi scegliere se eliminare il gruppo di utenti e gli utenti o lasciare una copia nelle organizzazioni target:
   - All’eliminazione, il gruppo di utenti viene rimosso dalle organizzazioni di destinazione. Gli utenti che non sono membri di altri gruppi condivisi vengono rimossi dalle organizzazioni target e perdono l’accesso a tutti i prodotti, i servizi e le risorse.
   - Quando si lascia una copia, il gruppo di utenti e gli utenti rimangono nelle organizzazioni di destinazione mantenendo intatte tutte le assegnazioni. Tuttavia, il gruppo di utenti non verrà più sincronizzato e può essere gestito dagli amministratori delle organizzazioni target.

6. Seleziona **[!UICONTROL Revoca accesso]**.

7. Selezionare **[!UICONTROL Rivedi modifiche in sospeso]** per rivedere gli aggiornamenti. Quindi, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/it/enterprise/global-admin-console/set-up-organizations.html#execute-jobs).



## Modifica gruppi di utenti

1. Accedi a [Global Admin Console](https://global-admin-console.adobe.com/), seleziona un&#39;organizzazione e passa alla scheda **[!UICONTROL Gruppi utenti]**.

2. Seleziona **[!UICONTROL Altre opzioni]** Icona <img src="assets/icon-more-options.png" alt="Icona Altre opzioni" width="14" height="14" style="vertical-align:middle"> per il gruppo di utenti rilevante e selezionare **[!UICONTROL Modifica gruppo di utenti]**.

   >[!NOTE]
   >
   >Non puoi modificare i gruppi di utenti di cui l’organizzazione selezionata non è proprietaria.

   ![Organizzazione selezionata con l&#39;opzione Modifica gruppo utenti evidenziata nella scheda Gruppi utenti.](assets/edit-user-group.png "Modifica gruppo utenti")

   _Modifica i gruppi di utenti per aggiornare il nome del gruppo di utenti, i profili di prodotto o gli amministratori._

3. Aggiorna il nome del gruppo di utenti, i profili di prodotto o gli amministratori. Quindi, seleziona **[!UICONTROL Salva]**.

   >[!NOTE]
   >
   >Nella procedura guidata **[!UICONTROL Modifica gruppo utenti]**, è possibile assegnare ruoli di amministratore solo agli utenti che dispongono già di un ruolo di amministratore assegnato in questa organizzazione. Scopri come [aggiungere nuovi amministratori](https://helpx.adobe.com/enterprise/global-admin-console/manage-admins.html).

4. Selezionare **[!UICONTROL Rivedi modifiche in sospeso]** per rivedere gli aggiornamenti. Quindi, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/it/enterprise/using/global-admin-set-up-organizations.html#execute-jobs).

   >[!NOTE]
   >
   >Se modifichi il nome di un gruppo utenti condiviso, le modifiche vengono aggiornate automaticamente nell’organizzazione di destinazione.



## Elimina gruppi di utenti

1. Accedi a [Global Admin Console](https://global-admin-console.adobe.com/), seleziona un&#39;organizzazione e passa alla scheda **[!UICONTROL Gruppi utenti]**.

2. Seleziona **[!UICONTROL Altre opzioni]** Icona <img src="assets/icon-more-options.png" alt="Icona Altre opzioni" width="14" height="14" style="vertical-align:middle"> per il gruppo di utenti rilevante e selezionare **[!UICONTROL Elimina gruppo di utenti]**.

   >[!NOTE]
   >
   >Non puoi eliminare i gruppi di utenti di cui l’organizzazione selezionata non è proprietaria.

3. Selezionare **[!UICONTROL Ok]** nella finestra di dialogo visualizzata.

   >[!CAUTION]
   >
   >L’eliminazione di un gruppo di utenti può avere un impatto sugli utenti. Assicurati che non vi siano accessi o informazioni che andranno perse quando il gruppo di utenti viene eliminato.

4. Dopo aver modificato le organizzazioni, selezionare **[!UICONTROL Rivedi le modifiche in sospeso]** per rivederle. Quindi, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/it/enterprise/using/global-admin-set-up-organizations.html#execute-jobs).
