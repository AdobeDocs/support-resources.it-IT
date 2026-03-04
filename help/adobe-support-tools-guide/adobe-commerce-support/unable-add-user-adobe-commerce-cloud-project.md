---
title: Impossibile aggiungere l’utente al progetto cloud di Adobe Commerce
description: Questo articolo fornisce una soluzione per quando non è possibile aggiungere un utente a un progetto cloud di Adobe Commerce.
feature: Cloud, Paas
solution: Commerce
feature-set: Commerce
role: Developer
exl-id: 2dc52d5e-0930-48c4-986e-ce3f9f6f8221
source-git-commit: 755c6dc9cff041b9ca9183fbecde21f90fbaee1a
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---

# Impossibile aggiungere l’utente al progetto cloud di Adobe Commerce

Questo articolo fornisce una soluzione per quando si tenta di aggiungere un utente a un progetto cloud, ma non riesce con un errore: *L&#39;utente XXX non esiste*.

## Prodotti e versioni interessati

* Adobe Commerce sull&#39;infrastruttura cloud, [tutte le versioni supportate](https://magento.com/sites/default/files/magento-software-lifecycle-policy.pdf)

## Problema

Questo articolo fornisce una soluzione per quando non è possibile aggiungere un utente a un progetto cloud di Adobe Commerce.

## Causa

L&#39;account dell&#39;utente deve essere creato in [https://accounts.magento.cloud](https://accounts.magento.cloud) e collegato al relativo Adobe SSO prima di poter essere aggiunto come utente al progetto. Se l’utente dispone di un account Adobe ma non di un account Commerce (magento.com), deve prima crearne uno.

## Soluzione

1. Chiedi all&#39;utente di accedere all&#39;indirizzo [https://accounts.magento.cloud](https://accounts.magento.cloud). L’utente deve essere già registrato con Adobe utilizzando lo stesso indirizzo e-mail.
   >[!NOTE]
   >La creazione o l&#39;utilizzo di un account in [https://account.adobe.com](https://account.adobe.com) non implica automaticamente che l&#39;utente disponga di un account in [https://accounts.magento.cloud](https://accounts.magento.cloud). L&#39;utente deve prima [creare il proprio account Commerce](https://experienceleague.adobe.com/it/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).

1. Se l&#39;utente dispone già di un account Adobe ma non è in grado di accedere, chiedere di inviare una [richiesta di supporto](https://experienceleague.adobe.com/home?lang=it#support) con [!UICONTROL Motivo del problema] impostato su *Gestione utenti*.

1. Dopo che l&#39;utente ha eseguito correttamente l&#39;accesso a [https://accounts.magento.cloud](https://accounts.magento.cloud), puoi aggiungere l&#39;utente al progetto. Per i passaggi dettagliati, consulta [Aggiungere utenti e gestire l&#39;accesso](https://experienceleague.adobe.com/it/docs/commerce-cloud-service/user-guide/project/user-access#add-users-and-manage-access) nella Guida all&#39;infrastruttura di Commerce su cloud.

## Lettura correlata:

* [Gestire l&#39;accesso degli utenti](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=it) nella Guida all&#39;infrastruttura di Commerce su cloud.
* [Impossibile accedere al supporto Adobe Commerce o all&#39;account cloud](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-to-log-in-to-support-or-cloud-project.html?lang=it)
