---
title: Barre nei blocchi di codice UGP-11189
description: Barre nel test UGP-11189 dei blocchi di codice
hide: true
hidefromtoc: true
source-git-commit: 4fc9b739d18941d276b88f8799163523c8bd5f85
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 4%

---

# Barra nei blocchi di codice

1. Esegui il comando:

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. Passaggio successivo

Non nel blocco di codice

vendor/bin/magento-patches -n stato |grep &quot;27015\|Stato&quot;

Barra rovesciata con escape:

vendor/bin/magento-patches -n stato |grep &quot;27015&amp;bsol;|Stato&quot;
