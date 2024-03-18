---
title: Correzioni di bug (nascosti)
description: Pagina di prova a scopo di test interno
hide: true
hidefromtoc: true
source-git-commit: 3c5839d71d68232c631fb9ff5bebfa5ea864d250
workflow-type: tm+mt
source-wordcount: '1358'
ht-degree: 4%

---

# Correzioni di bug

## I badge in linea non funzionano

Questi badge devono trovarsi sulla stessa riga degli elementi dell’elenco puntato.

* [[!DNL Mixpanel]](note-test.md) [!BADGE Note]{type=Informative}
* [[!DNL Pendo]](tables.md) [!BADGE Tabelle]{type=Positive}
* [[!DNL RainFocus]](syntax-style-guide.md) [!BADGE Guida allo stile di sintassi]{type=Positive}

## UGP-10560 - Distintivi nelle sezioni comprimibili

+++ Versioni precedenti

### Versione V1.16

_13 febbraio 2023_

[!BADGE Supportati]{type=Informative tooltip="Supportati"}

![Nuovo](assets/package.png) I video sui prodotti sono ora supportati dall’API Catalog Service.
![Correzione](assets/package.png) Sono ora supportati i prodotti in bundle a prezzi fissi.
![Correzione](assets/package.png) Le opzioni esaurite vengono ora visualizzate nel widget PDP.

#### Limitazioni note

Queste funzioni non sono ancora supportate:

* La dimensione massima per il payload degli attributi dinamici è di 9 MB.
* Prezzo del prodotto di gruppo. Può essere calcolato con prezzi di prodotto semplici.
* In un array di immagini, solo la prima immagine contiene ruoli.

Le seguenti limitazioni possono essere risolte utilizzando l’API Mesh e l’API core di GraphQL:

