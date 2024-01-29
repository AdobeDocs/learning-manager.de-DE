---
jcr-language: en_us
title: Kenntnisse Kenntnisdomänen zuordnen
description: Um einen Beitrag automatisch zu kuratieren, der von einem Benutzer von der AI-fähigen Kurations-Engine für eine bestimmte Kenntnisdomäne veröffentlicht wird, muss das Unternehmen des Benutzers über seine benutzerdefinierten Kenntnisse verfügen, die den unterstützten Kenntnisdomänen im Learning Manager-LMS zugeordnet werden können.
contentowner: kuppan
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---



# Kenntnisse Kenntnisdomänen zuordnen

Um einen Beitrag automatisch zu kuratieren, der von einem Benutzer von der AI-fähigen Kurations-Engine für eine bestimmte Kenntnisdomäne veröffentlicht wird, muss das Unternehmen des Benutzers über seine benutzerdefinierten Kenntnisse verfügen, die den unterstützten Kenntnisdomänen im Learning Manager-LMS zugeordnet werden können.

Beim Erstellen von Kenntnissen kann ein Administrator sie den relevantesten von Learning Manager unterstützten Kenntnisdomänen zuordnen. Dies wird im Prozess der automatischen Kuration weiter berücksichtigt. Learning Manager LMS listet die folgenden Kenntnisse auf:

* Supply Chain Management
* Buchhaltung
* Wissenschaftliche Forschung und Ingenieurwesen
* Computersicherheit
* Strategisches Management
* Social Media
* Medizin
* Finanzwesen
* Sicherheit am Arbeitsplatz
* Soft Skills
* Wirtschaftsrecht
* Management
* Personalmanagement
* Technische Kommunikation
* Geschäftsethik
* Customer Relationship Management
* Informationstechnologie
* Produktion und Fertigung
* Marketing
* Qualitätsmanagement
* Geschäftsprozess
* Lernressourcen
* Design
* Analytics
* Vertrieb

Um eine Kenntnisdomäne hinzuzufügen, führen Sie die folgenden Schritte aus:

1. Klicken Sie im linken Bereich der Administrator-App auf **[!UICONTROL Kenntnisse]**.
1. Um Kenntnisse hinzuzufügen, klicken Sie auf **[!UICONTROL Hinzufügen]** oben rechts auf der Seite.
1. Im Dialogfeld &quot; **[!UICONTROL Kenntnisse hinzufügen]** eine Qualifikation und eine Beschreibung der Qualifikation hinzu.
1. Im Dialogfeld &quot; **[!UICONTROL Kenntnisdomäne]** die Kenntnisdomänen hinzu. Wenn Sie eine Domäne eingeben, werden die Domänen hinzugefügt. Diese Domänen werden aus der oben genannten Liste ausgefüllt.

   ![](assets/skill-domain-mapping.png)

   *Fügen Sie die Kenntnisdomänen im Abschnitt Kenntnisdomäne hinzu*

1. Klicken Sie zum Speichern der Änderungen auf **[!UICONTROL Speichern]**.

Wenn ein Benutzer einen Inhalt in einem Board postet, wird der Inhalt kuratiert und genehmigt oder abgelehnt, je nachdem, welcher Confidence-Score den zugeordneten Kenntnissen dem Board zugeordnet ist.

<!--![](assets/content-uploaded.png)-->

Abhängig davon, ob der hochgeladene Inhalt einen Konfidenzwert von mehr als 50 % aufweist, wird der Inhalt in das Board hochgeladen. Wenn Ihr Inhalt die Kriterien erfüllt, wird eine Benachrichtigung angezeigt, dass der Inhalt erfolgreich kuratiert wurde und jetzt im Board verfügbar ist.

![](assets/curation-notification.png)

*Benachrichtigungen in Abhängigkeit vom Confidence-Ergebnis anzeigen*

