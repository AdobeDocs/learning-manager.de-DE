---
jcr-language: en_us
title: Standorte für Klassenzimmer hinzufügen
description: Administratoren können jetzt eine Bibliothek mit Standorten für Klassenzimmern einrichten. Für jeden Klassenraum können die Administratoren die Metadaten festlegen, die den Namen des Standorts, das Sitzplatzlimit sowie zusätzliche Informationen wie die URL des Standorts enthalten. Autoren und Administratoren können diese vorkonfigurierten Klassenzimmer dann für die Einrichtung von Schulungsveranstaltungen mit Kursleitern (Klassenzimmermodule) verwenden.
contentowner: saghosh
exl-id: 51a1e38f-d4e2-4c19-bbf7-6696505c0dfd
source-git-commit: 8cb8a95812c97b0b59a2ae5188500cfafe09bd27
workflow-type: tm+mt
source-wordcount: '1315'
ht-degree: 54%

---

# Klassenzimmer

## Übersicht

Administratoren können jetzt eine Bibliothek mit Standorten für Klassenzimmern einrichten. Für jeden Klassenraum können die Administratoren die Metadaten festlegen, die den Namen des Standorts, das Sitzplatzlimit sowie zusätzliche Informationen wie die URL des Standorts enthalten. Autoren und Administratoren können diese vorkonfigurierten Klassenzimmer dann für die Einrichtung von Schulungsveranstaltungen mit Kursleitern (Klassenzimmermodule) verwenden.

Sie können die folgenden zwei Möglichkeiten nutzen, um ein Klassenzimmer hinzuzufügen.

## Klassenzimmer über die Benutzeroberfläche hinzufügen

Sie können einen Speicherort für ein Klassenzimmer hinzufügen, indem Sie die Benutzeroberfläche verwenden:

1. Klicken Sie in der Admin-App (der Benutzeroberfläche für Administratorrollen) auf **[!UICONTROL Einstellungen]** > **[!UICONTROL Standorte für Klassenzimmer]**.

1. Klicken Sie auf **[!UICONTROL Hinzufügen]** > **[!UICONTROL Neuer Speicherort]**.

1. Geben Sie im Dialogfeld **[!UICONTROL Klassenzimmerstandort]** die folgenden Details ein:

   * Geben Sie den **[!UICONTROL Standortnamen]** ein. Verwenden Sie einen eindeutigen Namen. Andernfalls zeigt Learning Manager eine Fehlermeldung an.
   * Geben Sie die Positionsbeschreibung in das Feld **[!UICONTROL Standortinformationen]** ein. Dieses Feld ist optional.
   * Geben Sie die **[!UICONTROL URL des Standorts]** an. Der Teilnehmer kann diese Informationen in den Details des Klassenzimmers sehen. Bei Bedarf kann die URL auch eine URL für den Kartenstandort sein. Dies ist ein optionales Feld.
   * Geben Sie den Standort **[!UICONTROL Region]** ein, und wählen Sie ihn aus. Dieses Feld ist optional.
   * Geben Sie die Anzahl der verfügbaren Lizenzen in das Feld **[!UICONTROL Sitzplatzlimit]** ein. Dies gibt die Sitzplatzkapazität des Klassenzimmers an. Dieser Wert kann beim Erstellen des tatsächlichen Schulungsereignisses mit dem Kursleiter geändert werden.

   ![](assets/add-classroom-location.png)

   *Klassenzimmerspeicherort hinzufügen*

Nach dem Hinzufügen des Speicherorts werden auf der Seite **[!UICONTROL Einstellungen]** > **[!UICONTROL Speicherorte für Klassenzimmer]** die Meetingräume aufgeführt:

![](assets/list-meeting-rooms.png)

*Alle Meetingräume anzeigen*

Die Liste enthält die folgenden Felder:

**[!UICONTROL Standortname]** - Name des Klassenzimmerstandorts.

**[!UICONTROL Zukünftige Sitzungen]** - Anzahl der Ereignisse, die am entsprechenden Speicherort auftreten. Klicken Sie auf die Zahl, um die Details in einem Dialogfeld anzuzeigen.

![](assets/sessions-list.png)

*Zukünftige Sitzungen anzeigen*

Im Dialogfeld werden die Details jeder Sitzung angezeigt, einschließlich des Namens der Sitzung, des Namens der Schulung, die die Sitzung enthält, und des Sitzungszeitplans. Die angezeigte Zeit ist mit der Systemzeitzone des Teilnehmers ausgerichtet.

Im Feld **[!UICONTROL Zukünftige Sitzungen]** wird **Null** angezeigt, wenn das Klassenzimmer nicht für eine Sitzung verwendet wird oder wenn das Klassenzimmer früheren Sitzungen zugeordnet ist.

**[!UICONTROL Sitzplatzbeschränkung]** - Zeigt die Sitzplatzkapazität des Klassenzimmers an.

**URL des Speicherorts** - URL, die Sie beim Erstellen des Speicherorts für den Klassenzimmer angegeben haben.

