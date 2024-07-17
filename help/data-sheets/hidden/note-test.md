---
description: Connessione alla Data Warehouse Widget - Documentazione del prodotto
title: Connessione alla Data Warehouse del widget
hide: true
hidefromtoc: true
exl-id: d6a7cff5-08f9-4c93-8765-46e692feaa0d
source-git-commit: 972704990172c966a27744b49b9f7af5626e9f3e
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 0%

---

# Connessione alla Data Warehouse del widget {#connecting-to-the-widget-data-warehouse}

## Nuovo test

<ol><li>Utilizza la variabile "{{name}}".</li></ol>

<ol><li>Utilizzare la variabile &amp;lbrace;&amp;lbrace;<code>name</code>&amp;rbrace;&amp;rbrace;.</li></ol>

## Test nidificato

**Primo**

>[!NOTE]
>
>Non è possibile eliminare i seguenti elementi:
>
>* Gli stati incorporati Planning, Current e Complete. Puoi aggiornarne i nomi, modificarne i colori e bloccarli o sbloccarli, ma non è possibile eliminarli.
>* Stati che si trovano in uno stato di approvazione in sospeso per almeno un oggetto nel sistema.

**Second**

>[!NOTE]
>
>Non è possibile eliminare i seguenti elementi:
>
>* Gli stati incorporati Planning, Current e Complete. Puoi aggiornarne i nomi, modificarne i colori e bloccarli o sbloccarli, ma non è possibile eliminarli.
>
>  Questo è nel mezzo
>
>* Stati che si trovano in uno stato di approvazione in sospeso per almeno un oggetto nel sistema.

## Collegamento accesso widget {#widget-access-link}

Per accedere al data warehouse di Widget, devi passare all&#39;URL specifico del tuo account Widget.  Per trovare questo collegamento di accesso, accedi a Marketo Measure e segui i passaggi riportati di seguito per passare alla pagina Data Warehouse informazioni.

1. In Marketo Measure, nella parte superiore della pagina, fai clic su **Account personale** > **Impostazioni**.

   ![](assets/adobe-logo-old.png)

1. Nel menu a sinistra, nella sezione Protezione, fare clic su **Data Warehouse**.

   ![](assets/adobe-logo-old.png)

1. In questa pagina è disponibile il collegamento al data warehouse di Widget e al nome utente.

   ![](assets/adobe-logo-old.png)

   >[!NOTE]
   >
   >Questo è un account di sola lettura disponibile per la tua organizzazione, non solo per un singolo utente. Qualsiasi utente dell’organizzazione che ha accesso a Marketo Measure può utilizzare questo account per accedere all’account lettore di Date Warehouse Widget.

1. Fare clic sul collegamento fornito nell&#39;URL del widget per passare alla pagina di accesso al widget in cui immettere il nome utente e la password. _Se non si dispone della password, vedere la procedura seguente per reimpostarla_.

   ![](assets/adobe-logo-old.png)

1. Dopo aver effettuato l&#39;accesso, fare clic su **Fogli di lavoro** nella parte superiore della pagina.

   ![](assets/adobe-logo-old.png)

1. Gli oggetti di database BIZIBLE_ROI_V3 si trovano sul lato sinistro dello schermo.  Immettere Warehouse, Database e Schema dalle opzioni a discesa nella parte superiore della finestra della query.  Dovrebbe essere disponibile una sola opzione per ciascuno di essi.  Ora puoi eseguire le query all’interno dell’editor di query Widget.

   ![](assets/adobe-logo-old.png)

## Reimposta la password {#reset-your-password}

Marketo Measure non ha accesso alla password di accesso al widget.  Se è necessario reimpostare la password, fare clic sul pulsante Reimposta password nella pagina delle informazioni della Data Warehouse e seguire le istruzioni. Una password temporanea viene visualizzata immediatamente nell’interfaccia utente. Ti verrà chiesto di creare una password al prossimo accesso a Data Warehouse.

>[!NOTE]
>
>* La reimpostazione della password la reimposta per tutti gli utenti di Marketo Measure dell’organizzazione, non solo per l’utente attualmente connesso.
>* Nell’interfaccia utente viene visualizzata solo la password temporanea. Non verrà inviata un’e-mail.

