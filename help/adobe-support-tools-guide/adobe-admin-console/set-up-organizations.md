---
title: Gestisci gerarchia organizzazione
description: Scopri come gli amministratori globali possono gestire la gerarchia dell'organizzazione nel Global Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: 3b3b2711887f0db086e4eb8281344cc7356accf7
workflow-type: tm+mt
source-wordcount: '1626'
ht-degree: 0%

---

# Gestire la gerarchia organizzativa

Si applica all&#39;organizzazione.

Scopri come gli amministratori globali possono gestire la gerarchia dell&#39;organizzazione nel Global Admin Console.

Dopo aver ottenuto l&#39;[accesso a [!DNL Global Admin Console]](https://helpx.adobe.com/it/enterprise/global-admin-console/adopt-global-administration.html#request-access), puoi creare nuove organizzazioni, aggiungere organizzazioni esistenti alla gerarchia, eliminare organizzazioni e modificare un&#39;organizzazione principale.
[Accedi al Global Admin Console](https://global-admin-console.adobe.com/)

Un&#39;organizzazione è una struttura utilizzata per gestire i prodotti e gli utenti Adobe. [[!DNL Adobe Admin Console]](https://helpx.adobe.com/it/enterprise/using/admin-console.html) consente agli amministratori di gestire la distribuzione e la configurazione di prodotti e utenti nell&#39;organizzazione. [[!DNL Global Admin Console]](https://helpx.adobe.com/it/enterprise/global-admin-console/overview.html) consente agli amministratori globali di creare, gestire ed eliminare più organizzazioni.

## Creare un&#39;organizzazione secondaria

In qualità di [amministratore globale](https://helpx.adobe.com/it/enterprise/global-admin-console/manage-administrators.html), puoi creare organizzazioni secondarie di qualsiasi organizzazione nella gerarchia e impostare nome, paese, gruppi di utenti, prodotti, profili di prodotto, amministratori e criteri.

Quando viene creata una nuova organizzazione secondaria, i seguenti elementi vengono ereditati automaticamente dall&#39;organizzazione principale:

- Impostazioni [criteri](https://helpx.adobe.com/it/enterprise/global-admin-console/update-policies.html) dell&#39;organizzazione (inclusi i blocchi, se presenti).
- Elenco di amministratori di sistema (controllati da **[!UICONTROL Eredita amministratori di sistema al momento della creazione]** [criterio](https://helpx.adobe.com/it/enterprise/global-admin-console/update-policies.html)).
Di seguito sono riportati gli elementi che possono impedire l&#39;ereditarietà degli amministratori di sistema:
   - Mancanza di [trust di dominio](https://helpx.adobe.com/it/enterprise/using/directory-trust.html).
   - Restrizioni relative al tipo di utente (aggiungere i criteri per gli utenti Adobe ID/Enterprise ID/Federated ID). Informazioni sui [dettagli dei criteri](https://helpx.adobe.com/it/enterprise/global-admin-console/update-policies.html).
- Accesso a [[!DNL Federated ID]] o [[!DNL Enterprise ID]] utenti da domini a cui ha accesso l&#39;organizzazione principale. Ciò rende disponibili gli utenti del dominio nell&#39;organizzazione principale nell&#39;organizzazione secondaria. L&#39;ereditarietà dell&#39;accesso utente è controllata da **Eredita utenti dalle directory gestite dall&#39;organizzazione principale** [policy](https://helpx.adobe.com/it/enterprise/global-admin-console/update-policies.html).
- Policy di condivisione, policy delle password e contatti di sicurezza (controllati da **Eredita le impostazioni di condivisione delle risorse quando viene creata l&#39;organizzazione secondaria** [policy](https://helpx.adobe.com/it/enterprise/global-admin-console/update-policies.html)).

1. Accedi al [Global Admin Console](https://global-admin-console.adobe.com/). Nella scheda **[!UICONTROL Organizzazioni]**, seleziona l&#39;organizzazione a cui desideri aggiungere un&#39;organizzazione secondaria.
2. Seleziona l&#39;icona **[!UICONTROL Aggiungi+]**.
   ![Aggiungi organizzazione](/help/adobe-support-tools-guide/assets/add-an-organization-1.png)
3. Specificare un **nome** e il **paese** dell&#39;organizzazione.\
   Il nome semplice dell&#39;organizzazione deve essere compreso tra 4 e 100 caratteri; la lunghezza massima del nome del percorso è di 255 caratteri.
   ![Aggiungi organizzazione secondaria](/help/adobe-support-tools-guide/assets/add-an-child-organization.png)
4. Seleziona **[!UICONTROL Salva]**.
5. Dopo aver modificato le organizzazioni, seleziona **[!UICONTROL Verifica modifiche in sospeso]**. Dopo la revisione, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/it/enterprise/global-admin-console/execute-jobs.html).

## Eliminare un’organizzazione figlio

In qualità di [amministratore globale](https://helpx.adobe.com/it/enterprise/global-admin-console/manage-administrators.html), puoi eliminare le organizzazioni figlie. L&#39;operazione di eliminazione non può essere annullata e l&#39;organizzazione radice non può essere eliminata. Le risorse allocate all&#39;organizzazione eliminata vengono restituite all&#39;organizzazione padre. Prima che un&#39;organizzazione venga eliminata, la relativa organizzazione padre diventa automaticamente l&#39;organizzazione padre di qualsiasi organizzazione figlio.

Un’organizzazione può essere eliminata solo se sono soddisfatti i seguenti criteri:

- Non sono presenti account Sign, acquisti Adobe Stock o repository di archiviazione nell&#39;organizzazione.
- Non ci sono domini rivendicati nell&#39;organizzazione.
- Non ci sono prodotti con istanze nell&#39;organizzazione.
- Nessun prodotto Experience Cloud può includere le istanze nell’organizzazione.

>[!WARNING]
>
>L’eliminazione di un’organizzazione ha un impatto sugli utenti. Assicurati che non vi siano accessi o informazioni che andranno perduti quando un’organizzazione viene eliminata.

1. Accedi a [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/). Vai alla scheda **[!UICONTROL Organizzazioni]** e seleziona l&#39;organizzazione da eliminare.
1. Seleziona l&#39;icona **[!UICONTROL Elimina]**.
   ![Elimina organizzazione](/help/adobe-support-tools-guide/assets/delete-organization.png)
1. Nella finestra di dialogo **[!UICONTROL Elimina organizzazione]**, selezionare **[!UICONTROL OK]**.
1. Dopo aver modificato le organizzazioni, seleziona **[!UICONTROL Verifica modifiche in sospeso]**. Dopo la revisione, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/it/enterprise/global-admin-console/execute-jobs.html).

## Rinominare un&#39;organizzazione

Il nome dell’organizzazione è il nome ufficiale della tua azienda o del tuo istituto, impostato durante l’acquisto. Gli utenti visualizzano questo nome quando selezionano un profilo durante l&#39;accesso, soprattutto se hanno accesso ai prodotti Adobe di più organizzazioni o se devono scegliere tra un profilo aziendale e personale.

In qualità di [amministratore globale](https://helpx.adobe.com/it/enterprise/global-admin-console/manage-administrators.html), puoi modificare il nome di qualsiasi organizzazione principale o secondaria per aiutare gli utenti a identificare il profilo corretto quando accedono a [[!DNL Creative Cloud]] prodotti e servizi.

1. Accedi al [Global Admin Console](https://global-admin-console.adobe.com/). Nella scheda **[!UICONTROL Organizzazioni]**, seleziona l&#39;organizzazione che desideri rinominare.
1. Seleziona l&#39;icona **[!UICONTROL Modifica]**.
   ![Rinomina organizzazione](/help/adobe-support-tools-guide/assets/rename-organization.png)
1. Aggiorna il nome della tua organizzazione e seleziona **[!UICONTROL Salva]**.

>[!TIP]
>
>Utilizza un nome di organizzazione chiaro e riconoscibile, composto da un massimo di 255 caratteri, per aiutare gli utenti a selezionare il profilo corretto. Evita l’uso di caratteri speciali e considera l’inclusione di area geografica, reparto o diritto. Inoltre, evita acronimi non comuni e nomi vaghi o simili all’interno della gerarchia organizzativa.
>Utilizza un nome di organizzazione chiaro e riconoscibile, composto da un massimo di 255 caratteri, per aiutare gli utenti a selezionare il profilo corretto. Evita l’uso di caratteri speciali e considera l’inclusione di area geografica, reparto o diritto. Inoltre, evita acronimi non comuni e nomi vaghi o simili all’interno della gerarchia organizzativa.

Le modifiche vengono registrate nel registro di controllo, tutti gli utenti ricevono una notifica via e-mail e il nome non può essere aggiornato nuovamente per 24 ore. [Scopri come visualizzare e scaricare i registri di controllo](https://helpx.adobe.com/it/enterprise/global-admin-console/insights.html).

## Modificare l’elemento padre di un’organizzazione

In qualità di [[!DNL Global Administrator]](https://helpx.adobe.com/it/enterprise/global-admin-console/manage-administrators.html), è possibile riportare un&#39;organizzazione nella gerarchia organizzazione utilizzando il pulsante **[!UICONTROL Cambia gerarchia]**.

La modifica dell’elemento padre di un’organizzazione ha il seguente impatto:

- Se si ripristina un&#39;organizzazione, l&#39;intera struttura secondaria viene spostata a partire dall&#39;organizzazione principale. I percorsi dell&#39;organizzazione riproduttrice e dei relativi figli vengono aggiornati in modo da riflettere la nuova posizione.
- Le [policy](https://helpx.adobe.com/it/enterprise/global-admin-console/update-policies.html) delle organizzazioni spostate dell&#39;organizzazione vengono aggiornate in modo che eventuali blocchi sui criteri vengano mantenuti da un&#39;organizzazione nella nuova gerarchia.
- La modifica della posizione di un&#39;organizzazione nella gerarchia può modificare gli amministratori globali di quell&#39;organizzazione. I ruoli di amministrazione globale vengono ereditati in tutta la gerarchia, in modo che tutti gli amministratori globali della nuova organizzazione principale diventino automaticamente amministratori globali dell&#39;organizzazione spostata. Allo stesso modo, gli amministratori globali possono perdere il loro ruolo nell&#39;organizzazione spostata se avevano quel ruolo in virtù dell&#39;essere un amministratore globale della vecchia organizzazione principale. I ruoli di amministrazione globale ereditati non sono elencati nel riquadro Amministratori dell&#39;organizzazione.
- La modifica dell&#39;organizzazione principale influisce anche sui prodotti disponibili nelle organizzazioni spostate. Quando possibile, [le allocazioni di prodotti](https://helpx.adobe.com/it/enterprise/global-admin-console/allocate-products.html) vengono aggiornate in modo che vengano fornite tramite la nuova posizione principale.
- Se non è possibile aggiornare le allocazioni dei prodotti in modo che provengano dalla nuova organizzazione principale, i prodotti vengono rimossi insieme ai profili di prodotto di tali prodotti. Gli utenti possono perdere l&#39;accesso a causa di questa operazione. Affinché il prodotto sia disponibile nella nuova posizione, è necessario che il prodotto sia disponibile nel predecessore comune più vicino tra la vecchia e la nuova posizione.

>[!WARNING]
>
>Se i prodotti vengono rimossi a seguito del reparenting, gli utenti perdono l’accesso a tali prodotti.

1. Accedi a [Global Admin Console](https://global-admin-console.adobe.com/). Nella scheda **[!UICONTROL Organizzazioni]**, seleziona **[!UICONTROL Cambia gerarchia]** per abilitare il ripristino delle organizzazioni.
2. Selezionare **[!UICONTROL OK]** nella schermata popup visualizzata.
3. Per creare un padre, trascina l’organizzazione figlio sopra l’organizzazione desiderata.
4. Seleziona **[!UICONTROL Salva]** dopo aver completato il ripristino delle organizzazioni.
5. Seleziona **[!UICONTROL Rivedi modifiche in sospeso]** dopo aver completato la modifica delle organizzazioni. Dopo la revisione, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/it/enterprise/global-admin-console/execute-jobs.html).

Una volta completato il processo, puoi passare ad Allocazione prodotto e [modificare i valori di concessione](https://helpx.adobe.com/it/enterprise/global-admin-console/allocate-products.html) per riflettere la modifica nell&#39;allocazione delle risorse prodotto.

## Aggiungere organizzazioni esistenti utilizzando Organization Mapper

In qualità di [Amministratore globale](https://helpx.adobe.com/it/enterprise/global-admin-console/manage-administrators.html), puoi aggiungere organizzazioni esistenti che non fanno attualmente parte della gerarchia del Global Admin Console alla gerarchia delle organizzazioni.

Puoi anche aggiungere organizzazioni del team alla gerarchia dell&#39;organizzazione. Le organizzazioni del team non partecipano all&#39;allocazione del prodotto o al rollup dell&#39;utilizzo del prodotto e la gestione delle organizzazioni del team nel Global Admin Console è limitata. Puoi aggiungerli alla gerarchia dell&#39;organizzazione per tenerne traccia e avere visibilità sui prodotti che acquistano. Le organizzazioni del team non possono includere organizzazioni secondarie e non dispongono di molte funzioni delle organizzazioni aziendali.

Ulteriori informazioni sulle [limitazioni all&#39;allocazione dei prodotti](https://helpx.adobe.com/it/enterprise/global-admin-console/allocate-products.html#limitations).

>[!WARNING]
>
> Puoi aggiungere solo organizzazioni secondarie alle organizzazioni principali basate sullo stesso modello di archiviazione. Pertanto, le organizzazioni secondarie basate sul modello di archiviazione utente possono essere aggiunte solo alle organizzazioni principali basate sul modello di archiviazione utente. Inoltre, le organizzazioni secondarie basate sul modello di archiviazione aziendale possono essere aggiunte solo alle organizzazioni principali basate sul modello di archiviazione aziendale.
>Puoi aggiungere solo organizzazioni secondarie alle organizzazioni principali basate sullo stesso modello di archiviazione. Pertanto, le organizzazioni secondarie basate sul modello di archiviazione utente possono essere aggiunte solo alle organizzazioni principali basate sul modello di archiviazione utente. Inoltre, le organizzazioni secondarie basate sul modello di archiviazione aziendale possono essere aggiunte solo alle organizzazioni principali basate sul modello di archiviazione aziendale.

La scheda **[!UICONTROL Mappatura organizzazioni]** mostra quanto segue:

1. Un menu a discesa con un elenco di possibili organizzazioni principali in cui è possibile aggiungere un&#39;organizzazione secondaria. Queste sono le organizzazioni di cui sei un amministratore globale.
1. Un elenco di organizzazioni secondarie che possono essere aggiunte sotto l&#39;organizzazione principale selezionata nel passaggio 1. Si tratta di organizzazioni per le quali l&#39;utente è amministratore di sistema e che non sono già figlio di un&#39;altra organizzazione.

Quando un&#39;organizzazione viene aggiunta all&#39;amministrazione globale, i prodotti nelle organizzazioni aggiunte mediante Mapper organizzazione rimangono come acquisti; i numeri di [Allocazione prodotto](https://helpx.adobe.com/it/enterprise/global-admin-console/allocate-products.html) cessano l&#39;aggregazione in queste organizzazioni.

1. Accedi a [Global Admin Console](https://global-admin-console.adobe.com/) e passa a **[!UICONTROL Organization Mapper]**.
2. Seleziona un’organizzazione principale dall’elenco a discesa.\
   Si tratta delle organizzazioni per le quali si viene aggiunti direttamente come amministratore globale. Nell&#39;elenco a discesa, se non vedi un&#39;organizzazione che desideri utilizzare come principale, selezionane una più in alto nella gerarchia. Una volta completata l&#39;operazione di mappatura dell&#39;organizzazione, puoi utilizzare [Modifica gerarchia](https://helpx.adobe.com/it/enterprise/global-admin-console/set-up-organizations.html#change-the-parent-of-an-organization) per spostare la nuova organizzazione in basso nella struttura per ottenere l&#39;organizzazione principale che desideri utilizzare.
3. Seleziona le organizzazioni da aggiungere come secondarie dell&#39;organizzazione selezionata nel passaggio precedente.
4. Selezionare **[!UICONTROL Rivedi modifiche in sospeso]**. Quindi, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/it/enterprise/global-admin-console/execute-jobs.html).
5. Dopo aver eseguito le modifiche, è possibile ripetere i passaggi precedenti per aggiungere ulteriori organizzazioni figlio alla gerarchia organizzazione.

Una volta che un&#39;organizzazione si trova nella gerarchia, è possibile modificare i criteri dell&#39;organizzazione, gli amministratori o altre impostazioni passando alla scheda **[!UICONTROL Organizzazioni]**.
