---
title: Gestisci gerarchia organizzazione
description: Scopri come gli amministratori globali possono gestire la gerarchia dell’organizzazione in Global Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: 6fcf16e3-0408-4961-9981-14d526e1ea28
source-git-commit: 976bfc44cdae61376e2da89019f7758518c6fadc
workflow-type: tm+mt
source-wordcount: '1527'
ht-degree: 0%

---

# Gestisci gerarchia organizzazione

Applicabile all&#39;azienda.

Scopri come gli amministratori globali possono gestire la gerarchia dell’organizzazione in Global Admin Console.

Dopo aver ottenuto l&#39;[accesso a [!DNL Global Admin Console]](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console), puoi creare nuove organizzazioni, aggiungere organizzazioni esistenti alla gerarchia, eliminare organizzazioni e modificare un&#39;organizzazione padre. Vai qui per [accedere a Global Admin Console](https://global-admin-console.adobe.com/)

Un’organizzazione è una struttura utilizzata per gestire prodotti e utenti di Adobe. [[!DNL Adobe Admin Console]](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview) consente agli amministratori di gestire la distribuzione e la configurazione di prodotti e utenti nell&#39;organizzazione. [[!DNL Global Admin Console]](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration) consente agli amministratori globali di creare, gestire ed eliminare più organizzazioni.

## Creare un’organizzazione figlio

In qualità di [amministratore globale](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators), puoi creare organizzazioni figlie di qualsiasi organizzazione nella gerarchia e impostare il nome, il paese, i gruppi di utenti, i prodotti, i profili di prodotto, gli amministratori e i criteri.

Quando viene creata una nuova organizzazione figlio, vengono automaticamente ereditati i seguenti elementi dall&#39;elemento padre immediato:

