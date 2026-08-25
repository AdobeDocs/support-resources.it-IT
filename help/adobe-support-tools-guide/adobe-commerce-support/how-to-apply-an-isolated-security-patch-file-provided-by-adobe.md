---
title: Come applicare una patch isolata fornita da Adobe
description: Questo articolo spiega come applicare una patch isolata per Adobe Commerce on-premise, Adobe Commerce on Cloud Infrastructure e Magento Open Source.
feature: Best Practices, Compliance, Console
solution: Commerce
feature-set: Commerce
autotag-review: '2026-08-19T13:22:21.768Z'
TQID: 'https://experienceleague.adobe.com/tmaNqB6uOX2ukmfxQvcqFvYwm2UyO6USzb7t8hFQM1A'
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
source-git-commit: 45b00b9b0d2ceb422747c0a4a34f060f33ab127b
workflow-type: tm+mt
source-wordcount: 219
ht-degree: 0%

---

# Come applicare una patch isolata fornita da Adobe

Questo articolo spiega come applicare una patch isolata per Adobe Commerce on-premise, Adobe Commerce on Cloud Infrastructure e Magento Open Source.

>[!WARNING]
>
>Si consiglia vivamente di applicare e testare la patch nell’ambiente di staging/integrazione prima di applicarla alla produzione. Consigliamo inoltre di avere un backup recente prima di qualsiasi manipolazione.

## Come applicare una patch isolata per l’infrastruttura Adobe Commerce on Cloud {#cloud}

1. Se nella directory principale del progetto non è presente una directory denominata `m2-hotfixes`, crearne una.
1. Copiare i file `%patch_name%.patch` nella directory `m2-hotfixes`.
1. Aggiungi, esegui il commit e invia le modifiche al codice:

   ```git
   git add -A
   ```

   ```git
   git commit -m "Apply %patch_name%.patch patch"
   ```

   ```git
   git push origin
   ```

Per ulteriori informazioni sull&#39;applicazione di patch ai progetti Cloud, vedere [Applicare patch](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/upgrade/apply-patches).

## Come applicare una patch isolata per Adobe Commerce on-premise e Magento Open Source {#commerce}

1. Carica la patch nella directory principale di Adobe Commerce on-premise o Magento Open Source.
1. Esegui il seguente comando SSH:

   ```bash
   patch -p1 < %patch_name%.patch
   ```

   Se il comando precedente non funziona, provare a utilizzare `-p2` anziché `-p1`

1. Affinché le modifiche vengano applicate, aggiorna la cache in [!UICONTROL Admin] in **[!UICONTROL System]** > **[!UICONTROL Cache Management]**.
