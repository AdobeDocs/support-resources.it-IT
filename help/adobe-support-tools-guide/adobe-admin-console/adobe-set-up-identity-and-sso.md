---
title: Configurare identità e Single Sign-On
description: Scopri come gli amministratori di sistema dell’organizzazione possono impostare l’identità utente e il Single Sign-On (SSO) in Adobe Admin Console utilizzando Adobe ID, Enterprise ID o Federated ID.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 0c2992946f1cdbbcfb44a2baf37888bd05b2253b
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 1%

---

# Configurare identità e Single Sign-On

**Si applica a:** Enterprise

Scopri come impostare l’identità in Adobe Admin Console. Confronta Adobe ID, Enterprise ID e Federated ID e configura il Single Sign-On (SSO) per un accesso sicuro alle app Adobe.

Configura l&#39;identità e imposta il Single Sign-On (SSO) in modo che i dipendenti possano [accedere](https://adminconsole.adobe.com/settings/) con le credenziali organizzative esistenti.

Questo video tutorial spiega come [configurare identità e SSO (YouTube)](https://youtu.be/V57lU4zaSBs).

## Termini e concetti chiave

### Directory

Una directory in Admin Console è un’entità che contiene risorse come utenti e criteri come l’autenticazione. Queste directory sono simili alle directory LDAP o attive.

### Provider di identità (IdP)

Un provider di identità (IdP) è il provider di identità della tua organizzazione, ad esempio:

- Active Directory
- Microsoft Azure
- Ping
- Okta
- InCommon
- Shibboleth

### Persone coinvolte

| Ruolo | Responsabilità |
|------|----------------|
| Amministratore di sistema | Collabora con i gestori delle directory IdP e DNS per configurare l’identità in Admin Console. |
| Gestore DNS | Aggiorna i token DNS per convalidare la proprietà del dominio. |
| Gestore directory provider identità (IdP) | Gestisce il portale IdP e i connettori associati. |

### Adobe ID

Creato, di proprietà e gestito dall’utente finale. Adobe esegue l’autenticazione e l’utente finale gestisce l’identità. A seconda del [modello di archiviazione](https://helpx.adobe.com/enterprise/using/storage-for-business.html), gli utenti o le aziende mantengono il controllo su file e dati.

Per le organizzazioni che sono state aggiornate al modello di storage Enterprise, le risorse e i dati sono controllati dall&#39;organizzazione. Per le organizzazioni che non sono state aggiornate, il singolo utente possiede e controlla le risorse di Adobe ID.

### Enterprise ID

Creato, di proprietà e gestito da un’organizzazione. Adobe ospita l’Enterprise ID ed esegue l’autenticazione, ma l’organizzazione gestisce l’Enterprise ID. Gli amministratori creano un’Enterprise ID e la rilasciano a un utente. Gli amministratori possono revocare l’accesso a prodotti e servizi assumendo l’account o eliminando l’Enterprise ID per bloccare definitivamente l’accesso ai dati associati. Per ulteriori informazioni, fai clic [qui](https://helpx.adobe.com/enterprise/using/setup-enterprise-id.html).

### Federated ID

Creato e di proprietà di un’organizzazione e collegato alla directory aziendale tramite federazione. L’organizzazione gestisce le credenziali ed elabora il Single Sign-On tramite un provider di identità SAML2 (IdP).

Di seguito sono riportati alcuni requisiti e scenari in cui sono consigliati Federated ID:

- Se desideri eseguire il provisioning degli utenti in base alla directory aziendale della tua organizzazione.
- Se desideri gestire l’autenticazione degli utenti.
- Se devi mantenere un controllo rigoroso sulle app e sui servizi disponibili per un utente.

## Impostare l&#39;identità senza Single Sign-On

Puoi utilizzare Adobe ID o Enterprise ID se la tua organizzazione non utilizza l’SSO su altre applicazioni.

## Utilizzo di Adobe ID

Adobe sta aggiornando tutte le organizzazioni al [modello di storage aziendale](https://helpx.adobe.com/enterprise/using/storage-for-business.html). In questo modo la tua organizzazione ha un maggiore controllo sulle risorse e sui dati degli utenti.

Introduzione a [aggiungere utenti](https://helpx.adobe.com/it/enterprise/using/users.html) a Admin Console.

## Configurare l’identità con Enterprise ID

Puoi impostare una directory Enterprise ID se desideri un maggiore controllo sui dati degli utenti senza utilizzare l’SSO. Solo gli amministratori creano un’Enterprise ID e la rilasciano a un utente.

Consulta [Configurare l&#39;organizzazione con Enterprise ID](https://helpx.adobe.com/enterprise/using/setup-enterprise-id.html) per i requisiti e i passaggi per la creazione delle directory di Enterprise ID.

## Configurare l’identità con il Single Sign-On

Per utilizzare l&#39;SSO è necessario impostare l&#39;identità utente con gli account Federated ID.

I Federated ID sono consigliati quando:

- Devi mantenere un controllo rigoroso sulle app e sui servizi disponibili per un utente.
- Desideri gestire l’autenticazione degli utenti.
- Desideri eseguire il provisioning degli utenti in base alla directory aziendale della tua organizzazione.

## Configurare una nuova integrazione SSO

Puoi utilizzare i provider di identità più diffusi, come Microsoft Azure AD, Google o altri IdP basati su SAML per impostare l’SSO tra l’organizzazione e i prodotti Adobe.

**Azure AD** (consigliato) - [Configura SSO e sincronizzazione utente con Azure AD Connector](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html)

**Altro ID SAML** - [Configura SSO con altri provider SAML](https://helpx.adobe.com/enterprise/using/create-directory.html)

**Google** (consigliato) - [Configura SSO e sincronizzazione utente tramite Google Connector](https://helpx.adobe.com/enterprise/using/setup-sso-google.html)

## Gestisci configurazione SSO esistente

Dopo aver impostato l’SSO tra l’organizzazione e Adobe, utilizza quanto segue per gestire e modificare la configurazione.

Scopri come gestire i domini e le directory:

- [Gestione utenti](https://helpx.adobe.com/it/enterprise/using/users.html) e [gruppi](https://helpx.adobe.com/enterprise/using/user-groups..html)
- [Collega i domini alle directory](https://helpx.adobe.com/enterprise/using/add-domains-directories.html#link-domains-to-directoies) per controllare l&#39;accesso degli utenti ad app, servizi e impostazioni
- [Gestisci attendibilità directory](https://helpx.adobe.com/enterprise/using/directory-trust.html) per utilizzare i domini richiesti da un&#39;altra organizzazione

Scopri come cambiare il provider di identità:

- [Cambia il tuo IdP](https://helpx.adobe.com/enterprise/using/migrate-authentication-provider.html) senza interrompere il lavoro degli utenti
- [Sposta domini tra directory](https://helpx.adobe.com/enterprise/using/manage-domains-directories.html#move-domains-across-directories)
- [Rimuovi utenti directory legacy](https://helpx.adobe.com/enterprise/using/manage-directory-users.html)
- [Elimina domini e directory vuote obsoleti/non rivendicati](https://helpx.adobe.com/enterprise/using/manage-domains-directories.html#delete)

## Errori e domande comuni

Soluzioni per le domande e gli errori più comuni durante la configurazione e la gestione dell&#39;SSO:

### Azure AD - Domande frequenti e risoluzione dei problemi

#### Domande frequenti

- [Domande frequenti sul connettore Azure AD](https://helpx.adobe.com/enterprise/using/azure-ad-connector-faq.html)
- [Eliminare directory e domini](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html#Deletedirectoriesandremovedomains)

#### Risoluzione dei problemi

- [Accesso negato agli utenti](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html#sync-issues)
- [Problemi di sincronizzazione](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html#sync-issues)

### Altro ID SAML - Domande frequenti e risoluzione dei problemi

#### Domande frequenti

[Domande frequenti sull&#39;integrazione SAML](https://helpx.adobe.com/enterprise/using/sso-faq.html)

#### Risoluzione dei problemi

- [Risoluzione dei problemi generali SSO](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html)
- [ Errore &quot;Accesso negato&quot;](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html#Error_Access_Denied_logging_in)
- [&quot;Errore di un altro utente attualmente connesso&quot;](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html#ErrorAnotheruseriscurrentlyloggedin)
- [Esegui una traccia SAML](https://helpx.adobe.com/enterprise/kb/perform-a-saml-trace.html)

### Google - Domande frequenti

- [Domande frequenti sul connettore Google](https://helpx.adobe.com/enterprise/using/google-federation-faq.html)
- [Eliminare directory e domini](https://helpx.adobe.com/enterprise/using/setup-sso-google.html#Deletedirectoriesandremovedomains)

## Partecipa alla conversazione

Per collaborare, porre domande e chattare con altri amministratori, utilizzare la [community Enterprise e Teams](https://www.adobe.com/go/entcom).

## Legale e privacy

- [Note legali](https://helpx.adobe.com/legal/legal-notices.html)
- [Informativa sulla privacy online](https://www.adobe.com/it/privacy.html)
