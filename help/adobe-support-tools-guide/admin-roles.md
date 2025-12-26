---
title: Ruoli amministrativi
description: Utilizzando Adobe Admin Console, le organizzazioni possono definire una gerarchia amministrativa flessibile che consente una gestione dettagliata dell’accesso e dell’utilizzo dei prodotti Adobe.
source-git-commit: 13e89a152d9387a8b23544e6b6c6e3cad5856666
workflow-type: tm+mt
source-wordcount: '1642'
ht-degree: 0%

---

# Ruoli amministrativi

Utilizzando Adobe Admin Console, le organizzazioni possono definire una gerarchia amministrativa flessibile che consente una gestione dettagliata dell’accesso e dell’utilizzo dei prodotti Adobe. Uno o più amministratori di sistema, il cui provisioning è stato eseguito durante il processo di onboarding aziendale, si trovano nella parte superiore della gerarchia. Questi amministratori di sistema possono delegare responsabilità ad altri amministratori, pur mantenendo il controllo generale.

I ruoli amministrativi offrono alle aziende i seguenti vantaggi principali:

* decentramento controllato delle responsabilità amministrative
* Visualizzazione rapida delle assegnazioni dei prodotti, per utente e per prodotto
* Funzionalità per assegnare quote agli amministratori di prodotto

## Gerarchia amministrativa

Applicabile a: clienti aziendali Adobe.

La gerarchia amministrativa può essere utilizzata per soddisfare i requisiti specifici dell&#39;azienda. Ad esempio, un’azienda può nominare diversi amministratori per gestire i diritti alle offerte Adobe Creative Cloud e Adobe Marketing Cloud. In alternativa, un’azienda può avere diversi amministratori per gestire le adesioni degli utenti appartenenti a diverse unità aziendali.

>[!NOTE]
>
>La gerarchia amministrativa non si applica ai clienti dei team. I clienti Team hanno un solo ruolo di **Amministratore di sistema**. Il proprietario del contratto (_precedentemente denominato **Amministratore principale**_) è l&#39;amministratore di sistema con accesso ai dettagli del contratto e alla cronologia di fatturazione. Se sei il proprietario del contratto corrente, puoi nominare un amministratore di sistema esistente (_ precedentemente denominato **amministratore secondario**_) come proprietario del contratto.

![immagine amministratore](assets/storage_admin.png)

_Gerarchia ruoli amministratore_

| Ruolo | Descrizione |
|--- |--- |
| **Amministratore di sistema** | Utente privilegiato per l’organizzazione; autorizzato a eseguire tutte le attività amministrative nell’Admin Console.<br>Inoltre, dispone delle autorizzazioni per delegare le seguenti funzionalità amministrative ad altri utenti: amministratore di prodotto, amministratore del profilo di prodotto, amministratore del gruppo di utenti, amministratore della distribuzione e amministratore del supporto. |
| **Amministratore prodotto** | Amministra i prodotti assegnati a tale amministratore e tutte le funzioni amministrative associate, tra cui:<ul><li>Creare profili di prodotto</li><li>Aggiungi utenti e gruppi di utenti all’organizzazione, ma non rimuovi questi</li><li>Aggiungere o rimuovere utenti e gruppi di utenti dai profili di prodotto</li><li>Aggiungere o rimuovere gli amministratori dei profili di prodotto dai profili di prodotto</li><li>Aggiungi o rimuovi altri amministratori di prodotto dal prodotto</li><li>Aggiungere o rimuovere gli amministratori di gruppi dai gruppi</li></ul> |
| **Amministratore profilo prodotto** | Amministra le descrizioni del profilo di prodotto assegnate a tale amministratore e tutte le funzioni amministrative associate, tra cui:<ul><li>Aggiungi utenti e gruppi di utenti all’organizzazione, ma non rimuovi questi</li><li>Aggiungere o rimuovere utenti e gruppi di utenti dai profili di prodotto</li><li>Assegnare o revocare le autorizzazioni di prodotto a utenti e gruppi di utenti dai profili di prodotto</li><li>Gestire i ruoli prodotto di utenti e gruppi di utenti per i profili di prodotto |
| **Amministratore gruppo utenti** | Amministra le descrizioni dei gruppi di utenti assegnate a tale amministratore e tutte le funzioni amministrative associate, tra cui:<ul><li>Aggiungere o rimuovere utenti dai gruppi</li><li>Aggiungere o rimuovere gli amministratori dei gruppi di utenti dai gruppi |
| **Amministratore distribuzione** | Crea, gestisce e distribuisce pacchetti software e aggiornamenti agli utenti finali. |
| **Amministratore supporto** | Ruolo non amministrativo che ha accesso a informazioni relative al supporto, ad esempio i report sui problemi segnalati dai clienti. |
| **Amministratore archiviazione** | Gestisce l&#39;amministrazione dello storage dell&#39;organizzazione. L’amministratore può visualizzare il consumo di archiviazione degli utenti attivi e inattivi e trasferire i contenuti ad altri destinatari. |

