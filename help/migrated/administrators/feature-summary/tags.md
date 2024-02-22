---
description: Erfahren Sie, wie Sie Tags in Learning Manager verwalten.
jcr-language: en_us
title: Tags
contentowner: dvenkate
source-git-commit: 0534bd52c80b77d985cfe715f74054f3aabac9a2
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 63%

---



# Tags

Administratoren können jetzt Tags in Learning Manager verwalten. Verwenden Sie besseres Tagging und eine verwaltbare Datenbank, damit Lernende bessere Suchvorgänge ausführen können und rasch die passenden Ergebnisse erhalten. Mit dieser Funktion können Sie redundante, falsch geschriebene und irrelevante Tags verwalten. Sie können auch Tags hinzufügen, bearbeiten, löschen, anhängen oder ersetzen.

Die Liste der Lernobjekte, die mit dem Tag verknüpft sind, kann durch Klicken auf die Anzahl neben jedem Tag angezeigt werden. Die Liste enthält die Anzahl der Kurse, Lernprogramme, Zertifikate, Arbeitshilfen und Inhaltsgruppen. Klicken Sie auf eine dieser Optionen, um die Liste anzuzeigen.

Sie können die Tags anhand der Nutzung oder in alphabetischer Reihenfolge mit der Option **[!UICONTROL Sortieren nach]** sortieren.

## Einführung in Tags

In dieser Schulung erfahren Sie, wie Sie Tags hinzufügen, bearbeiten, ersetzen, anhängen und löschen. Außerdem erfahren Sie, wie Sie Berechtigungseinstellungen ändern und Tag-Filter verwenden.

[![Knopf](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=5S7K7ZCT&amp;mv=display&amp;mv2=display#/course/8318920)

Wenn Sie die Schulung nicht starten können, schreiben Sie an <almacademy@adobe.com>.

## Hinzufügen/Löschen/Bearbeiten von Tags {#adddeleteedittags}

1. Klicken Sie als Administrator im linken Navigationsbereich auf **[!UICONTROL Tags]**. Die Seite **[!UICONTROL Tag-Management]** wird geöffnet.
1. Um ein neues Tag hinzuzufügen, klicken Sie auf **[!UICONTROL Hinzufügen]**. Die Schaltfläche „Hinzufügen“ finden Sie in der rechten oberen Ecke der Seite. Wenn keine Tags vorhanden sind, steht die Schaltfläche **[!UICONTROL Hinzufügen]** auch in der Mitte der Seite **[!UICONTROL Tag-Management]** zur Verfügung.

   Wenn Sie mehrere Tags hinzufügen, trennen Sie sie mit (,) oder (;). Ein Tag-Name darf maximal 50 Zeichen lang sein.

1. Um ein vorhandenes Tag zu löschen, wählen Sie das Tag aus, indem Sie auf das Kontrollkästchen klicken. Sie können mehrere Tags mit einer Anzahl von bis zu fünfzig auswählen, um sie gleichzeitig zu löschen. Zum Löschen gehen Sie wie folgt vor:

   * Wählen Sie die zu löschenden Tags aus > öffnen Sie das Dropdown-Menü **[!UICONTROL Aktion]** aus > wählen Sie **[!UICONTROL Löschen]**.

1. Sie können jeweils nur ein einzelnes Tag bearbeiten. Gehen Sie dazu wie folgt vor:

   * Tag zum Bearbeiten auswählen > ** öffnen[!UICONTROL Aktionen]**Dropdown-Menü > klicken Sie auf **[!UICONTROL Bearbeiten]**.

   Das Dialogfeld **[!UICONTROL Tag bearbeiten]** wird angezeigt. Geben Sie den neuen Tag-Namen und klicken Sie auf **[!UICONTROL Speichern]**.

   Wenn der eingegebene Tag-Name bereits vorhanden ist, zeigt der Adobe Learning Manager eine Warnmeldung an. Es können keine zwei Tags mit demselben Namen existieren.

## Tags ersetzen {#replacetags}

1. Wählen Sie die Tags aus, die Sie ersetzen möchten. Sie können bis zu 50 Tags gleichzeitig auswählen. Öffnen Sie die **[!UICONTROL Aktionen]** &quot; und wählen Sie **[!UICONTROL Ersetzen]**.
1. Die **[!UICONTROL Tags ersetzen]** wird mit den ausgewählten Tags angezeigt.

1. Geben Sie für **[!UICONTROL Name für ersetzte Tags]** den Namen des neuen Tags ein, durch das die ausgewählten Tags ersetzt werden sollen. Sie können sie entweder durch ein vorhandenes Tag aus dem Dropdown-Menü ersetzen oder ein neues Tag hinzufügen.

   Semikolon oder Komma können nicht Teil des Tag-Namens sein.  Beachten Sie, dass Tags ohne Semikolon und die Anzeige von Fehlermeldungen bei der Verwendung solcher Tags als Teil eines LO für Migrationsszenarien nicht behandelt werden.

1. Klicken Sie auf **[!UICONTROL Ersetzen]**.

## Tags anhängen {#appendtags}

Bei Anhängen von Tags wird das neue/vorhandene Tag an alle Listen von LOs und Inhaltsgruppen angehängt, die den ausgewählten Tags zugeordnet sind.

1. Wählen Sie die Tags aus, die Sie anhängen möchten. Sie können bis zu 50 Tags gleichzeitig auswählen. Öffnen Sie das Dropdown-Menü Aktionen und wählen Sie **[!UICONTROL Anfügen]**.
1. Die  **[!UICONTROL Tags anhängen]** wird mit den ausgewählten Tags angezeigt.
1. Sie können ein zusätzliches Tag an alle Lernobjekte mit den ausgewählten Tags anhängen, indem Sie den Namen des **[!UICONTROL neuen Tags]** eingeben oder aus der Dropdown-Liste der vorhandenen Tags eines auswählen. Der neue Tag wird allen zugehörigen Lernobjekten in Learning Manager angehängt.

   Semikolon oder Komma können nicht Teil des Tag-Namens sein. Andernfalls zeigt Prime eine Fehlermeldung an. Beachten Sie, dass Tags ohne Semikolon und die Anzeige von Fehlermeldungen bei der Verwendung solcher Tags als Teil eines LO für Migrationsszenarien nicht behandelt werden.

1. Klicken Sie auf **[!UICONTROL Anhängen]**.

## Einstellungen {#settings}

Als Administrator können Sie dem Autor die Berechtigung zum Erstellen von Tags erteilen, indem Sie auf die Option &quot;Einstellungen&quot; klicken.

![](assets/unknown-1.jpeg)

*Einstellungsseite zum Erstellen eines Tags*

* Wenn ein Benutzer über die Berechtigung zum Erstellen von Tags verfügt und vorhandene Tags auswählt, die derzeit ungültig sind,

  Eine Fehlermeldung wird angezeigt, die darauf hinweist, dass das ausgewählte Tag nicht mehr gültig ist. Neue Tags werden durch Entfernen nicht unterstützter Zeichen erstellt. In diesem Fall sollte der Autor in der Lage sein, seine alten Tags vor dem Speichern in neue Tags umzuwandeln.

* Wenn der Benutzer nicht über die Berechtigungen zum Erstellen neuer Tags verfügt, wird eine Fehlermeldung angezeigt, dass das ausgewählte Tag nicht mehr gültig ist. Autoren können die Administratoren kontaktieren, um ungültige Tags zu ändern.

  Autoren können keine ungültigen Tags erstellen oder speichern. Sie können ungültige Tags entfernen und ein anderes vorhandenes gültiges Tag hinzufügen und fortfahren.
