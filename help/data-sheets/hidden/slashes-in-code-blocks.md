---
title: Barre nei blocchi di codice UGP-11189
description: Barre nel test UGP-11189 dei blocchi di codice
hide: true
hidefromtoc: true
source-git-commit: 2255dad674f1b4d456ffb50ebec9313bc4b3d7f5
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 0%

---

# Barra nei blocchi di codice

1. Esegui il comando:

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. Esegui il comando (con escape):

   ```bash
   vendor/bin/magento-patches -n status |grep "27015&bsol;|Status"
   ```

Non nel blocco di codice

vendor/bin/magento-patches -n stato |grep &quot;27015\|Stato&quot;

Con escape:

vendor/bin/magento-patches -n stato |grep &quot;27015&amp;bsol;|Stato&quot;

