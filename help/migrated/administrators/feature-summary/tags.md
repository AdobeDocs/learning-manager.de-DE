---
description: Erfahren Sie, wie Sie Tags im Lern-Manager verwalten.
jcr-language: en_us
title: Tags
contentowner: dvenkate
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---



# Tags

Administratoren können jetzt Tags im Lern-Manager verwalten. Verwenden Sie besseres Tagging und eine verwaltbare Datenbank, damit die Teilnehmer besser suchen und schnell die passenden Suchergebnisse erhalten. Mit dieser Funktion können Sie redundante, falsch geschriebene und irrelevante Tags verwalten. Darüber hinaus können Sie Tags hinzufügen, bearbeiten, löschen, anhängen oder ersetzen.

Die Liste der Lernobjekte, die mit dem Tag verknüpft sind, kann angezeigt werden, indem Sie auf die Anzahl neben jedem Tag klicken. Die Liste enthält die Anzahl der Kurse, Lernprogramme, Zertifikate, Arbeitshilfen und Inhaltsgruppen. Klicken Sie auf eine dieser Optionen, um die Liste anzuzeigen.

Sie können die Tags anhand der Verwendung oder in alphabetischer Reihenfolge mit dem Befehl **[!UICONTROL Sortieren]** aus.

## Tags hinzufügen/löschen/bearbeiten {#adddeleteedittags}

1. Klicken Sie als Administrator im linken Navigationsbereich auf **[!UICONTROL Tags]**. Die **[!UICONTROL Tag Management]** wird geöffnet.
1. Um ein neues Tag hinzuzufügen, klicken Sie auf **[!UICONTROL Hinzufügen]**. Die Schaltfläche Hinzufügen ist in der rechten oberen Ecke der Seite verfügbar. Wenn keine Tags vorhanden sind, wird das Dialogfeld &quot; **[!UICONTROL Hinzufügen]** wird auch in der Mitte der **[!UICONTROL Tag Management]** angezeigt.

   Trennen Sie beim Hinzufügen mehrerer Tags diese mithilfe von (,) oder (;). Ein Tag-Name darf maximal 50 Zeichen enthalten.

1. Um ein vorhandenes Tag zu löschen, wählen Sie das Tag aus, indem Sie auf das Kontrollkästchen klicken. Sie können mehrere Tags mit einer Anzahl von bis zu fünfzig auswählen, um sie gleichzeitig zu löschen. Gehen Sie zum Löschen wie folgt vor:

   * Wählen Sie die zu löschenden Tags aus > öffnen Sie die **[!UICONTROL Aktion]** Dropdown-Menü > select **[!UICONTROL Löschen]**.

1. Sie können jeweils nur ein einzelnes Tag bearbeiten. Um ein Tag zu bearbeiten, führen Sie diesen Schritt aus:

   * Tag zum Bearbeiten auswählen > ** öffnen[!UICONTROL Aktionen]**Dropdown-Menü > klicken Sie auf **[!UICONTROL Bearbeiten]**.

   Die **[!UICONTROL Tag bearbeiten]** &quot; wird angezeigt. Geben Sie den neuen Tag-Namen ein und klicken Sie auf **[!UICONTROL Speichern]**.

   Wenn der eingegebene Tag-Name bereits vorhanden ist, zeigt der Adobe Learning Manager eine Warnmeldung an. Es können keine zwei Tags mit demselben Namen vorhanden sein.

## Tags ersetzen {#replacetags}

1. Wählen Sie die Tags aus, die Sie ersetzen möchten. Sie können bis zu 50 Tags gleichzeitig auswählen. Öffnen Sie die **[!UICONTROL Aktionen]** &quot; und wählen Sie **[!UICONTROL Ersetzen]**.
1. Die **[!UICONTROL Tags ersetzen]** wird mit den ausgewählten Tags angezeigt.

1. Im Dialogfeld &quot; **[!UICONTROL Name für ersetzte Tags]** den Namen des neuen Tags ein, mit dem die ausgewählten Tags ersetzt werden sollen. Sie können sie entweder durch ein vorhandenes Tag aus der Dropdown-Liste ersetzen oder ein neues Tag hinzufügen.

   Semikolon oder Komma können nicht Teil des Tag-Namens sein.  Beachten Sie, dass Tags ohne Semikolons und die Anzeige von Fehlermeldungen bei der Verwendung solcher Tags als Teil eines LO für Migrationsszenarien nicht behandelt werden.

1. Klicken **[!UICONTROL Ersetzen]**.

## Tags anhängen {#appendtags}

Bei Anhängen von Tags wird das neue/vorhandene Tag an alle Listen von LOs und Inhaltsgruppen angehängt, die den ausgewählten Tags zugeordnet sind.

1. Wählen Sie die Tags aus, die angehängt werden sollen. Sie können bis zu 50 Tags gleichzeitig auswählen. Öffnen Sie das Dropdown-Menü Aktionen und wählen Sie **[!UICONTROL Anfügen]**.
1. Die  **[!UICONTROL Tags anhängen]** wird mit den ausgewählten Tags angezeigt.
1. Sie können ein zusätzliches Tag an alle Teilnehmer mit den ausgewählten Tags anhängen, indem Sie den Namen des **[!UICONTROL Neues Tag]** oder aus der Dropdown-Liste der vorhandenen Tags. Das neue Tag wird an alle verknüpften Lernaktivitäten im Lern-Manager angehängt.

   Semikolon oder Komma können nicht Teil des Tag-Namens sein. Wenn diese Option verwendet wird, zeigt Prime eine Fehlermeldung an. Beachten Sie, dass Tags ohne Semikolons und die Anzeige von Fehlermeldungen bei der Verwendung solcher Tags als Teil eines LO für Migrationsszenarien nicht behandelt werden.

1. Klicken **[!UICONTROL Anfügen]**.

## Einstellungen {#settings}

Als Administrator können Sie dem Autor die Berechtigung zum Erstellen von Tags erteilen, indem Sie auf die Option &quot;Einstellungen&quot; klicken.

![](assets/unknown-1.jpeg)

*Einstellungsseite zum Erstellen eines Tags*

* Wenn ein Benutzer über die Berechtigung zum Erstellen von Tags verfügt und vorhandene Tags auswählt, die derzeit ungültig sind,

  Eine Fehlermeldung wird angezeigt, die darauf hinweist, dass das ausgewählte Tag nicht mehr gültig ist. Neue Tags werden erstellt, indem nicht unterstützte Zeichen entfernt werden. In diesem Fall sollte der Autor in der Lage sein, seine alten Tags vor dem Speichern in neue Tags umzuwandeln.

* Wenn der Benutzer nicht über die Berechtigungen zum Erstellen neuer Tags verfügt, wird eine Fehlermeldung angezeigt, dass das ausgewählte Tag nicht mehr gültig ist. Autoren können sich an die Administratoren wenden, um ungültige Tags zu ändern.

  Autoren können keine ungültigen Tags erstellen oder speichern. Sie können ungültige Tags entfernen und ein anderes vorhandenes gültiges Tag hinzufügen und fortfahren.