**Standortinformationen** - Die Klassenzimmerinformationen, die Sie beim Erstellen des Klassenzimmers angegeben haben.

### Bearbeiten der Speicherorte der Klassenzimmer

Um die Speicherorte der Klassenzimmer zu bearbeiten, führen Sie die folgenden Schritte aus:

1. Wählen Sie in der Admin-App (der Benutzeroberfläche für Administratorrollen) **[!UICONTROL Einstellungen]** > **[!UICONTROL Standorte für Klassenzimmer]**.

1. Bewegen Sie den Mauszeiger über den gewünschten Speicherort des Klassenzimmers, den Sie bearbeiten möchten.

1. Wählen Sie das Symbol **[!UICONTROL Speicherort des Klassenzimmers bearbeiten]** aus.

1. Ändern Sie den Speicherort des Klassenzimmers und wählen Sie **[!UICONTROL Speichern]**.

## Klassenzimmer über CSV hinzufügen

Alternativ können Sie einen oder mehrere Standorte für Klassenzimmer hinzufügen, indem Sie eine CSV-Datei importieren, die die Informationen zum Klassenzimmer enthält.

Klicken Sie in **[!UICONTROL Admin-App]** > **[!UICONTROL Einstellungen]** > **[!UICONTROL Speicherorte für Klassenzimmer]** > **[!UICONTROL Hinzufügen]** auf die Schaltfläche **[!UICONTROL Speicherorte für Massenimport]**. Navigieren Sie zum Speicherort der CSV-Datei und wählen Sie die Datei aus.

In der CSV-Datei werden diese Felder verwendet, um Details zu einem oder mehreren Standorten für Klassenzimmer zu speichern:

* name
* info
* url
* Region
* seatLimit

Sie können die Kopfzeilen anpassen.

Die CSV-Datei muss zwingend alle Spalten in der hier angegebenen Reihenfolge enthalten.

Nachdem das System die CSV-Datei importiert hat, werden die Standorte der Bibliothek hinzugefügt.

## Nach Klassenzimmern suchen

Um nach Klassenzimmern zu suchen, wählen Sie den Kurs für virtuelle Klassenzimmer aus und gehen Sie zu **[!UICONTROL Instanzen]** > **[!UICONTROL Sitzungen]**. Ein Autor oder Administrator kann mit der Eingabe des Standortnamens beginnen, um die relevanten Ergebnisse anzuzeigen, die angezeigt werden. Sie können dann einen Speicherort aus den angezeigten Ergebnissen auswählen. Wenn in den Ergebnissen des vorausgehenden Typs kein Speicherort angezeigt wird, kann der Benutzer dennoch den Namen des Speicherorts für das neue Klassenzimmer hinzufügen. Beachten Sie, dass der Name des Standorts, der mit dem Arbeitsablauf für die Sitzungserstellung erstellt wurde, nicht der vom Administrator erstellten Standortbibliothek hinzugefügt wird.

Wenn ein Klassenzimmer hinzugefügt wird, zeigt die Lernplattform auch an, ob das Klassenzimmer bereits für den genannten Zeitraum gebucht ist. Es bietet sogar alternative Zeitfenster als Vorschläge an. Dadurch kann der Autor die Besprechungszeit anpassen, wenn er beschließt, denselben Standort für das Klassenzimmer zu verwenden.

![](assets/classroom-search.png)

*Klassenzimmer suchen*

## Administrator

Als Administrator können Sie die Kursleiter und die Kursinstanzen verwalten.

### Einrichten von Kursleitern:

In der Admin-App finden Administratoren unter **[!UICONTROL Einstellungen]** > **[!UICONTROL Allgemein]** die Option **[!UICONTROL Kursleiterverwaltung]**. Diese Funktion stellt sicher, dass nur vorab genehmigte Benutzer, die als Kursleiter zugewiesen wurden, zu Durchführungsveranstaltungen hinzugefügt werden können.

Um einen Kursleiter zuzuweisen, führen Sie die folgenden Schritte aus:

1. Wechseln Sie zur Seite **[!UICONTROL Erste Schritte]** und wählen Sie im linken Fensterbereich **[!UICONTROL Benutzer]** aus.

1. Wählen Sie den gewünschten Benutzer aus.

1. Weisen Sie dem Benutzer die Kursleiterrolle zu, indem Sie **[!UICONTROL Aktionen]** > **[!UICONTROL Rolle zuweisen]** auswählen.

### Sitzungen abbrechen:

Auf der Seite **[!UICONTROL Kursinstanz]** können Administratoren eine oder mehrere Sitzungen abbrechen. Wenn Sitzungen abgebrochen werden, entfernt das System alle Sitzungsdetails, behält aber die Sitzplatzbeschränkung bei.

Darüber hinaus können Administratoren:

