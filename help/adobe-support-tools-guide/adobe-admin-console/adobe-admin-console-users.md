---
title: Utenti Adobe Admin Console
description: 'Pianifica la tua strategia di gestione degli utenti su Adobe Admin Console: aggiungi amministratori e utenti finali, scegli un metodo di gestione degli utenti e assegna le licenze.'
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: d92f4190b68a480409f4126a877de3469ed836f0
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 3%

---

# Utenti Adobe Admin Console

Applicabile alle aziende e ai team.

Affrontare uno di questi problemi? Seleziona un problema per visualizzare la risoluzione.

- [Ruoli di amministratore](https://helpx.adobe.com/it/enterprise/using/admin-roles.html)
- [Problemi di download-installazione](https://helpx.adobe.com/it/download-install.html)
- [Reimposta password utente Enterprise ID](https://helpx.adobe.com/it/enterprise/kb/enterprise-id-faq.html#faq)
- [Risolvi errori Federated ID](https://helpx.adobe.com/it/enterprise/kb/tshoot-fed-id.html)
- [Elimina utente o ripristina utente eliminato](https://helpx.adobe.com/it/enterprise/using/manage-directory-users.html)

**Adobe Admin Console - Utenti** - [Guarda su YouTube](https://youtu.be/w8b36YX2TEM)

## Perché aggiungere utenti a Adobe Admin Console

>[!NOTE]
>
>In qualità di amministratore di Adobe Admin Console, dopo aver scelto il [tipo di identità](https://helpx.adobe.com/it/enterprise/using/identity.html) e [configurare l&#39;identità](https://helpx.adobe.com/it/enterprise/using/set-up-identity.html), la prossima attività consiste nell&#39;aggiungere utenti a Admin Console.

Adobe enterprise e i team definiscono in generale due tipi di utenti:

### Amministratori (amministratori)

Gli amministratori Enterprise o Team eseguono attività amministrative su Admin Console. Aggiungere gli amministratori per definire una gerarchia amministrativa flessibile che consenta una gestione dettagliata dell’accesso ai prodotti Adobe, dell’utilizzo e di altre attività amministrative.

Tutti gli amministratori devono essere aggiunti all’Admin Console. Quando vengono aggiunti, i privilegi di amministratore si basano sui relativi [ruoli amministrativi](https://helpx.adobe.com/it/enterprise/using/admin-roles.html).

### Utenti finali

Gli utenti finali sono gli utenti della tua organizzazione o istituzione che utilizzano i prodotti e i servizi Adobe ottenuti dalla tua organizzazione o istituzione in virtù dell’accordo con Adobe.

## Decidere la strategia di gestione degli utenti

A seconda delle tue esigenze, puoi aggiungere, rimuovere o aggiornare gli utenti *singolarmente* o utilizzare uno dei *metodi di caricamento in blocco* disponibili. Utilizza la seguente matrice come guida per pianificare la gestione degli utenti.

>[!NOTE]
>
>Se sei un nuovo cliente Adobe Enterprise o Team, ti consigliamo di esaminare attentamente questa tabella prima di iniziare a gestire gli utenti su Admin Console. I clienti esistenti possono utilizzarlo, soprattutto se stanno pianificando la migrazione da un tipo di identità a un altro (vedi [Modifica tipo di identità](https://helpx.adobe.com/it/enterprise/using/switch-user-identity.html)).

<table>
<thead>
<tr>
<th scope="col"></th>
<th scope="col"><strong>Singolarmente (Admin Console)</strong></th>
<th scope="col"><strong>Caricamento in blocco CSV (Admin Console)</strong></th>
<th scope="col"><strong>Connettori Azure/Google</strong></th>
<th scope="col"><strong>Strumento User Sync</strong></th>
<th scope="col"><strong>API REST per la gestione utente</strong></th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>Applicabile a</strong></th>
<td colspan="2">Team Adobe e clienti aziendali</td>
<td colspan="3">Clienti aziendali Adobe</td>
</tr>
<tr>
<th scope="row"><strong>Descrizione</strong></th>
<td>Gestisci singolarmente gli utenti in Admin Console.</td>
<td>Gestisci gli utenti con il caricamento di file CSV in Admin Console.</td>
<td>Gestisci utenti (e gruppi) in base al portale Azure AD esistente o alla federazione Google.</td>
<td colspan="2">Gestisci utenti (e gruppi) in base al protocollo LDAP della tua organizzazione.</td>
</tr>
<tr>
<th scope="row"><strong>Aggiunta di utenti</strong></th>
<td>Scheda <strong>Utenti</strong> in <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/it/enterprise/using/manage-users-individually.html#add-users">Ulteriori informazioni</a>.</td>
<td>Utilizza <strong>Aggiungi utenti tramite CSV</strong> in <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/it/enterprise/using/bulk-upload-users.html">Ulteriori informazioni</a>. <em>(Usa modello CSV predefinito)</em></td>
<td>Aggiungi utenti in <a href="https://helpx.adobe.com/it/enterprise/using/sso-setup-azure.html">Azure</a> o <a href="https://helpx.adobe.com/it/enterprise/using/setup-sso-google.html">Google</a>. Oppure tramite <strong>Admin Console</strong>.</td>
<td colspan="2">Gli utenti devono essere aggiunti al LDAP dell’organizzazione.</td>
</tr>
<tr>
<th scope="row"><strong>Rimuovi utenti</strong></th>
<td>Selezionare e rimuovere l'utente in <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/it/enterprise/using/manage-users-individually.html#remove-users">Ulteriori informazioni</a>.</td>
<td>Scegli <strong>Rimuovi utenti per CSV</strong> nella scheda <strong>Utenti</strong> di <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/it/enterprise/using/bulk-upload-users.html#remove-users">Ulteriori informazioni</a>. <em>(Usa modello CSV predefinito)</em></td>
<td>Gli utenti devono essere rimossi da <a href="https://helpx.adobe.com/it/enterprise/using/sso-setup-azure.html">Azure</a> o <a href="https://helpx.adobe.com/it/enterprise/using/setup-sso-google.html">Google</a>.</td>
<td colspan="2">Verificare che le informazioni utente siano sincronizzate. <strong>Attenzione:</strong> gli utenti non inclusi nel protocollo LDAP dell'organizzazione vengono rimossi da Admin Console.</td>
</tr>
<tr>
<th scope="row"><strong>Modifica dettagli utente</strong></th>
<td>Selezionare l'utente e quindi <strong>Modifica dettagli utente</strong> in Admin Console. <a href="https://helpx.adobe.com/it/enterprise/using/manage-users-individually.html#edit-user-details">Ulteriori informazioni</a>.</td>
<td>Scegli <strong>Modifica dettagli utente per CSV</strong> nella scheda <strong>Utenti</strong> di <strong>Admin Console</strong>. <a href="https://helpx.adobe.com/it/enterprise/using/bulk-upload-users.html#edit-user-details">Ulteriori informazioni</a>. <em>(Usa modello CSV predefinito)</em></td>
<td>Tutte le informazioni utente devono essere modificate in <a href="https://helpx.adobe.com/it/enterprise/using/sso-setup-azure.html">Azure</a> o <a href="https://helpx.adobe.com/it/enterprise/using/setup-sso-google.html">Google</a>.</td>
<td colspan="2">Verificare che le informazioni utente siano sincronizzate.</td>
</tr>
<tr>
<th scope="row"><strong>Tipi di identità supportati</strong></th>
<td colspan="2">Tutto</td>
<td>Federated ID</td>
<td colspan="2">FEDERATED ID e ENTERPRISE ID</td>
</tr>
<tr>
<th scope="row"><strong>Max aggiornamenti per operazione</strong></th>
<td>10</td>
<td>25.000 (<em>5.000 per prestazioni ottimali</em>)</td>
<td colspan="3">Senza limiti (mappato al protocollo LDAP della tua organizzazione)</td>
</tr>
<tr>
<th scope="row"><strong>Richiede</strong></th>
<td>Adobe Admin Console</td>
<td>Creazione e aggiornamento dei formati di file .csv, preferibilmente con Microsoft Excel</td>
<td>È necessario configurare Azure AD o la federazione Google</td>

<td>
  <ul>
    <li>Prompt dei comandi di macOS Terminal o Windows</li>
    <li>Informazioni su LDAP</li>
  </ul>
</td>

<td>Conoscenza operativa di un linguaggio di programmazione (come Python) per utilizzare le API REST</td>
</tr>
<tr>
<th scope="row"><strong>Maggiori informazioni</strong></th>
<td><a href="https://helpx.adobe.com/it/enterprise/using/manage-users-individually.html">Gestione di singoli utenti</a></td>

<td>
  <ul>
    <li>
      <a href="https://helpx.adobe.com/it/enterprise/using/bulk-upload-users.html">
        Gestione utenti | Caricamento in blocco CSV
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/it/enterprise/kb/troubleshoot-bulk-user-csv-upload.html">
        Risolvere i problemi relativi al caricamento di file CSV per utenti in blocco
      </a>
    </li>
  </ul>
</td>

<td>
  <ul>
    <li>
      <a href="https://helpx.adobe.com/it/enterprise/using/sso-setup-azure.html">
        Connettore Azure AD
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/it/enterprise/using/setup-sso-google.html">
        Connettore federativo Google
      </a>
    </li>
  </ul>
</td>

<td>
  <ul>
    <li>
      <a href="https://adobe-apiplatform.github.io/user-sync.py/en/">
        Informazioni sulla sincronizzazione degli utenti
      </a>
    </li>
    <li>
      <a href="https://github.com/adobe-apiplatform/user-sync.py">
        Archivio Git
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/it/enterprise/using/user-sync.html">
        Guida dettagliata
      </a>
    </li>
  </ul>
</td>
<td><a href="https://developer.adobe.com/umapi/">Informazioni su UMAPI</a></td>
</tr>
</tbody>
</table>

## Passaggi successivi

### Creare pacchetti

Una volta aggiunti, gli utenti saranno pronti per ricevere le app e i servizi designati.

Assegnare le licenze agli utenti finali in base al metodo utilizzato per la gestione delle licenze:

- **Licenze utente nominative:** Aggiungi questi utenti a **prodotti** ([per i team](https://helpx.adobe.com/it/enterprise/using/assign-licenses-to-teams-users.html)) o **profili di prodotto** ([per le aziende](https://helpx.adobe.com/it/enterprise/using/manage-product-profiles.html)) per assegnare loro i diritti per prodotti e servizi Adobe. Per ulteriori dettagli, vedere come [creare pacchetti di licenze utente denominate](https://helpx.adobe.com/it/enterprise/using/create-nul-packages.html) e [profili di prodotto](https://helpx.adobe.com/it/enterprise/using/manage-product-profiles.html#create-product-profile).
- **Gestione licenze per dispositivi condivisi:** [Gli utenti aggiunti](https://helpx.adobe.com/it/enterprise/using/sdl-deployment-guide.html#add-users-admin-console) possono utilizzare i dispositivi condivisi configurati, accessibili solo da **Utenti organizzazione**. Per ulteriori dettagli, vedere [Creare pacchetti SDL](https://helpx.adobe.com/it/enterprise/using/create-sdl-packages.html).

### Distribuire i pacchetti

Dopo aver creato il pacchetto, distribuirlo ai computer client utilizzando uno dei seguenti metodi:

- Passare al computer client e fare doppio clic sul file del pacchetto (Windows o macOS).
- Utilizzare il prompt dei comandi di Windows o il terminale di macOS.
- Utilizzare strumenti di terze parti:
   - [Microsoft Intune](https://helpx.adobe.com/it/enterprise/kb/deploy-packages-using-ms-intune.html)
   - [Gestione configurazione di Microsoft System Center (SCCM)](https://helpx.adobe.com/it/enterprise/kb/deploy-packages-using-sccm.html)
   - [Desktop remoto Apple](https://helpx.adobe.com/it/enterprise/kb/deploy-packages-using-ard.html)
   - [JAMF Pro](https://helpx.adobe.com/it/enterprise/kb/deploy-packages-using-jamf-pro.html)
   - [Munki](https://helpx.adobe.com/it/enterprise/kb/deploy-packages-using-munki.html)

## Lettura correlata

- [Gestisci utenti | Singolarmente](https://helpx.adobe.com/it/enterprise/using/manage-users-individually.html)
- [Gestione utenti | Caricamento CSV in blocco](https://helpx.adobe.com/it/enterprise/using/bulk-upload-users.html)
- [Gestione utenti directory](https://helpx.adobe.com/it/enterprise/using/manage-directory-users.html)
- [Admin Console](https://helpx.adobe.com/it/enterprise/using/admin-console.html)
- [Assegna utenti ai profili di prodotto (per aziende e istituzioni)](https://helpx.adobe.com/it/enterprise/using/manage-product-profiles.html#assign-users)
- [Assegna licenze agli utenti dei team](https://helpx.adobe.com/it/enterprise/using/assign-licenses-to-teams-users.html)
- [Modello di archiviazione aziendale](https://helpx.adobe.com/it/enterprise/kb/business-storage-model-introduction.html)