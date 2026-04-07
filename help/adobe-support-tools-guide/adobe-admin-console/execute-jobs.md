---
title: Esegui processi in sospeso
description: Scopri come eseguire i processi in sospeso in Adobe Admin Console per garantire che tutte le modifiche vengano applicate alla tua organizzazione.
exl-id: 18549d19-7985-4a45-8894-e69836ddb23c
source-git-commit: 9085108231aaa46d8417d346686c211ea48f6b81
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# Esegui processi in sospeso

Questa funzionalità si applica alle organizzazioni Enterprise che utilizzano [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/).

- Le modifiche in [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/) sono completate in due fasi:

   1. **Fase di modifica**: apporta modifiche alle organizzazioni o alloca prodotti.
   2. **Fase di esecuzione**: rivedere ed eseguire le modifiche in sospeso affinché diventino effettive.

- Per assicurarsi che tutte le modifiche apportate in [[!DNL Global Admin Console]](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html) siano implementate e abbiano effetto, selezionare la scheda **[!UICONTROL Esecuzione processo]** e procedere con l&#39;esecuzione delle modifiche in sospeso.

  Accedi a [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/).

## Persistenza e visibilità delle modifiche

### Cambia persistenza

- Puoi disconnetterti e tornare in un secondo momento senza perdere le modifiche in sospeso.
- Modifiche non eseguite:
   - Vengono eliminati dopo 30 giorni.
   - Vengono cancellati al termine della sessione, ad esempio quando la scheda del browser o la finestra viene chiusa.

> [!NOTE]
>
> Esegui tempestivamente le modifiche importanti per assicurarti che vengano applicate correttamente.

### Più amministratori e conflitti

- Due amministratori che lavorano nella stessa organizzazione:
   - Non visualizzare le rispettive modifiche non eseguite.
   - Vedi le modifiche solo dopo:
      - Esecuzione e
      - Aggiornamento della visualizzazione o accesso di nuovo.
- Le modifiche non eseguite possono entrare in conflitto con le modifiche già eseguite.

### Gestione dei conflitti

I conflitti vengono segnalati:
- Al momento dell&#39;esecuzione, oppure
- Quando i dati vengono aggiornati (ad esempio, dopo la disconnessione e il riaccesso).

## Esecuzione delle modifiche in sospeso

In qualità di amministratore globale, puoi rivedere ed eseguire le modifiche in sospeso dalla scheda **[!UICONTROL Esecuzione processo]**.

### Passaggi per eseguire le modifiche

1. Accedi a [!DNL Global Admin Console].
2. Seleziona la scheda **[!UICONTROL Esecuzione processo]** dal pannello di navigazione a sinistra.
3. Esamina le modifiche in sospeso.
4. Seleziona **[!UICONTROL Invia modifiche]** per eseguirle.

Dopo aver inviato il processo:

- Il processo entra nella coda di esecuzione.
- Lo stato è **[!UICONTROL In sospeso]** durante l&#39;esecuzione del processo.
- Adobe consiglia di eseguire un solo processo alla volta per migliorarne la prevedibilità e semplificare la risoluzione dei problemi.

> [!IMPORTANT]
>
> Se si verifica un errore durante l&#39;esecuzione, le modifiche non applicate correttamente devono essere reinserite e inviate.

### Allocazioni con tempi di esecuzione lunghi

Se l’allocazione di un prodotto richiede più di 12 ore:
- Il processo è contrassegnato come **[!UICONTROL Non riuscito]**.
- Eventuali task successivi in sospeso in quel processo non vengono eseguiti.

![processi in sospeso](assets/pending-jobs.png)

## Annullare un processo in esecuzione

È possibile annullare un processo attualmente in esecuzione dalla scheda **[!UICONTROL Esecuzione processo]**.

### Passaggi per annullare un processo in esecuzione

1. Accedi a [!DNL Global Admin Console].
2. Selezionare **[!UICONTROL Esecuzione processo]**.
3. Selezionare **[!UICONTROL Annulla processo in esecuzione]**.

### Comportamento di annullamento

1. Il processo viene interrotto alla fine del passaggio corrente.
2. Il processo non si arresta nel mezzo di un passaggio.
3. Alcuni passaggi possono richiedere minuti o ore.
4. Durante questo periodo, il processo potrebbe rimanere nello stato **[!UICONTROL Annullamento]**.

> [!NOTE]
>
> Pianificare gli annullamenti con la consapevolezza che il completamento del passaggio corrente può ritardare significativamente quando l&#39;OdL si interrompe.

## Visualizza cronologia processo

- Per visualizzare i processi eseguiti negli ultimi 30 giorni:

   1. Accedi a [!DNL Global Admin Console].
   2. Selezionare **[!UICONTROL Esecuzione processo]**.
   3. Scorri fino alla parte inferiore della pagina.
   4. Seleziona **[!UICONTROL Processi recenti]**.

- Visualizzazione processi recenti:
   - **comandi processo** inviati.
   - **Errori** e **avvisi** associati all&#39;esecuzione.

> [!NOTE]
>
> Le successive ridenominazioni o eliminazioni degli oggetti correlati **non influiscono** sulla visualizzazione dei comandi nella cronologia dei processi. La cronologia riflette lo stato al momento della sottomissione.