* **[!UICONTROL Registrierung anzeigen]**: Erhalten Sie Informationen zu registrierten und auf die Warteliste gesetzten Teilnehmern für jede Sitzung.
* **[!UICONTROL Registrierung von Teilnehmern aufheben]**: Entfernen Sie Teilnehmer aus einem Kurs mit abgebrochenen Sitzungen, ohne ihren Registrierungsstatus zu ändern.
* **[!UICONTROL Anwesenheitsverwaltung]**: Vermerken Sie die Anwesenheit für Sitzungen, selbst wenn die Sitzungen abgebrochen werden.
* **[!UICONTROL Kursabschluss]**: Administratoren können einen Kurs als abgeschlossen markieren, selbst wenn Sitzungen abgebrochen wurden.
* **[!UICONTROL Neuplanung]**: Planen Sie abgebrochene Sitzungen für spätere Termine, und fügen Sie während der Neuplanung einen Kursleiter hinzu.

Beachten Sie, dass die Teilnehmer nach der Kündigung für die Schulungsinstanz registriert bleiben. Ihr Registrierungsstatus - wie bestätigte Registrierung, Warteliste und Genehmigung durch den Manager - bleibt unverändert. Dies ist hilfreich, da der Administrator die abgebrochene Sitzung in Zukunft einrichten und neu planen kann.

## Autor

Wenn der Administrator die Option **[!UICONTROL Kursleiterverwaltung]** auswählt, kann ein Autor die Benutzer mit Kursleiterrolle nur nach den Klassenzimmersitzungen, virtuellen Klassenzimmersitzungen, Checklisten und den Modulen für die Dateiübermittlung suchen und diesen hinzufügen.

Darüber hinaus kann ein Autor:

* Kursleiter zu den bestehenden Sitzungen hinzufügen oder aus ihnen entfernen.
* den bestehenden Sitzungen, die bereits einen oder mehrere Kursleiter haben, Kursleiter hinzufügen.

Nachdem ein Administrator die Option **[!UICONTROL Kursleiterverwaltung]** aktiviert hat, können daher nur die Benutzer mit der Kursleiterrolle als Kursleiter hinzugefügt werden.

>[!NOTE]
>
>Dies gilt nicht, wenn Sie Sitzungen mithilfe der CSV-Datei der Sitzungen migrieren. In diesem Fall kann ein Benutzer, der nicht über die Kursleiterrolle verfügt, als Kursleiter hinzugefügt werden.

Auf der Seite **[!UICONTROL Kursinstanz]** kann ein Autor eine oder mehrere Sitzungen abbrechen. Wenn Sitzungen abgebrochen werden, entfernt das System alle Sitzungsdetails, behält aber die Sitzplatzbeschränkung bei.

Daher kann ein Autor die Links **[!UICONTROL Sitzung abbrechen]** verwenden, um eine oder mehrere Klassenzimmersitzungen oder virtuelle Klassenzimmersitzungen abzubrechen, die in derselben oder in verschiedenen Kursinstanzen verfügbar sind.

## Auf vordefinierte Liste von Kursleitern beschränken

Derzeit können die Benutzer jeden registrierten Benutzer als Kursleiter hinzufügen, wenn sie ein Klassenzimmer oder eine virtuelle Klassenzimmersitzung erstellen. Diese Funktionalität bleibt in dieser Version unverändert.

Administratoren haben jetzt jedoch eine zusätzliche Option, um zu steuern, wer als Kursleiter auf der Lernplattform zugewiesen wird. Dadurch wird verhindert, dass beim Erstellen einer Sitzung versehentlich ein neuer Kursleiter hinzugefügt wird.

## Bestehende Sitzung abbrechen

Ein Autor oder Administrator kann eine Sitzung abbrechen und bei Bedarf neu planen.

Wenn ein Benutzer eine Sitzung abbricht, sendet das System eine E-Mail zum Abbruch der Sitzung an alle registrierten Teilnehmer und Kursleiter. Die E-Mail enthält die aktualisierten Sitzungsdetails.

Es gibt eine Vorlage namens **[!UICONTROL Sitzungsabbruch]** , die das Abbrechen einer Sitzung erleichtert.

Auf der Seite **[!UICONTROL Kursinstanz]** enthält jede Sitzung, die unter einer Kursinstanz aufgelistet ist, eine Option zum Abbrechen der Sitzung.

![](assets/cancel-session.png)

*Vorhandene Sitzung abbrechen*

Wenn Sie auf den Link **[!UICONTROL Sitzung abbrechen]** klicken, erscheint eine Warnmeldung.

Wenn Sie im Dialogfenster mit der Warnmeldung auf **[!UICONTROL Fortfahren]** klicken, bricht das System die Sitzung ab.

Das System löscht auch die folgenden Details, nachdem eine Sitzung abgebrochen wurde:

* Startdatum der Sitzung
* Enddatum der Sitzung
* Startzeit der Sitzung
* Endzeit der Sitzung
* Kursleiter zur Sitzung hinzugefügt
* URL des virtuellen Klassenzimmers
* Standort/Ort der Sitzung hinzugefügt
* Wartelistengrenze, die vom Kursleiter hinzugefügt wurde
