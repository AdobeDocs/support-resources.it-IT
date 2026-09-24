---
title: Impossibile aggiungere l’utente al progetto cloud Adobe Commerce
description: Questo articolo fornisce una soluzione per i casi in cui non è possibile aggiungere un utente a un progetto cloud di Adobe Commerce.
feature: Cloud, Paas
solution: Commerce
feature-set: Commerce
role: Developer
exl-id: 2dc52d5e-0930-48c4-986e-ce3f9f6f8221
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: 00451af3-7b97-5414-9992-3a6c269e413f
    internal-label: Paas
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: a4ba265c36bd4ba6c7c563879834f2c59fdc58a4
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%
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
   >[!NOTE]
   >La creazione o l&#39;utilizzo di un account in [https://account.adobe.com](https://account.adobe.com) non implica automaticamente che l&#39;utente disponga di un account in [https://accounts.magento.cloud](https://accounts.magento.cloud). L&#39;utente deve prima [creare il proprio account Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).

1. Se l&#39;utente dispone già di un account Adobe ma non è in grado di accedere, chiedere di inviare una [richiesta di supporto](https://experienceleague.adobe.com/home#support) con [!UICONTROL Motivo del problema] impostato su *Gestione utenti*.

1. Dopo che l&#39;utente ha effettuato l&#39;accesso a [https://accounts.magento.cloud](https://accounts.magento.cloud), è possibile aggiungerlo al progetto. Per i passaggi dettagliati, consulta [Aggiungere utenti e gestire l&#39;accesso](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access#add-users-and-manage-access) nella Guida all&#39;infrastruttura cloud di Commerce.

## Lettura correlata:

* [Gestire l&#39;accesso degli utenti](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) nella Guida all&#39;infrastruttura di Commerce su Cloud.
* [Impossibile accedere al supporto Adobe Commerce o all’account cloud](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-to-log-in-to-support-or-cloud-project.html)
