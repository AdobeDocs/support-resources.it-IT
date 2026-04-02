---
title: Selezionare un'organizzazione in Global Admin Console
description: Scopri come scegliere un’organizzazione per la modifica in Global Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: 6a94922a-3343-433d-96e7-0af0f26581a1
source-git-commit: 976bfc44cdae61376e2da89019f7758518c6fadc
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 1%

---

# Selezionare un&#39;organizzazione in Global Admin Console

Scopri come scegliere un’organizzazione per la modifica in Global Admin Console.

>[!NOTE]
>
>Dopo aver avuto accesso a [Global Admin Console](https://experienceleague.adobe.com/it/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console), puoi iniziare selezionando un&#39;organizzazione per visualizzarne e gestirne il nome, i gruppi di utenti, i profili di prodotto, gli amministratori e i criteri di organizzazione. Per accedere a Global Admin Console, [fai clic qui](https://global-admin-console.adobe.com/).

Global Admin Console funge da hub di gestione centrale dell’organizzazione per le risorse Adobe. Gli amministratori globali possono:

- Creare organizzazioni figlio nell’ambito della propria organizzazione
- Assegnare gli amministratori di sistema per gestirli
- Distribuisci le risorse alle organizzazioni figlie per la gestione e l&#39;assegnazione agli utenti di tali organizzazioni

>[!NOTE]
>
> Gli utenti e gli amministratori di un&#39;organizzazione non hanno visibilità su utenti, storage o altre risorse esterne all&#39;organizzazione.

## Seleziona la tua organizzazione

Le organizzazioni elencate nell&#39;elenco a discesa **[!UICONTROL selettore organizzazione]** sono quelle di cui sei esplicitamente amministratore globale, ovvero che sei stato aggiunto all&#39;elenco degli amministratori per tale organizzazione con un ruolo di amministratore globale o di visualizzatore globale. Sei implicitamente un amministratore globale (o visualizzatore globale) di tutte le organizzazioni al di sotto di quel punto nella gerarchia, ma tali organizzazioni non sono elencate nel selettore [!UICONTROL org].

![Selettore organizzazione](/help/adobe-support-tools-guide/assets/org-picker.png)

Se desideri che vengano elencate, aggiungi te te stesso o te stessa come amministratore globale alle organizzazioni che desideri elencare. Quando selezioni un&#39;organizzazione nel [!UICONTROL selettore organizzazione], le tue autorizzazioni amministrative si basano sul fatto di essere un amministratore globale dell&#39;organizzazione selezionata. Potresti anche essere elencato come amministratore globale di un’organizzazione principale più in alto nella struttura, il che potrebbe darti più autorizzazioni. Devi selezionare l&#39;organizzazione di livello superiore per ottenere le autorizzazioni aggiuntive.

In Global Admin Console, dopo aver selezionato un&#39;organizzazione dalla [!UICONTROL struttura gerarchica], è possibile iniziare a modificare le informazioni per una determinata organizzazione.

**Le modifiche possono interessare:**

- Nome organizzazione
- Gruppi di utenti
- Profili di prodotto
- Amministratori
- Criteri dell’organizzazione

**Le modifiche non possono interessare:**

- Utenti (ad eccezione dell’eliminazione di gruppi o profili di prodotto)
- Aggiunta di utenti (tranne per gli amministratori)

Quando un’organizzazione viene selezionata dalla struttura gerarchica, vengono visualizzate le seguenti informazioni:

- Nome organizzazione
- Area geografica
- Numero di utenti
- Elenco dei prodotti
- Profili di prodotto
- Gruppi di utenti
- Amministratori
- Domini dichiarati
- Valori dei criteri dell&#39;organizzazione

Per visualizzare o modificare prodotti, gruppi di utenti, amministratori, domini, criteri o modelli di criteri, selezionare la scheda appropriata. Nella maggior parte dei casi è possibile utilizzare il campo [!UICONTROL ricerca] per individuare un elemento specifico all&#39;interno della scheda.

![Modifica un&#39;organizzazione](/help/adobe-support-tools-guide/assets/edit-an-organization.png)

Tutti gli amministratori aggiunti o rimossi da un’organizzazione riceveranno una notifica e-mail. Alcune modifiche dei criteri apportate a un&#39;organizzazione generano una notifica in [!DNL Admin Console] dell&#39;organizzazione.

## Scopri i vincoli e le condizioni necessarie

- La profondità massima per le organizzazioni di nidificazione è cinque. Quindi, a/b/c/d/e è consentito ma a/b/c/d/e/f è un errore. Ad esempio, Acme Corp/ International Region/ Acme Europe/ Acme UK/ Acme London è consentito, ma Acme Corp/ International Region/ Acme Europe/ Acme UK/ Acme London/ Acme Mayfair è un errore.

- La lunghezza massima del percorso (incluse tutte le organizzazioni) è di 255 caratteri (incluso &quot;/&quot;). La lunghezza massima per un nome di organizzazione singolo è compresa tra 4 e 100 caratteri.

- Il percorso dell’organizzazione è univoco, ma il nome semplice è univoco solo tra i suoi pari livello. In altre parti della gerarchia delle organizzazioni possono essere presenti organizzazioni con lo stesso nome semplice.

- Puoi visualizzare l’elenco dei domini collegati all’organizzazione selezionata solo utilizzando Global Admin Console. Se sei un amministratore di sistema dell&#39;organizzazione selezionata, seleziona **[!UICONTROL Apri in Admin Console]** per [gestire i domini](https://helpx.adobe.com/it/enterprise/using/manage-domains-directories.html). Per informazioni visualizzate nella scheda Domini, vedere [esportare e importare schemi](https://experienceleague.adobe.com/it/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/export-or-import-organization-structure-and-product-allocations#export-and-import-schemas).

- IE 11 non è supportato per l&#39;accesso all&#39;amministrazione globale. Utilizza un browser diverso o una versione più recente del browser IE.
