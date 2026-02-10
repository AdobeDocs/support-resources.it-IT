---
title: Come includere un membro del team nelle notifiche di supporto
description: Questo articolo spiega come includere un membro del team nelle notifiche di supporto.
feature: Cloud, Support, Admin Workspace
role: Admin, Developer
solution: Commerce
feature-set: Commerce
source-git-commit: 3d2865871a355ff70d146bb83780f7b92fd8f677
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 10%

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
1. Verificare se il membro del team è stato aggiunto al progetto ed è un [!DNL Super User].

Se non sono stati aggiunti al progetto, dovrai aggiungerli come [!DNL Super User] e concedere [!DNL Shared Access]:

* [Gestire l&#39;accesso utente](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) nella guida utente.
* [Impossibile aggiungere l&#39;utente al progetto cloud Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-add-user-adobe-commerce-cloud-project.html?lang=it) nella Knowledge Base di Commerce.
* [Guida utente di Adobe Commerce Help Center: accesso condiviso](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#shared-access) nella Knowledge Base di Commerce.

Se sono stati aggiunti a [!DNL cloud project], ma non dispongono di [!DNL Super User role], aggiorna di conseguenza [!DNL role] in [Gestisci accesso utente](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html).

Se desideri consentire a un membro del team di essere un osservatore in tutti i casi aperti per la tua organizzazione, invia un [ticket di supporto](https://experienceleague.adobe.com/home?lang=en&support-tab=home#support).

## Lettura correlata

[Gli ex membri del team ricevono le e-mail di notifica cloud di Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails.html)