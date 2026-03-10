---
title: Avviso di fine del supporto di MySQL e istruzioni sulla compatibilità del database per Adobe Commerce
description: Questo articolo fornisce informazioni sulle timeline di fine del supporto di MySQL e indicazioni sulla compatibilità del database per le versioni di Adobe Commerce supportate.
solution: Commerce
source-git-commit: 2198e1882260ca17b8b99f7ed6d415791ec0d177
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Avviso di fine del supporto di MySQL e istruzioni sulla compatibilità del database per Adobe Commerce

Questo articolo fornisce informazioni importanti sulla fine del supporto di MySQL (EOS) e sulla compatibilità del database per le versioni di Adobe Commerce supportate.
Adobe consiglia vivamente ai commercianti di rivedere questo annuncio e adottare misure per mantenere la stabilità della piattaforma e rimanere in conformità con i requisiti di supporto.
Ulteriori informazioni sono disponibili in [Prerequisiti per l&#39;aggiornamento di MariaDB](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/maintenance/mariadb-upgrade) e [Requisiti di sistema](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/system-requirements).

## Fine del supporto di MySQL 8.0 (EOS)

MySQL 8.0 raggiunge la fine del supporto (EOS) il 30 aprile 2026.
Dopo questa data, le seguenti versioni di Adobe Commerce non supporteranno o manterranno la compatibilità con le versioni di MySQL rilasciate dopo MySQL 8.0:

* Adobe Commerce 2.4.7
* Adobe Commerce 2.4.6
* Adobe Commerce 2.4.5

Adobe non convalida o fornisce supporto per le versioni principali di MySQL più recenti in queste versioni di Adobe Commerce.

## Azione richiesta per i clienti on-premise

Si consiglia vivamente alle installazioni Adobe Commerce on-premise in esecuzione nelle seguenti versioni di migrare i server di database a una versione MariaDB compatibile:

* 2.4.5.
* 2.4.6.
* 2.4.7.

MariaDB è completamente supportato per queste versioni ed è la piattaforma di database consigliata per il futuro.

* 2.4.5.
* 2.4.6.
* 2.4.7.

Si consiglia vivamente di migrare i server di database a una versione compatibile di MariaDB.
MariaDB è completamente supportato per queste versioni di Adobe Commerce ed è la piattaforma di database consigliata.

## Supporto di MySQL in Adobe Commerce 2.4.8 e 2.4.9

Adobe Commerce 2.4.8 e 2.4.9 sono le ultime versioni di Adobe Commerce che supportano MySQL.

Per queste versioni:
* MySQL 8.4 è la versione finale di MySQL supportata da Adobe Commerce.
* Nessuna versione MySQL rilasciata dopo la versione 8.4 sarà certificata o supportata in Adobe Commerce.

## Direzione futura: MariaDB come piattaforma di database predefinita

In futuro, Adobe Commerce continuerà a supportare MariaDB come piattaforma di database predefinita e consigliata.

Adobe consiglia vivamente ai seguenti clienti di iniziare a pianificare la migrazione a MariaDB per mantenere la compatibilità a lungo termine e l’allineamento del supporto:
* Tutti i clienti Adobe Commerce 2.4.8 e 2.4.9 on-premise
* Clienti che eseguono versioni precedenti supportate di Adobe Commerce
