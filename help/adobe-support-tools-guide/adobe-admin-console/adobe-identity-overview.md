---
title: Panoramica sull’identità
description: Comprendi e scegli i tipi di identità (Federated ID, Enterprise ID, Adobe ID e Personal Adobe ID) per la tua organizzazione e gestisci l’accesso degli utenti in Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: c066e95c05f8e8a0953daecda9a220268d325f98
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 4%

---


# Panoramica sull’identità

Applicabile alle aziende e ai team.

Il sistema di gestione delle identità di Adobe consente agli amministratori di creare e gestire l’accesso degli utenti alle applicazioni e ai servizi. Adobe offre questi tipi di identità o account per l’autenticazione e l’autorizzazione degli utenti.

## Tipi di identità su Adobe Admin Console

I tipi di identità consentono all’organizzazione di diversi livelli di controllo sugli account e sui dati degli utenti. La scelta del modello di identità ha un impatto considerevole sul modo in cui l’organizzazione archivia e condivide le risorse. Mentre i modelli Federated ID e Enterprise ID vengono creati e gestiti dall’organizzazione, gli Adobe ID vengono creati e gestiti dall’utente.

La tabella seguente ti guida nella scelta del modello di identità più adatto alla tua organizzazione.

>[!NOTE]
>Se la tua organizzazione non è stata aggiornata al modello di storage aziendale di Adobe e stai ancora utilizzando gli Adobe ID per singoli utenti, consulta la descrizione nella [tabella dei tipi di identità](https://helpx.adobe.com/it/enterprise/using/identity.html#using-personal-adobe-id) di seguito.

<table>
<thead>
<tr>
<th scope="col">Tipi di identità</th>

<th scope="col" style="text-align: center;">
  <img src="./assets/federated-id.png" alt="Icona Federated ID"><br>
  Federated ID
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/enterprise-id.png" alt="Enterprise ID"><br>
  Enterprise ID
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/adobe-id.png" alt="Adobe ID"><br>
  Adobe ID
</th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>Offerte principali</strong></th>
<td>Creato, di proprietà e gestito dall’organizzazione. L’organizzazione gestisce le credenziali utente e utilizza il Single Sign-On (SSO) tramite un provider di identità SAML2 (IdP).</td>
<td>Creato, di proprietà e gestito dall’organizzazione. L’organizzazione mantiene diritti esclusivi per la creazione di account utente su domini verificati.</td>
<td>Creato, di proprietà e gestito dall’utente finale. Adobe esegue l’autenticazione e l’utente finale gestisce l’identità. A seconda del <a href="https://helpx.adobe.com/it/enterprise/using/storage-for-business.html">modello di archiviazione</a>, gli utenti o le aziende mantengono il controllo su file e dati. Gli account Adobe ID vengono creati in domini non verificati, pubblici o attendibili. Fare riferimento al punto 2 della sezione delle note di seguito.</td>
</tr>
<tr>
<th scope="row"><strong>Account e proprietà dei dati</strong></th>
<td colspan="2">Organizzazione posseduta e controllata</td>
<td>Di proprietà dell'organizzazione per lo storage aziendale e di proprietà dell'utente per lo storage utente</td>
</tr>
<tr>
<th scope="row"><strong>Sicurezza e monitoraggio</strong></th>
<td colspan="2">
  <ul>
    <li>Registri di controllo</li>
    <li>Registri di contenuto</li>
    <li>Restrizioni alla condivisione</li>
    <li>Impostazioni di autenticazione dell’organizzazione</li>
  </ul>
</td>

<td>
  <ul>
    <li>Registri di contenuto</li>
    <li>Restrizioni alla condivisione</li>
    <li>Criterio password</li>
  </ul>
</td>

</tr>
<tr>
<th scope="row"><strong>Reimposta password</strong></th>
<td colspan="2">Non supportato</td>
<td><a href="https://helpx.adobe.com/it/manage-account/using/change-or-reset-password.html">Reimposta la password dell'account</a></td>
</tr>
<tr>
<th scope="row"><strong>Creative Cloud for enterprise e Document Cloud for enterprise</strong></th>
<td colspan="3">Supportato</td>
</tr>
<tr>
<th scope="row"><strong>Creative Cloud for teams e Document Cloud for teams</strong></th>
<td colspan="2">Non supportato</td>
<td>Supportato</td>
</tr>
<tr>
<th scope="row"><strong>Experience Cloud</strong></th>
<td colspan="3">Supportato</td>
</tr>
<tr>
<th scope="row"><strong>Consigliato per</strong></th>
<td>
  <ul>
    <li>Organizzazioni che già utilizzano SSO o SAML</li>
    <li>Servizi di directory esistenti (ad esempio, Google e Azure AD)</li>
    <li>Richiedi una facile integrazione con i servizi non Adobe</li>
    <li>Può dimostrare la proprietà del dominio</li>
  </ul>
</td>
<td>
  <ul>
    <li>Può dimostrare la proprietà del dominio</li>
    <li>Non richiedere SSO</li>
  </ul>
</td>
<td>
  <ul>
    <li>Creative Cloud for teams</li>
    <li>L’organizzazione preferisce utilizzare i domini di cui non è proprietaria</li>
    <li>Domini pubblici (ad esempio Hotmail, Gmail)</li>
    <li>Accedi ad app come Adobe Experience Manager Mobili</li>
  </ul>
</td>
</tr>
<tr>
<th scope="row"><strong>Introduzione</strong></th>
<td><a href="https://helpx.adobe.com/it/enterprise/using/set-up-identity.html">Configurare l’identità</a></td>
<td><a href="https://helpx.adobe.com/it/enterprise/using/add-domains-directories.html#claim-domains">Domini richiesta di risarcimento</a></td>
<td><a href="https://helpx.adobe.com/enterprise/using/users.html#add-users">Aggiungi utente</a></td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>1. I criteri per le password di Creative Cloud for teams sono gli stessi di quelli di Creative Cloud for individual.
>1. Gli utenti di Adobe ID si autenticano con le proprie credenziali Adobe ID o tramite il modello di autenticazione della loro organizzazione proprietaria (SSO, 2FA, ecc.). In tali scenari, gli utenti vengono reindirizzati alla pagina SSO dell’organizzazione proprietaria. Dopo l&#39;autenticazione, gli utenti potrebbero dover [scegliere un profilo di business](https://helpx.adobe.com/it/enterprise/kb/enterprise-id-faq.html#choose-profile).

## Utilizzo degli ID personali di Adobe

Adobe sta aggiornando tutti i team e i clienti aziendali per utilizzare il modello di storage aziendale di Adobe. Se nella tua organizzazione sono presenti utenti che utilizzano gli ID personali di Adobe per accedere alle app e ai servizi Adobe dell’azienda o dell’istituto di istruzione, consulta la tabella seguente.

### Adobe ID personale

<table>
<thead>
<tr>
<th scope="col">Tipo di identità</th>
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/personal-adobe-id.png" alt="Adobe ID"><br>
  Adobe ID personale
</th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>Offerte principali</strong></th>
<td>Creato, di proprietà e gestito dall’utente finale. Adobe esegue l’autenticazione e l’utente finale gestisce l’identità.</td>
</tr>
<tr>
<th scope="row"><strong>Account e proprietà dei dati</strong></th>
<td>Controllato dall'utente</td>
</tr>
<tr>
<th scope="row"><strong>Sicurezza e monitoraggio</strong></th>
<td>Criterio password. Fare riferimento al punto 1 nella sezione seguente delle note.</td>
</tr>
<tr>
<th scope="row"><strong>Reimposta password</strong></th>
<td><a href="https://helpx.adobe.com/it/manage-account/using/change-or-reset-password.html">Reimpostare la password dell'account.</a> Fare riferimento al punto 2 nella sezione nota seguente.</td>
</tr>
<tr>
<th scope="row"><strong>Creative Cloud for enterprise e Document Cloud for enterprise</strong></th>
<td>Supportato</td>
</tr>
<tr>
<th scope="row"><strong>Experience Cloud</strong></th>
<td>Supportato</td>
</tr>
<tr>
<th scope="row"><strong>Disponibile solo per / Consigliato per</strong></th>
<td>
  <ul>
    <li>Clienti Enterprise e Team integrati prima della migrazione</li>
    <li>Creative Cloud for teams</li>
    <li>Desideri il controllo nella mano dell’utente</li>
    <li>Accedi ad app come Digital Publishing Suite</li>
    <li>Gli utenti possiedono le risorse dopo la separazione dall’organizzazione</li>
  </ul>
</td>
</tr>
<tr>
<th scope="row"><strong>Introduzione</strong></th>
<td><a href="https://helpx.adobe.com/enterprise/using/users.html#add-users">Aggiungi utente</a></td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>1. I criteri per le password di Creative Cloud for teams sono gli stessi di quelli di Creative Cloud for individual.
>1. Per i clienti Creative Cloud for enterprise che utilizzano [lo storage aziendale](https://helpx.adobe.com/it/enterprise/using/manage-adobe-storage.html), gli amministratori possono aggiungere utenti Adobe ID a Admin Console ma non possono aggiungerli ai profili di prodotto. Gli amministratori devono eseguire la migrazione degli utenti di Adobe ID a un altro tipo di identità.
>1. Alcuni prodotti e servizi, ad esempio il **sito Web Adobe Licensing, supportano solo** Adobe ID.

## Altri argomenti correlati

- [Imposta identità](https://helpx.adobe.com/it/enterprise/using/set-up-identity.html)
- [Cambia identità utente](https://helpx.adobe.com/it/enterprise/using/switch-user-identity.html)
- [Panoramica di Admin Console](https://helpx.adobe.com/enterprise/using/admin-console-overview.html)
- [Domande frequenti sull&#39;istruzione](https://helpx.adobe.com/enterprise/using/education-faq.html)
- [Aggiungi e gestisci utenti](https://helpx.adobe.com/it/enterprise/using/users.html)