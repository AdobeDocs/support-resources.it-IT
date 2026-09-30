---
title: Monitoraggio e osservabilità
description: Consigli di monitoraggio e osservabilità per aiutare i commercianti di Adobe Commerce a preparare i loro ambienti per eventi a traffico elevato, come le feste.
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: 4239b8a6-e74f-567d-a7a5-b98b9ead0ea4
    internal-label: Observability
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: 3c398179-d35a-51ba-b317-6c5b95feef5e
    internal-label: Logs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 71589dd124714805fbf844540fb2d272433631ee
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 2%
---

# Monitoraggio e osservabilità

Questa sezione fornisce consigli tecnici per il monitoraggio degli ambienti Adobe Commerce in preparazione ad eventi con traffico elevato, come le feste.

>[!NOTE]
>
>I passaggi contrassegnati come **(solo cloud)** si applicano a Commerce sull&#39;infrastruttura cloud. La maggior parte delle altre raccomandazioni si applica anche alle distribuzioni locali.

## Monitorare il traffico con New Relic (solo cloud) {#monitor-traffic-with-new-relic}

Adobe Commerce su infrastruttura cloud include un abbonamento alla piattaforma di osservabilità [!DNL New Relic], che incorpora perfettamente [!DNL Fastly] registri in streaming in [!DNL New Relic] quasi in tempo reale. Questa integrazione ti consente di monitorare i pattern e le tendenze del traffico in tempo reale, in modo da poter intraprendere azioni correttive.

Utilizza questi registri per:

* Identifica i paesi da cui provengono le tue richieste web.
* Trova indirizzi IP o agenti utente abusivi che scansionano il tuo sito.
* Identifica il traffico dannoso che esegue il targeting di endpoint specifici, ad esempio il pagamento.
* Crea rapporti sui tipi di dispositivi e browser utilizzati dai clienti.

Ad esempio, monitora il paese di origine del traffico per confermare che rifletta le posizioni geografiche delle promozioni e dei clienti:

```sql
SELECT count(*) FROM Log
WHERE cache_status IS NOT NULL
AND project_id = '<YOUR_PROJECT_ID>'
AND (content_type LIKE 'text/html;%' or url LIKE '%graphql%' or url like '%rest%')
FACET geo_country_code
SINCE 7 days ago until today
```

Modifica questa query in base alle tue esigenze, segmentala ulteriormente o trasformala in una dashboard per il tracciamento centralizzato. Per ulteriori dettagli, vedere [Gestione registro di New Relic](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/monitor/new-relic/log-management).

## Personalizzare gli avvisi di New Relic (solo Cloud) {#customize-new-relic-alerts}

Oltre agli avvisi gestiti impostati da Adobe Commerce sull’infrastruttura cloud, puoi impostare un’ampia gamma di avvisi e notifiche per la tua piattaforma durante la stagione di vendita di picco, ad esempio, per notificare il traffico da bot o un aumento dei tempi di risposta su una query GraphQL. Per l&#39;elenco completo degli avvisi incorporati, vedere [Avvisi gestiti per Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/tools/managed-alerts-for-adobe-commerce/managed-alerts-for-magento-commerce).

[!DNL New Relic] avvisi e IA supportano strutture di query basate su NRQL. Impostare avvisi personalizzati dal dashboard [!DNL New Relic] in **[!UICONTROL Avvisi e IA]**.

## Rivedi punteggio Apdex (solo Cloud) {#review-apdex-score}

Il punteggio Apdex misura la soddisfazione degli utenti in relazione ai tempi di risposta delle applicazioni e dei servizi web. Puoi rivedere il punteggio Apdex del tuo Adobe Commerce sull&#39;infrastruttura cloud utilizzando [!DNL New Relic].

Un punteggio Apdex va da 0 a 1. Un punteggio pari a 0 rappresenta il punteggio peggiore possibile, ovvero il 100% dei tempi di risposta è stato **frustrato**. Un punteggio pari a 1 rappresenta il miglior punteggio possibile, ovvero il 100% dei tempi di risposta è stato **soddisfatto**. [!DNL New Relic] riporta sia un punteggio di App Server, che riflette le prestazioni del back-end, che un punteggio di Utente finale, che riflette le prestazioni lato client.

Un punteggio Apdex di 0,5 o inferiore garantisce un&#39;indagine. Un punteggio inferiore a 0,4 è considerato un’interruzione.

Insieme ad Apdex, [!DNL New Relic] fornisce una serie di statistiche per analizzare i problemi di prestazioni in Adobe Commerce sull&#39;infrastruttura cloud. Per i passaggi, consulta [Risoluzione dei problemi relativi alle prestazioni con New Relic su Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/troubleshoot-performance-using-new-relic-on-magento-commerce).

## Rivedere le informazioni sul supporto (rapporto SWAT) {#review-support-insights-swat-report}

Per un rapporto più dettagliato sull’ambiente, genera un rapporto Site-Wide Analysis Tool (SWAT) (Strumento di analisi a livello di sito). Per ulteriori informazioni sullo strumento SWAT, vedere [Strumento di analisi a livello di sito](https://experienceleague.adobe.com/it/docs/commerce-operations/tools/site-wide-analysis-tool/intro).