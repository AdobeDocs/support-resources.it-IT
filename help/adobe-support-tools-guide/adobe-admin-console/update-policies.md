---
title: Aggiornare i criteri dell’organizzazione in Global Admin Console
description: Scopri come un amministratore globale può impostare e modificare i criteri per un’organizzazione e i relativi elementi secondari in Global Admin Console.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2:
  - id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
exl-id: bf8d4e71-30a6-4d6c-8749-47070e5b1906
source-git-commit: 90807a4e803de702c9e0975df551efefc254030a
workflow-type: tm+mt
source-wordcount: 1007
ht-degree: 0%

---

# Aggiornare i criteri dell’organizzazione in Global Admin Console

**Si applica a:** Enterprise

Scopri come un amministratore globale può impostare e modificare i criteri per un’organizzazione e i relativi elementi secondari in Global Admin Console.

>[!NOTE]
>
>In [Global Admin Console](https://helpx.adobe.com/it/enterprise/global-admin-console/adopt-global-administration.html), selezionare un&#39;organizzazione dalla gerarchia e passare alla scheda **Criteri** per consentire o disabilitare i criteri oppure bloccarli.
>
> [Accedi a Global Admin Console](https://global-admin-console.adobe.com/)

I criteri sono associati a un&#39;organizzazione e limitano le operazioni che possono essere eseguite su tale organizzazione. Quando un valore di criterio viene impostato, limita o abilita le azioni da quel momento in poi.
Ad esempio, se il criterio **Domini attestazione** è impostato su *non consentito*, non è possibile richiedere domini aggiuntivi, ma non influisce su eventuali domini dichiarati prima di impostare il valore del criterio.

## Configurare i criteri

Per modificare i criteri di un&#39;organizzazione, eseguire le operazioni seguenti:

1. In Global Admin Console, [seleziona un&#39;organizzazione](https://helpx.adobe.com/it/enterprise/global-admin-console/overview.html) da modificare, quindi passa alla scheda **[!UICONTROL Criteri]**.
1. Seleziona l’opzione per il criterio pertinente per consentirlo o disattivarlo. È inoltre possibile bloccare un criterio in modo che solo un amministratore globale dell&#39;[organizzazione selezionata](https://helpx.adobe.com/it/enterprise/global-admin-console/overview.html) o la relativa organizzazione padre possa modificarlo o sbloccarlo.
1. Per bloccare un criterio, selezionare l&#39;icona **[!UICONTROL Blocca]** ![Blocca](./assets/lock.png). Passando il mouse sul blocco viene visualizzato il nome dell&#39;organizzazione selezionata. Ulteriori informazioni sui [blocchi dei criteri](#policy-locks).
1. Seleziona **[!UICONTROL Rivedi modifiche in sospeso]** dopo aver completato la modifica delle organizzazioni. Dopo la revisione, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/it/enterprise/global-admin-console/execute-jobs.html).

## Blocchi dei criteri {#policy-locks}

Quando un criterio è bloccato, il suo valore non può essere modificato finché il criterio non viene sbloccato. Global Admin Console ricorda la [organizzazione selezionata](https://helpx.adobe.com/it/enterprise/global-admin-console/overview.html) nel selettore organizzazione come l&#39;organizzazione da cui è stato bloccato il criterio. Qualsiasi amministratore globale dell’organizzazione selezionata o di qualsiasi organizzazione più in alto nella struttura dispone dell’autorizzazione per sbloccare il criterio. Gli amministratori globali il cui ambito è inferiore a quello dell&#39;organizzazione non dispongono dell&#39;autorizzazione per sbloccare e modificare i valori dei criteri.

Per creare un ambiente bloccato, imposta i valori dei criteri desiderati nelle organizzazioni figlie e quindi bloccalo. Gli amministratori globali di tali organizzazioni figlio non saranno in grado di modificare i valori dei criteri.

### Esempio: ambiente bloccato

Se Elissa, l&#39;amministratore globale della *Divisione Acme*, crea organizzazioni figlio *Marketing* e *Engineering*, aggiunge Robert come amministratore globale di *Marketing* e Sarah come amministratore globale di *Engineering*. Quindi imposta diversi criteri su *Non consentito* e *blocca*. Elissa può sbloccare e modificare i valori dei criteri quando sceglie *Divisione Acme* come organizzazione selezionata, ma Robert e Sarah non possono sbloccare i criteri per le organizzazioni di cui sono amministratori globali perché i criteri sono bloccati dall&#39;organizzazione *Divisione Acme*.

## Dettagli criterio

### Gestione organizzazione

| Nome criterio | Descrizione |
| --- | --- |
| **Crea organizzazioni figlio** | Consente agli amministratori globali di creare organizzazioni figlio. Se *off*, non è possibile creare organizzazioni figlio. |
| **Rinomina organizzazione** | Se consentito, un amministratore globale o di sistema può rinominare l’organizzazione. Controlla anche la modifica del paese dell’organizzazione. È inoltre possibile modificare il percorso di un&#39;organizzazione indipendentemente da questa impostazione dei criteri se un&#39;organizzazione padre viene rinominata o se l&#39;organizzazione o un predecessore dell&#39;organizzazione è rigenitore. |
| **Elimina organizzazioni** | Consente agli amministratori globali di eliminare le organizzazioni figlie. Ciò diventa ancora più importante quando le organizzazioni con storage aziendale sono abilitate a causa del rischio di eliminazione delle risorse utente. |

### Gestione amministratore

| Nome criterio | Descrizione |
| --- | --- |
| **Aggiungi o elimina amministratori** | Consente agli amministratori globali di aggiungere nuovi amministratori a un’organizzazione. Se *off*, non è possibile aggiungere nuovi amministratori. |
| **Eredita gli amministratori di sistema dal padre quando viene creata l&#39;organizzazione figlio** | Quando gli amministratori globali creano nuove organizzazioni figlie, gli amministratori di sistema del padre diventano automaticamente amministratori di sistema della nuova organizzazione. Il criterio è *off* per impostazione predefinita. |
| **Gestisci amministratori** | Consente agli amministratori globali di modificare o rimuovere/modificare le autorizzazioni di amministratore. |

### Gestione utente

| Nome criterio | Descrizione |
| --- | --- |
| **Eredita utenti da directory gestite dall&#39;organizzazione padre** | Il criterio deve essere attivato *il* e attivo prima di creare la nuova organizzazione figlio. Quando viene creata un’organizzazione figlio, gli utenti dell’organizzazione padre vengono resi disponibili come utenti nell’organizzazione figlio. In altre parole, questo criterio imposta automaticamente una relazione di trust tra l&#39;elemento padre e l&#39;elemento figlio quando viene creato il nuovo elemento figlio all&#39;interno della CAG. Per le organizzazioni esistenti, tutte le relazioni di trust precedenti all&#39;aggiunta alla CAG rimarranno una volta inserite nella CAG. Se non sono presenti relazioni di trust, è necessario seguire il processo di richiesta di trust abituale. Per il successo di questo criterio, l&#39;amministratore globale che crea la nuova organizzazione deve essere anche un amministratore di sistema dell&#39;organizzazione padre con il dominio richiesto. In caso contrario, la relazione di trust tra domini non verrà ereditata nell’organizzazione appena creata. |
| **Aggiungi utenti Adobe ID** | Se questa opzione è impostata, l’organizzazione non può aggiungere utenti di tipo Adobe ID tramite Admin Console, User Management API (UMAPI) né il meccanismo di sincronizzazione. |
| **Gestione gruppi utenti** | Se consentito, gli amministratori globali, di sistema e dei gruppi di utenti possono creare, modificare ed eliminare gruppi di utenti. |

### Applicazione di directory e domini

| Nome criterio | Descrizione |
| --- | --- |
| **Domini attestazione** | Se questa opzione è impostata, gli amministratori di sistema possono richiedere i domini su Admin Console. |
| **Modifica configurazione identità** | Se questa opzione è impostata, gli amministratori di sistema possono modificare la configurazione dell’identità utente in Admin Console. |

### Allocazione prodotti

| Nome criterio | Descrizione |
| --- | --- |
| **Gestisci prodotti** | Consente agli amministratori globali di aggiungere o rimuovere prodotti e modificare le sovvenzioni per le risorse dei prodotti. |

### Condivisione di risorse

| Nome criterio | Descrizione |
| --- | --- |
| **L&#39;amministratore del sistema o dell&#39;archiviazione può modificare le impostazioni di condivisione delle risorse** | Se consentito, gli amministratori di sistema e di storage possono modificare le impostazioni di condivisione delle risorse, inclusi i contatti di sicurezza, le regole per le password e le regole di archiviazione. |
| **Eredita criterio di condivisione da un elemento padre quando viene creata un&#39;organizzazione** | Se consentite, le impostazioni di condivisione delle risorse vengono ereditate dall&#39;elemento padre quando viene creata un&#39;organizzazione figlio. Le impostazioni di condivisione delle risorse includono contatti di sicurezza, criteri per le password e criteri di archiviazione. Questo vale solo per le organizzazioni appena create al momento della creazione. È impostata su un elemento padre e influisce sulla creazione di organizzazioni figlio sotto tale elemento padre. |
