---
title: Comprimi bug sezioni
description: Le sezioni comprimibili UGP-13446 non vengono sottoposte a rendering, probabilmente a causa di schede di pagina incorporate
hide: true
hidefromtoc: true
source-git-commit: f2d8eb9125df5f542c1ed075348586965f4adaad
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 7%

---

# Sezioni comprimibili

<http://jira.corp.adobe.com/browse/UGP-13446> Le sezioni comprimibili UGP-13446 non vengono sottoposte a rendering, probabilmente a causa di schede di pagina incorporate

## Esempi

Primo con linguette di pagina; secondo senza

### Opzione 2: con linguette pagina

+++ Installazione manuale hotfix per 6.5.18.0 - 6.5.22.0

**Passaggio 1: scarica ed estrai il pacchetto Hotfix**

- Scarica [hotfix per 6.5.18.0 - 6.5.22](https://www.adobe.com) dal portale di distribuzione software di Adobe
- Estrai localmente

**Passaggio 2: passare alla cartella della versione corretta**

- In base alla versione del Service Pack installata nel tuo ambiente, vai alla cartella corrispondente.

  Esempio per Service Pack 20 la cartella è:

  ```
  <extracted-hotfix>/SP20/
  ```

**Passaggio 3: individuare la directory di distribuzione**

- Nel server AEM Forms su JEE, vai a:

  ```
  [AEM installation directory]/deploy
  ```

  Esempio: `adobe/adobe-experience-manager-forms/deploy`



**Passaggio 4: aggiornare e sostituire i file EAR**

>[!BEGINTABS]

>[!TAB JBoss]

1. Apri `adobe-core-jboss.ear` e sostituisci `adminui.war` con

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adminui.war
   ```

   Ad esempio, `adobe-xxe-configuration-hotfix/SP20/jboss/adminui.war`

1. All&#39;interno di `adobe-core-jboss.ear`, passare alla cartella `lib/` e sostituire `adobe-uisupport.jar` con:

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   Ad esempio, `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. Salvare l&#39;EAR. Assicurati che le modifiche siano salvate correttamente.


1. Sostituisci `adobe-edcserver-jboss.ear` con

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adobe-edcserver-jboss.ear
   ```

   Ad esempio, `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-edcserver-jboss.ear`

1. Sostituisci `adobe-forms-jboss.ear` con

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adobe-forms-jboss.ear
   ```

   Ad esempio, `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-forms-jboss.ear`



>[!TAB WebLogic]

1. Apri `adobe-core-weblogic.ear` e sostituisci `adminui.war` con

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adminui.war
   ```

   Ad esempio, `adobe-xxe-configuration-hotfix/SP20/weblogic/adminui.war`

1. All&#39;interno di `adobe-core-weblogic.ear`, sostituisci `adobe-uisupport.jar` con:

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   Ad esempio, `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. Salvare l&#39;EAR. Assicurati che le modifiche siano salvate correttamente.


1. Sostituisci `adobe-edcserver-weblogic.ear` con

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adobe-edcserver-weblogic.ear
   ```

   Ad esempio, `adobe-xxe-configuration-hotfix/SP20/weblogic/adobe-edcserver-weblogic.ear`

1. Sostituisci `adobe-forms-weblogic.ear` con

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adobe-forms-weblogic.ear
   ```

   Ad esempio, `adobe-xxe-configuration-hotfix/SP20/weblogic/adobe-forms-weblogic.ear`

>[!TAB WebSphere]

1. Apri `adobe-core-websphere.ear` e sostituisci `adminui.war` con

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adminui.war
   ```

   Ad esempio, `adobe-xxe-configuration-hotfix/SP20/websphere/adminui.war`

1. All&#39;interno di `adobe-core-websphere.ear`, sostituisci `adobe-uisupport.jar` con:

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   Ad esempio, `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. Salvare l&#39;EAR. Assicurati che le modifiche siano salvate correttamente.


1. Sostituisci `adobe-edcserver-websphere.ear` con

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adobe-edcserver-websphere.ear
   ```

   Ad esempio, `adobe-xxe-configuration-hotfix/SP20/websphere/adobe-edcserver-websphere.ear`

1. Sostituisci `adobe-forms-websphere.ear` con

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adobe-forms-websphere.ear
   ```

   Ad esempio, `adobe-xxe-configuration-hotfix/SP20/websphere/adobe-forms-websphere.ear`

>[!ENDTABS]



**Passaggio 5: aggiorna `adobe-rightsmanagement-<appserver>-dsc.jar`file con**

```
adobe-xxe-configuration-hotfix/SP[version]/<appserver>/adobe-rightsmanagement-<appserver>-dsc.jar
```

Ad esempio, `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-rightsmanagement-jboss-dsc.jar`

**Passaggio 6: configurazione aggiuntiva per Document Security su WebSphere e WebLogic**:

Se utilizzi Document Security (precedentemente Rights Management), imposta la seguente proprietà di sistema Java (argomento JVM) prima di avviare il server AEM Forms:

```
-Dcom.adobe.forms.jee.services.allowDoctypeDeclaration=true
```


**Passaggio 7: rieseguire Configuration Manager**

- Avvia Configuration Manager per ridistribuire l’EAR aggiornato e applicare l’hotfix

+++

### Opzione 2: senza linguette pagina

+++ Installazione manuale hotfix per 6.5.18.0 - 6.5.22.0

**Passaggio 1: scarica ed estrai il pacchetto Hotfix**

- Scarica [hotfix per 6.5.18.0 - 6.5.22](https://www.adobe.com) dal portale di distribuzione software di Adobe
- Estrai localmente

**Passaggio 2: passare alla cartella della versione corretta**

- In base alla versione del Service Pack installata nel tuo ambiente, vai alla cartella corrispondente.

  Esempio per Service Pack 20 la cartella è:

  ```
  <extracted-hotfix>/SP20/
  ```

**Passaggio 3: individuare la directory di distribuzione**

- Nel server AEM Forms su JEE, vai a:

  ```
  [AEM installation directory]/deploy
  ```

  Esempio: `adobe/adobe-experience-manager-forms/deploy`



**Passaggio 4: aggiornare e sostituire i file EAR**

Schede pagina eliminate

**Passaggio 5: aggiorna `adobe-rightsmanagement-<appserver>-dsc.jar`file con**

```
adobe-xxe-configuration-hotfix/SP[version]/<appserver>/adobe-rightsmanagement-<appserver>-dsc.jar
```

Ad esempio, `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-rightsmanagement-jboss-dsc.jar`

**Passaggio 6: configurazione aggiuntiva per Document Security su WebSphere e WebLogic**:

Se utilizzi Document Security (precedentemente Rights Management), imposta la seguente proprietà di sistema Java (argomento JVM) prima di avviare il server AEM Forms:

```
-Dcom.adobe.forms.jee.services.allowDoctypeDeclaration=true
```


**Passaggio 7: rieseguire Configuration Manager**

- Avvia Configuration Manager per ridistribuire l’EAR aggiornato e applicare l’hotfix

+++

Fin