- Impostazioni [criterio](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html) dell&#39;organizzazione (inclusi i blocchi, se presenti).
- Elenco di amministratori di sistema (controllati da **[!UICONTROL Eredita amministratori di sistema al momento della creazione]** [criterio](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)).
Di seguito sono riportati gli elementi che possono impedire l&#39;ereditarietà degli amministratori di sistema:
   - Mancanza di [trust di dominio](https://helpx.adobe.com/enterprise/using/directory-trust.html).
   - Limitazioni per tipo di utente (aggiungere i criteri per utenti di Adobe ID/Enterprise ID/Federated ID). Scopri i [dettagli dei criteri](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html).
- Accesso a [[!DNL Federated ID]] o [[!DNL Enterprise ID]] utenti da domini a cui l&#39;organizzazione principale ha accesso. In questo modo gli utenti del dominio nell’elemento padre sono disponibili nell’organizzazione figlio. L&#39;ereditarietà dell&#39;accesso utente è controllata da **Eredita utenti dalle directory gestite dall&#39;organizzazione padre** [policy](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html).
- Criteri di condivisione, criteri password e contatti di sicurezza (controllati da **Eredita impostazioni di condivisione risorse al momento della creazione dell&#39;organizzazione figlio** [criteri](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)).

1. Accedi a [Global Admin Console](https://global-admin-console.adobe.com/). Nella scheda **[!UICONTROL Organizzazioni]**, seleziona l&#39;organizzazione a cui desideri aggiungere un&#39;organizzazione figlio.
2. Seleziona l&#39;icona **[!UICONTROL Aggiungi+]**.
   ![Aggiungi organizzazione](/help/adobe-support-tools-guide/assets/add-an-organization-1.png)
3. Specifica un **nome** e il **paese** dell&#39;organizzazione.\
   Il nome semplice dell’organizzazione deve contenere tra 4 e 100 caratteri; la lunghezza massima per il percorso è di 255 caratteri.
   ![Aggiungi organizzazione figlio](/help/adobe-support-tools-guide/assets/add-a-child-organization.png)
4. Seleziona **[!UICONTROL Salva]**.
5. Seleziona **[!UICONTROL Rivedi modifiche in sospeso]** dopo aver completato la modifica delle organizzazioni. Dopo la revisione, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Eliminare un’organizzazione figlio

In qualità di [amministratore globale](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators), puoi eliminare le organizzazioni figlie. L&#39;operazione di eliminazione non può essere annullata e l&#39;organizzazione radice non può essere eliminata. Le risorse allocate all&#39;organizzazione eliminata vengono restituite all&#39;organizzazione padre. Prima che un&#39;organizzazione venga eliminata, la relativa organizzazione padre diventa automaticamente l&#39;organizzazione padre di qualsiasi organizzazione figlio.

Un’organizzazione può essere eliminata solo se sono soddisfatti i seguenti criteri:

- Nell’organizzazione non sono presenti account Sign, acquisti Adobe Stock o archivi di archiviazione.
- Nell’organizzazione non sono presenti domini rivendicati.
- Non ci sono prodotti con istanze nell&#39;organizzazione.
- Nessun prodotto Experience Cloud può includere le istanze nell’organizzazione.

>[!WARNING]
>
>L’eliminazione di un’organizzazione ha un impatto sugli utenti. Assicurati che non vi siano accessi o informazioni che andranno perduti quando un’organizzazione viene eliminata.

1. Accedi a [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/). Vai alla scheda **[!UICONTROL Organizzazioni]** e seleziona l&#39;organizzazione da eliminare.
1. Seleziona l&#39;icona **[!UICONTROL Elimina]**.
   ![Elimina organizzazione](/help/adobe-support-tools-guide/assets/delete-organization.png)
1. Nella finestra di dialogo **[!UICONTROL Elimina organizzazione]** selezionare **[!UICONTROL OK]**.
1. Seleziona **[!UICONTROL Rivedi modifiche in sospeso]** dopo aver completato la modifica delle organizzazioni. Dopo la revisione, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

## Rinominare un’organizzazione

Il nome dell&#39;organizzazione è il nome ufficiale della società o dell&#39;istituzione, impostato durante l&#39;acquisto. Gli utenti visualizzano questo nome quando selezionano un profilo durante l’accesso, soprattutto se hanno accesso ai prodotti Adobe di più organizzazioni o se devono scegliere tra un profilo aziendale e un profilo personale.

In qualità di [amministratore globale](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators), puoi modificare il nome di qualsiasi organizzazione principale o secondaria per aiutare gli utenti a identificare il profilo corretto al momento dell&#39;accesso a [[!DNL Creative Cloud]] prodotti e servizi.

1. Accedi a [Global Admin Console](https://global-admin-console.adobe.com/). Nella scheda **[!UICONTROL Organizzazioni]**, seleziona l&#39;organizzazione che desideri rinominare.
1. Seleziona l&#39;icona **[!UICONTROL Modifica]**.
   ![Rinomina organizzazione](/help/adobe-support-tools-guide/assets/rename-organization.png)
1. Aggiorna il nome della tua organizzazione e seleziona **[!UICONTROL Salva]**.

>[!TIP]
>
>Utilizza un nome di organizzazione chiaro e riconoscibile, composto da un massimo di 255 caratteri, per aiutare gli utenti a selezionare il profilo corretto. Evita l’uso di caratteri speciali e considera l’inclusione di area geografica, reparto o diritto. Inoltre, evita acronimi non comuni e nomi vaghi o simili all’interno della gerarchia organizzativa.

Le modifiche vengono registrate nel registro di controllo, tutti gli utenti ricevono una notifica via e-mail e il nome non può essere aggiornato nuovamente per 24 ore. [Scopri come visualizzare e scaricare i registri di controllo](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/download-audit-logs-and-export-reports).

## Modificare l’elemento padre di un’organizzazione

In qualità di [!DNL Global Administrator](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators), è possibile riportare un&#39;organizzazione nella gerarchia organizzazione utilizzando il pulsante **[!UICONTROL Cambia gerarchia]**.

La modifica dell’elemento padre di un’organizzazione ha il seguente impatto:

- Se si ripristina un&#39;organizzazione, l&#39;intera struttura secondaria viene spostata a partire dall&#39;organizzazione principale. I percorsi dell&#39;organizzazione riproduttrice e dei relativi figli vengono aggiornati in modo da riflettere la nuova posizione.
- L&#39;organizzazione [criteri](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html) delle organizzazioni spostate viene aggiornata in modo che eventuali blocchi sui criteri siano gestiti da un&#39;organizzazione nella nuova gerarchia.
- Se si modifica la posizione di un&#39;organizzazione nella gerarchia, è possibile modificare gli amministratori globali dell&#39;organizzazione. I ruoli di amministrazione globale vengono ereditati nella gerarchia, pertanto tutti gli amministratori globali della nuova organizzazione principale diventano automaticamente amministratori globali dell&#39;organizzazione spostata. Allo stesso modo, gli amministratori globali possono perdere il loro ruolo nell&#39;organizzazione trasferita se hanno avuto quel ruolo in virtù del fatto di essere un amministratore globale del vecchio genitore. I ruoli di amministrazione globale ereditati non sono elencati nel riquadro Amministratori dell’organizzazione.
- Il ripristino influisce anche sui prodotti disponibili nelle organizzazioni spostate. Quando possibile, [le allocazioni di prodotti](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html) vengono aggiornate in modo che passino attraverso la nuova posizione padre.
- Se non è possibile aggiornare le allocazioni di prodotto in modo che provengano dal nuovo elemento padre, i prodotti vengono rimossi insieme ai profili di prodotto di tali prodotti. Gli utenti possono perdere l&#39;accesso a seguito di questa operazione. Affinché il prodotto sia disponibile nella nuova posizione, è necessario che il prodotto sia disponibile nel predecessore comune più vicino tra la vecchia e la nuova posizione.

>[!WARNING]
>
>Se i prodotti vengono rimossi a seguito del reparenting, gli utenti perdono l’accesso a tali prodotti.

1. Accedi a [Global Admin Console](https://global-admin-console.adobe.com/). Nella scheda **[!UICONTROL Organizzazioni]**, seleziona **[!UICONTROL Cambia gerarchia]** per abilitare il ripristino delle organizzazioni.
2. Selezionare **[!UICONTROL OK]** nella finestra popup visualizzata.
3. Per creare un padre, trascina l’organizzazione figlio sopra l’organizzazione desiderata.
4. Seleziona **[!UICONTROL Salva]** dopo aver completato il ripristino delle organizzazioni.
5. Seleziona **[!UICONTROL Rivedi modifiche in sospeso]** dopo aver completato la modifica delle organizzazioni. Dopo la revisione, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).

Una volta completato il processo, puoi passare ad Allocazione prodotto e [modificare i valori di concessione](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html) per riflettere la modifica nell&#39;allocazione delle risorse prodotto.

## Aggiungere organizzazioni esistenti utilizzando Organization Mapper

In qualità di [Amministratore globale](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators), puoi aggiungere alla gerarchia delle organizzazioni le organizzazioni esistenti che non fanno attualmente parte della gerarchia di Global Admin Console.

È inoltre possibile aggiungere organizzazioni di team alla gerarchia dell&#39;organizzazione. Le organizzazioni del team non partecipano all’allocazione dei prodotti o all’aggregazione dell’utilizzo dei prodotti e la gestione delle organizzazioni del team in Global Admin Console è limitata. Puoi aggiungerli alla gerarchia dell’organizzazione per tenerne traccia e avere visibilità sui prodotti che acquistano. Le organizzazioni del team non possono includere organizzazioni figlio e non dispongono di molte delle caratteristiche delle organizzazioni dell&#39;azienda.

Ulteriori informazioni sulle [limitazioni all&#39;allocazione dei prodotti](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html#limitations).

>[!WARNING]
>
> È possibile aggiungere solo organizzazioni figlio alle organizzazioni radice basate sullo stesso modello di archiviazione. Pertanto, le organizzazioni figlio basate sul modello di storage dell’utente possono essere aggiunte solo alle organizzazioni principali basate sul modello di storage dell’utente. Inoltre, le organizzazioni figlio basate sul modello di storage aziendale possono essere aggiunte solo alle organizzazioni radice basate sul modello di storage aziendale.

Nella scheda **[!UICONTROL Organization Mapper]** sono visualizzati i seguenti elementi:

1. Elenco a discesa con un elenco di possibili organizzazioni padre in cui è possibile aggiungere un&#39;organizzazione figlio. Si tratta di organizzazioni per le quali si è un amministratore globale.
1. Un elenco di organizzazioni figlio che possono essere aggiunte sotto l&#39;organizzazione padre selezionata nel passaggio 1. Si tratta di organizzazioni per le quali l&#39;utente è amministratore di sistema e che non sono già figlio di un&#39;altra organizzazione.

Quando un&#39;organizzazione viene aggiunta all&#39;amministrazione globale, i prodotti nelle organizzazioni aggiunte mediante Mapper organizzazione rimangono come acquisti; i numeri di [Allocazione prodotto](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html) cessano l&#39;aggregazione in queste organizzazioni.

1. Accedi a [Global Admin Console](https://global-admin-console.adobe.com/) e passa a **[!UICONTROL Organization Mapper]**.
2. Seleziona un’organizzazione principale dall’elenco a discesa.\
   Si tratta delle organizzazioni per le quali si viene aggiunti direttamente come amministratore globale. Nell’elenco a discesa, se non trovi un’organizzazione da utilizzare come principale, selezionane una più in alto nella gerarchia. Una volta completata l&#39;operazione di mappatura dell&#39;organizzazione, è possibile utilizzare [Cambia gerarchia](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/set-up-organizations#change-the-parent-of-an-organization) per spostare la nuova organizzazione verso il basso nella struttura ad albero in modo che disponga dell&#39;elemento padre che si desidera utilizzare.
3. Seleziona le organizzazioni da aggiungere come figli dell’organizzazione selezionata nel passaggio precedente.
4. Selezionare **[!UICONTROL Rivedi modifiche in sospeso]**. Quindi, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html).
5. Dopo aver eseguito le modifiche, è possibile ripetere i passaggi precedenti per aggiungere ulteriori organizzazioni figlio alla gerarchia organizzazione.

Una volta che un&#39;organizzazione si trova nella gerarchia, è possibile modificare i criteri dell&#39;organizzazione, gli amministratori o altre impostazioni passando alla scheda **[!UICONTROL Organizzazioni]**.
