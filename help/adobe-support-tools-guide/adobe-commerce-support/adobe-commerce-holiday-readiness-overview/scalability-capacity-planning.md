---
title: Scalabilità e pianificazione della capacità
description: Consigli su scalabilità e pianificazione della capacità per aiutare i commercianti di Adobe Commerce a preparare i loro ambienti per eventi a traffico elevato, come le feste.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 71589dd124714805fbf844540fb2d272433631ee
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%
---

# Scalabilità e pianificazione della capacità

Questa sezione fornisce consigli tecnici per ridimensionare gli ambienti Adobe Commerce in modo da prepararsi ad eventi con traffico elevato, come le feste.

>[!NOTE]
>
>I passaggi contrassegnati come **(solo cloud)** si applicano a Commerce sull&#39;infrastruttura cloud. La maggior parte delle altre raccomandazioni si applica anche alle distribuzioni locali.

## Pianifica l&#39;upsize del cluster in anticipo (solo per cloud) {#plan-cluster-upsize-early}

Per i clienti Commerce su infrastrutture cloud, un aumento temporaneo delle dimensioni del cluster alloca più risorse di elaborazione per gestire i picchi di traffico nella stagione di punta. Crea un ticket di supporto in anticipo con l’intervallo di date e le dimensioni richieste del cluster, quindi coordinati con l’Account Manager dedicato in merito al consumo e ai requisiti correnti delle risorse. Invia la richiesta almeno 48 ore lavorative prima che la capacità sia necessaria; per la stagione delle feste in particolare, invia il prima possibile, poiché la capacità durante il Black Friday e il Cyber Monday è limitata. Vedi [Come richiedere un upsize temporaneo](https://experienceleague.adobe.com/it/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/how-to-request-temporary-adobe-commerce-on-cloud-infrastructure-upsize).

Ad esempio, un cliente Pro-architettura con una linea di base giornaliera di 24 core (24 vCPU, 96 GB di RAM) che esegue l’upsize a 96 core per 7 giorni utilizzerebbe circa 4 volte le risorse (96 vCPU, 384 GB di RAM), un consumo incrementale di circa 504 vCPU-giorni (96×7 − 24×7).

## Schermatura di origine rapida {#fastly-origin-shielding}

Lo scopo della schermatura dell&#39;origine di Adobe Commerce [!DNL Fastly] è quello di ridurre il traffico direttamente all&#39;origine Adobe Commerce. Quando viene ricevuta una richiesta, una posizione edge [!DNL Fastly] (punto di presenza) controlla il contenuto memorizzato nella cache e lo distribuisce. Se non è memorizzato in cache, continua fino a Shield POP per verificare se è memorizzato in cache. Se il contenuto è stato precedentemente richiesto anche da un altro POP globale, verrà memorizzato in cache. Infine, se non è memorizzato nella cache del POP Shield, procederà solo al server di origine.

La schermatura dell&#39;origine [!DNL Fastly] può essere abilitata nell&#39;amministratore Adobe Commerce, nelle impostazioni di back-end della configurazione [!DNL Fastly]. Scegli una posizione di schermatura più vicina al tuo data center di origine Adobe Commerce per ottenere le migliori prestazioni. Per ulteriori dettagli, vedere [Configurare back-end e schermatura origine](https://experienceleague.adobe.com/it/docs/commerce-on-cloud/user-guide/cdn/setup-fastly/fastly-custom-cache-configuration#configure-back-ends-and-origin-shielding).

Per impostazione predefinita, la schermatura dell&#39;origine [!DNL Fastly] non è abilitata.

## Esecuzione di test di carico e failover {#conduct-load-and-failover-tests}

Eseguire test di carico e ripristino prima delle campagne principali per convalidare le configurazioni di scalabilità e i piani di rollback.