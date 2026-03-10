---
title: Esporta o importa la struttura dell'organizzazione e le allocazioni di prodotti
description: Scopri in che modo gli amministratori globali esportano e importano i dati relativi alla gerarchia organizzativa e all’allocazione dei prodotti in Global Admin Console utilizzando JSON, CSV o XLSX. Applicabile a Enterprise.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 3220086a-4603-465f-a3e3-194193ca10ba
source-git-commit: ee2da1708a19eb7871ffb03f2840c0b7d82bd159
workflow-type: tm+mt
source-wordcount: '4423'
ht-degree: 3%

---

# Esporta o importa la struttura dell&#39;organizzazione e le allocazioni di prodotti

**Si applica a:** Enterprise

Scopri come gli amministratori globali possono semplificare l’organizzazione e la gestione dei prodotti con le funzioni di esportazione e importazione in Global Admin Console.

Accedi alla scheda **[!UICONTROL Organizzazioni]** in [Global Admin Console](https://helpx.adobe.com/it/enterprise/global-admin-console/adopt-global-administration.html) per esportare o importare la struttura dell&#39;organizzazione. Vai alla scheda **[!UICONTROL Allocazione prodotto]** per i dati di allocazione. Utilizza l&#39;icona **[!UICONTROL Altre opzioni]** **⋮** per selezionare esporta o importa. [Accedi a Global Admin Console](https://global-admin-console.adobe.com).

## Esportare la struttura dell’organizzazione

In qualità di [amministratore globale](https://helpx.adobe.com/it/enterprise/global-admin-console/manage-administrators.html), puoi esportare la gerarchia dell&#39;organizzazione. È possibile scaricare una rappresentazione JSON, CSV o XLSX dell’intera gerarchia organizzativa o di un suo sottoinsieme. Puoi quindi utilizzare questi dati per l’analisi o la modifica.

Il formato di esportazione scelto influisce sulla struttura dei dati esportati:

- Formato CSV — consente di esportare un solo tipo di dati alla volta. Durante l’esportazione dei profili di prodotto in formato CSV, i profili e le risorse vengono combinati in un’unica tabella. Sono disponibili più voci per il profilo di prodotto, una per ogni risorsa.
- Formato XLSX - Consente di visualizzare i dettagli di ogni organizzazione in un foglio separato. I record sono collegati tra i diversi tipi di oggetto da un ID di riferimento. In alcuni casi, possono essere presenti più righe per un particolare oggetto (ad esempio, oggetti Resource se a una determinata risorsa è associato un set di valori).
- Formato JSON: il più flessibile. Può sfruttare le relazioni strutturali tra gli oggetti esportati (ad esempio, i prodotti di un’organizzazione appaiono direttamente nell’elemento organizzazione). Gli stessi campi vengono esportati in tutti e tre i formati, ma alcuni valori sono ridondanti nel formato JSON.

### Passaggi da esportare

1. Accedi a [Global Admin Console](https://global-admin-console.adobe.com/). Nella scheda **[!UICONTROL Organizzazioni]**, utilizza il selettore organizzazione per selezionare la gerarchia organizzazione in cui desideri esportare. Vengono esportati i dati per tutte le organizzazioni nella gerarchia.
2. Seleziona l&#39;icona **[!UICONTROL Altre opzioni]** ⋮ e scegli **[!UICONTROL Esporta]**.

   ![Esporta struttura organizzazione](./assets/export-org-structure.png)

3. Nella finestra di dialogo **[!UICONTROL Esporta]**, seleziona gli elementi da esportare e un formato in cui esportare i dati.

   ![Finestra di dialogo di esportazione di Admin Console](./assets/export-12.png)

4. Seleziona **[!UICONTROL Esporta]**. La generazione del file di esportazione può richiedere alcuni minuti. Una volta completato, per scaricare il report, passa a **[!UICONTROL Global Admin Console]** > **[!UICONTROL Insights]** > **[!UICONTROL Esporta report]**.

>[!NOTE]
>
>I file JSON vengono esportati in formato zip. Puoi aprirli utilizzando un’utility zip o le funzioni zip del sistema operativo.

Dopo aver scaricato il file, puoi manipolare i dati e quindi importarli nuovamente. Gli aggiornamenti importati vengono visualizzati in Global Admin Console come se i dati fossero stati modificati manualmente.

## Importare la struttura dell’organizzazione

In qualità di [amministratore globale](https://helpx.adobe.com/it/enterprise/global-admin-console/manage-administrators.html), puoi importare dati potenzialmente modificati. Una volta caricati, i nuovi dati vengono confrontati con i dati correnti e le eventuali modifiche vengono applicate alla gerarchia dell’organizzazione. Tutte le operazioni di importazione vengono eseguite sulla copia aggiornata della gerarchia organizzazione. Se sono presenti modifiche in sospeso, le modifiche di importazione verranno aggiunte alle modifiche in sospeso nella gerarchia.

### Passaggi per importare

1. Accedi a [Global Admin Console](https://global-admin-console.adobe.com). Nella scheda **[!UICONTROL Organizzazioni]**, utilizza il selettore organizzazione per selezionare la gerarchia organizzazione in cui desideri eseguire l&#39;importazione.
2. Seleziona l&#39;icona **[!UICONTROL Altre opzioni]** **⋮** e seleziona **[!UICONTROL Importa]**. A seconda delle dimensioni e della complessità del file di importazione, l’elaborazione può richiedere da alcuni secondi a diversi minuti.
3. Seleziona **[!UICONTROL Seleziona un file]** e scegli un file JSON, CSV o XLSX da caricare. Per il file CSV, è possibile importare un solo dettaglio dell’organizzazione alla volta e non supporta l’importazione di prodotti. Le modifiche importate vengono visualizzate come se i dati fossero stati modificati manualmente.
4. Seleziona **[!UICONTROL Chiudi]**.
5. Selezionare **[!UICONTROL Rivedi modifiche in sospeso]**. Quindi, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/it/enterprise/global-admin-console/execute-jobs.html). Prima di eseguire le modifiche, le azioni in sospeso vengono visualizzate nello stesso modo di quando le modifiche vengono apportate manualmente in Global Admin Console.

## Esportare e importare schemi

Durante l’importazione di dati utilizzando un file CSV, i campi possono essere visualizzati in qualsiasi ordine ma devono sempre corrispondere alla riga di intestazione.

Durante l’importazione dei dati, è necessario specificare un’operazione per ciascun elemento. L&#39;operazione può essere una delle seguenti:

- Aggiorna: indica una modifica.
- Crea: indica la creazione di un nuovo oggetto, ad esempio organizzazione, gruppo di utenti o amministratore.
- Elimina: indica l’eliminazione di un oggetto (ad esempio organizzazione, gruppo di utenti o amministratore).

I record di input senza campo di operazione o con campo vuoto vengono ignorati.

### Organizzazioni

<table>
  <tr>
    <th>Nome campo</th>
    <th>Descrizione</th>
    <th>Note</th>
  </tr>

<tr>
    <td>ID</td>
    <td>
      ID organizzazione.<br><br>
      Quando aggiungi una nuova organizzazione, questa può essere vuota o impostata su un identificatore segnaposto, ad esempio,
      nuova_organizzazione_1. L’identificatore del segnaposto viene utilizzato nei casi in cui altre voci importate debbano fare riferimento a
      a questa organizzazione. Dopo la creazione, verrà assegnato un ID organizzazione effettivo che sostituirà tutto
      utilizzi dell’id organizzazione segnaposto.
    </td>
    <td>Può essere impostato su un valore temporaneo quando operation=create</td>
  </tr>

<tr>
    <td>name</td>
    <td>
      Nome semplice dell’organizzazione. Lunghezza min 4, max 100.
      I nomi possono contenere caratteri UTF-8 fino a 3 byte,
      I caratteri a 4 byte non sono supportati.
    </td>
    <td>
      Può essere impostato o aggiornato rispettivamente quando operation=create o operation=update
    </td>
  </tr>

<tr>
    <td>countryCode</td>
    <td>Codice paese</td>
    <td>
      Deve essere impostato quando operation=create, può essere aggiornato quando operation=update
    </td>
  </tr>

<tr>
    <td>tipo</td>
    <td>Tipo di organizzazione</td>
    <td>Sola lettura</td>
  </tr>

<tr>
    <td>parentOrgId</td>
    <td>
      ID organizzazione principale. Vuoto per l’organizzazione principale.
      Durante l’aggiornamento, si applicano restrizioni significative, tra cui quella per cui il nuovo elemento principale si trova nella stessa gerarchia e
      disporre dei prodotti presenti nell’organizzazione.
    </td>
    <td>
      Può essere impostato o aggiornato rispettivamente quando operation=create o operation=update
    </td>
  </tr>

<tr>
    <td>adminCount</td>
    <td>Numero di amministratori</td>
    <td>Sola lettura</td>
  </tr>

<tr>
    <td>domainCount</td>
    <td>Numero di domini</td>
    <td>Sola lettura</td>
  </tr>

<tr>
    <td>userCount</td>
    <td>Numero di utenti</td>
    <td>Sola lettura</td>
  </tr>

<tr>
    <td>userGroupCount</td>
    <td>Numero di gruppi di utenti</td>
    <td>Sola lettura</td>
  </tr>

<tr>
    <td>amministratori</td>
    <td>Set di oggetti admin che rappresentano gli amministratori di questa organizzazione</td>
    <td rowspan="6">
      Può mancare se non selezionato per l'esportazione. Viene visualizzato in una scheda separata nei file XLSX.
    </td>
  </tr>

<tr>
    <td>domini</td>
    <td>Set di oggetti di dominio che rappresentano i domini di questa organizzazione</td>
  </tr>

<tr>
    <td>products</td>
    <td>Set di oggetti prodotto che rappresentano i prodotti di questa organizzazione</td>
  </tr>

<tr>
    <td>productProfiles</td>
    <td>Set di oggetti profilo di prodotto che rappresentano i profili di prodotto in questa organizzazione</td>
  </tr>

<tr>
    <td>userGroups</td>
    <td>Set di oggetti gruppo utenti che rappresentano gruppi di utenti in questa organizzazione</td>
  </tr>

<tr>
    <td>orgPolicies</td>
    <td>Struttura che rappresenta le politiche e i loro valori</td>
  </tr>

<tr>
    <td>operazione</td>
    <td>
      Può essere vuoto, Crea, Aggiorna o Elimina. Azione da eseguire quando i dati vengono importati.
    </td>
    <td>Sempre vuoto durante l'esportazione.</td>
  </tr>
</table>


**Requisiti di importazione:**

- Per l’aggiornamento o l’eliminazione, l’ID organizzazione deve fare riferimento a un’organizzazione esistente nella gerarchia.
- Se stai creando una nuova organizzazione, puoi lasciare vuoto il campo orgId o impostarlo su un ID univoco che puoi creare (ad esempio nuovo-1 o nuovo-2). Questo fornisce un ID che può essere utilizzato per fare riferimento all’organizzazione da creare.
- Il codice paese deve essere valido.
- L&#39;orgId per l&#39;operazione *Update* e *Delete* deve essere già presente nella gerarchia organizzazione.
- L&#39;orgId contrassegnato come *Delete* non deve essere selezionato come parentOrgId per le organizzazioni con *Update* o *Create* operazione.
- Le organizzazioni figlio allo stesso livello e dello stesso padre non devono avere gli stessi nomi organizzazione.
- Per creare un&#39;organizzazione o aggiornarne il nome, il nome dell&#39;organizzazione non deve corrispondere al nome di un elemento figlio esistente dello stesso elemento padre.

### Amministratori

<table>
  <tr>
    <th>Nome campo</th>
    <th>Descrizione</th>
    <th>Utilizzo di </th>
  </tr>

<tr>
    <td>orgId</td>
    <td>Riferimento all’organizzazione in cui risiede l’amministratore.</td>
    <td>Utilizzato come riferimento per trovare oggetti contenenti o associati.</td>
  </tr>

<tr>
    <td>firstName</td>
    <td>
     Nome utente amministratore.
Quando l’utente accetta l’invito, il nome e il cognome degli utenti di Adobe ID possono essere sostituiti da un valore fornito dall’utente.
    </td>
    <td rowspan="4">
      Può essere impostato o aggiornato rispettivamente quando operation=create o operation=update
    </td>
  </tr>

<tr>
    <td>lastName</td>
    <td>Cognome utente amministratore</td>
  </tr>

<tr>
    <td>e-mail</td>
    <td>Indirizzo e-mail utente amministratore. Questa è una chiave primaria per l’utente e deve essere univoca.</td>
  </tr>

<tr>
    <td>countryCode</td>
    <td>
Codice paese o area geografica in cui opera l’utente. Si applica solo ai tipi Federated ed Enterprise Id.
    </td>
  </tr>

<tr>
    <td>userType</td>
    <td>Uno tra "Adobe ID", "Enterprise ID" o "Federated ID".</td>
    <td>Sola lettura</td>
  </tr>

<tr>
    <td>adminType</td>
    <td>Uno tra "GLOBAL ADMIN", "GLOBAL VIEWER", "SYSTEM ADMIN", "USER GROUP ADMIN", "PRODUCT ADMIN", "PRODUCT PROFILE ADMIN", "DEPLOYMENT ADMIN" e "STORAGE_ADMIN".</td>
    <td rowspan="4">Può essere impostato quando operation=Create</td>
  </tr>

<tr>
    <td>groupId</td>
    <td>ID gruppo del gruppo di cui questo utente è amministratore. Rilevante solo per gli amministratori di gruppi di utenti e profili di prodotto.</td>

</tr>

<tr>
    <td>licenseId</td>
    <td>ID licenza prodotto del prodotto di cui questo utente è amministratore. Rilevante solo per gli amministratori di prodotto.</td>

</tr>

<tr>
    <td>dominio</td>
    <td>Nome di dominio dell’utente se non si utilizza il dominio e-mail</td>

</tr>

<tr>
    <td>userName</td>
    <td>Nome utente dell’utente se non si utilizza l’indirizzo e-mail</td>
    <td></td>
  </tr>

<tr>
    <td>operazione</td>
    <td>Può essere vuoto, Crea, Aggiorna o Elimina. Azione da eseguire quando i dati vengono importati.</td>
    <td></td>
  </tr>
</table>


**Requisiti di importazione:**

- orgId, e-mail, adminType e userType devono contenere valori validi.
- countryCode deve essere valido.
- Se l&#39;utente esiste già e viene aggiornato, userType deve corrispondere all&#39;utente.
- Verifica la presenza di indirizzi e-mail duplicati nell’organizzazione.

### Profili di prodotto

Le esportazioni e le importazioni di profili di prodotto sono costituite da due parti: i dettagli del profilo di prodotto e un set di risorse associate al profilo di prodotto. Queste risorse identificano i servizi che possono essere configurati, in genere solo per abilitarli o disabilitarli.

- Gli oggetti risorsa sono nidificati all’interno del profilo di prodotto in formato JSON.
- Quando utilizzi CSV o XLSX con i profili di prodotto, questi ultimi e le relative risorse vengono combinati in un’unica tabella. Ci saranno più voci per il profilo di prodotto, una per ogni risorsa.
- Il campo &quot;selezionato&quot; nella risorsa controlla se il servizio è abilitato.
- Durante l’importazione dei profili di prodotto, è necessario eseguire un’operazione Crea o Aggiorna sul profilo di prodotto stesso e su tutti gli oggetti risorsa da aggiornare o creare.


<table>
  <tr>
    <th>Nome campo</th>
    <th>Descrizione</th>
    <th>Utilizzo di </th>
  </tr>

<tr>
    <td>productProfileId</td>
    <td>
     <br><br>
      Identificatore del profilo di prodotto
Il valore segnaposto può essere utilizzato durante la creazione in modo che altri oggetti possano fare riferimento al nuovo profilo.
    </td>
    <td>Può essere impostato su un valore temporaneo quando operation=create</td>
  </tr>

<tr>
    <td>productProfileName</td>
    <td>
     Nome del profilo di prodotto. Non può essere un duplicato di altri profili di prodotto o gruppi di utenti nella stessa organizzazione.
    </td>
    <td rowspan="2">
   Può essere impostato o aggiornato rispettivamente quando operation=create o operation=update
    </td>
  </tr>

<tr>
    <td>productProfileDescription</td>
    <td>Descrizione testuale del profilo di prodotto</td>
  </tr>

<tr>
    <td>licenseId</td>
    <td>Riferimento ID licenza al prodotto</td>
    <td rowspan="2"> Utilizzato come riferimento per trovare l'oggetto contenitore o associato
    </td>
  </tr>

<tr>
    <td>orgId</td>
    <td>
Organizzazione contenente il gruppo di utenti
    </td>
  </tr>

<tr>
    <td>Notifiche</td>
    <td>True o false per indicare se la notifica e-mail deve essere inviata agli utenti quando vengono aggiunti o rimossi da questo profilo di prodotto</td>
    <td>Può essere impostato o aggiornato rispettivamente quando operation=create o operation=update</td>
  </tr>

<tr>
    <td>risorse</td>
    <td> Array di risorse associate a questo profilo di prodotto.
Il campo delle risorse è presente solo per il formato JSON. Per i formati CSV e XLSX, le risorse sono rappresentate con i seguenti campi aggiuntivi: resourceName, resourceId, resourceDescription, icon, selected, quota, resourceType. Per informazioni dettagliate su questi campi, vedere [Prodotti e risorse](#products-and-resources).
Se il profilo di prodotto contiene più di una risorsa, saranno presenti più righe, una per ogni risorsa. Gli altri campi avranno gli stessi valori per ogni risorsa. </td>
    <td></td>
  </tr>

<tr>
    <td>operazione</td>
    <td>Può essere vuoto, Crea, Aggiorna o Elimina. Azione da eseguire quando i dati vengono importati.</td>  
    <td></td>
  </tr>
</table>



**Requisiti di importazione:**

- productProfileId, licenseId e orgId devono avere valori validi.
- Durante la creazione di un profilo di prodotto, productProfileName deve essere un nome valido e non deve duplicare un altro nome di profilo di prodotto o di gruppo di utenti nella stessa organizzazione.
- Il campo quota deve contenere un valore valido per il tipo di unità. Questo valore è numerico o &quot;illimitato&quot; se resourceType=QUOTA o vuoto in caso contrario.
- Il campo di notifica deve essere true o false.
- Per le importazioni CSV e XLSX, convalida productProfileId; tutte le voci devono avere gli stessi orgId, licenseId e productProfileName.
- Convalida productProfileName duplicato nel file di input e nell’organizzazione.
- I profili da aggiornare ed eliminare devono essere presenti nell’organizzazione.
- Le risorse da aggiornare ed eliminare (disattivate) devono essere presenti nel profilo.
- Per creare i profili, verifica quanto segue:
   - L’orgId deve essere una nuova organizzazione o un’organizzazione esistente.
   - LicenseId deve essere un nuovo prodotto o un prodotto esistente.
   - Convalida le risorse per il profilo.

### Risorse nei profili di prodotto

<table>
  <tr>
    <th>Nome campo</th>
    <th>Descrizione</th>
    <th>Utilizzo di </th>
  </tr>

<tr>
    <td>resourceName</td>
    <td>Nome della risorsa</td>
    <td>Sola lettura</td>
  </tr>

<tr>
    <td>resourceId</td>
    <td>Identificatore della risorsa</td>
    <td>Sola lettura</td>
  </tr>

<tr>
    <td>resourceDescription</td>
    <td>Descrizione testuale della risorsa</td>
    <td>Sola lettura</td>
  </tr>

<tr>
    <td>icona</td>
    <td>URL per immagine per risorsa</td>
    <td>Sola lettura</td>
  </tr>

<tr>
    <td>selezionato</td>
    <td>
      Per una voce di configurazione, indica se la funzione è abilitata.
      Questo campo è presente solo in JSON.
    </td>
    <td rowspan="2">
      Può essere impostato o aggiornato rispettivamente quando operation=create o operation=update.
    </td>
  </tr>

<tr>
    <td>quota</td>
    <td>
      Quantità di risorsa principale che può essere distribuita agli utenti tramite questo profilo di prodotto.
      Questo campo è presente solo in JSON.
    </td>
  </tr>


<tr>
    <td>resourceType</td>
    <td>
      Se presente, il valore è SERVICE. Indica che questa risorsa rappresenta un servizio che può essere
      abilitato o disabilitato in base al valore del campo selezionato.
      Questo campo è presente solo in JSON.
    </td>
    <td>Sola lettura</td>
  </tr>

<tr>
    <td>operazione</td>
    <td>
      Può essere vuoto, Crea, Aggiorna o Elimina. Azione da eseguire quando i dati vengono importati.
    </td>
    <td></td>
  </tr>
</table>


**Requisiti di importazione:**

- Il campo Operazione sulle risorse viene ignorato quando per il profilo di prodotto a cui appartengono sono impostate operazioni come *Elimina* o *Crea*.
- Nessuna risorsa deve essere contrassegnata per l&#39;eliminazione. Operazione non valida.
- Per creare i profili di prodotto, il numero di risorse deve corrispondere al numero di risorse del profilo di prodotto sorgente.
- Per le risorse con l&#39;operazione *Update*, la risorsa deve essere presente nel profilo di prodotto.

### Gruppi di utenti

<table>
  <tr>
    <th>Nome campo</th>
    <th>Descrizione</th>
    <th>Utilizzo di </th>
  </tr>

<tr>
    <td>userGroupId</td>
    <td>
      Identificatore del gruppo di utenti. Il valore segnaposto può essere utilizzato al momento della creazione in modo che
      altri oggetti possono fare riferimento al nuovo gruppo di utenti.
    </td>
    <td>Può essere impostato su un valore temporaneo quando operation=create</td>
  </tr>

<tr>
    <td>userGroupName</td>
    <td>Nome del gruppo di utenti</td>
    <td rowspan="2">
      Può essere impostato o aggiornato rispettivamente quando operation=create o operation=update.
    </td>
  </tr>

<tr>
    <td>userGroupDescription</td>
    <td>Descrizione del gruppo di utenti</td>
  </tr>

<tr>
    <td>userCount</td>
    <td>Numero di utenti nel gruppo di utenti</td>
    <td>Sola lettura</td>
  </tr>

<tr>
    <td>profili</td>
    <td>
      Array di ID del profilo di prodotto a cui è associato il gruppo di utenti.
      XLSX ha una riga per valore con gli stessi valori per gli altri campi.
    </td>
    <td>
      Può essere impostato o aggiornato rispettivamente quando operation=create o operation=update.
    </td>
  </tr>

<tr>
    <td>orgId</td>
    <td>Organizzazione contenente il gruppo di utenti</td>
    <td>Utilizzato come riferimento per trovare l'oggetto contenitore o associato</td>
  </tr>

<tr>
    <td>operazione</td>
    <td>
      Può essere vuoto, Crea, Aggiorna o Elimina. Azione da eseguire quando i dati vengono importati.
    </td>
    <td></td>
  </tr>
</table>

**Requisiti di importazione:**

- orgId deve fare riferimento a un’organizzazione esistente o in fase di creazione nella stessa importazione.
- userGroupId deve fare riferimento a un gruppo esistente per l&#39;aggiornamento o l&#39;eliminazione e può essere un ID definito per i nuovi gruppi di utenti.
- Per l’aggiornamento o la creazione, userGroupName non deve essere vuoto e non deve duplicare un altro nome di profilo utente o di prodotto nella stessa organizzazione.
- Verificare che userGroupName non sia duplicato nel file di input e nell&#39;organizzazione.
- userGroups da aggiornare ed eliminare deve essere presente nell&#39;organizzazione.
- Il profilo da rimuovere dal gruppo di utenti deve essere presente nel gruppo di utenti. Impossibile eseguire operazioni di aggiornamento sul profilo di un gruppo di utenti.
- Per creare i gruppi di utenti, verifica quanto segue:
   - L’orgId deve essere una nuova organizzazione o un’organizzazione esistente.
   - Il licenseId, se applicabile, deve essere un nuovo prodotto o un prodotto esistente.
   - ProductProfileId deve essere un nuovo profilo di prodotto o un profilo di prodotto esistente.

### Domini

Le informazioni sul dominio forniscono informazioni di sola lettura sui domini disponibili in ogni organizzazione. Dati non modificabili.


| Nome campo | Descrizione | Utilizzo di  |
| ------------- | ----------------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| orgId | Riferimento all&#39;organizzazione in cui è elencato il dominio | Utilizzato come riferimento per trovare oggetti contenenti o associati. |
| domainName | Nome del dominio (ad esempio, adobe.com). | Sola lettura |
| directoryName | Nome della directory in cui è elencato il dominio | Sola lettura |
| directoryType | Uno di Federated ID o Enterprise ID. | Sola lettura |
| domainStatus | Uno tra &quot;ATTIVO&quot;, &quot;RISERVATO&quot;, &quot;NON RIVENDICATO&quot;, &quot;RIVENDICATO&quot;, &quot;CONVALIDATO&quot;, &quot;RITIRATO&quot;, &quot;SCADUTO&quot;. | Sola lettura |


### Prodotti e risorse {#products-and-resources}

Nei file XLSX sono disponibili due fogli, uno per i prodotti e uno per le risorse. In JSON, gli oggetti risorsa sono nidificati nell’oggetto prodotto.

**Prodotti**


| Nome campo | Descrizione | Utilizzo di  |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| licenseId | ID che identifica il prodotto. Ogni prodotto ha un ID di licenza univoco nell’organizzazione in cui è elencato. Quando si aggiunge un nuovo prodotto, questo campo può essere vuoto o utilizzare un identificatore segnaposto (ad esempio, new_product_1). Dopo la creazione, viene assegnato un ID licenza effettivo che sostituisce tutti gli utilizzi dell’ID licenza segnaposto. | Può essere impostato su un valore temporaneo quando operation=create |
| productName | Nome del prodotto | Sola lettura |
| productDescription | Descrizione testuale del prodotto | Sola lettura |
| allowOverallocation | Valore booleano che indica se è consentita la sovrassegnazione di questa istanza di prodotto. La sovrassegnazione si riferisce alla possibilità di concedere a un&#39;organizzazione figlio una quantità maggiore di quella che ti è stata concessa. | Può essere impostato o aggiornato rispettivamente quando operation=create o operation=update |
| icona | URL dell’icona del prodotto | Sola lettura |
| sourceLicenseId | ID licenza dell’istanza del prodotto nell’organizzazione da cui è stato allocato il prodotto. Il valore è nullo se questa istanza non è un prodotto allocato, ma è un prodotto acquistato. | Può essere impostato quando operation=Create |
| productId | Identificatore del prodotto. | Sola lettura |
| orgId | Identificatore dell’organizzazione contenente questa istanza di prodotto | Utilizzato come riferimento per trovare l&#39;oggetto contenitore o associato |
| ridistribuibile | Valore booleano che indica se il prodotto dispone di risorse che possono essere concesse alle organizzazioni figlie. | Sola lettura |
| risorse | Oggetto contenente un set di oggetti risorsa che rappresenta le risorse e le impostazioni del prodotto |                                                                               |
| operazione | Può essere vuoto, Crea, Aggiorna o Elimina. Azione da eseguire quando i dati vengono importati. |                                                                               |


**Requisiti di importazione:**

- Per creare, licenseId deve essere un ID univoco creato dall&#39;utente.
- Per l&#39;aggiornamento, licenseId deve essere l&#39;ID di un prodotto esistente nell&#39;organizzazione specificata.
- orgId deve fare riferimento a un&#39;organizzazione esistente o che viene creata nella stessa operazione di importazione.
- Per creare, sourceLicenseId deve fare riferimento a un prodotto esistente o all&#39;ID definito per un prodotto creato nella stessa operazione di importazione.
- licenseId e sourceLicenseId non devono essere uguali per i prodotti con l&#39;operazione *Create*.
- Convalidare organizzazioni di prodotti; l’organizzazione deve essere nuova o già presente nella gerarchia dell’organizzazione.
- Per l&#39;operazione *Aggiorna* e *Elimina*, il prodotto deve essere già presente nella gerarchia dell&#39;organizzazione.
- licenseId contrassegnato come *Delete* non deve essere utilizzato come sourceLicenseId di prodotti con *Create* e *Update* operazione.
- Per i prodotti con l&#39;operazione *Create*, verificare che sourceLicenseId sia presente nell&#39;organizzazione padre.

**Risorse per i prodotti**

Gli oggetti risorsa possono essere visualizzati nei prodotti e nei profili di prodotto.


| Nome campo | Descrizione | Utilizzo di  |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| resourceName | Nome della risorsa | Sola lettura |
| resourceId | Identificatore della risorsa | Sola lettura |
| resourceDescription | Descrizione testuale della risorsa | Sola lettura |
| icona | URL per immagine per risorsa | Sola lettura |
| productName | Nome del prodotto di cui fa parte questa risorsa. | Sola lettura |
| licenseId | ID licenza (istanza prodotto) del prodotto di cui fa parte questa risorsa. | Utilizzato come riferimento per trovare l&#39;oggetto contenitore o associato |
| grantQuantity | Quantità assegnata della risorsa: quantità di risorse disponibili per l&#39;organizzazione da utilizzare localmente o allocare alle organizzazioni figlio. | Può essere impostato o aggiornato rispettivamente quando operation=create o operation=update |
| unità | Nome dell&#39;unità di quantità della sovvenzione. | Sola lettura |
| currentQuantity | Quantità utilizzabile corrente in questa organizzazione. Si tratta della quantità concessa meno le risorse allocate alle organizzazioni figlio. Questo è il valore visualizzato nell’Admin Console per questo prodotto/risorsa. | Sola lettura |
| ProvisionedQuantity | Quantità effettivamente fornita: può essere minore di sovvenzione o corrente, può essere minore di currentQuantity se è presente un limite. | Sola lettura |
| operazione | Può essere vuoto, Crea, Aggiorna o Elimina. Azione da eseguire quando i dati vengono importati. |                                                                               |


**Requisiti di importazione:**

Il campo Operazione sulle risorse viene ignorato quando per il prodotto a cui appartengono sono impostate operazioni come *Elimina* o *Crea*.
- Nessuna risorsa deve essere contrassegnata per l&#39;eliminazione. Operazione non valida.
- Per i prodotti da creare, il numero di risorse deve corrispondere al numero di risorse del prodotto di origine.
- Per le risorse con l&#39;operazione *Update*, la risorsa deve essere presente nel prodotto.

## Importare ed esportare dati di allocazione prodotti

In qualità di [Amministratore globale](https://helpx.adobe.com/it/enterprise/global-admin-console/manage-administrators.html), puoi esportare i dati di allocazione prodotto come file JSON o CSV. Puoi quindi manipolare questi dati e caricarli nuovamente per importare le modifiche. Quando vengono caricati i dati potenzialmente modificati, i nuovi dati vengono confrontati con i dati correnti e le eventuali modifiche vengono applicate ai dati di allocazione del prodotto. È quindi possibile rivedere e sottomettere le modifiche in sospeso affinché diventino effettive.

## Esporta il modello di allocazione prodotto

Per esportare il modello di allocazione prodotto, effettuare le seguenti operazioni:

1. Accedi a [Global Admin Console](https://global-admin-console.adobe.com/) e passa alla scheda **[!UICONTROL Allocazione prodotti]**.
2. Seleziona l&#39;icona di ⋮ **[!UICONTROL Altre opzioni]**, quindi seleziona **[!UICONTROL Esporta CSV]** o **[!UICONTROL Esporta JSON]**. Il file è stato scaricato. [Ulteriori informazioni](#export-and-import-formats-for-product-allocation) sui formati di esportazione.

## Importa il modello di allocazione prodotto

È possibile esportare i dati, modificarli e quindi importare il file modificato. Per importare il modello di allocazione prodotto, effettuare le seguenti operazioni:

1. Accedi a [Global Admin Console](https://global-admin-console.adobe.com/) e passa alla scheda **[!UICONTROL Allocazione prodotti]**.
2. Seleziona l&#39;icona **[!UICONTROL Altre opzioni]** ⋮ e seleziona **[!UICONTROL Importa]**.
3. Seleziona un file JSON o CSV da caricare.
4. Selezionare **[!UICONTROL Rivedi modifiche in sospeso]**. Dopo aver esaminato le modifiche, seleziona **[!UICONTROL Invia modifiche]** per [eseguirle](https://helpx.adobe.com/it/enterprise/global-admin-console/execute-jobs.html).

## Esportazione e importazione di formati per l&#39;allocazione dei prodotti

I formati di esportazione e importazione sono gli stessi. Durante l’importazione in formato CSV, i campi possono essere visualizzati in qualsiasi ordine, ma devono corrispondere alla riga di intestazione. Durante l’importazione in formato JSON, i campi possono essere visualizzati in qualsiasi ordine.

È necessario specificare l&#39;operazione durante l&#39;importazione dei dati di allocazione prodotto. L&#39;operazione può essere una delle seguenti:

- Aggiorna: indica una modifica (modifica ai valori grantQuantity, allowOverAllocation).
- Crea: indica di aggiungere una risorsa prodotto all’organizzazione specificata.
- Elimina: indica l’eliminazione del prodotto.

Se non viene specificata alcuna operazione, non si verificano modifiche quando i dati vengono importati per quella riga in CSV o nell’oggetto in JSON.

Nel file esportato esiste una riga o un record per ogni risorsa prodotto. Alcuni prodotti hanno più di una risorsa.

Se un prodotto dispone di più risorse, le operazioni di aggiornamento possono essere applicate a risorse indipendenti, un&#39;operazione di eliminazione elimina il prodotto, incluse tutte le risorse, da un&#39;organizzazione e un&#39;operazione di creazione richiede un record per ciascuna delle risorse nel file di importazione in modo da poter specificare la quantità corretta di ciascuna risorsa. Il campo allowOverAllocation si applica a tutto il prodotto e non importa in quale risorsa si trovi un aggiornamento per questo campo.

### Descrizione delle intestazioni


| Nome campo | Descrizione | Utilizzo di  |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| productName | Nome del prodotto. | Sola lettura |
| licenseId | ID di un prodotto (univoco per un prodotto in un’organizzazione). Quando si aggiunge un nuovo prodotto, questo campo può essere vuoto o impostato su un identificatore segnaposto (ad esempio, new_product_1). L’identificatore del segnaposto viene utilizzato nei casi in cui altre voci importate debbano fare riferimento a questo prodotto. Dopo la creazione, verrà assegnato un ID licenza effettivo e sostituirà tutti gli utilizzi dell’ID licenza segnaposto. | Può essere impostato quando operation=Create |
| sourceLicenseId | ID del prodotto principale. È vuoto o nullo se rappresenta un acquisto invece di un’allocazione. | Può essere impostato quando operation=Create |
| productId | ID che identifica questa classe di prodotto. Questo ID è condiviso tra prodotti dello stesso tipo e differisce dal licenseId che identifica un’istanza del prodotto. | Sola lettura |
| resourceName | Nome della risorsa prodotto. Ad esempio, Licenze utente. | Sola lettura |
| resourceId | ID che identifica questa risorsa prodotto. | Può essere impostato quando operation=Create |
| orgPathName | Nome percorso dell&#39;organizzazione in cui si trova la risorsa prodotto. Segmenti separati da &quot;/&quot;. | Sola lettura |
| orgName | Nome semplice dell’organizzazione contenente questa risorsa prodotto. Segmento finale di orgPathName. | Sola lettura |
| orgId | ID organizzazione dell’organizzazione contenente questa risorsa prodotto. | Può essere impostato quando operation=Create |
| grantQuantity | Numero di unità di quantità di risorsa concesse a questa organizzazione dal relativo padre o l&#39;importo acquistato se questa voce di risorsa prodotto rappresenta un acquisto. Questo campo è aggiornabile, ad eccezione dei prodotti acquistati o delle allocazioni principali per i quali l’amministratore globale non dispone delle autorizzazioni necessarie per apportare modifiche. | Può essere aggiornato quando operation=Update o operation=Create |
| unità | Nome dell&#39;unità di risorsa. Ad esempio, Utenti. | Sola lettura |
| totalAllocations | Somma delle sovvenzioni alle organizzazioni figlio di questa organizzazione per questa risorsa prodotto. Questo valore comprende le sovvenzioni dirette ai figli più le sovrassegnazioni da parte di tali organizzazioni. Ad esempio, se questa organizzazione ha concesso a un figlio 10 e il figlio ha quindi allocato il figlio 25, il valore di totalAllocations sarà 25: il valore di 10 concesso al figlio più un&#39;eccedenza di 15 in tale figlio. | Sola lettura |
| grantOverage | Importo per il quale totalAllocations supera la quantità concessa. Se totalAllocations non supera grantQuantity, questo valore è null o zero. | Sola lettura |
| localLicensedQuantity | Quantità di questa risorsa concessa a questa organizzazione rimanente per l&#39;utilizzo dopo la detrazione della quantità allocata ai figli. Questo è l’importo mostrato come disponibile in Admin Console. Questo valore può essere zero ma non è mai negativo anche se l&#39;organizzazione ha sovrassegnato le risorse ai relativi figli. | Sola lettura |
| localUsage | Numero di unità della risorsa utilizzate in questa organizzazione. Ad esempio, la delega di una licenza utente a un utente conta come 1 unità di utilizzo. | Sola lettura |
| totalUsage | Numero di unità della risorsa utilizzate da questa organizzazione e da tutti gli elementi figlio. Mostra l’utilizzo di questa risorsa nella parte della gerarchia organizzativa con radice in questa organizzazione. | Sola lettura |
| useOverage | Quantità di utilizzo totale rispetto alla concessione dell&#39;organizzazione (organizzazione e figli hanno utilizzato più risorse di quelle disponibili). Questo mostra un valore diverso da zero quando totalUsage supera localLicensedQuantity. | Sola lettura |
| allowOverAllocation | Indica se all&#39;utente è consentito concedere più risorse ai figli anche se non è più consentito concedere (consentito concedere nonostante il superamento del limite di sovvenzione). Questo valore si applica a tutte le risorse di questo prodotto. Se si tenta di aggiornare allowOverallocation per più risorse dello stesso prodotto a valori diversi, il risultato è casuale. | Può essere aggiornato quando operation=Update |
| isPurchasedProduct | true se il prodotto è un prodotto di acquisto (non allocato dall&#39;elemento padre). Equivale a sourceLicenseId con un valore vuoto. | Sola lettura |
| ridistribuibile | true se il prodotto può essere allocato a figli, false significa che il prodotto è disponibile solo nell&#39;organizzazione in cui viene visualizzato e che le risorse non possono essere allocate a un&#39;altra organizzazione. | Sola lettura |
| operazione | Può essere vuoto, Crea, Aggiorna o Elimina. Azione da eseguire quando i dati vengono importati. |                                                          |


**Requisiti per l&#39;importazione**

**Convalida dei dati**

- Il campo dell&#39;operazione deve contenere un&#39;operazione valida.
- I dati di importazione del prodotto devono avere proprietà e valori per i campi obbligatori.
- Le proprietà dei dati di importazione del prodotto devono essere del tipo corretto.
- Il campo criterio prodotto (overAllocation) non deve essere fornito per risorse diverse.
- Il campo grantQuantity:
   - Non può essere cambiato in *unlimited* se non è già *unlimited*.
   - Deve essere un numero intero non negativo o il valore stringa *unlimited.*

**Autorizzazione/convalida accessibile**

- L&#39;organizzazione associata ai dati di importazione deve esistere. Se stai eseguendo l’aggiornamento, accertati che il prodotto e la risorsa associati ai dati di importazione esistano effettivamente.

**Aggiungi convalida prodotto**

- SourceLicenseId deve esistere.
- L’organizzazione associata al nuovo prodotto deve esistere.
- Il prodotto da creare non deve esistere (prodotto con lo stesso licenseId).
- Le risorse associate a un prodotto in fase di creazione devono avere un productId corrispondente a tale prodotto.