Per un elenco dettagliato delle autorizzazioni e dei privilegi per ogni ruolo amministratore, vedere [Autorizzazioni](#enterprise-admins-permissions-matrix).

## Aggiungere un ruolo di amministratore Enterprise {#add-enterprise-role}

Applicabile a: clienti aziendali Adobe.

In qualità di amministratore, puoi assegnare un ruolo di amministratore ad altri utenti, concedendo loro gli stessi privilegi che hai, o i privilegi per un ruolo sotto il tuo ruolo di amministratore nella gerarchia come descritto [sopra](#administrative-hierarchy). Ad esempio, in qualità di amministratore di prodotto puoi assegnare a un utente i privilegi di amministratore di prodotto o i privilegi di amministratore del profilo di prodotto, ma non i privilegi di amministratore della distribuzione. Per informazioni sulle autorizzazioni in Admin Console, vedere la [Matrice di autorizzazioni](#enterprise-admins-permissions-matrix).

Per aggiungere o invitare un amministratore:

1. In **[!UICONTROL Adobe Admin Console](https://adminconsole.adobe.com/)** scegliere **[!UICONTROL Utenti]** > **[!UICONTROL Amministratori]**.

   In alternativa, vai al prodotto, al profilo di prodotto o al gruppo di utenti pertinente e passa alla scheda **[!UICONTROL Amministratori]**.

1. Fai clic su **[!UICONTROL Aggiungi amministratore]**.
1. Immetti un nome o un indirizzo e-mail. Puoi cercare utenti esistenti o aggiungere un nuovo utente specificando un indirizzo e-mail valido e compilando le informazioni sullo schermo.
1. Fai clic su **[!UICONTROL Avanti]**. Viene visualizzato un elenco di ruoli di amministratore.

   >[!NOTE]
   >
   >* Le opzioni di questa schermata dipendono dall’account e dal ruolo di amministratore. Puoi assegnare gli stessi privilegi che hai o i privilegi per un ruolo sotto il tuo nella gerarchia.
   >* In qualità di amministratore di sistema di un team, puoi assegnare un solo ruolo amministratore: amministratore di sistema.

1. Seleziona uno o più ruoli di amministratore.
1. Per i tipi di amministratore come Amministratore prodotto, Amministratore profilo prodotto e Amministratore gruppo utenti, seleziona rispettivamente prodotti, profili e gruppi specifici.

   >[!NOTE]
   >
   >Per un amministratore del profilo di prodotto, puoi includere profili per più di un prodotto.

   ![aggiungi amministratore](assets/add-admin.png)

1. Rivedi i ruoli di amministratore assegnati all&#39;utente e fai clic su **Salva**.

L&#39;utente riceve un invito e-mail relativo ai nuovi privilegi di amministratore da `message@adobe.com`.

Gli utenti devono fare clic su **[!UICONTROL Inizia]** nell&#39;e-mail per partecipare all&#39;organizzazione. Se i nuovi amministratori non utilizzano il collegamento **[!UICONTROL Inizia]** nell&#39;invito e-mail, non potranno accedere ad Admin Console.

Come parte del processo di accesso, agli utenti può essere richiesto di impostare un profilo Adobe se non ne hanno già uno. Se all’indirizzo e-mail sono associati più profili, gli utenti devono scegliere &quot;Unisciti al team&quot; (se richiesto) e quindi selezionare il profilo associato alla nuova organizzazione.

![immagine diritti amministratore](assets/admin-get-started-email.png)

## Aggiungi un amministratore team {#add-admin-teams}

Applicabile a: Team di clienti di Adobe.

In qualità di amministratore, puoi assegnare il ruolo di amministratore di sistema ad altri utenti, concedendo loro gli stessi privilegi che hai.

Per aggiungere o invitare un amministratore di sistema:

1. In **[!UICONTROL Adobe Admin Console]** scegliere **[!UICONTROL Utenti]** > **[!UICONTROL Amministratori]**.

   Viene visualizzato un elenco degli amministratori esistenti.

1. Fai clic su **[!UICONTROL Aggiungi amministratore]**.

   Viene visualizzata la schermata **[!UICONTROL Aggiungi un amministratore]**.

1. Immetti un nome o un indirizzo e-mail. Puoi cercare utenti esistenti o aggiungere un nuovo utente specificando un indirizzo e-mail valido e compilando le informazioni sullo schermo.

   Per impostazione predefinita, l&#39;opzione Amministratore di sistema è selezionata.

1. Fai clic su **[!UICONTROL Salva]**.

![immagine amministratore team](assets/teams-admin.png)

Poiché tutti gli utenti di un&#39;organizzazione team sono utenti Business ID, ricevono un invito e-mail riguardante i nuovi privilegi di amministratore da `message@adobe.com`.
Per aderire all’organizzazione, gli utenti devono fare clic su Inizia nell’e-mail.

Come parte del processo di accesso, agli utenti può essere richiesto di impostare un profilo Adobe se non ne hanno già uno. Se all’indirizzo e-mail sono associati più profili, gli utenti devono scegliere &quot;Unisciti al team&quot; (se richiesto) e quindi selezionare il profilo associato alla nuova organizzazione.

![immagine diritti amministratore](assets/admin-get-started-email.png)

## Modifica ruolo amministratore organizzazione

Applicabile a: clienti aziendali Adobe.

In qualità di amministratore, puoi modificare il ruolo di amministratore in altri amministratori che si trovano sotto di te nella gerarchia Amministrativa. Ad esempio, puoi rimuovere i privilegi di amministratore di altri amministratori.

Per modificare i ruoli di amministratore:

1. In **[!UICONTROL Adobe Admin Console]** scegliere **[!UICONTROL Utenti]** > **[!UICONTROL Amministratori]**. Viene visualizzato l’elenco degli amministratori esistenti.

   In alternativa, vai al prodotto, al profilo di prodotto o al gruppo di utenti pertinente e passa alla scheda **[!UICONTROL Amministratori]**.

1. Fai clic sul nome dell’amministratore da modificare.
1. In **[!UICONTROL Dettagli utente]**, fai clic su ![icona](assets/one-console-ellipses.png) per la sezione **Diritti amministrativi** e scegli **[!UICONTROL Modifica diritti amministratore]**.

   ![modifica diritti amministratore](assets/admin-rights-section.png)

1. Modifica i diritti di amministrazione e salva le modifiche.

## Modifica ruolo amministratore team

Applicabile a: Team di clienti di Adobe.

In qualità di amministratore di sistema dei team, puoi rimuovere i privilegi di amministratore di sistema di altri amministratori.

Per revocare i privilegi di amministratore di sistema:

1. In **[!UICONTROL Adobe Admin Console]** scegliere **[!UICONTROL Utenti]** > **[!UICONTROL Amministratori]**.

   Viene visualizzato l’elenco degli amministratori esistenti.

1. In **[!UICONTROL Dettagli utente]**, fai clic su ![icona](assets/one-console-ellipses.png) a destra della sezione **[!UICONTROL Diritti amministrativi]** e scegli **[!UICONTROL Modifica diritti amministratore]**.

   ![modifica diritti amministratore](assets/admin-rights-section.png)

1. Modifica i diritti di amministrazione e salva le modifiche.

## Rimuovere un amministratore

Applicabile a: Adobe unisce i clienti aziendali.

Per revocare le autorizzazioni di amministratore, selezionare un utente e quindi fare clic su **[!UICONTROL Rimuovi amministratore]**.

![rimuovi immagine amministratore](assets/remove-admin.png)

>[!NOTE]
>
>La rimozione di un amministratore non comporta l’eliminazione dell’utente da Admin Console, ma solo la rimozione dei privilegi associati al ruolo di amministratore.

## Matrice delle autorizzazioni per gli amministratori Enterprise

Applicabile a: clienti aziendali Adobe.

Nella tabella seguente sono elencate tutte le autorizzazioni per i diversi tipi di amministratori, suddivise per le seguenti aree di funzionalità:

### Gestione delle identità

| Autorizzazione | Amministratore di sistema | Amministratore del supporto |
|--- |--- |--- |
| Aggiungi dominio (richiedi/richiedi un dominio) | ✔ | |
| Visualizza elenco domini e domini | ✔ | |
| Gestire le chiavi di crittografia del dominio | ✔ | |
| Gestisci criteri password organizzazione predefiniti | ✔ | |
| Visualizza criterio password organizzazione predefinito | ✔ | |

### Gestione degli utenti

| Autorizzazione | Amministratore di sistema | Amministratore del supporto |
|--- |--- |--- |
| Aggiungi utente all&#39;organizzazione | ✔ | |
| Rimuovi utente dall’organizzazione | ✔ | |
| Visualizza dettagli utente ed elenco | ✔ | |
| Modifica profilo utente | ✔ | |
| Aggiungi profilo prodotto a utente o gruppo | ✔ | |
| Rimuovi profilo prodotto a utente o gruppo | ✔ | |
| Aggiungere un profilo di prodotto a più utenti | ✔ | |
| Visualizzare i profili di prodotto di un utente | ✔ | |
| Visualizza elenco utenti prodotti | ✔ | |
| Aggiungere utenti in blocco all’organizzazione | ✔ | |

### Gestione amministratore

| Autorizzazione | Amministratore di sistema | Amministratore del supporto |
|--- |--- |--- |
| Concedere l’amministratore dell’organizzazione a un utente | ✔ | |
| Revoca dell&#39;amministratore dell&#39;organizzazione da un utente | ✔ | |
| Concedere l’amministratore della licenza di prodotto a un utente | ✔ | |
| Revoca dell’amministratore della licenza del prodotto da un utente | ✔ | |
| Concedere l’amministratore della distribuzione a un utente | ✔ | |
| Revoca dell&#39;amministratore della distribuzione da un utente | ✔ | |
| Concedere a un utente l’amministratore di un gruppo di utenti | ✔ | |
| Revoca dell&#39;amministratore del gruppo utenti da un utente | ✔ | |
| Concedere l’amministratore del proprietario del prodotto a un utente | ✔ | |
| Revoca l&#39;amministratore del proprietario del prodotto da un utente | ✔ | |

### Gestione della configurazione della licenza del prodotto

| Autorizzazione | Amministratore di sistema | Amministratore del supporto |
|--- |--- |--- |
| Concedi diritto prodotto all&#39;organizzazione | | |
| Rimuovi adesione prodotto da organizzazione | | |
| Visualizza il numero totale di licenze di proprietà dell’organizzazione | ✔ | |
| Visualizza prodotti e famiglie di prodotti disponibili | ✔ | |
| Modifica descrizione/dati licenza prodotto | ✔ | |
| Fornire la licenza del prodotto a un utente | ✔ | |
| Annullamento del provisioning della licenza di un prodotto da parte di un utente | ✔ | |
| Aggiungi nuova configurazione licenza prodotto | ✔ | |
| Modifica configurazione servizio licenze prodotto | ✔ | |
| Elimina configurazione servizio licenze prodotto | ✔ | |
| Rimuovere l’accesso al prodotto da un utente (rimuovere tutte le configurazioni) | ✔ | |

### Gestione dello storage

| Autorizzazione | Amministratore di sistema | Amministratore del supporto |
|--- |--- |--- |
| Visualizzare cartelle utente attive e inattive | ✔ | |
| Eliminare le cartelle utente inattive e trasferire il contenuto | ✔ | |

### Distribuzione

| Autorizzazione | Amministratore di sistema | Amministratore del supporto |
|--- |--- |--- |
| Scheda Visualizza/utilizza pacchetti | ✔ | |

### Supporto

| Autorizzazione | Amministratore di sistema | Amministratore del supporto |
|--- |--- |--- |
| Visualizza scheda supporto | ✔ | |
| Gestire i casi di supporto | ✔ | ✔ |

### Gestione dei gruppi di utenti

| Autorizzazione | Amministratore di sistema | Amministratore del supporto |
|--- |--- |--- |
| Crea gruppo utenti | ✔ | |
| Rimuovi gruppo utenti | ✔ | |
| Aggiungi utente a gruppo di utenti | ✔ | |
| Rimuovi utente dal gruppo di utenti | ✔ | |
| Assegna gruppo di utenti alla licenza del prodotto | ✔ | |
| Rimuovi gruppo utenti dalla licenza del prodotto | ✔ | |
| Visualizza membro del gruppo di utenti | ✔ | ✔ |
| Visualizza elenco gruppi di utenti | ✔ | ✔ |