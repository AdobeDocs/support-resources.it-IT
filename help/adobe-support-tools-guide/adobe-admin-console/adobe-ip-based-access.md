---
title: Limitare l’accesso ai prodotti tramite indirizzi IP
description: Utilizza l’accesso basato su IP per controllare l’accesso degli utenti ai prodotti Adobe e limitare l’utilizzo agli intervalli IP pubblici approvati.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: e4595040-3930-48af-9888-cf1349596c77
source-git-commit: d5f0473b100cda574b4980e6c871a9c275f9f95a
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%

---

# Limitare l’accesso ai prodotti tramite indirizzi IP

Applicabile all&#39;azienda.

Utilizza l’accesso basato su IP per controllare l’accesso degli utenti ai prodotti Adobe e impedire l’uso non autorizzato di indirizzi IP pubblici non elencati.

Vai a [Admin Console](https://adminconsole.adobe.com/settings/identity) per aggiungere indirizzi IP pubblici attendibili al **accesso basato su IP** per utilizzare in modo sicuro le app e i servizi Adobe. Il inserisco nell&#39;elenco Consentiti di accesso basato su IP consente di utilizzare in modo sicuro le app e i servizi.

## Vantaggi dell&#39;accesso basato su IP

Il controllo degli accessi basato su IP utilizza un inserisco nell&#39;elenco Consentiti di degli indirizzi IP per limitare l’uso dei prodotti Adobe da indirizzi IP pubblici casuali. L’accesso basato su IP si applica a tutte le directory e ai prodotti associati nel Adobe Admin Console.

Puoi aggiungere indirizzi IP pubblici attendibili all&#39;elenco **Indirizzi IP consentiti** per impedire agli utenti di:

- Accesso a prodotti da IP pubblici che non rientrano negli intervalli IP consentiti
- Accesso a [profili utente](https://helpx.adobe.com/it/enterprise/using/manage-adobe-profiles.html) di Adobe da IP pubblici che non rientrano negli intervalli IP consentiti
- Cambio dei profili utente nelle app web al di fuori degli intervalli IP consentiti

  ![Esporta struttura organizzazione](./assets/ip-based-access.avif)

## Abilita accesso basato su IP

### Considerazioni importanti

>[!IMPORTANT]
>
>- Gli amministratori devono iniziare aggiungendo il proprio indirizzo IP pubblico e solo in seguito aggiungere altri intervalli IP. In caso contrario, potrebbe verificarsi un errore.
>- L’accesso basato su IP non si applica agli indirizzi IP privati.

Puoi aggiungere fino a 150 intervalli IP pubblici diversi solo in formato CIDR.

Per abilitare l’accesso basato su IP nel Adobe Admin Console, segui la procedura riportata di seguito:

1. Passare alla sezione **[Impostazioni Adobe Admin Console](https://adminconsole.adobe.com/settings/identity)**.
2. Seleziona ed espandi **[!UICONTROL Privacy e sicurezza]** nel menu di selezione, quindi seleziona **[!UICONTROL Impostazioni autenticazione]**.
3. Nella sezione **[!UICONTROL Accesso basato su IP]** selezionare il pulsante **[!UICONTROL Aggiungi indirizzo IP]**.
4. Nella finestra **[!UICONTROL Aggiungi indirizzo IP]**:
   - Immetti gli indirizzi IP pubblici o il blocco CIDR da aggiungere al inserisco nell&#39;elenco Consentiti di.
   - Usa una virgola per separare più indirizzi IP.
   - Seleziona **[!UICONTROL Salva]**.

   Al momento è supportato solo il formato IPv4. Di seguito sono riportati alcuni esempi:
   - Indirizzo IP v4: 1.3.4.6
   - Indirizzo subnet IP v4: 1.2.0.0/24

Gli indirizzi IP vengono aggiunti in pochi minuti. Gli utenti associati vedranno la restrizione la prossima volta che tenteranno di accedere o cambiare profilo al di fuori degli indirizzi IP pubblici consentiti. È consigliabile informare in anticipo gli utenti di questa modifica.

Puoi modificare o rimuovere qualsiasi indirizzo IP elencato selezionando le opzioni di modifica o eliminazione accanto a ciascuna voce.

>[!NOTE]
>
>- Quando l&#39;accesso basato su IP è abilitato, **non si verifica alcuna disconnessione forzata**. Gli utenti sono interessati solo quando tentano di selezionare il profilo con restrizioni all’accesso o al passaggio da un profilo Web all’altro.
>- Se utilizzi un gateway web protetto, assicurati che tutto il traffico venga indirizzato attraverso di esso. Visualizza l&#39;[elenco di domini da consentire](https://helpx.adobe.com/it/enterprise/kb/network-endpoints.html) per il corretto funzionamento delle app e dei servizi Adobe.
>- Se sei bloccato fuori da Admin Console perché hai inserito un indirizzo IP non valido, contatta l&#39;[Assistenza clienti Adobe](https://helpx.adobe.com/it/enterprise/using/support-for-enterprise.html).

## Partecipa alla conversazione

Per collaborare, porre domande e chattare con altri amministratori, visita la [community Enterprise e Teams](https://www.adobe.com/go/entcom_it).
