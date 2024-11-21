---
title: Guida alla sintassi e alla formattazione della documentazione collaborativa di Self Service Excellence
description: Introduzione di base allo stile Markdown
mini-toc-levels: 1
hide: true
hidefromtoc: true
exl-id: 9f15436b-156a-4c07-bfaf-8557cd948197
source-git-commit: 0c01084577891a2869a2f5538381ca952514ff9c
workflow-type: tm+mt
source-wordcount: '4305'
ht-degree: 13%

---

# Guida allo stile della sintassi Markdown

Questa pagina illustra il componente markdown per l’authoring della documentazione tecnica delle esperienze digitali utilizzando il formato markdown (.md). Questa pagina include i dettagli per i dipendenti Adobe.

EDS

Consulta qui: [Adobe.com](https://www.adobe.com){rel=nofollow}

<!--
* You can [view a basic sample file](sample.md) or [view a sample file with advanced syntax examples](sample-full.md)
-->

>[!TIP]
>
>Guarda questo [video su AdobeDocs Markdown](https://video.tv.adobe.com/v/26165).

Per la maggior parte, usiamo la sintassi standard GFM (Git-Flavored Markdown) per la formattazione del testo. Tuttavia, alcune sintassi (come le righe orizzontali) non sono supportate e Markdown è stato esteso in diversi modi per soddisfare le esigenze di documentazione.

## Formattazione testo di base

Un paragrafo non richiede una sintassi speciale in Markdown. Aggiungi una riga vuota tra ciascun paragrafo.

Per formattare il testo come **grassetto**, è necessario racchiuderlo in due asterischi:

```
This text is **bold**.
```

Per formattare il testo in *corsivo*, è necessario racchiuderlo in un singolo asterisco:

```
This text is *italic*.
```

Per formattare il testo in ***grassetto e corsivo***, è necessario racchiuderlo in tre asterischi:

```
This is text is both ***bold and italic***.
```

Per ignorare i caratteri di formattazione di Markdown, utilizza `\` prima del carattere:

`This is not \*italicized\* type.`

Rendering: non è di tipo \*italicized\*.

## Badge

In corso. In attesa di Loc.

<!--

See the [dev version of this article](https://experienceleague-dev.corp.adobe.com/docs/authoring-guide-exl/using/markdown/syntax-style-guide.html#badges) for an example. Or [this one](https://experienceleague-dev.corp.adobe.com/docs/internal-test/test/badge.html).

There are two ways to create badges:

* **Metadata badge** - Specify the badge information in metadata so that the badge appears above the title in the article. This is especially useful for adding a badge to all articles in a guide or repo via the TOC.md or metadata.me files.
* **Inline badge** - Specify the badge information on its own line or in a heading, table, or other page element.

![badge examples](assets/badge-examples.png)

**Badge syntax**

*Metadata*: `badge: "Beta Content" type="Informative" url="https://www.example.com" tooltip="Go to example.com"`

*Inline*: `[!BADGE Beta Content]{type=Informative url="https://www.example.com" tooltip="Go to example.com"}`

**Examples**

```
|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off his horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|
```

**Rendered**

|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off his horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|

**More details**

* Only the badge label is required. The `type`, `url`, and `tooltip` parameters are optional. The `type` parameter determines the color. The `url` parameter lets users click the badge to open an article. The `tooltip` parameter displays the tooltip text on mouseover.
* If you want multiple badges to appear at the top of the page, use different badge names. For example, you can create badge names such as `badgeBeta` or `badgeWeb`. Example:

  ```
  badge1: "Beta"
  badge2: "Campaign Web"
  ```

* For metadata badges, make sure that all values are wrapped in quotes. For inline badges, make sure that `url` and `tooltip` are wrapped in quotes.
* Valid type values include *Informative* (default, blue), *Positive* (green), *Negative* (red), *Neutral* (dark gray), and *Caution* (yellow). 

-->

## Virgolette

Il nostro sistema di authoring utilizza la sintassi dei blockquote (`>` all&#39;inizio delle righe) per identificare le estensioni personalizzate per markdown per suggerimenti, note e video. È possibile creare i blockquote effettivi aggiungendo un carattere `>` davanti a un paragrafo.

>Si tratta di un&#39;offerta blockquote.

```
>This is a blockquote quotation.
```

## Blocco di codice (in linea){#code-block}

**Quando utilizzare**

Utilizzato per eseguire il rendering di un codice in linea in una frase. Ideale per richiamare un nome di cookie, un nome di file, un valore o un comando che non richiede un blocco di codice completo.

Il contenuto all’interno dei blocchi di codice viene rappresentato così come è e non localizzato. L&#39;unica eccezione a questa regola è la sintassi `!UICONTROL` e `!DNL`, che viene eliminata durante la creazione del pacchetto per la pubblicazione.

Utilizzare anche blocchi di codice per URL di esempio che non devono essere convalidati: `https://www.example.com`

**Sintassi**

Un blocco di codice utilizza singoli apici retroversi per racchiudere l’elemento di codice che desideri evidenziare.

```
This is `inline code` within a paragraph of text.
```

**Esempio**

This is `inline code` within a paragraph of text.

>[!TIP]
>
>Puoi anche racchiudere il testo in tre apici posteriori (&grave;&grave;&grave;&grave;) per creare un blocco di codice in linea. Questa funzione è particolarmente utile quando devi fare riferimento a un carattere di apice inverso all’interno di un blocco di codice in linea. Esempio:
>
&grave;&grave;&grave;`Use a back tick (`&grave;`) for formatting`&grave;&grave;&grave;

## Blocco di codice (delimitato)

**Quando utilizzare**

Utilizza un blocco di codice per visualizzare la sintassi del codice. Un blocco di codice delimitato utilizza tre apici retroversi per racchiudere l’elemento di codice che desideri evidenziare. Aggiungi righe vuote sopra e sotto il blocco di codice delimitato.

I blocchi di codice non sono localizzati.

>[!TIP]
>
Specifica una lingua quando crei un blocco di codice delimitato. La specifica di una lingua consente l&#39;evidenziazione della sintassi specifica della lingua e visualizza un pulsante **Copia** per gli utenti. È inoltre possibile visualizzare i numeri di riga se si specifica una lingua.

**Sintassi**

Utilizza tre apici posteriori ( &grave;&grave;&grave; ) prima e dopo le righe di codice. Assicuratevi che i segni di graduazione apri e chiudi all&#39;indietro siano rientrati nello stesso numero di spazi. Per un rendering ottimale, specifica un linguaggio di codice.

&grave;&grave;&grave;`javascript`

**Esempio**

```javascript
var visitor = Visitor.getInstance("INSERT-MARKETING-CLOUD-ORGANIZATION ID-HERE", {
     trackingServer: "INSERT-TRACKING-SERVER-HERE", // same as s.trackingServer
     trackingServerSecure: "INSERT-SECURE-TRACKING-SERVER-HERE", // same as s.trackingServerSecure

     // To enable CNAME support, add the following configuration variables
     // If you are not using CNAME, DO NOT include these variables
     marketingCloudServer: "INSERT-TRACKING-SERVER-HERE",
     marketingCloudServerSecure: "INSERT-SECURE-TRACKING-SERVER-HERE" // same as s.trackingServerSecure
});
```

### Evidenziazione della sintassi per blocchi di codice

Experience League supporta l’evidenziazione della sintassi per i blocchi di codice. Assicurati di specificare una lingua come `java` dopo la coppia di apici retroversi di apertura per verificare che la sintassi sia evidenziata correttamente. Per un elenco delle lingue valide, consulta [https://prismjs.com](https://prismjs.com/#supported-languages). Se mancano delle lingue, inoltra un ticket jira.

### Numerazione delle righe nei blocchi di codice

Aggiungi `{line-numbers="true"}` dopo la lingua per abilitare la numerazione delle righe.

Esempio con numeri di riga (&grave;&grave;&grave;`html {line-numbers="true"}`):

```html {line-numbers="true"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```

**Inizia numerazione alla riga _**

Aggiungi `start-number="n"` dopo la sintassi dei numeri di riga per iniziare la numerazione con un numero diverso da 1.

Esempio con nuova riga iniziale (&grave;&grave;&grave;`html {line-numbers="true" start-line="7"}`):

```html {line-numbers="true" start-line="7"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

### Evidenziazione riga nei blocchi di codice

Aggiungi `highlight="n"` dopo la sintassi dei numeri di riga per evidenziare le righe all’interno di un blocco di codice. Specificando `11-13, 16` verranno evidenziate le righe da 11 a 13 e 16.

Esempio con evidenziazione riga (&grave;&grave;&grave;`html {line-numbers="true" start-line="7" highlight="11-13, 16"}`):

```html {line-numbers="true" start-line="7" highlight="11-13, 16"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

### Formattazione delle variabili nei blocchi di codice

La sintassi della variabile, ad esempio `<i>italic</i>`, non è supportata nei blocchi di codice. Per indicare il testo variabile, è possibile utilizzare le parentesi angolari `< >`.

## Sezioni comprimibili

È possibile creare una sezione comprimibile, a volte denominata **Pannello a soffietto**, nascosta per impostazione predefinita. L’utente può fare clic sul titolo per espandere o comprimere la sezione.

Il testo comprimibile può essere utilizzato per semplificare contenuti complessi, ad esempio per semplificare una pagina di domande frequenti o per rendere meno complessa una procedura con elenchi nidificati. Ad esempio, invece di visualizzare un set di passaggi secondari, è possibile comprimerli in una sezione &quot;Visualizza dettagli&quot;.

**Sintassi**

```
+++See details
This is text inside a collapsible section.

* Bullet one
* Bullet two
* Bullet three

+++
```

**Esempio**

+++Vedi i dettagli
Testo all&#39;interno di una sezione comprimibile.

* Punto elenco uno
* Punto due
* Punto tre

+++

**Note**

* Non nidificare sezioni comprimibili all&#39;interno di sezioni comprimibili. Le sezioni comprimibili nidificate non vengono riprodotte correttamente. Tuttavia, non causano errori di convalida, pertanto gli utenti visualizzeranno la sintassi `+++` della sezione nidificata.
* Assicurati di aggiungere righe vuote sopra e sotto elementi come elenchi puntati e blocchi di codice all’interno della sezione comprimibile, altrimenti si verificherà un errore di convalida.
* È possibile aggiungere titoli all&#39;interno di sezioni comprimibili, ma non è consigliabile.
* [Le Accordions non sono sempre la risposta per i contenuti complessi sui desktop](https://www.nngroup.com/articles/accordions-complex-content/)
* Uno svantaggio storico delle sezioni comprimibili è che **Trova nella pagina** (Ctrl/Comando+F) ignora il testo compresso. Anche se questo è ancora vero in Safari, non lo è più in Chrome; Trova nella pagina rileva il testo compresso in Chrome.
* Esempio di [aggiornamenti di manutenzione](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=en) pagina utilizzando sezioni comprimibili.

## Commenti e osservazioni

I commenti non vengono visualizzati nel sistema della guida sottoposto a rendering. Utilizzare i commenti per lasciare note a se stessi o ad altri autori. È inoltre possibile utilizzare i commenti per le sezioni di testo 2D.

Per i commenti, tieni presente che anche se non vengono visualizzati nella guida di, sono visibili agli utenti che modificano i file Markdown su GitHub.com. Non includere informazioni riservate nei commenti.

```
<!-- standard comment code -->

DO NOT USE the following:
<!--> bad comment syntax <-->
```

Non è possibile visualizzare il testo sottostante (&quot;Non è possibile visualizzare&quot;) a meno che non si stia modificando il documento.

<!--
You can't see me (unless you're editing in Git).
-->

**Promemoria:** i commenti (osservazioni) non vengono visualizzati negli articoli della guida rivolti al pubblico. Tuttavia, i commenti vengono visualizzati nei file Markdown rivolti al pubblico che gli utenti possono visualizzare e modificare.

>[!IMPORTANT]
>
Evita di aggiungere commenti all’interno di componenti di blocco come gli elenchi puntati, in particolare gli elenchi puntati nidificati. Il commento può modificare il rendering dell’elenco puntato.
>
Nel file TOC.md, non inserire commenti nelle righe al centro dell&#39;elenco del sommario. Ciò potrebbe causare la suddivisione dell’elenco sommario e causare errori di convalida. Spostare invece i commenti nel sommario alla fine del file.

## CONTEXTUALHELP

Gli autori possono lavorare con i team di prodotto per aggiungere finestre a comparsa di aiuto nell’interfaccia utente di prodotto di Experience Cloud o Experience Platform. Esempio:

```markdown
>[!CONTEXTUALHELP]
>id="platform_destinations_activate_mandatorykey_4"
>title="About mandatory attributes"
>abstract="Select the XDM schema attributes that all exported profiles should include. Profiles without the mandatory key are not exported to the destination. Not selecting a mandatory key exports all qualified profiles regardless of their attributes."
>additional-url="http://www.adobe.com/go/destinations-mandatory-attributes-en" text="Learn more in documentation"
```

## Elenchi di definizioni

Per gli elenchi di definizioni, non è ancora supportata la sintassi standard di Markdown. Utilizza invece la formattazione manuale come segue:

```
**Frog** - An amphibious green creature. Likes flies.
```

Rendering:

**Rana** - Una creatura verde anfibia. A me piacciono le mosche.

<!--
A definition list is a Markdown extension that supports the Definition List component in AEM. A definition list consists of a term and its definition.

**When to use**

Using a definition list is optional. To define lists of features or options, you can use either the definition list syntax or use basic Markdown formatting, such as applying bold to option names.

**Syntax**

```
Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
```

**Example**

Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
-->

## Scarica file

Carica il file .zip o un altro file scaricabile nella directory delle risorse, quindi collegalo. Se si tratta di un file .zip, facendo clic sul collegamento verrà scaricato il file. Se si tratta di un tipo di file, ad esempio PDF o PNG, che può essere aperto in un browser, facendo clic sul collegamento verrà aperta una nuova scheda. Per tali file, è consigliabile comprimerli o fornire istruzioni per fare clic con il pulsante destro del mouse sul collegamento e scaricarli.

`Download` &amp;lbrack;`download-test.zip`&amp;rbrack;`(assets/download-test.zip)`

Rendering:

Scarica [scarica zip di prova](assets/download-test.zip)

>[!NOTE]
>
La dimensione massima del file per il download di file e immagini è di 100 MB. Questo è il limite di github.com. Il limite di git.corp.adobe.com è più alto (250 MB), ma è necessario poter copiare i file nel mirror di github.com.

## Intestazioni {#headings}

In Markdown si utilizzano i cancelletti (`#`) per identificare i livelli di intestazione. Il primo livello (`#`) è il titolo dell&#39;articolo, anch&#39;esso specificato nell&#39;intestazione dei metadati. Mantenerli invariati. Il secondo livello (`##`) rappresenta le intestazioni principali della pagina che verranno incluse nel mini-sommario. Se si è abituati a scrivere in AEM (chl-author), le intestazioni di livello 2 (`##`) vengono mappate al componente &quot;Titolo 1&quot; nell&#39;AEM.

Numero massimo di caratteri per le intestazioni: 69 caratteri (inglese) / 120 caratteri (LOC).

```
# This is level 1 (article title)

## This is level 2
   
### This is level 3
```

**Best practice per i titoli**

* Assicurarsi che un&#39;intestazione di livello 1 (`#`) segua una riga vuota dopo i metadati in ogni articolo.
* Non saltare i livelli, ad esempio passare dal livello 2 (`##`) al livello 4 (`####`).
* Includi una riga vuota *prima* e *dopo* ogni intestazione.
* Se un&#39;intestazione include numeri, specificare un ID titolo esplicito che non inizi con un numero, ad esempio `## Release notes for 2016 {#release-notes-2016}`.
* Consigliamo solo 3 livelli di intestazione. Al momento, i livelli 4 e successivi non vengono riprodotti correttamente.
* Le intestazioni vengono visualizzate nella barra di spostamento a destra, in modo che gli utenti possano fare clic per passare a una sezione. Per impostazione predefinita, nella barra di navigazione a destra vengono visualizzati due livelli di intestazione. Se si desidera modificare il numero di livelli, utilizzare i metadati `mini-toc-levels`, ad esempio `mini-toc-levels: 3`.

**ID intestazione**

Gli ID intestazione (detti anche *ID di ancoraggio*) vengono utilizzati per creare collegamenti profondi personalizzati alle sezioni all&#39;interno degli articoli. Per specificare un ID intestazione, usa questo formato:

```
## Creating processing rules {#processing-rules}
```

Gli ID intestazione devono essere minuscoli e sillabati.

Se non si specifica un ID titolo per un titolo, l&#39;ID titolo predefinito è l&#39;intestazione &quot;slugificato&quot; (minuscolo e sillabato). Ad esempio, l&#39;intestazione `## Creating widgets and Such` avrà un ancoraggio `#creating-widgets-and-such`.

## Sintassi HTML {#html}

Per vari motivi, tra cui sicurezza e accessibilità, limitiamo la sintassi HTML che può essere utilizzata in markdown. L’elenco seguente mostra la sintassi HTML supportata. Qualsiasi sintassi HTML non presente nell&#39;elenco genererà un errore di convalida.

```html
<table>
<tbody>
<td>
<tfoot>
<thead>
<th>
<tr>
<col>
<colgroup>
<p> (paragraph break)
<ul> (unordered list / numbered list)
<ol> (ordered list / bullet list)
<li> (list item)
<br> (line break)
<b>
<caption>
<i>
<strong> (bold)
<u> (underline)
<s> (strikethrough)
<span>
<sub> (subscript)
<sup> (superscript)
<a>
<img>
<div>
<em> (emphasis, italics)
<pre> (codeblock)
<code>
<codeblock>
```

<!--
Bob: Check above no space char. (ignore the space; I can't add a codeblock inside this codeblock)
-->

Se desideri aggiungere la sintassi HTML a questo elenco, registra un ticket o contatta il team SSE.

## Immagini {#images}

Utilizza la sintassi `![]()` per le immagini. Le parentesi quadre `[ ]` includono il testo alternativo e le parentesi `( )` includono la posizione dell&#39;immagine e il testo al passaggio del mouse facoltativo (descrizione comando). Il punto esclamativo distingue un&#39;immagine da un collegamento.

```
![alt text](assets/logo.png "Hover text")
```

![Testo alternativo](assets/logo.png "Testo al passaggio del mouse")

Per le immagini condivise, puoi posizionarle in una cartella di risorse principale e quindi utilizzare un collegamento principale che funziona da qualsiasi file all’interno di un archivio:

```
/help/assets/imagename.png
```

### Ridimensionamento e allineamento delle immagini

**Proprietà immagine (con immagine allineata a destra)** ![testo alternativo](assets/premium.png "Testo al passaggio del mouse Premium"){align="right"}

Utilizza una sintassi come quella riportata di seguito per modificare la larghezza o il centro predefiniti dell’immagine oppure per allineare l’immagine a destra all’interno della visualizzazione pagina o della cella della tabella.

```
![Dive image alt text](assets/maui-dive.jpg "Hover text - Maui dive width is 300 pixels and centered"){width="300" align="center"}
```

Rendering:

Bob - Larghezza = 300 pixel sotto

![Testo alternativo immagine immersione](assets/maui-dive.jpg "Testo al passaggio del mouse - La larghezza dell&#39;immersione Maui è di 300 pixel e centrata"){width="300" align="center"}

* Per le immagini di grandi dimensioni, si consiglia di creare immagini di dimensioni sufficienti per essere ridimensionate in modo da rientrare nella larghezza della pagina, ovvero con una larghezza di almeno 640 pixel. La larghezza consigliata è di 1500 pixel. Non è necessario creare immagini di dimensioni superiori a 2500 pixel o 500 kilobyte. La dimensione massima del file per le immagini è 100 MB.
* Per le immagini di piccole dimensioni, creare le immagini utilizzando la larghezza desiderata in pixel oppure utilizzare il parametro width, ad esempio `{width="250"}` (pixel) o `{width="50%"}` (percentuale dell&#39;area di visualizzazione, non le dimensioni dell&#39;immagine originale). Le immagini vengono ridimensionate proporzionalmente. Tieni presente che le immagini possono essere ridimensionate verso l’alto o il basso, quindi fai attenzione alla pixelazione.
* In alcuni casi, le immagini della stessa interfaccia appariranno sproporzionate sulla pagina perché le immagini più grandi (come una barra degli strumenti) vengono ridimensionate, mentre le immagini più strette (come un pannello) non vengono ridimensionate. In questi casi, puoi ridimensionare immagini più ampie per migliorare la coerenza visiva.
* È possibile modificare l&#39;allineamento di un&#39;immagine all&#39;interno dell&#39;area di visualizzazione. Utilizzare `{align="center"}` o `{align="right"}`. Il parametro `valign` non è supportato.

>[!NOTE]
>
La dimensione massima del file per le immagini è 100 MB. Questo è il limite di github.com. Il limite di git.corp.adobe.com è più alto (250 MB), ma è necessario poter copiare i file nel mirror di github.com.

### Collegamenti immagine

Se desideri consentire agli utenti di fare clic su un’immagine per passare a una pagina diversa, utilizza questo formato.

**Sintassi**

```
[![image](assets/core-services_96.png)](https://www.adobe.com)
```

**Esempio**

Fai clic su questa immagine per passare al sito web di Adobe.

[![immagine](assets/core-services_96.png)](https://www.adobe.com)

### Immagini con zoom e clic

Utilizzare il parametro `zoomable` per consentire agli utenti di fare clic su un&#39;immagine per visualizzarne una versione ingrandita. Quando si posiziona il puntatore su un&#39;immagine ingrandita, il puntatore assume la forma di una lente di ingrandimento. Quando fai clic su, l’immagine si espande a tutta la larghezza del browser. Può essere chiuso con un pulsante di chiusura.

**Esempio**

![Immagine di immersione](/help/data-sheets/hidden/assets/maui-dive.jpg "Immersione in Maui"){width="100" zoomable="yes"}

**Sintassi**

```
![Diving image](/help/data-sheets/hidden/assets/maui-dive.jpg "Diving in Maui"){width="100" zoomable="yes"}
```

## Collegamenti e riferimenti incrociati {#links-and-cross-references}

I collegamenti esterni sono diretti e possono essere visualizzati come didascalia collegata o come URL puro.

```
[Adobe](https://www.adobe.com)
```

Rendering:

[Adobe](https://www.adobe.com)

Se aggiungi un URL direttamente al testo, non viene convertito automaticamente in un collegamento. Se si desidera che un URL venga visualizzato come collegamento, aggiungere la sintassi `< >`. Esempi:

```
https://www.adobe.com

<https://www.adobe.com>
```

Rendering:

https://www.adobe.com

<https://www.adobe.com>

I collegamenti agli articoli (rimandi) possono essere un po’ più complessi.

**Opzione 1: collegamento relativo standard**

Ecco l’aspetto di un collegamento relativo standard:

```
See [Overview example article](collaborative-doc-instructions/overview.md)
```

Il percorso deve tenere conto della posizione del file di origine e del file di destinazione. È possibile utilizzare tutti gli operandi di collegamento relativo, ad esempio `./` (directory corrente), `../` (indietro di una directory) e `../../` (indietro di due directory).

**Opzione 2: collegamento relativo principale**

Il vantaggio di questo tipo di collegamento è che deve tenere conto solo del file di destinazione. Funziona da qualsiasi file di origine all’interno dell’archivio, indipendentemente dalla posizione del file di origine.

```
/help/using/docile-rules/introduction.md
```

**Collegamenti profondi**

Per creare un collegamento a un’intestazione all’interno di un articolo, l’intestazione di destinazione deve avere un ID intestazione esplicito (chiamato anche &quot;ID ancoraggio&quot;). Esempio:

`## Creating audience segments {#creating-audience-segments}`

Per creare un collegamento a questo titolo all’interno della stessa pagina, utilizza l’ID titolo del collegamento:

`See [Creating audience segments](#creating-audience-segments)`

Per collegare questa intestazione da un articolo diverso nell’archivio, aggiungi il suffisso ID intestazione alla fine del collegamento:

`See [Audiences: Creating audience segments](audiences.md#creating-audience-segments)`

**Apri in una nuova scheda**

Se si desidera che un collegamento apra una nuova scheda, ad esempio quando si passa a un&#39;altra guida, utilizzare la proprietà `{target="_blank"}` nel collegamento.

Esempio:

`[See What's new](whats-new.md){target="_blank"}`

## Metadati

Aggiungi i metadati nella parte superiore del file Markdown. La riga successiva dopo la riga dei metadati (e la riga vuota) DEVE essere il titolo dell’articolo (# Titolo).

```
---
title: Title for search optimization
description: This is the article description used for search optimization. Use common search keywords and synonyms.
---

# Article title
```

## Tag di localizzazione: UICONTROL, DNL e DONOTLOCALIZE

Tutto il contenuto della guida Markdown viene localizzato inizialmente utilizzando la traduzione automatica. Se la guida non è mai stata localizzata, viene mantenuta la traduzione automatica. Se invece il contenuto della guida è stato localizzato in passato, la traduzione automatica verrà temporaneamente utilizzata come segnaposto finché la traduzione umana non sarà stata finalizzata.

## Altri argomenti correlati

Utilizza il componente &quot;Altri argomenti correlati&quot; per visualizzare i collegamenti correlati alla fine di un articolo. Quando viene eseguito il rendering, il componente MORELIKETHIS viene renderizzato come &quot;Articoli correlati&quot; (e localizzato in altre lingue).

**Sintassi**

![Altri argomenti correlati a questa sintassi](assets/morelikethis.png)

**Esempio**

>[!MORELIKETHIS]
>
* [Article 1](https://helpx.adobe.com/it/support/analytics.html)
* [Article 2](https://helpx.adobe.com/it/support/audience-manager.html)

## Appunti/ammonizioni

Abbiamo esteso Markdown per formattare vari tipi di note: Nota, Suggerimento, Importante e Avvertenza.

**Sintassi**

```
>[!NOTE]
>
>This is a standard NOTE block.
```

**Esempio**

>[!NOTE]
>
Questo è un blocco per le NOTE standard.

**Sintassi**

```
>[!TIP]
>
>This is a standard tip.
```

**Esempio**

>[!TIP]
>
Questo è un suggerimento standard.

**Sintassi**

```
>[!WARNING]
>
>This is a standard warning block.
```

**Esempio**

>[!WARNING]
>
Questo è un blocco di avviso standard.

**Sintassi**

```
>[!IMPORTANT]
>
>This is a standard important block.
```

**Esempio**

>[!IMPORTANT]
>
Questo è un blocco importante standard.

**Sintassi**

```
>[!NOTE]
>
>This is a standard NOTE block.
>
>It includes multiple paragraphs.
```

**Esempio**

>[!NOTE]
>
Questo è un blocco per le NOTE standard.
>
Include più paragrafi.

Nuovi tipi di note supportati:

>[!ADMIN]
>
Questa è una nota dell&#39;amministratore. Solo EXL.

>[!AVAILABILITY]
>
Questa è una nota sulla disponibilità. Solo EXL.

>[!PREREQUISITES]
>
Questa è una nota sui prerequisiti. Solo EXL.

>[!INFO]
>
Questa è una nota informativa. Solo EXL.

>[!ERROR]
>
Questa è una nota di errore. Solo EXL.

>[!SUCCESS]
>
Questa è una nota di successo. Solo EXL.

## Elenchi numerati ed elenchi puntati {#lists}

Per creare elenchi numerati, iniziare una riga con `1.` o `1)`, ma scegliere un metodo e utilizzarlo in modo coerente all&#39;interno dell&#39;articolo. Non è necessario specificare i numeri, che sono gestiti automaticamente da GitHub.

Utilizzare il numero `1` per ogni passaggio dell&#39;elenco numerato.

Aggiungere righe vuote prima e dopo gli elenchi.

**Sintassi**

```
1. This is step 1.

1. This is the next step.

   1. This is a sub-step

   1. This is a sub-step

1. This is yet another step, the third.
```

**Esempio**

1. This is step 1.

   1. Passaggio secondario

   1. Passaggio secondario

1. This is the next step.

1. This is yet another step, the third.

Per creare elenchi puntati, iniziare una riga con `*` o `-` o `+`, ma scegliere un metodo e utilizzarlo in modo coerente all&#39;interno dell&#39;articolo. Se si combinano i formati, ad esempio `*` e `+`, verrà restituito un errore di convalida Markdown quando si archivia il file.

**Best practice:** utilizza `*` per i punti elenco. In Visual Studio Code viene applicato l&#39;asterisco per i punti elenco, pertanto è più semplice utilizzare gli asterischi per automatizzare la creazione di un elenco non ordinato. È possibile che il file TOC.md utilizzi i segni più `+` per gli elenchi. È una perdita dovuta alla migrazione. Qualsiasi carattere punto elenco valido funziona se è coerente all’interno dell’articolo.)

**Sintassi**

```
* First item in an unordered list.
* Another item.
* Here we go again.
```

**Esempio**

* First item in an unordered list.
* Another item.
* Here we go again.

È inoltre possibile incorporare elenchi all’interno di elenchi e aggiungere contenuto tra gli elementi di un elenco. Rientra il contenuto tra le voci di elenco per evitare di iniziare un nuovo elenco. Gli elementi compresi tra i passi devono essere rientrati all&#39;inizio del testo, ovvero 3 spazi per gli elenchi numerati e 2 spazi per gli elenchi puntati.

```
1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/core-services_96.png)
   
1. Make sure that your table looks like this: 

   | Hello | World |
   |---|---|
   | How | are you? |
   
1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.
   
1. Do another step.

   This is an indented line.
```

**Esempio**

1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/core-services_96.png)

1. Make sure that your table looks like this:

   | Hello | World |
   |---|---|
   | How | are you? |

1. This is the fourth step.

   >[!NOTE]
   >
   This is note text.

1. Do another step.

   Questa è una linea rientrata.

NOTA: se esegui un rientro eccessivo, ad esempio 6 spazi invece di 3, il contenuto in quella riga verrà trattato come un blocco di codice.

## Scatole ombreggiature

Le caselle di ombreggiatura sono utili per impostare una sezione di contenuto dal resto della pagina. Ad esempio, al team di Workfront piace aggiungere caselle di esempio contenenti testo, immagini ed esempi di codice per raggiungere uno scopo specifico. Una casella di ombreggiatura può essere utile anche per sezioni &quot;In proprio&quot; o &quot;Caso d’uso&quot; o per note o suggerimenti estesi.

Per creare una casella ombreggiata, aggiungere `>[!BEGINSHADEBOX]` all&#39;inizio della sezione e `>[!ENDSHADEBOX]` alla fine. Tutto il contenuto tra questi tag di inizio e di fine avrà uno sfondo grigio. L&#39;aggiunta di un&#39;etichetta a `BEGINSHADEBOX` (ad esempio `>[!BEGINSHADEBOX "Use Case]` è un metodo facoltativo per creare un titolo di riquadro ombreggiato. È inoltre possibile aggiungere semplicemente testo in grassetto o un titolo alla riga successiva.

Esempio:

>[!BEGINSHADEBOX]

**Rimozione del bordo in una tabella HTML**

In alcuni casi, si utilizza una tabella HTML per creare una progettazione equilibrata, ma non si desidera che il contenuto abbia l&#39;aspetto di una tabella. Per disattivare un bordo per una tabella HTML a una riga, utilizzare la sintassi seguente:

```
<table>
<tr style="border: 0;">
```

>[!NOTE]
>
Non usi troppo. Per le tabelle normali, vogliamo mantenere una progettazione coerente per tutto il contenuto.

![suggerimento tabella](assets/table-no-border.png)

In una tabella a tre colonne è inoltre possibile aggiungere `<td align="center">` e `<td align="right">` per distribuire il contenuto delle celle in modo uniforme nell&#39;area di visualizzazione. Se non fosse stato così, te l&#39;avrei detto.

Questa è l&#39;ultima riga della casella di ombreggiatura.

>[!ENDSHADEBOX]

## Snippet e include

Per condividere il testo tra gli articoli di un repository, creare una cartella `_includes` nella cartella `help`. La cartella `_includes` può contenere file con estensione md a cui è possibile fare riferimento (inclusi) da altri file nell&#39;archivio. Inoltre, un file `snippets.md` in questo repository può includere ancoraggi Head2 a cui è possibile fare riferimento da qualsiasi file nel repository.

Riferimento a H2 nel file snippets.md: `{{id-name}}`

Riferimento al file di inclusione: `{{$include /help/_includes/filename.md}}`

## Tabelle

Le tabelle possono essere problematiche in Markdown. Quando si esegue la migrazione delle tabelle dal sistema di authoring precedente, le tabelle semplici (una riga per cella) vengono formattate come tabelle Markdown native (preferite). Le tabelle più avanzate vengono formattate come HTML.

>[!TIP]
>
Guarda il video [Tabelle Markdown](https://video.tv.adobe.com/v/26220)

Le tabelle native hanno spesso un aspetto migliore in Markdown. Le colonne vengono ridimensionate in base al contenuto. Le tabelle HTML vengono sottoposte a rendering con colonne di uguale larghezza.

Per impostazione predefinita, Markdown non supporta più righe o elenchi nelle celle. Tuttavia, sono disponibili tabelle Markdown estese per consentire più righe nelle celle (utilizzando `<p>` o `<br>`) o elenchi di base (utilizzando `<ul><li>` e così via).

>[!IMPORTANT]
>
Presta attenzione quando aggiungi questi codici HTML alle tabelle Markdown. Se la sintassi non è corretta, si verificherà un errore di convalida che non descrive con precisione il problema. Controlla la sintassi HTML per assicurarti che sia ben formata.

Non consentito in alcuna tabella: iframe, estensioni di celle, tabelle incorporate.

Non consentito nella tabella nativa Markdown: elenchi nidificati o complessi.

Vedi [Tabelle](tables.md)

**Sintassi**

```
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | row 1 column 2 | row 1 column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

**Esempio**

| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | row 1 column 2 | row 1 column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |

Le tabelle semplici funzionano correttamente in Markdown, mentre le tabelle che includono più paragrafi o elenchi all’interno di una cella sono difficili da utilizzare. Per tali contenuti, si consiglia di utilizzare un altro formato, ad esempio intestazioni e testo.

**Tabella Markdown con interruzioni di paragrafo ed elenchi**

```
| Header | Another header | Yet another header |
|------------|----------|----------------|
| row 1 | first paragraph in cell<p>second paragraph in cell(`<p>`)<br>line break (`br`) | row 1 column 3 |
| row 2 | bullet list<ul><li>item 1</li><li>item 2</li><li>item 3</li></ul> | row 2 column 3 |
```

**Esempio**

| Header | Another header | Yet another header |
|------------|----------|----------------|
| row 1 | primo paragrafo della cella<p>secondo paragrafo nella cella (`<p>`)<br>interruzione di riga (`br`) | row 1 column 3 |
| row 2 | elenco puntato<ul><li>elemento 1</li><li>elemento 2</li><li>elemento 3</li></ul> | row 2 column 3 |

**Tabella Markdown con interruzioni di riga e elenco non valido**

Soluzione alternativa con i punti elenco manuali.

```
| Color | Things to Do |
|--- |--- |
| Red | * Read <br> * Write <br> * Study |
| Blue | * Swim <br> * Run <br> * Lift <br> **Note**: Remember to train smart.|
```

**Esempio**

| Colore | Cose da fare |
|--- |--- |
| Rosso | * Lettura di <br> * Scrittura di <br> * Studio |
| Blu | * Nuotare <br> * Eseguire <br> * Incrementare <br> **Nota**: ricorda di addestrare gli smart. |


## Schede

Una scheda è un’area cliccabile nella parte superiore di una sezione che mostra contenuti diversi. Quando si fa clic su una scheda, viene visualizzato il contenuto della scheda e quello delle altre schede è nascosto.

Per creare un set di schede, aggiungere `>[!BEGINTABS]` all&#39;inizio del set di schede e `>[!ENDTABS]` dopo l&#39;ultima scheda. Aggiungi `>[!TAB <tab title>]` tag per ogni sezione della scheda e aggiungi il contenuto di ogni scheda sotto di essa.

**Sintassi della scheda**

```
>[!BEGINTABS]

>[!TAB iOS]

This content appears in the iOS tab.

>[!TAB Android]

This content appears in the Android tab.

>[!TAB Windows]

This content appears in the Windows tab.

>[!TAB MacOS]

This content appears in the MacOS tab.

>[!TAB Linux]

This content appears in the Linux tab.

>[!ENDTABS]
```

**Rendering** eseguito

>[!BEGINTABS]

>[!TAB iOS]

Questo contenuto viene visualizzato nella scheda iOS.

>[!TAB Android]

Questo contenuto viene visualizzato nella scheda Android.

>[!TAB Windows]

Il contenuto viene visualizzato nella scheda Windows.

>[!TAB MacOS]

Questo contenuto viene visualizzato nella scheda MacOS.

>[!TAB Linux]

Questo contenuto viene visualizzato nella scheda Linux.

>[!ENDTABS]

**Note scheda**

* Gli utenti non possono utilizzare la ricerca nella pagina (Ctrl+F/Comando+F) per individuare il contenuto all’interno di schede non visualizzate.
* Se i titoli delle schede si estendono oltre la larghezza della visualizzazione della pagina nel browser dell’utente, viene visualizzata una barra di scorrimento orizzontale.
* Non è possibile formattare i titoli delle schede. Qualsiasi sintassi aggiunta verrà trasmessa come parte del titolo. `>[!TAB **iOS**]` verrà visualizzato come `**iOS**`.
* È possibile creare più set di schede in una pagina, ma non è possibile nidificare un set di schede all&#39;interno di un altro set di schede.
* Al set di schede viene applicato uno sfondo ombreggiato che consente agli utenti di distinguere il contenuto della scheda dagli altri contenuti.

## Evidenziazione testo

Il team Workfront ha chiesto di poter utilizzare l’evidenziazione gialla per indicare l’anteprima delle funzioni in arrivo. Ecco come funziona.

Esempio:

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

Rendering:

L’intero paragrafo NON deve essere evidenziato. <span class="preview"> Questa parola è in **grassetto** all&#39;interno di una frase evidenziata.</span> E questa è solo l’ultima frase.

Come regola generale, utilizza `<span class="preview">` per evidenziare un paragrafo o un testo all&#39;interno di un paragrafo e utilizza `<div class="preview">` per più paragrafi e componenti.

>[!NOTE]
>
Stiamo ancora lavorando al miglioramento della visualizzazione evidenziazione di alcuni elementi di pagina come note e tabelle. Sentiti libero di registrare i bug JIRA se vedi un rendering improprio. In corso.
>
L&#39;anteprima VSC non supporta ancora l&#39;evidenziazione.

## Video

I video non verranno riprodotti in modo nativo in Markdown. Per visualizzare un video in linea, utilizzare l&#39;indicatore del componente `[!VIDEO]` e quindi l&#39;URL.

**Sintassi**

```
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

**Esempio**

>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)

## Informazioni aggiuntive sulla sintassi markdown

### Componenti Markdown estesi

È necessario estendere Markdown per supportare gli elementi non inclusi in Markdown comune.

I componenti speciali vengono dichiarati in un block quote contenitore utilizzando parentesi quadre e un punto esclamativo più il riferimento per il tipo di block che è. Ad esempio, ecco come dichiarare una nota:

```
>[!NOTE]
>
>This is a note.
```

* Note (avvertenze), tra cui Nota, Importante, Suggerimento, Attenzione e Avvertenza
* Video incorporato
* Articoli correlati
* Vari tag dell’interfaccia utente per la localizzazione
* Proprietà dei componenti per intestazioni, immagini e blocchi di codice
* Sezioni comprimibili
* Evidenziazione testo
* Schede pagina

Utilizzare il block quote di Markdown ( `>` ) all&#39;inizio di ogni riga per collegare un componente basato su paragrafi, ad esempio una nota. Per migliorare l&#39;anteprima, aggiungere una riga immediatamente dopo l&#39;inizio della sezione che contiene solo un simbolo di virgolette di blocco (`>`). Per terminare la sezione, aggiungi una riga vuota.

Se è necessario utilizzare sottocomponenti all&#39;interno di componenti, aggiungere un ulteriore livello di block quote (`>  >`) per la sezione di quel sottocomponente. Ad esempio, una NOTA all&#39;interno di una sezione DONOTLOCALIZE deve iniziare con `>  >`.

In alcuni casi, è necessario supportare impostazioni specifiche per gli elementi Markdown, ad esempio i titoli. Se è necessario modificare le impostazioni predefinite, aggiungere i parametri tra parentesi graffe `{# }` dopo il componente.

### Righe vuote

È possibile aggiungere un po&#39; di spazio di respirazione alle pareti di testo con righe vuote. Utilizzare `<br>&nbsp;` come soluzione alternativa per aggiungere una riga vuota.

Esempio: questa è una prima frase di quello che potrebbe essere un testo molto lungo. Consentitemi di inserire una riga vuota tra questo paragrafo e quello successivo.

<br> 

Questo potrebbe non sembrare molto impressionante qui, ma provare righe vuote quando si sente che le pagine sono troppo affollate.

### Caratteri per &quot;escape&quot; {#characters-to-escape}

Diversi caratteri (`# { } [ ] < > * + - . !`) hanno un significato speciale in Markdown o HTML per la creazione di intestazioni, immagini, elenchi e altri componenti. Quando si utilizzano questi caratteri, il motore di rendering ritiene che si stia aggiungendo codice. Tuttavia, in alcuni casi, è necessario visualizzare questi caratteri nel testo. Per farlo, devi &quot;fuggire&quot; dai personaggi. Il metodo di escape più semplice consiste nell&#39;anteporre al carattere una barra rovesciata (`\`). Se ad esempio si desidera iniziare una riga con un carattere `#` in modo che non venga interpretata come intestazione, digitare `\#`:

`\# This is not a heading`

**Rendering eseguito:**

\# Non è un titolo

La barra rovesciata funziona solo con i seguenti caratteri: `# { } [ ] * + - . !`. Se è necessario applicare caratteri di escape come parentesi angolari (ad esempio `<yourname>`), è possibile racchiudere il testo tra apici retroversi per applicare un blocco di codice in linea oppure utilizzare il codice dell&#39;entità HTML al posto del carattere. Esempi di codici HTML comuni:

* `&lt;` (&lt;)
* `&gt;` (>)
* `&amp;` (&amp;)
* `&Hat;` (^)
* `&mdash;` (—)
* `&ndash;` (-)

Un elenco completo delle entità HTML è disponibile nel [sito Web Freeformatter](https://www.freeformatter.com/html-entities.html). In questo modo sarà possibile cercare tutti i caratteri speciali.

>[!NOTE]
>
Per passaggi a catena come &quot;Scegli file > Salva con nome&quot;, non è necessario eseguire l&#39;escape del carattere `>` perché non è accanto ad altri caratteri. Per le variabili come `<filename>` è necessario applicare l&#39;escape alle parentesi angolari utilizzando il blocco di codice `backticks` o i codici di carattere (`&lt;filename&gt;`).

Se utilizzi entità HTML nei blocchi di codice, il testo dell’entità non viene convertito nel carattere speciale. Ad esempio, `&gt;` viene visualizzato in un blocco di codice come &quot; `&gt;` &quot; invece di &quot; > &quot;.

Per eseguire l&#39;escape per gli apici retroversi ( &grave; ), utilizzare `&grave;` o inserire l&#39;apice retroverso all&#39;interno di apici tripli che racchiudono un blocco di codice in linea.

### Elementi non supportati

Ci sono alcuni articoli di Markdown aromatizzati con Git che non intendiamo supportare. Lo strumento di anteprima utilizzato potrebbe abilitare alcune di queste funzioni, ma non fare affidamento su di esse.

**Elenco attività**

Non supportato

```
* [x] Set up Jersey Shore recording
* [x] Buy donuts with sprinkles
* [x] Take nap
* [ ] Wash ferret
```

**Emoji**

Non supportato

```
:bowtie:
```

**Regola orizzontale**

Non supportato

```
***
```

**Citazioni**

Per indicare la sintassi Markdown estesa, ad esempio note e video, usiamo block quote (`>` all&#39;inizio di una riga), come descritto di seguito. È tuttavia possibile utilizzare la sintassi `>` anche per creare una sezione di block quote.

>[!NOTE]
>
Se applica un rientro eccessivo, ad esempio sei spazi invece di tre, il contenuto viene rappresentato come virgolette. Utilizza la quantità corretta di rientro per evitare che il contenuto venga rappresentato erroneamente come un’offerta di blocco.
