---
title: Tabelle
description: Utilizzo delle tabelle markdown e delle tabelle HTML.
hide: true
hidefromtoc: true
source-git-commit: cd9f841a3f720ee366b33f3a78f7ca731c0b865a
workflow-type: tm+mt
source-wordcount: '1420'
ht-degree: 3%

---

# Tabelle

Matt era qui ancora e ancora

Standard Markdown supporta solo tabelle di base. Per AdobeDocs Markdown, sono disponibili le seguenti opzioni:

* Tabelle Markdown di base
* Tabelle HTML
* Tabelle Markdown con sintassi HTML limitata per le interruzioni di paragrafo (`<p>`), interruzioni di riga (`<br>`) ed elenchi di base (`<ul>`, `<ol>`).

## Conversione di tabelle HTML in tabelle Markdown

In alcuni casi, è necessario convertire una tabella HTML in una tabella Markdown o in testo Markdown. Forse è necessario migliorare l’aspetto, risolvere un errore di convalida o semplificare la modifica in futuro.

Sfortunatamente, non è stato possibile trovare un singolo strumento che converta correttamente le tabelle di HTML. Di solito usiamo una combinazione di strumenti per assemblare un tavolo Markdown decente.

| Strumento | Effetto |
|--- |--- |
| [Generatore di tabelle Markdown](https://www.tablesgenerator.com/markdown_tables) | Ideale per creare tabelle Markdown da zero. |
| [Convertitore tabella avanzato](https://tableconvert.com/html-to-markdown) | Convertire le tabelle da qualsiasi formato in qualsiasi formato. <p>**Nota:** I collegamenti e le immagini vengono appiattiti al momento della conversione. |
| [Tabella di base html > convertitore markdown](https://jmalarcon.github.io/markdowntables/) | Convertitore HTML semplice <p>**Nota:** I collegamenti e le immagini vengono appiattiti al momento della conversione. |
| [HTML non tabella > Convertitore Markdown](https://codebeautify.org/html-to-markdown) | Converte le tabelle HTML in sintassi markdown non di tabella. Usare in combinazione con gli strumenti di cui sopra per copiare collegamenti, immagini e qualsiasi altro elemento appiattito. |

## Tabelle Markdown di base

* Assicurarsi di aggiungere almeno tre trattini nella seconda riga che determina le proprietà della tabella. Esempio: `|--- |--- |--- |` per una tabella a 3 colonne.
* Le tabelle Markdown devono avere almeno una riga di intestazione e una riga di corpo. Non è possibile creare una tabella markdown a una riga o a una cella (utilizzare invece HTML).
* Assicurarsi che ogni riga abbia lo stesso numero di caratteri di barra verticale ( &amp;vert; ). Se è necessario includere un carattere barra rovesciata all&#39;interno di una cella di tabella, eseguire l&#39;escape premendo una barra rovesciata (`\|`) o utilizzando il codice entità HTML (`&vert;`).
* Presta attenzione quando utilizzi i blocchi di codice nelle tabelle. I blocchi di codice in linea possono causare larghezze di colonna sproporzionate.
* È possibile modificare il rendering della tabella specificando Automatico o Fisso. Consulta [Modifica del rendering delle tabelle](#table-rendering).

## Creazione di tabelle Markdown con bonus HTML

Per facilitare la migrazione, abbiamo esteso le tabelle Markdown per supportare le interruzioni di paragrafo di HTML (`<p>`), interruzioni di riga (`<br>`) ed elenchi di HTML di base (`<ul>` e `<ol>`) nelle tabelle Markdown.

**Tabella Markdown con interruzioni di riga ed elenchi**

```
| Header 1 | Header 2 | Header 3 |
|--- |--- |--- |
| Normal row | row 1 column 2 | row 1 column 3 |
| Line break | first line in cell<br>second line in cell | row 1 column 3 |
| Bullet list | Bullet list:<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul> | row 2 column 3 |
| Bullet list with line break | Bullet list:<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul><br>This is a new line after the bullet list | row 2 column 3 |
```

**Esempio**

| Intestazione 1 | Intestazione 2 | Intestazione 3 |
|--- |--- |--- |
| Riga normale | row 1 column 2 | row 1 column 3 |
| Interruzione di riga | prima riga nella cella<br>seconda riga nella cella | row 1 column 3 |
| Elenco puntato | Elenco puntato:<ul><li>Elemento 1</li><li>Elemento 2</li><li>Elemento 3</li></ul> | row 2 column 3 |
| Elenco puntato con interruzione di riga | Elenco puntato:<ul><li>Elemento 1</li><li>Elemento 2</li><li>Elemento 3</li></ul><br>Nuova riga dopo l&#39;elenco puntato | row 2 column 3 |

>[!IMPORTANT]
>
>Se decidi di utilizzare HTML nelle tabelle native, assicurati di utilizzare la sintassi HTML corretta. Errori nella sintassi HTML causano errori di convalida difficili da comprendere. Ricontrolla il lavoro.

## Utilizzo delle tabelle HTML

Lo strumento di migrazione ha cercato di mantenere il più possibile la formattazione dalla tabella originale. La maggior parte di questa sintassi HTML viene ignorata, mentre alcune di esse generano errori di convalida.

**Esempio di tabella HTML migrata**

```
<table> 
 <tbody>
  <tr>
   <th>Property</th> 
   <th>Type</th> 
   <th>Value Description</th> 
  </tr>
  <tr>
   <td>badgingPath</td> 
   <td>String[]</td> 
   <td><p><i>(Required)</i> A multi-value string of badge images up to the number of badgingLevels. The badge image paths must be ordered so the first is awarded to the highest expert. If there are less badges than indicated by badgingLevels, the last badge in the array fills out the rest of the array. Example entry:</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>badgingLevels</td> 
   <td>Long</td> 
   <td><i><p>(Optional)</i> Specifies the levels of expertise to be awarded. For example, if there should be an <code>expert </code>and an <code>almost expert</code> (two badges), then the value should be set to 2. The badgingLevel should correspond with the number of expert-related badge images listed for the badgingPath property. Default is 1.</p></td> 
  </tr>
  <tr>
   <td>badgingType</td> 
   <td>String</td> 
   <td><p><i>(Required)</i> Identifies the scoring engine as either "basic" or "advanced". Set to "advanced" else the default is "basic".</p></td> 
  </tr>
 </tbody>
</table>
```

**Rendering**

<table> 
 <tbody>
  <tr>
   <th>Proprietà</th> 
   <th>Tipo</th> 
   <th>Descrizione valore</th> 
  </tr>
  <tr>
   <td>badgingPath</td> 
   <td>Stringa[]</td> 
   <td><p><i>(Obbligatorio)</i> Una stringa con più valori di immagini di badge fino al numero di badgeLevels. I percorsi delle immagini del badge devono essere ordinati in modo che il primo venga assegnato al massimo esperto. Se il numero di badge è inferiore a quello indicato da badgingLevels, l’ultimo badge nell’array occuperà il resto dell’array. Esempio di voce:</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>badgingLevels</td> 
   <td>Lungo</td> 
   <td><p><i>(Facoltativo)</i> Specifica i livelli di esperienza da assegnare. Ad esempio, se deve essere <code>expert </code>e un <code>almost expert</code> (due badge), il valore deve essere impostato su 2. Il valore badgingLevel deve corrispondere al numero di immagini badge correlate all’esperto elencate per la proprietà badgingPath. Il valore predefinito è 1.</p></td> 
  </tr>
  <tr>
   <td>badgingType</td> 
   <td>Stringa</td> 
   <td><p><i>(Obbligatorio)</i> Identifica il motore di punteggio come "di base" o "avanzato". Impostate questo parametro su "Advanced", altrimenti l'impostazione predefinita è "Basic".</p></td> 
  </tr>
 </tbody>
</table>

**Quando utilizzare le tabelle HTML**

* Per bilanciare le colonne.
* Per omettere le intestazioni di tabella (le tabelle markdown devono avere una riga di intestazione).
* Per rimuovere il bordo di una tabella a una riga (`<tr style="border: 0;">`).
* Per aggiungere estensioni di colonne o righe.
* Per allineare il testo all&#39;interno di una cella di tabella.

**Note per l&#39;utilizzo delle tabelle HTML**

* Non utilizzare la sintassi Markdown nelle tabelle HTML. Ad esempio, se aggiungi `[!NOTE]` in una tabella HTML, verrà riprodotto così com’è (`[!NOTE]`). Utilizza invece la sintassi HTML per elementi come note e immagini.

  I tag localizzati rappresentano un’eccezione a questa regola, perché i tag UICONTROL e DNL vengono eliminati prima del rendering delle pagine.

* Nelle tabelle non è supportata tutta la sintassi HTML. Gli elementi di larghezza, altezza, colore e altri elementi di sintassi HTML vengono ignorati durante il rendering in EXL. È possibile lasciare questi valori in a meno che non generino errori di convalida.
* Per allineare il testo, utilizza `align: "left|center|right"` in HTML. Ad esempio, per centrare il contenuto di una cella di tabella, utilizzare `<td align="center">`.
* Le tabelle HTML non possono includere tabelle nidificate.

>[!TIP]
>
>Se si desidera disattivare un bordo per una tabella HTML a una riga, utilizzare la sintassi seguente:
>
>```
><table>
><tr style="border: 0;">
>```

## Specifica della modalità di rendering delle tabelle {#table-rendering}

È possibile eseguire il rendering delle tabelle in due modi:

* **Fisso** (attualmente l’impostazione predefinita) - Include regole personalizzate per il rendering delle tabelle, incluse le tabelle HTML con immagini. Le tabelle vengono riprodotte a larghezza intera senza scorrimento, il che a volte causa la sovrapposizione del testo.
* **Automatico** - Simile al Git-Flavored Markdown (GFM). Le tabelle possono scorrere, pertanto il testo non si sovrappone.

Nella maggior parte dei casi, le tabelle vengono visualizzate con lo stesso aspetto. Tuttavia, se la tabella include testo sovrapposto, è necessario applicare `auto` tag. Oppure, se il rendering della tabella HTML con le schede immagine non viene eseguito correttamente, potrebbe essere utile applicare il `fixed` tag.

Stiamo considerando di modificare il valore predefinito da `fixed` a `auto`.

## Modifica delle tabelle Markdown

Se si desidera specificare la modalità di rendering di una tabella di markdown nativa, aggiungere una delle seguenti righe di sintassi DOPO la tabella, con righe vuote prima e dopo:

* `{style="table-layout:auto"}`
* `{style="table-layout:fixed"}`

![rendering di tabelle](assets/table-render.png)

### Modifica delle tabelle di HTML

Se si desidera specificare la modalità di rendering di una tabella HTML, utilizzare una delle seguenti righe di sintassi nella prima riga della tabella:

* `<table style="table-layout:auto">`
* `<table style="table-layout:fixed">`

```
<table style="table-layout:fixed">
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>$100</td>
  </tr>
</table>
```

### Quando utilizzare Automatico o Fisso

**Testo sovrapposto**

Utilizzare `auto` per tabelle con blocchi di codice lunghi o testo che causa la sovrapposizione del testo quando `fixed` (impostazione predefinita) è selezionato.

*Fisso (predefinito)*

| Metrica Approfondimenti | Descrizione | Parametro query ID |
| ---- | ---- | ---- |
| **timeseries.data.collection.validation.category.type.count** | Numero totale di messaggi di &quot;tipo&quot; non validi per un set di dati o per tutti i set di dati. | ID set di dati |
| **timeseries.data.collection.validation.category.range.count** | Numero totale di messaggi &quot;intervallo&quot; non validi per un set di dati o per tutti i set di dati. | ID set di dati |
| **timeseries.data.collection.validation.category.format.count** | Numero totale di messaggi &quot;format&quot; non validi per un set di dati o per tutti i set di dati. | ID set di dati |
| **timeseries.data.collection.validation.category.pattern.count** | Numero totale di messaggi &quot;pattern&quot; non validi per un set di dati o per tutti i set di dati. | ID set di dati |
| **timeseries.data.collection.validation.category.presence.count** | Numero totale di messaggi di &quot;presenza&quot; non validi per un set di dati o per tutti i set di dati. | ID set di dati |
| **timeseries.data.collection.validation.category.enum.count** | Numero totale di messaggi &quot;enum&quot; non validi per un set di dati o per tutti i set di dati. | ID set di dati |

{style="table-layout:fixed"}

*Automatico*

| Metrica Approfondimenti | Descrizione | Parametro query ID |
| ---- | ---- | ---- |
| **timeseries.data.collection.validation.category.type.count** | Numero totale di messaggi di &quot;tipo&quot; non validi per un set di dati o per tutti i set di dati. | ID set di dati |
| **timeseries.data.collection.validation.category.range.count** | Numero totale di messaggi &quot;intervallo&quot; non validi per un set di dati o per tutti i set di dati. | ID set di dati |
| **timeseries.data.collection.validation.category.format.count** | Numero totale di messaggi &quot;format&quot; non validi per un set di dati o per tutti i set di dati. | ID set di dati |
| **timeseries.data.collection.validation.category.pattern.count** | Numero totale di messaggi &quot;pattern&quot; non validi per un set di dati o per tutti i set di dati. | ID set di dati |
| **timeseries.data.collection.validation.category.presence.count** | Numero totale di messaggi di &quot;presenza&quot; non validi per un set di dati o per tutti i set di dati. | ID set di dati |
| **timeseries.data.collection.validation.category.enum.count** | Numero totale di messaggi &quot;enum&quot; non validi per un set di dati o per tutti i set di dati. | ID set di dati |

{style="table-layout:auto"}

**Tabelle HTML con immagini bilanciate**

Utilizzare `fixed` per le tabelle HTML che richiedono immagini bilanciate che si sbilanciano quando `auto` è selezionato. In questo esempio, le dimensioni delle immagini sono identiche, ma la colonna centrale contiene più testo.

*Automatico*

<table style="table-layout:auto">
<tr>
  <td>
    <a href="table-breaks.md">
    <img alt="Lead" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="table-breaks.md"><strong>Flusso di lavoro per lead di Adobe</strong></a>
    </div>
    <em>Flusso di lavoro di modifica principale per autori di lead.</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="Non frequente" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>Flusso di lavoro per utenti non frequenti</strong></a>
    </div>
    <em>Non sei uno scrittore? Scopri i modi più semplici per apportare contributi. Non sei uno scrittore? Scopri i modi più semplici per apportare contributi. Non sei uno scrittore? Scopri i modi più semplici per apportare contributi. Non sei uno scrittore? Scopri i modi più semplici per apportare contributi. Non sei uno scrittore? Scopri i modi più semplici per apportare contributi. Non sei uno scrittore? Scopri i modi più semplici per apportare contributi.</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="Convalida" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>Convalida</strong></a>
    </div>
    <em>Scopri come risolvere gli errori di convalida.</em>
    <br>
  </td>
</tr>
</table>

*Fisso (in più modi)*

<table style="table-layout:fixed">
<tr>
  <td>
    <a href="table-breaks.md">
    <img alt="Lead" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="table-breaks.md"><strong>Flusso di lavoro per lead di Adobe</strong></a>
    </div>
    <em>Flusso di lavoro di modifica principale per autori di lead.</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="Non frequente" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>Flusso di lavoro per utenti non frequenti</strong></a>
    </div>
    <em>Non sei uno scrittore? Scopri i modi più semplici per apportare contributi. Non sei uno scrittore? Scopri i modi più semplici per apportare contributi. Non sei uno scrittore? Scopri i modi più semplici per apportare contributi. Non sei uno scrittore? Scopri i modi più semplici per apportare contributi. Non sei uno scrittore? Scopri i modi più semplici per apportare contributi. Non sei uno scrittore? Scopri i modi più semplici per apportare contributi.</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="Convalida" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>Convalida</strong></a>
    </div>
    <em>Scopri come risolvere gli errori di convalida.</em>
    <br>
  </td>
</tr>
</table>