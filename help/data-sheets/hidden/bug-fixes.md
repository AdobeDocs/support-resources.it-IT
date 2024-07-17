---
title: Correzioni di bug (nascosti)
description: Pagina di prova a scopo di test interno
hide: true
hidefromtoc: true
exl-id: e6270f95-3550-4e35-ad4c-760584bb9b5d
source-git-commit: 0cefcf5bb4a021593a6bbe44eed0ad83e8bd259f
workflow-type: tm+mt
source-wordcount: '1926'
ht-degree: 27%

---

# Correzioni di bug

## Test di attivazione automatica

Questi bug devono essere corretti.

## Collegamenti UGP-10866 non in grassetto nelle caselle ombra

>[!BEGINSHADEBOX]

**Sommario**

* [Introduzione all’assistente IA](note-test.md)
* **[Generazione di e-mail con l&#39;Assistente AI](syntax-style-guide.md)**
* [Generazione di SMS con l’assistente IA](test-page.md)
* [Generazione di push con l’assistente IA](tables.md)
* [Esperimento contenuti con l’assistente IA](test-redirection.md)

>[!ENDSHADEBOX]

Nessuna casella ombreggiata

**Sommario**

* [Introduzione all’assistente IA](note-test.md)
* **[Generazione di e-mail con l&#39;Assistente AI](syntax-style-guide.md)**
* [Generazione di SMS con l’assistente IA](test-page.md)
* [Generazione di push con l’assistente IA](tables.md)
* [Esperimento contenuti con l’assistente IA](test-redirection.md)


## I badge in linea UGP-10584 non funzionano

Questi badge devono trovarsi sulla stessa riga degli elementi dell’elenco puntato.

* [[!DNL Mixpanel]](note-test.md) [!BADGE Note]{type=Informative}
* [[!DNL Pendo]](tables.md) [!BADGE Tabelle]{type=Positive}
* [[!DNL RainFocus]](syntax-style-guide.md) [!BADGE Guida allo stile di sintassi]{type=Positive}

## UGP-10560 - Distintivi nelle sezioni comprimibili

+++ Versioni precedenti

### Versione V1.16

_13 febbraio 2023_

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

![I nuovi](assets/package.png) video di prodotto sono ora supportati dall&#39;API Catalog Service.
![Correzione](assets/package.png) I prodotti in bundle con prezzi fissi sono ora supportati.
![Correzione](assets/package.png) Le opzioni esaurite sono ora visualizzate nel widget PDP.

#### Limitazioni note

Queste funzioni non sono ancora supportate:

* La dimensione massima per il payload degli attributi dinamici è di 9 MB.
* Prezzo del prodotto di gruppo. Può essere calcolato con prezzi di prodotto semplici.
* In un array di immagini, solo la prima immagine contiene ruoli.

Le seguenti limitazioni possono essere risolte utilizzando l’API Mesh e l’API core di GraphQL:

* Prezzo minimo annunciato
* [Prezzo livello](https://www.adobe.com)

### Versione V1.13

_venerdì 12 ottobre 2023_

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

![New](assets/package.png) Catalog Service supporta il flag `inStock` per le varianti di prodotto.
Sono stati aggiunti ![nuovi](assets/package.png) `urlKey` e `externalId` allo schema GraphQL.
Sono ora supportati ![Nuovi](assets/package.png) prodotti scaricabili e gift card.

### Versione V1.12

_mercoledì 19 settembre 2023_

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

![Nuovo](https://www.adobe.com).
![Correzione](assets/package.png) Questa versione contiene correzioni di bug e miglioramenti sul lato servizio.

### Versione V1.11

_mercoledì 18 luglio 2023_

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

![New](assets/package.png) Catalog Service ora supporta la query GraphQL [`recommendations`](https://developer.adobe.com/commerce/services/graphql/recommendations/recommendations/) per Product Recommendations.

### Versione V1.10

_mercoledì 27 giugno 2023_

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

L&#39;API di ![New](assets/package.png) Catalog Service ora supporta i &quot;prodotti correlati&quot;.

### Versione V1.7

_giovedì 12 aprile 2023_

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

![New](assets/package.png) Catalog Service ora ripulisce le varianti di prodotto eliminate.
![Correggi](assets/package.png) Miglioramenti a livello di scalabilità e prestazioni dell&#39;infrastruttura.

### Versione V1.6

_mercoledì 28 marzo 2023_

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

![Nuovi](assets/package.png) campioni aggiunti alla query [`products`](https://developer.adobe.com/commerce/services/graphql/catalog-service/products/).
![Nuovo](https://www.adobe.com).

### Versione V1.5

_martedì 6 marzo 2023_

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

![Nuovo](assets/package.png) Aggiunta funzionalità di [`categories`](https://developer.adobe.com/commerce/services/graphql/schema/catalog-service/categories/) GraphQL.
![Correzione](assets/package.png) Prestazioni e scalabilità API migliorate.

### Versione V1.4

_mercoledì 7 febbraio 2023_

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

![Nuovo](assets/package.png) Metapackage del servizio catalogo pubblicato per semplificare i passaggi dell&#39;installazione.
![Correggi](assets/package.png) miglioramenti a livello di scalabilità e prestazioni dell&#39;API.

### Versione V1.3

_mercoledì 17 gennaio 2023_

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

![Nuovo](assets/package.png) ha semplificato e migliorato l&#39;esperienza di onboarding.
![Nuovi](assets/package.png) nuovi endpoint sandbox del cliente sono disponibili per il test di pre-produzione.
![Nuovo](assets/package.png) supporto aggiunto per i prodotti virtuali.
![Correggi](assets/package.png) miglioramenti a livello di scalabilità e prestazioni dell&#39;API.

### Versione V1.1

_sabato 18 novembre 2022_

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

![New](assets/package.png) Catalog Service ora supporta [API Mesh](https://developer.adobe.com/graphql-mesh-gateway/) di Adobe.
![Correzione](assets/package.png) Miglioramento della scalabilità API e delle prestazioni complessive.

### Versione V1.0

_mercoledì 4 ottobre 2022_

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

![Nuovo](assets/package.png) ora supporta i prodotti raggruppati e raggruppati.
![Nuovo](assets/package.png) Aggiunte Override Di Visibilità B2B. È ora possibile cercare i prodotti e aggiungerli al carrello per gruppi di clienti specifici.
Il servizio ![Correzione](assets/package.png) è ora più stabile e offre prestazioni migliorate.

### Versione 0.3 - Beta+

_martedì 12 settembre 2022_

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

![Nuove](assets/package.png) immagini per le varianti supportate: le immagini del prodotto vengono restituite in base alle opzioni selezionate
![Nuovi](assets/package.png) ruoli per supporto prezzi: consente solo ai membri di gruppi di clienti specifici di visualizzare il prezzo dei prodotti
![Correzione](assets/package.png) Stabilità e prestazioni migliorate del servizio
![Nuovi](assets/package.png) aggiornamenti ricevuti quando i prodotti vengono eliminati dal catalogo

### Versione Beta

_mercoledì 9 agosto 2022_

[!BADGE Supportato]{type=Informative tooltip="Supportato"}

![Nuovo](assets/package.png) Le query `products` e `refineProduct` restituiscono i dati seguenti:

* Attributi di prodotto predefiniti (di sistema).
* Attributi di prodotto dinamici e filtrali per ruolo (pagina di visualizzazione prodotto/pagina di elenco prodotti).
* Opzioni prodotto.
* Immagini dei prodotti e filtrale per ruolo (PDP/PLP).
* Un prezzo specifico per prodotti semplici e fasce di prezzo per prodotti configurabili.
* Prezzi e fasce di prezzo del gruppo di clienti. Restituiscono un prezzo predefinito di fallback sugli acquirenti senza un gruppo di clienti.
* Tipi di prodotto che utilizzano prezzi specifici per il cliente B2B.

+++

## [!BADGE Obsoleta]{type=negative}

Vedi il titolo precedente. E la prossima.

## Test attivazione automatica

Ho aggiunto questo venerdì pomeriggio ma non ho fatto clic su Publish Now.

### [!BADGE Beta]{type=Informative}

Bob

## UGP-10565 - Evidenziazione testo

Testo prima di `<div class="preview">`

<div class="preview">

### Aggiungi campi nativi Workfront

Puoi aggiungere campi nativi di Workfront ai moduli personalizzati. Quando il modulo personalizzato viene allegato a un oggetto, il campo viene popolato dai dati dell’oggetto. Ad esempio, il campo Description (Descrizione) in un modulo personalizzato allegato a un progetto estrae la descrizione del progetto. (Il campo può mostrare &quot;N/D&quot; se non sono disponibili dati).

1. Nella parte sinistra della schermata, individua **Campo nativo** e trascinalo in una sezione dell&#39;area di lavoro.
1. Sul lato destro della schermata, configura le opzioni per il campo personalizzato:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">Etichetta</td> 
      <td> <p>(Obbligatorio) Digita un’etichetta descrittiva da visualizzare sopra il campo. Puoi modificare l’etichetta in qualsiasi momento.</p> <p><b>IMPORTANTE</b>: evitare di utilizzare caratteri speciali in questa etichetta. Non vengono visualizzati correttamente nei rapporti.</p> </td> 
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

1. Per salvare le modifiche, fai clic su **Applica** e passa a un&#39;altra sezione per continuare a creare il modulo.

   oppure

   Fare clic su **Salva e chiudi**.

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
    <td> <p>(Obbligatorio) Digita un’etichetta descrittiva da visualizzare sopra il campo personalizzato. Puoi modificare l’etichetta in qualsiasi momento. Per ulteriori informazioni, vedere <a href="https://www.adobe.com" class="MCXref xref">Aggiungere un campo personalizzato a un modulo personalizzato</a> in questo articolo.</p> <p><b>IMPORTANTE</b>: evitare di utilizzare caratteri speciali in questa etichetta. Non vengono visualizzati correttamente nei rapporti.</p> </td> 
    <td>
    <ul>
    <li>Pulsanti di scelta. Per ulteriori informazioni, vedere <a href="https://www.adobe.com">Aggiungere un campo personalizzato a un modulo personalizzato</a> in questo articolo. (Nessuna classe)</li>
    <li>Gruppo di caselle di controllo</li>
    <li>A discesa</li>
    </ul></td>
</tr> 
</tbody> 
</table>

## UGP-9176 - Vecchio bug

Il tag &quot;span&quot; non funziona correttamente in una NOTA (e un elenco)

Per informazioni sulle funzionalità disponibili nella nuova esperienza di commento e sugli oggetti, vedere [Nuova esperienza di commento](note-test.md).

1. Passare all&#39;oggetto a cui si desidera aggiungere una risposta.
1. Fai clic su **Aggiornamenti**, quindi fai clic sulla scheda **Commenti** per l&#39;oggetto e trova il commento o la risposta a cui desideri rispondere

   Oppure

   <span class="preview">Fare clic sulla scheda **Tutti**, quindi fare clic su **Rispondi in commenti** per aprire il commento nella scheda Commenti e rispondervi. Impossibile rispondere nella scheda Tutti.</span>

1. (Facoltativo) Per includere nella risposta il testo di un aggiornamento precedente, fai clic sul menu **Altro** nell&#39;angolo superiore destro del commento a cui desideri rispondere, quindi fai clic su **Risposta preventivo**. Il testo dell&#39;aggiornamento precedente viene visualizzato nell&#39;area di input, contrassegnato da una linea grigia verticale.
1. Fai clic su **Risposta**.

   ![](assets/package.png)

   Nella parte inferiore della casella **Aggiungi risposta...** è possibile visualizzare gli utenti coinvolti attivamente nella conversazione e aggiungerne altri o rimuovere quelli non più rilevanti. Questi utenti, insieme a tutti gli utenti abbonati all’oggetto, ricevono una notifica ogni volta che viene effettuato un aggiornamento o una risposta sull’oggetto. Puoi anche assegnare tag a più utenti per includerli nella risposta.  Per assegnare tag ad altri utenti, vedere [Assegnare tag ad altri utenti negli aggiornamenti](note-test.md).

   >[!TIP]
   >
   >   Per aggiungere altre risposte a una risposta esistente, puoi iniziare a digitare nella casella **Aggiungi risposta ...** oppure fare clic su **Rispondi** nel commento originale. La risposta viene aggiunta alla fine del thread.

1. Inizia a digitare la risposta e utilizza eventuali opzioni aggiuntive dalla barra degli strumenti Testo formattato. Per informazioni sull&#39;utilizzo di Rich Text o di altre funzionalità di aggiornamento, vedere [Aggiorna lavoro](note-test.md).

1. Fai clic su **Invia** per salvare la risposta.

1. (Facoltativo) Fai clic sul menu **Altro** nell&#39;angolo superiore destro del commento a cui desideri rispondere per altre opzioni di gestione della risposta. Per ulteriori informazioni, vedere [Aggiorna lavoro](note-test.md).


## UGP-10614 - Tabelle dei problemi con le immagini

Il parametro `{width="20"}` causa problemi nelle tabelle.

## Confronto tra i piani di successo Expert e Ultimate

|  | Piano di successo Expert | Piano di successo Ultimate |
|--- |--- |--- |
|  | Con il piano di successo Expert, puoi accedere all’**assistenza di esperti 24 ore su 24, 7 giorni su 7** per la risoluzione dei problemi tecnici e indicazioni sui problemi aziendali critici. Oppure puoi trovare soluzioni rapide attingendo alle nostre risorse autonome, alle best practice esclusive e a una community online di esperti e colleghi di Adobe. <p> *Incluso con tutte le licenze di Adobe Experience Cloud.* | Con il piano di successo Ultimate, potrai contare su un’**assistenza strategica e tecnica proattiva per fornire esperienze digitali ad alte prestazioni**. L’ambiente di Adobe sarà supportato da un team di esperti che ha familiarità con la tua azienda e si concentrerà sull’esecuzione di una roadmap in linea con gli obiettivi e le priorità per l’impatto aziendale. |
| **Team di successo** | Gruppo di team di tecnici del supporto | Include: <ul><li> Technical Account Manager designato </li><li> Customer Success Manager designato </li><li> Support Services Manager designato</li><li> Gruppo di team di tecnici ed esperti strategici che forniscono acceleratori per il successo </li><li> Gruppo di team di tecnici del supporto </li></ul> |
| **Supporto proattivo tecnico e operativo** | ![icona non incluso](../assets/Cross_red_circle.svg){width="20"} Non incluso | Include: <ul><li>Aggiornamento e valutazione della migrazione, preparazione delle versioni </li><li>Valutazione della roadmap dei prodotti</li><li> Roadmap tecniche e strategiche allineate</li><li>Preparazione e pianificazione degli eventi chiave</li><li>Pianificazione dell’abilitazione pertinente e tempestiva</li><li>Best practice tecniche e linee guida del settore</li><li>Sostegno/allineamento con i team di prodotto</li><li>Piano unificato per il raggiungimento dei principali obiettivi aziendali: piano d’azione reciproco (MAP)</li></ul> |
| **Supporto tecnico** | Include: <ul><li>**P1**: supporto per problemi 24 ore su 24, 7 giorni su 7</li><li>**P2, P3, P4**: supporto nell’orario di lavoro</li><li>Gestione delle interruzioni standard</li><li>Gestione di gruppi di escalation</li></ul> | Include: <ul><li>**P1**: supporto dei problemi 24 ore su 24, 7 giorni su 7</li><li>**P2/P3**: supporto dei problemi 24 ore su 24, 5 giorni su 7</li><li>**P4**: supporto nell’orario di lavoro</li><li>Gestione delle interruzioni con priorità</li><li>Gestione dell’escalation da parte di esperti dedicati</li></ul> |
| **Acceleratori per il successo** | ![icona non incluso](../assets/Cross_red_circle.svg){width="20"} Non incluso | Acceleratori per il successo pianificati regolarmente dal TAM e dal CSM<p>*(per ulteriori informazioni, consulta il Catalogo acceleratori per il successo)* |
| **Canali di supporto** | Online, telefono, Experience League, forum | Portale online personalizzato, supporto telefonico con priorità, Experience League, forum |

{style="table-layout:fixed"}

## Componenti aggiuntivi di supporto

| Componenti aggiuntivi | Piano di successo Expert | Piano di successo Ultimate |
|--- |--- |--- |
| **Componente aggiuntivo Gestione eventi**<br> Offre guida e supporto end-to-end necessari per gestire l’intero ciclo di vita degli eventi chiave | ![icona disponibile](../assets/Plus_blue.svg){width="20"} Disponibile | ![icona disponibile](../assets/Plus_blue.svg){width="20"} Disponibile |
| **Componente aggiuntivo Direttore tecnico dell’account**<br> La risorsa tecnica principale che fornisce supervisione sulla leadership, è responsabile del coinvolgimento dei dirigenti e garantisce la governance per massimizzare i risultati aziendali | ![icona non disponibile](../assets/Cross_red_circle.svg){width="20"} Non disponibile | ![icona disponibile](../assets/Plus_blue.svg){width="20"} Disponibile |
| **Componente aggiuntivo Supporto cloud avanzato**<br> Assistenza e garanzia del valore di massimo livello per i clienti di Adobe Experience Manager as a Cloud Service | ![icona disponibile](../assets/Plus_blue.svg){width="20"} Disponibile | ![icona disponibile](../assets/Plus_blue.svg){width="20"} Disponibile |
| **Componente aggiuntivo Sessioni tutor**<br> Fornisce apprendimento basato sulle abilità in un metodo di formazione just-in-time | ![icona disponibile](../assets/Plus_blue.svg){width="20"} Disponibile | ![icona disponibile](../assets/green_checkmark.svg){width="20"} Inclusa |
| **Componente aggiuntivo Developer Boost**<br> Fornisce agli esperti tecnici l’accesso sul campo per fornire assistenza per il break-fix | ![icona disponibile](../assets/Plus_blue.svg){width="20"} Disponibile | ![icona incluso](../assets/green_checkmark.svg){width="20"} Incluso |
| **Pacchetto componente aggiuntivo coda di priorità**<br> Salta la coda per far sì che i tuoi biglietti siano i primi con accesso aggiuntivo a Sessioni tutor e Developer Boost | ![icona disponibile](../assets/Plus_blue.svg){width="20"} Disponibile | ![icona incluso](../assets/green_checkmark.svg){width="20"} Incluso |

{style="table-layout:fixed"}
