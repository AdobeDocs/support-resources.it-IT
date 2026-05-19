---
title: Come includere un membro del team nelle notifiche di supporto
description: Questo articolo spiega come includere un membro del team nelle notifiche di supporto.
feature: Cloud, Support, Admin Workspace
role: Admin, Developer
solution: Commerce
feature-set: Commerce
exl-id: 392ef795-f710-401f-8b0e-3c8dfec7bb3a
TQID: 'https://experienceleague.adobe.com/fWRfvDT8NCwPfzmAx1Zowo4T8KvKLKWqhDkZDfX8stU'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: e7dae43f-215c-4cdf-90d3-c5a461a6e669
subfeature_v2:
  - id: bb2df8be-afdd-4818-b6b5-95ca1dd3bc3a
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9f1760d31cd80e0358aa341c3f6091b2a86b6d67
workflow-type: tm+mt
source-wordcount: 305
ht-degree: 12%

---


# Come includere un membro del team nelle notifiche di supporto

Questo articolo spiega come includere un membro del team per ricevere automaticamente gli aggiornamenti di supporto tramite notifiche via e-mail.

## Prodotti e versioni interessati

* Adobe Commerce sull&#39;infrastruttura cloud, tutte le [versioni supportate](https://www.adobe.com/content/dam/cc/en/legal/terms/enterprise/pdfs/Adobe-Commerce-Software-Lifecycle-Policy.pdf).

## Causa

* Il membro del team non è stato aggiunto a [!DNL cloud project] con i privilegi necessari.
* Il membro del team non dispone di un account di supporto.

## Soluzione

1. Passare a **[!DNL Cloud Project URL]** (esempio: `https://us-3.magento.cloud/projects/xxxxxx/edit`).
1. Verificare se il membro del team è stato aggiunto al progetto ed è un [!DNL Project Admin].

Se non sono stati aggiunti al progetto, dovrai aggiungerli come [!DNL Project Admin] e concedere [!DNL Shared Access]:

* [Gestire l&#39;accesso utente](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=it) nella guida utente.
* [Impossibile aggiungere l&#39;utente al progetto cloud Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-add-user-adobe-commerce-cloud-project.html?lang=it) nella Knowledge Base di Commerce.
* [Guida utente di Adobe Commerce Help Center: accesso condiviso](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=it#shared-access) nella Knowledge Base di Commerce.

Se sono stati aggiunti a [!DNL cloud project], ma non dispongono di [!DNL Project Admin role], aggiorna di conseguenza [!DNL role] in [Gestisci accesso utente](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=it).

Se desideri consentire a un membro del team di essere un osservatore in tutti i casi aperti per la tua organizzazione, invia un [ticket di supporto](https://experienceleague.adobe.com/home?lang=it&support-tab=home#support).

## Lettura correlata

[Gli ex membri del gruppo ricevono le e-mail di notifica cloud di Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails.html?lang=it)