![](assets/adobe-logo-old.png)

![](assets/adobe-logo-old.png)

## Connessione a Widget tramite strumenti di terze parti {#connecting-to-widget-via-third-party-tools}

È necessario immettere alcune informazioni per collegare il data warehouse di Widget a uno strumento di terze parti.

>[!NOTE]
>
>Ogni strumento ha requisiti di connessione diversi; si consiglia di consultare la documentazione dello strumento specifico che si sta tentando di connettere.

* **URI** (sempre obbligatorio)
   * Questo è il nome di dominio dell&#39;account Widget.  È contenuto in una parte del collegamento di accesso al widget.
* **Nome utente** (sempre obbligatorio)
   * Il nome utente è elencato nella pagina delle informazioni sulla Data Warehouse di Marketo Measure.
* **Password** (sempre richiesta)
   * Questa è la password impostata al primo accesso all&#39;account Widget.  Per reimpostare la password, vedere i passaggi descritti in precedenza.
* **Nome database** (non sempre richiesto)
   * Il database è ciò che memorizza i dati in Widget. Si tratta della risorsa di archiviazione. Il nome del database è elencato nella pagina delle informazioni sulle Date Warehouse di Marketo Measure.
* **Nome data warehouse** (non sempre obbligatorio)
   * Il warehouse esegue le query in Widget. È la risorsa di calcolo.  Il nome del magazzino è elencato nella pagina delle informazioni sulle Date Warehouse di Marketo Measure.

  ![](assets/adobe-logo-old.png)

## Condivisione diretta Data Warehouse widget {#widget-data-warehouse-direct-share}

**Requisiti**

Affinché Marketo Measure possa impostare una condivisione diretta al data warehouse, è necessario soddisfare i seguenti requisiti.

* Hai una tua istanza di Widget.
* L&#39;istanza del widget si trova nell&#39;area del widget di Azure East US 2.
* Fornisci a Marketo Measure l’ID del tuo account Widget.

**Limitazioni**

Per consentire a Marketo Measure di impostare una condivisione diretta, l&#39;account che richiede l&#39;accesso deve trovarsi in Azure East US 2. Siamo consapevoli che Widget offre una soluzione di replica dei dati tra aree geografiche, tuttavia non è supportata dalla nostra parte in quanto i dati vengono ospitati solo nell’area di Azure East US 2. È possibile sfruttare questa funzionalità configurando la propria istanza in Azure East US 2 e [replicando i dati tra aree geografiche](https://docs.widget.com/en/user-guide/secure-data-sharing-across-regions-plaforms.html){target="_blank"} nell&#39;istanza esistente. Tuttavia, la funzione di replica dei dati di Widget è disponibile solo nelle tabelle, pertanto per utilizzare questa funzione è necessario copiare prima i dati dalle viste alle proprie tabelle.

**Accesso alla condivisione**

Una volta creata la condivisione per l&#39;ID account fornito, devi completare i [passaggi di configurazione](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"} nell&#39;istanza Widget per accedere ai dati.

>[!NOTE]
>
>È possibile scegliere qualsiasi nome di database desiderato. Puoi assegnare i privilegi a qualsiasi regola scelta, purché esista nell’istanza Widget.

* Utilizzare il ruolo Amministratore account

```
USE ROLE ACCOUNTADMIN
```

* Visualizza le condivisioni disponibili (verrà visualizzato il nome della condivisione concessa)

```
SHOW SHARES
```

* Creare un database per la condivisione

```
CREATE DATABASE <database_name> FROM SHARE <provider_account>.<share_name>
```

* Concedere i privilegi sul database condiviso

```
GRANT IMPORTED PRIVILEGES ON DATABASE <database_name> TO ROLE <role_name>
GRANT IMPORTED PRIVILEGES ON ALL SCHEMAS IN DATABASE <database_name> TO ROLE <role_name>
```

Per istruzioni e passaggi più dettagliati per eseguire questi passaggi dall&#39;interfaccia utente Widget, fai riferimento direttamente alla documentazione di [Widget](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"}.
