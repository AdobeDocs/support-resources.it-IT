---
title: Migrare gli utenti esistenti a Adobe Admin Console
description: Linee guida per le organizzazioni che utilizzano licenze di abbonamento Adobe e devono eseguire la migrazione degli utenti esistenti in Admin Console a un diverso programma di acquisto o tipo di licenza.
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 42ab19551ba5c70712245236ffc7daf687486fb2
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---

# Migrare gli utenti esistenti a Adobe Admin Console

Applicabile alle aziende e ai team.

Questo documento è destinato alle organizzazioni con licenze Creative Cloud, Document Cloud e Acrobat esistenti tramite un abbonamento a Enterprise Term License Agreement (ETLA) o Value Incentive Plan (VIP) che eseguono la migrazione a un programma di acquisto o a un tipo di licenza diverso.

>[!NOTE]
>
>Se ti trovi in Nord America e hai bisogno di assistenza per il rinnovo annuale del contratto Adobe VIP dal tuo Account Manager, invia un&#39;e-mail a **renewalhelp@adobe.com**, dove verrai contattato al più presto.

Per evitare una perdita di accesso ai prodotti da parte dell’utente finale, assegna le licenze nel Adobe Admin Console prima della scadenza del periodo di abbonamento a VIP esistente.

* Per i clienti ETLA, consenti almeno 30 giorni di sovrapposizione dei prodotti. Completa la migrazione prima della data dell’anniversario in modo che gli utenti possano continuare ad accedere alle app e ai servizi di Adobe. Per i dettagli sulla scadenza del contratto ETLA, vedi [Fasi di scadenza automatizzate per i contratti ETLA](https://helpx.adobe.com/it/enterprise/using/contract-expiry.html).
* Per i clienti VIP, acquista le licenze prima della data dell’anniversario e assegna le licenze prima che la finestra di rinnovo si chiuda nel periodo VIP corrente.
* I clienti CLP o TLP possono migrare da Acrobat o Creative Suite con numero di serie alle licenze per utenti con nome seguendo le istruzioni di migrazione in [Licenze](https://helpx.adobe.com/it/enterprise/using/licensing.html).

>[!NOTE]
>
>Se il tipo di licenza della tua organizzazione cambia, gli utenti finali devono disconnettersi da qualsiasi prodotto o servizio Adobe e accedere nuovamente con le stesse credenziali.
>
>Per i prodotti desktop come Photoshop, Acrobat e Illustrator, utilizza le opzioni Disconnetti e Accedi nel menu ?. Su Adobe.com, utilizza l’icona nell’angolo in alto a destra per disconnetterti, quindi accedi nuovamente.

## Assegnazione rapida licenza (da VIP a VIP)

Gli attuali membri di VIP che hanno acquistato Creative Cloud for enterprise o Acrobat (for enterprise) tramite VIP potrebbero essere in grado di assegnare rapidamente le licenze durante la finestra di rinnovo utilizzando Assegnazione rapida licenze. I clienti idonei soddisfano i seguenti criteri.

* I prodotti sono gli stessi

   1. La finestra di rinnovo è aperta (30 giorni prima o dopo la data anniversario del contratto VIP).
   2. I prodotti enterprise nell’ordine sono nuovi SKU equivalenti alle versioni del team nel termine corrente.
   3. La quantità dell&#39;ordine di licenza dell&#39;organizzazione è maggiore o uguale alla quantità della licenza del team esistente.

* I prodotti hanno un valore più elevato

   1. Finestra di rinnovo aperta.
   2. I prodotti aziendali nell’ordine sono nuovi SKU che sono prodotti di valore superiore rispetto ai prodotti del team nel termine corrente.
   3. La quantità dell&#39;ordine di licenza dell&#39;organizzazione è maggiore o uguale alla quantità della licenza del team esistente.

* Assegnazione rapida licenza non disponibile quando

   * La quantità di licenze enterprise nell&#39;ordine è inferiore al numero di licenze team esistenti.
   * L&#39;ordine è relativo a prodotti aziendali di valore superiore, ma la quantità di licenze aziendali ordinate è inferiore alla quantità di licenze del team esistente.
   * L&#39;ordine combina i prodotti del team e dell&#39;organizzazione, indipendentemente dalla quantità.
   * Il cliente ha già acquistato i prodotti del team e dell&#39;azienda prima del periodo di rinnovo.
   * Gli SKU di rinnovo Enterprise vengono utilizzati per il nuovo ordine Enterprise.
   * L&#39;ordine dei prodotti aziendali è per un numero di contratto VIP diverso.
   * I prodotti del team corrente includono elementi privi di versioni Enterprise.

Dopo che Adobe elabora l’ordine di acquisto Enterprise, ricevi un’e-mail di conferma con le istruzioni, incluso il giorno in cui devi trasferire gli utenti dalle licenze del team alle licenze Enterprise in Admin Console prima che perdano l’accesso.

In Admin Console, viene richiesto di assegnare le licenze utilizzando Assegnazione rapida licenze:

1. Confermare il numero di licenze per l&#39;assegnazione.

   ![Licenze di trasferimento](assets/migrate-transfer-licenses.png)

2. Verificare che le licenze del prodotto team non assegnate corrispondano alle licenze aziendali assegnate.

3. Ricevi un’e-mail al termine del processo.

   ![Conferma assegnazione licenza](assets/migrate-license-assignment.png)

Scarica il [report dei risultati](https://helpx.adobe.com/it/enterprise/using/users.html#main-pars_header_1346350355) in Admin Console per verificare che tutte le licenze siano state assegnate. Se la data di fine dell’e-mail di conferma è anteriore a quella indicata, gli utenti finali non dovranno notare alcuna interruzione del servizio.

Pianifica una chiamata di onboarding 1:1 con uno specialista di onboarding di Adobe (se non lo hai già fatto) per ulteriori informazioni su Admin Console, inclusi [Ruoli amministrativi](https://helpx.adobe.com/it/enterprise/using/admin-roles.html) e [Identità](https://helpx.adobe.com/it/enterprise/using/identity.html).

>[!NOTE]
>
>Assegnazione rapida licenze non esegue la migrazione degli utenti con inviti in sospeso in Team Admin Console.

## Assegnazione di licenza in blocco (da VIP a VIP)

Assegnare le licenze con un&#39;operazione in blocco utilizzando un modello CSV di [!DNL Admin Console]. Utilizza questo approccio quando:

* Sei un cliente VIP che non soddisfa i requisiti di assegnazione della licenza rapida, o
* È necessario assegnare le licenze al di fuori della finestra di rinnovo.

1. Dopo aver avuto accesso a [Adobe Admin Console](https://adminconsole.adobe.com/enterprise) e aver aggiunto le licenze, passa a **[!UICONTROL Utenti]** > **[!UICONTROL Utenti]**.
2. Fai clic sul ![menu Altre opzioni](assets/migrate-more-options.png) nell&#39;angolo superiore destro della pagina **[!UICONTROL Utenti]**, quindi scegli **[!UICONTROL Modifica dettagli utente per CSV]**.
3. Nella finestra di dialogo **[!UICONTROL Modifica utenti per CSV]**, fai clic su **[!UICONTROL Scarica modello CSV]** e scegli **[!UICONTROL Elenco utenti corrente]**.

   ![Modifica utenti per CSV](assets/migrate-edit-users-by-csv.png)

   Per le descrizioni dei campi nel file scaricato, vedere [Formato file CSV](https://helpx.adobe.com/it/enterprise/using/users.html#main-pars_header).
4. Aggiungi le assegnazioni di licenza al file CSV, quindi trascina il file aggiornato nella finestra di dialogo **[!UICONTROL Modifica utenti in base al file CSV]** e fai clic su **[!UICONTROL Carica]**. Ricevi un’e-mail al completamento dell’operazione.

   ![Modifica utente completata](assets/migrate-user-edit-complete.png)

Scarica il [report dei risultati](https://helpx.adobe.com/it/enterprise/using/users.html#main-pars_header_1346350355) per convalidare le assegnazioni. Quindi pianifica l&#39;onboarding con uno specialista di onboarding Adobe per scoprire [ruoli amministrativi](https://helpx.adobe.com/it/enterprise/using/admin-roles.html) e [identità](https://helpx.adobe.com/it/enterprise/using/identity.html).

## Assegnazione di licenza in blocco (da VIP ad ETLA)

Se disponi di una sottoscrizione a VIP e trasferisci gli utenti ad ETLA, utilizza questo flusso di massa:

1. Accedi a [Adobe Admin Console](https://adminconsole.adobe.com/enterprise) e apri l&#39;organizzazione che contiene gli utenti VIP.
2. Vai a **[!UICONTROL Utenti]** > **[!UICONTROL Utenti]**.
3. Fai clic sul ![menu Altre opzioni](assets/migrate-more-options.png) nell&#39;angolo superiore destro, quindi scegli **[!UICONTROL Esporta elenco utenti in CSV]**.
4. Apri l’organizzazione ETLA in cui desideri tali utenti.
5. Vai a **[!UICONTROL Utenti]** > **[!UICONTROL Utenti]**.
6. Fai clic su **[!UICONTROL Aggiungi utenti per CSV]**.
7. Fai clic su **[!UICONTROL Scarica modello CSV]**, quindi aggiungi gli utenti VIP dal file CSV esportato al passaggio 3.
8. Carica il file CSV aggiornato.

Ricevi un’e-mail quando gli utenti vengono aggiunti all’organizzazione ETLA.

![Utenti aggiunti dopo la migrazione da VIP ad ETLA](assets/migrate-users-added-vip-etla.png)

Scarica il [report dei risultati](https://helpx.adobe.com/it/enterprise/using/users.html#main-pars_header_1346350355) per convalidare le assegnazioni. Pianifica l&#39;onboarding con uno specialista di onboarding di Adobe per [ruoli amministrativi](https://helpx.adobe.com/it/enterprise/using/admin-roles.html) e [identità](https://helpx.adobe.com/it/enterprise/using/identity.html).

Per problemi relativi al caricamento in blocco, vedi [Risoluzione dei problemi relativi al caricamento in blocco degli utenti](https://helpx.adobe.com/it/enterprise/kb/troubleshoot-bulk-user-csv-upload.html).

## Assegnazione di licenza in blocco (da ETLA a VIP)

Se disponi di una sottoscrizione ETLA e trasferisci gli utenti a VIP:

1. Accedi a [Adobe Admin Console](https://adminconsole.adobe.com/enterprise) e apri l&#39;organizzazione che contiene gli utenti ETLA.
2. Vai a **[!UICONTROL Utenti]** > **[!UICONTROL Utenti]**.
3. Fai clic sul ![menu Altre opzioni](assets/migrate-more-options.png) nell&#39;angolo superiore destro, quindi scegli **[!UICONTROL Esporta elenco utenti in CSV]**.

   ![Esporta menu elenco utenti](assets/migrate-export-user-list.png)

4. Apri l’organizzazione VIP in cui desideri tali utenti.
5. Vai a **[!UICONTROL Utenti]** > **[!UICONTROL Utenti]**.
6. Fai clic su **[!UICONTROL Aggiungi utenti per CSV]**.
7. Fai clic su **[!UICONTROL Scarica modello CSV]**, quindi aggiungi gli utenti ETLA dal file CSV esportato al passaggio 3.
8. Carica il file CSV aggiornato.

Ricevi un’e-mail quando gli utenti vengono aggiunti all’organizzazione VIP.

![Utenti aggiunti dopo la migrazione da ETLA a VIP](assets/migrate-users-added-etla-vip.png)

Scarica il [report dei risultati](https://helpx.adobe.com/it/enterprise/using/users.html#main-pars_header_1346350355) per convalidare le assegnazioni. Pianifica l&#39;onboarding con uno specialista di onboarding di Adobe per [ruoli amministrativi](https://helpx.adobe.com/it/enterprise/using/admin-roles.html) e [identità](https://helpx.adobe.com/it/enterprise/using/identity.html).

Per problemi relativi al caricamento in blocco, vedi [Risoluzione dei problemi relativi al caricamento in blocco degli utenti](https://helpx.adobe.com/it/enterprise/kb/troubleshoot-bulk-user-csv-upload.html).


