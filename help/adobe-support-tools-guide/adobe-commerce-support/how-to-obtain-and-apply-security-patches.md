---
title: Ottenere e applicare [!UICONTROL patch di sicurezza]
description: Questo articolo fornisce istruzioni su come ottenere e applicare una [!UICONTROL patch di sicurezza] rilasciata, ma le istruzioni non sono disponibili.
source-git-commit: 93ee9bd110930e244befca682fadd3edc24d138a
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Ottenere e applicare una [!UICONTROL patch di sicurezza]

>[!NOTE]
>Se si dispone di un&#39;installazione on-premise e non si utilizzano sistemi di controllo della versione come [!DNL CVS] o GitHub per gestire il codice, l&#39;host Web potrebbe essere in grado di fornire assistenza nell&#39;applicazione della patch. Sentiti libero di contattarli per il supporto.

Questo articolo fornisce istruzioni su come ottenere e applicare una [!UICONTROL patch di sicurezza] rilasciata, ma le istruzioni non sono disponibili.

## Prodotti e versioni interessati

Infrastruttura Adobe Commerce on-premise e cloud - tutte le versioni supportate


## Causa

La maggior parte delle [!UICONTROL patch di sicurezza] viene rilasciata senza alcuna patch isolata o hotfix da applicare e richiederà l&#39;aggiornamento alla versione [!UICONTROL patch di sicurezza].

## Soluzione


### Caso I:

* Se nelle [Note sulla versione](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/release-notes/cloud-tools-suite) è menzionato un file/hotfix di patch isolato, scaricare il file dalla sezione di download di [https://account.magento.com](https://account.magento.com/downloads/view/). Agli utenti con accesso condiviso devono prima essere concessi i privilegi di download dal proprietario dell’account/titolare della licenza.

**Avvertenze:**

Se utilizzi una versione precedente di Adobe Commerce (2.4.4), avrai ricevuto automaticamente il supporto esteso. La versione deve essere una delle seguenti versioni non supportate per poter applicare le ultime patch di sicurezza disponibili:

2.4.4 - 2.4.4-p11

Le versioni non supportate (2.3.x, 2.4.0 - 2.4.3) non sono idonee per il supporto e devi prima eseguire l’aggiornamento a una versione supportata per sfruttare le ultime correzioni di sicurezza.

Se non disponi del supporto esteso, puoi richiedere al supporto di condividere le patch con te, ma non saranno in grado di risolvere eventuali problemi/errori che potresti riscontrare durante l’applicazione delle patch.

### Caso II:

Le patch isolate vengono fornite solo in casi eccezionali e non è la forma preferita per implementare correzioni di sicurezza.

Se nelle Note sulla versione non è menzionato un file patch o un hotfix isolato:

* **Cloud:**

1. Alcune [!UICONTROL patch di sicurezza] potrebbero essere incluse/rilasciate nell&#39;ultima versione di Cloud Tools Suite (Strumenti ECE) in Cloud Patches for Commerce. Controllare le [Note sulla versione](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) e, se nella versione è menzionata una correzione di sicurezza, aggiornare il pacchetto a tale versione.
1. Se le Note sulla versione non menzionano una correzione di sicurezza, continua a leggere.

* **Infrastruttura cloud o locale:**

* Se un file/hotfix di patch isolato non è disponibile, [aggiorna la versione di Adobe Commerce sull&#39;infrastruttura cloud](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) 2.4.X all&#39;ultima versione della patch 2.4.X-pY.
* Se un file/hotfix di patch isolato non è disponibile, [aggiorna la versione di Adobe Commerce On-Premise](https://experienceleague.adobe.com/en/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade) 2.4.X all&#39;ultima versione della patch 2.4.X-pY.

## Lettura correlata

* Consulta le [note sulla versione della suite di strumenti Commerce Cloud](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite) nella *Guida di Adobe Commerce sull&#39;infrastruttura cloud*.
* Consulta [Aggiornare Adobe Commerce versione](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) nella *Guida di Adobe Commerce sull&#39;infrastruttura cloud*.