* Prezzo minimo annunciato
* [Prezzi a livelli](https://www.adobe.com)

### Versione V1.13

_venerdì 12 ottobre 2023_

[!BADGE Supportati]{type=Informative tooltip="Supportati"}

![Nuovo](assets/package.png) Catalog Service supporta `inStock` flag per varianti prodotto.
![Nuovo](assets/package.png) `urlKey` e `externalId` sono stati aggiunti allo schema GraphQL.
![Nuovo](assets/package.png) Sono ora supportati i prodotti scaricabili e le gift card.

### Versione V1.12

_mercoledì 19 settembre 2023_

[!BADGE Supportati]{type=Informative tooltip="Supportati"}

![Nuovo](https://www.adobe.com).
![Correzione](assets/package.png) Questa versione contiene correzioni di bug e miglioramenti sul lato servizio.

### Versione V1.11

_mercoledì 18 luglio 2023_

[!BADGE Supportati]{type=Informative tooltip="Supportati"}

![Nuovo](assets/package.png) Catalog Service ora supporta [`recommendations`](https://developer.adobe.com/commerce/services/graphql/recommendations/recommendations/) Query GraphQL per Product Recommendations.

### Versione V1.10

_mercoledì 27 giugno 2023_

[!BADGE Supportati]{type=Informative tooltip="Supportati"}

![Nuovo](assets/package.png) L’API di Catalog Service ora supporta i &quot;prodotti correlati&quot;.

### Versione V1.7

_giovedì 12 aprile 2023_

[!BADGE Supportati]{type=Informative tooltip="Supportati"}

![Nuovo](assets/package.png) Catalog Service ora pulisce le varianti di prodotto eliminate.
![Correzione](assets/package.png) Scalabilità dell&#39;infrastruttura e miglioramenti delle prestazioni.

### Versione V1.6

_mercoledì 28 marzo 2023_

[!BADGE Supportati]{type=Informative tooltip="Supportati"}

![Nuovo](assets/package.png) Campioni aggiunti al [`products`](https://developer.adobe.com/commerce/services/graphql/catalog-service/products/) query.
![Nuovo](https://www.adobe.com).

### Versione V1.5

_martedì 6 marzo 2023_

[!BADGE Supportati]{type=Informative tooltip="Supportati"}

![Nuovo](assets/package.png) Aggiunto [`categories`](https://developer.adobe.com/commerce/services/graphql/schema/catalog-service/categories/) funzionalità GraphQL.
![Correzione](assets/package.png) Prestazioni e scalabilità API migliorate.

### Versione V1.4

_mercoledì 7 febbraio 2023_

[!BADGE Supportati]{type=Informative tooltip="Supportati"}

![Nuovo](assets/package.png) È stato pubblicato il metapacchetto catalogo-servizio per semplificare i passaggi di installazione.
![Correzione](assets/package.png) Miglioramenti a livello di scalabilità e prestazioni delle API.

### Versione V1.3

_mercoledì 17 gennaio 2023_

[!BADGE Supportati]{type=Informative tooltip="Supportati"}

![Nuovo](assets/package.png) L’esperienza di onboarding è stata semplificata e migliorata.
![Nuovo](assets/package.png) Sono disponibili nuovi endpoint sandbox per i clienti per i test di pre-produzione.
![Nuovo](assets/package.png) È stato aggiunto il supporto per i prodotti virtuali.
![Correzione](assets/package.png) Miglioramenti a livello di scalabilità e prestazioni delle API.

### Versione V1.1

_sabato 18 novembre 2022_

[!BADGE Supportati]{type=Informative tooltip="Supportati"}

![Nuovo](assets/package.png) Catalog Service ora supporta Adobe [Mesh API](https://developer.adobe.com/graphql-mesh-gateway/).
![Correzione](assets/package.png) Sono state migliorate la scalabilità API e le prestazioni complessive.

### Versione V1.0

_mercoledì 4 ottobre 2022_

[!BADGE Supportati]{type=Informative tooltip="Supportati"}

![Nuovo](assets/package.png) Ora supporta prodotti in bundle e raggruppati.
![Nuovo](assets/package.png) Sono state aggiunte sostituzioni di visibilità B2B. È ora possibile cercare i prodotti e aggiungerli al carrello per gruppi di clienti specifici.
![Correzione](assets/package.png) Il servizio è ora più stabile e offre prestazioni migliori.

### Versione 0.3 - Beta+

_martedì 12 settembre 2022_

[!BADGE Supportati]{type=Informative tooltip="Supportati"}

![Nuovo](assets/package.png) Supporto immagini per varianti: le immagini del prodotto vengono restituite in base alle opzioni selezionate
![Nuovo](assets/package.png) Ruoli per supporto prezzi: consente solo ai membri di gruppi di clienti specifici di visualizzare il prezzo dei prodotti
![Correzione](assets/package.png) Miglioramento della stabilità e delle prestazioni del servizio
![Nuovo](assets/package.png) Ricevi aggiornamenti quando i prodotti vengono eliminati dal catalogo

### Versione beta

_9 agosto 2022_

[!BADGE Supportati]{type=Informative tooltip="Supportati"}

![Nuovo](assets/package.png) Il `products` e `refineProduct` le query restituiscono i dati seguenti:

* Attributi di prodotto predefiniti (di sistema).
* Attributi di prodotto dinamici e filtrali per ruolo (pagina di visualizzazione prodotto/pagina di elenco prodotti).
* Opzioni prodotto.
* Immagini dei prodotti e filtrale per ruolo (PDP/PLP).
* Un prezzo specifico per prodotti semplici e fasce di prezzo per prodotti configurabili.
* Prezzi e fasce di prezzo del gruppo di clienti. Restituiscono un prezzo predefinito di fallback sugli acquirenti senza un gruppo di clienti.
* Tipi di prodotto che utilizzano prezzi specifici per il cliente B2B.

+++

## UGP-10565 - Evidenziazione testo

Testo prima `<div class="preview">`

<div class="preview">

### Aggiungi campi nativi Workfront

Puoi aggiungere campi nativi di Workfront ai moduli personalizzati. Quando il modulo personalizzato viene allegato a un oggetto, il campo viene popolato dai dati dell’oggetto. Ad esempio, il campo Description (Descrizione) in un modulo personalizzato allegato a un progetto estrae la descrizione del progetto. (Il campo può mostrare &quot;N/D&quot; se non sono disponibili dati).

1. Sul lato sinistro dello schermo, trovare **Campo nativo** e trascinarlo in una sezione dell’area di lavoro.
1. Sul lato destro della schermata, configura le opzioni per il campo personalizzato:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Etichetta</td> 
      <td> <p>(Obbligatorio) Digita un’etichetta descrittiva da visualizzare sopra il campo. Puoi modificare l’etichetta in qualsiasi momento.</p> <p><b>IMPORTANTE</b>: evita di utilizzare caratteri speciali in questa etichetta. Non vengono visualizzati correttamente nei rapporti.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">Nome</td> 
      <td> <p>(Obbligatorio) Questo nome indica il modo in cui il sistema identifica il campo.</p><p> Quando configuri il campo per la prima volta e digiti l’etichetta, il campo Nome si popola automaticamente in modo che corrisponda a esso. Tuttavia, i campi Etichetta e Nome non sono sincronizzati. In questo modo è possibile modificare l'etichetta visualizzata dagli utenti senza dover cambiare il nome visualizzato dal sistema.</p>
      <p><b>IMPORTANTE</b>:
      <ul> 
      <li>Sebbene sia possibile farlo, si consiglia di non modificare questo nome dopo che l’utente o altri utenti hanno iniziato a utilizzare il modulo personalizzato in Workfront. In questo caso, il sistema non riconoscerà più il campo a cui potrebbe ora essere fatto riferimento in altre aree di Workfront.</p> </li>
      <li> <p>Ogni nome di campo deve essere univoco nell’istanza Workfront della tua organizzazione. In questo modo, è possibile riutilizzare un modulo già creato per un altro modulo personalizzato.</p> </li>
      <li><p>È consigliabile non utilizzare il carattere punto/punto nel nome del campo personalizzato, per evitare errori quando si utilizza il campo in aree diverse di Workfront.</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">Istruzioni</td> 
      <td> <p>Digitare eventuali informazioni aggiuntive sul campo. Quando gli utenti compilano il modulo personalizzato, possono passare il cursore sull’icona del punto interrogativo per visualizzare una descrizione comando contenente le informazioni digitate qui.</td> 
     </tr> 
     <tr> 
      <td role="rowheader">Campo di riferimento</td> 
      <td><p>(Obbligatorio) Seleziona un campo nativo di Workfront.<p><p>Sono disponibili solo campi nativi per gli oggetti del modulo. Se ad esempio l'elenco Tipi di oggetto nella parte superiore del progettista del modulo mostra Project, sarà possibile selezionare campi nativi per i progetti ma non campi specifici delle attività.</p></td>
     </tr>
     <tr> 
      <td role="rowheader">Dimensione</td> 
      <td>(Facoltativo) Modifica la dimensione di visualizzazione del campo in base alle esigenze.</td> 
     </tr> 
    </tbody> 
   </table>

1. Per salvare le modifiche, fai clic su **Applica** e passare a un&#39;altra sezione per continuare a creare il modulo.

   oppure

   Clic **Salva e chiudi**.

</div>

Testo dopo evidenziazione

## UGP-10566 - Il testo del collegamento è inferiore al testo normale nelle tabelle HTML

Cfr. anche UGP-9780

<table style="table-layout:auto"> 
<tbody> 
<tr>
<td>Input in</td>
<td>Descrizione</td>
<td>Disponibile per </td>
</tr>
<tr> 
    <td role="rowheader">Etichetta</td> 
    <td> <p>(Obbligatorio) Digita un’etichetta descrittiva da visualizzare sopra il campo personalizzato. Puoi modificare l’etichetta in qualsiasi momento. Per ulteriori informazioni, consulta <a href="https://www.adobe.com" class="MCXref xref">Aggiungere un campo personalizzato a un modulo personalizzato</a> in questo articolo.</p> <p><b>IMPORTANTE</b>: evita di utilizzare caratteri speciali in questa etichetta. Non vengono visualizzati correttamente nei rapporti.</p> </td> 
    <td>
    <ul>
    <li>Pulsanti di scelta. Per ulteriori informazioni, consulta <a href="https://www.adobe.com">Aggiungere un campo personalizzato a un modulo personalizzato</a> in questo articolo. (Nessuna classe)</li>
    <li>Gruppo di caselle di controllo</li>
    <li>A discesa</li>
    </ul></td>
</tr> 
</tbody> 
</table>

## UGP-9176 - Vecchio bug

Il tag &quot;span&quot; non funziona correttamente in una NOTA (e un elenco)

Per informazioni sulle funzioni disponibili nella nuova esperienza di commento e sugli oggetti, consulta [Nuova esperienza di commento](note-test.md).

1. Passare all&#39;oggetto a cui si desidera aggiungere una risposta.
1. Clic **Aggiornamenti**, quindi fare clic su **Commenti** scheda per l&#39;oggetto e trovare il commento o la risposta a cui si desidera rispondere

   Oppure

   <span class="preview">Fai clic su **Tutti** , quindi fai clic su **Rispondi nei commenti** per aprire il commento nella scheda Commenti e rispondere. Non è possibile rispondere nella scheda Tutto.</span>

1. (Facoltativo) Per includere nella risposta il testo di un aggiornamento precedente, fare clic sul pulsante **Altro** nell’angolo superiore destro del commento a cui desideri rispondere, quindi fai clic su **Risposta preventivo**. Il testo dell&#39;aggiornamento precedente viene visualizzato nell&#39;area di input, contrassegnato da una linea grigia verticale.
1. Clic **Rispondi**.

   ![](assets/package.png)

   Puoi vedere gli utenti attivamente coinvolti nella conversazione nella parte inferiore della sezione **Aggiungi risposta...** e puoi aggiungerne altre o rimuovere quelle che non sono più pertinenti. Questi utenti, insieme a tutti gli utenti abbonati all’oggetto, ricevono una notifica ogni volta che viene effettuato un aggiornamento o una risposta sull’oggetto. Puoi anche assegnare tag a più utenti per includerli nella risposta.  Per assegnare tag a più utenti, consulta [Assegna tag ad altri utenti in caso di aggiornamenti](note-test.md).

   >[!TIP]
   >
   >   Per aggiungere ulteriori risposte a una risposta esistente, puoi iniziare a digitare nella **Aggiungi risposta...** o fai clic su **Rispondi** sul commento originale. La risposta viene aggiunta alla fine del thread.

1. Inizia a digitare la risposta e utilizza eventuali opzioni aggiuntive dalla barra degli strumenti Testo formattato. Per informazioni sull’utilizzo di Rich Text o di altre funzionalità di aggiornamento, consulta [Aggiorna lavoro](note-test.md).

1. Clic **Invia** per salvare la risposta.

1. (Facoltativo) Fai clic su **Altro** nell’angolo in alto a destra del commento a cui desideri rispondere per ulteriori opzioni per gestire la risposta. Per ulteriori informazioni, consulta [Aggiorna lavoro](note-test.md).
