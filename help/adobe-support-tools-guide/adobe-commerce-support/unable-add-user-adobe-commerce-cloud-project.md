---
title: Impossibile aggiungere l’utente al progetto cloud Adobe Commerce
description: Questo articolo fornisce una soluzione per i casi in cui non è possibile aggiungere un utente a un progetto cloud di Adobe Commerce.
feature: Cloud, Paas
solution: Commerce
feature-set: Commerce
role: Developer
source-git-commit: dfb3e7ea8638755cdff16b0765125403f429ef2e
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---

# Impossibile aggiungere l’utente al progetto cloud Adobe Commerce

Questo articolo fornisce una soluzione per quando si tenta di aggiungere un utente a un progetto cloud, ma non riesce e viene visualizzato un errore: *L&#39;utente XXX non esiste*.

## Prodotti e versioni interessati

* Adobe Commerce sull&#39;infrastruttura cloud, [tutte le versioni supportate](https://magento.com/sites/default/files/magento-software-lifecycle-policy.pdf)

## Problema

Questo articolo fornisce una soluzione per i casi in cui non è possibile aggiungere un utente a un progetto cloud di Adobe Commerce.

## Causa

L&#39;account dell&#39;utente deve essere creato all&#39;indirizzo [https://accounts.magento.cloud](https://accounts.magento.cloud) e collegato al relativo SSO Adobe prima di poter essere aggiunto come utente al progetto. Se l’utente dispone di un account Adobe ma non di un account Commerce (magento.com), deve prima crearne uno.

## Soluzione

1. Chiedi all&#39;utente di accedere a [https://accounts.magento.cloud](https://accounts.magento.cloud). L’utente deve già essere registrato con Adobe utilizzando lo stesso indirizzo e-mail.
   > **NOTA**\
   > La creazione o l&#39;utilizzo di un account in [https://account.adobe.com](https://account.adobe.com) non implica automaticamente che l&#39;utente disponga di un account in [https://accounts.magento.cloud](https://accounts.magento.cloud). L&#39;utente deve prima [creare il proprio account Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).

1. Se l&#39;utente dispone già di un account Adobe ma non è in grado di accedere, chiedere di inviare una [richiesta di supporto](https://experienceleague.adobe.com/home#support) con [!UICONTROL Motivo del problema] impostato su *Gestione utenti*.

1. Dopo che l&#39;utente ha effettuato l&#39;accesso a [https://accounts.magento.cloud](https://accounts.magento.cloud), è possibile aggiungerlo al progetto. Per i passaggi dettagliati, consulta [Aggiungere utenti e gestire l&#39;accesso](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access#add-users-and-manage-access) nella Guida all&#39;infrastruttura cloud di Commerce.

## Lettura correlata:

* [Gestire l&#39;accesso degli utenti](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) nella Guida all&#39;infrastruttura di Commerce su Cloud.
* [Impossibile accedere al supporto Adobe Commerce o all&#39;account cloud](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-to-log-in-to-support-or-cloud-project.html)