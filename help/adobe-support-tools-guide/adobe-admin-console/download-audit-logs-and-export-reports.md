---
title: Scaricare i registri di audit ed esportare i rapporti
description: Scopri come gli amministratori globali visualizzano, filtrano ed esportano i registri e i rapporti di controllo in Global Admin Console.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 4b562a4d-14e5-4687-a1ae-6a435f087627
source-git-commit: 7211d382c6cfba6070c8c3203956a1193f64ffbe
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 2%

---

# Scaricare i registri di audit ed esportare i rapporti

Applicabile all&#39;azienda.

Scopri in che modo gli amministratori globali visualizzano, filtrano ed esportano i registri e i rapporti di controllo utilizzando Global Admin Console.

Per iniziare, accedi a [Global Admin Console](https://global-admin-console.adobe.com/). Quindi vai alla scheda **[!UICONTROL Approfondimenti]** e seleziona **[!UICONTROL Registri di controllo]** per tenere traccia di tutte le modifiche apportate nelle organizzazioni.

## Visualizzare e scaricare i registri di audit

In qualità di amministratore globale, hai piena visibilità delle modifiche apportate in Global Admin Console. Puoi cercare nei registri di controllo di tutte le organizzazioni le azioni intraprese negli ultimi 90 giorni, compreso quando si sono verificate e chi le ha eseguite.
- I registri di audit garantiscono la conformità continua proteggendo il sistema da accessi inappropriati e controllando comportamenti sospetti all’interno dell’organizzazione.
- I registri disponibili in Global Admin Console includono solo gli eventi a cui un amministratore globale può accedere. Non includono assegnazioni utente o eventi utente. [Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview) sulle diverse funzionalità offerte da ciascuna console.
- I registri coprono gli eventi per tutte le organizzazioni nella gerarchia, consentendo di cercare i registri di audit in tutte le organizzazioni contemporaneamente.

>[!NOTE]
>
> In qualità di amministratore di sistema in un&#39;organizzazione [Adobe Admin Console](https://adminconsole.adobe.com), puoi utilizzare il [Registro di controllo](https://helpx.adobe.com/enterprise/using/audit-logs.html) per rivedere le assegnazioni utente e gli eventi utente. Nei registri di audit vengono incluse anche le azioni eseguite dagli amministratori di sistema nelle organizzazioni figlie dell’organizzazione selezionata. Scopri come gli amministratori di sistema possono [tenere traccia delle modifiche](https://helpx.adobe.com/enterprise/using/audit-logs.html) apportate in Admin Console.

Per visualizzare o scaricare i registri di audit per la tua organizzazione:

1. Come amministratore globale, accedi a [Global Admin Console](https://global-admin-console.adobe.com/insights).
1. Seleziona **[!UICONTROL Informazioni]** > **[!UICONTROL Registri di controllo]**.

I registri di audit mostrano le seguenti informazioni per gli eventi filtrati:

| Campo | Descrizione |
|------ |-------------|
| Data | Data e ora dell’evento, visualizzate nel fuso orario locale. |
| Nome evento | Descrizione dell’azione eseguita. |
| Dettagli evento | Dettagli aggiuntivi dell’evento, se disponibili. |
| Nome oggetto | Nome del prodotto, profilo di prodotto o gruppo di utenti coinvolti nell’evento, a seconda dei casi. |
| Utente interessato | Indirizzo e-mail dell’utente interessato, se applicabile. |
| Amministrazione | Indirizzo e-mail dell’amministratore che ha eseguito l’azione. *System* viene visualizzato se l&#39;azione è stata eseguita da un sistema back-end di Adobe. |
| Indirizzo IP | Indirizzo IP del computer in cui è stata eseguita l’azione. Questo di solito riflette la posizione fisica, ma può essere un server proxy o un indirizzo VPN. |
| Organizzazione | Nome dell’organizzazione interessata dall’evento. |

1. Puoi filtrare i registri di audit utilizzando le seguenti opzioni:

   - Cerca per utente o amministratore interessato.
   - Seleziona una o più organizzazioni.
   - Definisci un intervallo di date.
   - Filtra per nome evento.
   - Combina i filtri per limitare i risultati, ad esempio la visualizzazione degli eventi degli ultimi sette giorni per un’organizzazione specifica.

   ![registri di controllo](assets/audit-logs.png)

   *Filtrare i registri di audit in base al nome dell&#39;evento, all&#39;organizzazione interessata o all&#39;intervallo di date.*

   ![select-organization](assets/select-organizations.png)

   *Selezionare le organizzazioni per filtrare i registri di controllo.*

1. Per esportare i registri di controllo, selezionare **[!UICONTROL Esporta CSV]** per esportare i risultati filtrati. I risultati vengono scaricati in formato CSV.

Per informazioni dettagliate sui campi inclusi nell&#39;esportazione, vedere [Schema registro](#log-schema).

>[!NOTE]
>
>I rapporti dei registri di controllo esportati vengono conservati per 90 giorni dopo la loro generazione.


## Comprendere il rapporto del registro di controllo {#log-schema}

Il rapporto del registro di controllo esportato include i campi seguenti per ogni organizzazione:

| Campo | Descrizione |
|------|------------|
| ID | ID evento |
| eventTime | Data e ora dell’evento (fuso orario locale) |
| eventType | Nome dell’evento |
| eventSubType | Dettagli aggiuntivi dell’evento, se disponibili |
| actorEmail | Indirizzo e-mail dell’amministratore che ha eseguito l’evento. *System* viene visualizzato se l&#39;evento è stato eseguito da un sistema back-end di Adobe. |
| targetUserEmail | E-mail dell’utente interessato, se applicabile |
| targetGroupName | Gruppo di utenti interessato, se applicabile |
| targetProductName | Prodotto interessato, se applicabile |
| targetProfileName | Profilo di prodotto interessato, se applicabile |
| ipAddress | Indirizzo IP del computer in cui è stata eseguita l’azione. Di solito riflette la posizione fisica, ma potrebbe essere un server proxy o un indirizzo VPN. |
| organizationName | Nome dell’organizzazione interessata |

## Scaricare i rapporti di esportazione

Quando un amministratore globale esporta i dati dell&#39;organizzazione da [Global Admin Console](https://global-admin-console.adobe.com/insights), il report viene elaborato e reso disponibile nella scheda **[!UICONTROL Insights]** in **[!UICONTROL Esporta report]**.

Tutti i rapporti generati da qualsiasi amministratore globale sono disponibili in un’unica posizione. La funzionalità di esportazione di rapporti è utile nei seguenti scenari:

- Se si dispone di una gerarchia di grandi dimensioni con molte organizzazioni, non è più necessario attendere l&#39;elaborazione del file di esportazione. Puoi utilizzare i rapporti generati dai tuoi colleghi amministratori.
- Non è più necessario conservare o salvare questi rapporti per confrontarli in un secondo momento. I rapporti vengono conservati per 90 giorni e puoi scaricarli in qualsiasi momento per confrontarli.


Per scaricare un rapporto di esportazione:

1. Accedi a [Global Admin Console](https://global-admin-console.adobe.com/insights) e passa a **[!UICONTROL Insights]** > **[!UICONTROL Esporta report]**.

   Vengono visualizzati i rapporti generati negli ultimi 90 giorni. Dopo 90 giorni, puoi generare nuovamente il rapporto. Scopri come generare rapporti per [la struttura dell&#39;organizzazione](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/export-or-import-organization-structure-and-product-allocations#export-the-organization-structure).


   | Campo | Descrizione |
   |------|------------|
   | Rapporto | Data e ora di generazione del rapporto (fuso orario locale) |
   | Formato | Formato file (CSV, JSON, XLSX) |
   | Dimensione | Dimensione file |
   | Creato da | Indirizzo e-mail dell’amministratore che ha generato il rapporto |
   | Azione | Collegamento per scaricare il report |

1. Per scaricare un report, selezionare **[!UICONTROL Scarica]**.

   Se il report appena generato non è presente nell&#39;elenco, selezionare **[!UICONTROL Aggiorna]**.

   ![export-reports](assets/export-reports.png)

*Scarica qualsiasi rapporto generato negli ultimi 90 giorni.*
