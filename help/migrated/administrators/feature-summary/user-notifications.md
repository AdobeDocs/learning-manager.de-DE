---
jcr-language: en_us
title: Benachrichtigungen
description: Die Benachrichtigungsfunktion gilt für alle Benutzer des Adobe Learning Manager. Jeder Benutzer erhält jedoch basierend auf seiner Rolle in verschiedenen Szenarien unterschiedliche Arten von Benachrichtigungen.
contentowner: manochan
source-git-commit: 147e9edfe323f3d0851880cd401067daa1cee84f
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 0%

---



# Benachrichtigungen

Die Benachrichtigungsfunktion gilt für alle Benutzer des Adobe Learning Manager. Jeder Benutzer erhält jedoch basierend auf seiner Rolle in verschiedenen Szenarien unterschiedliche Arten von Benachrichtigungen. Alle Warnungen und Benachrichtigungen an Benutzer werden über das Popup-Dialogfeld &quot;Benachrichtigungen&quot; angezeigt.

## Auf Benachrichtigungen zugreifen {#accessnotifications}

Benutzer können Benachrichtigungen anzeigen, indem sie auf das Benachrichtigungssymbol in der oberen rechten Ecke des Fensters klicken. Dieses Popup-Dialogfeld zeigt Hervorhebungen aller Benachrichtigungen zusammen mit dem Zeitpunkt des Auftretens mit einer Bildlaufleiste an. Um weitere Informationen zu allen Benachrichtigungen anzuzeigen, klicken Sie unten im Popup-Dialogfeld auf &quot;Alle Benachrichtigungen anzeigen&quot;. Die Seite &quot;Benachrichtigungen&quot; wird angezeigt.

Die Anzahl der neuesten Benachrichtigungen wird durch die markierte Zahl oben auf dem Benachrichtigungssymbol angezeigt. Wenn es beispielsweise nach Ihrer vorherigen Anmeldung fünf neueste Benachrichtigungen gibt, wird die Zahl 5 über dem Benachrichtigungssymbol angezeigt. Diese Nummern werden ausgeblendet, sobald Sie alle neuesten Benachrichtigungen gelesen haben.

## Benachrichtigungstypen für Administratoren {#typesofnotificationsforadministrators}

Administratoren erhalten Benachrichtigungen in folgenden Fällen:

* Immer, wenn eine CSV-Benutzerliste erfolgreich hochgeladen wurde.
* Immer, wenn der Upload einer CSV-Benutzerliste nicht erfolgreich ist. Der Administrator erhält eine Meldung mit dem Grund für den Fehler.
* Der Administrator kann auch Benachrichtigungen auf Instanzebene für Kurse und Lernprogramme einrichten. In diesem Fall erhält der Administrator die Benachrichtigungen entsprechend der auf Instanzebene ausgewählten Häufigkeit.

>[!NOTE]
>
>Wenn ein Administrator zusätzlich zu seiner Rolle über Autoren- oder Managerberechtigungen verfügt, erhält der Administrator Benachrichtigungen für jede Rolle.

Ein Beispiel-Benachrichtigungsfenster für die Administratorrolle wird im folgenden Screenshot angezeigt:

![](assets/admin-notification.png)

*Administratorbenachrichtigungen anzeigen*

In diesem Popupfenster werden Markierungen aller Benachrichtigungen zusammen mit dem Zeitpunkt des Auftretens und einer Bildlaufleiste angezeigt. Die Anzahl der neuesten Benachrichtigungen wird durch die markierte Zahl oben auf dem Benachrichtigungssymbol angezeigt. Wenn es beispielsweise nach Ihrer vorherigen Anmeldung fünf neueste Benachrichtigungen gibt, wird die Zahl 5 über dem Benachrichtigungssymbol angezeigt. Diese Nummern werden ausgeblendet, sobald Sie alle neuesten Benachrichtigungen gelesen haben.

Klicken **[!UICONTROL Alle Benachrichtigungen anzeigen]** am unteren Rand des Benachrichtigungs-Popup-Fensters, um alle Benachrichtigungen auf einer separaten Seite anzuzeigen.

## Eskalationsbenachrichtigungen auf mehreren Ebenen einrichten {#setupmultilevelescalationnotifications}

Eskalations-E-Mails, wenn Teilnehmer Fristen nicht einhalten, können an den Manager und einen Skip-Manager gesendet werden. Sie können mehrstufige Eskalationsbenachrichtigungen für den nicht abgeschlossenen Kurs während des Erstellungsprozesses oder sogar nach der Erstellung eines Kurses einrichten. Eskalationsbenachrichtigungen können so eingerichtet werden, dass sie mit einer festgelegten Häufigkeit an einen Manager oder einen Skip-Manager gesendet werden.

1. Melden Sie sich als Administrator oder Autor an und klicken Sie auf &quot;Kurse&quot;.
1. Wählen Sie den Kurs aus, für den Sie die Eskalationsbenachrichtigungen ändern möchten, und klicken Sie auf **[!UICONTROL Kurs anzeigen]**.

   ![](assets/view-courses.png)

   *Wählen Sie die Option Kurs anzeigen*

1. Klicken Sie auf **[!UICONTROL Instanzen]** > **[!UICONTROL Benachrichtigungswarnungen]**.

   ![](assets/notification-alert.png)

   *Wählen Sie die Option Benachrichtigungswarnungen.*

1. Es wird ein Kalender geöffnet, der die Frist angibt, die für den rot hervorgehobenen Kurs festgelegt wurde. Klicken Sie auf das hervorgehobene Datum, um die Erinnerungen für den Teilnehmer festzulegen.

   ![](assets/deadline-calender.png)

   *Fristerinnerungen anzeigen*

1. Legen Sie Erinnerungen fest, indem Sie Datumsangaben auswählen, die vor dem Stichtag liegen. Auf diese Weise können Sie Erinnerungen für den Teilnehmer an den nahenden Termin einrichten.

   ![](assets/deadline-reminder.png)

   *Termin für Erinnerung festlegen*

1. Wählen Sie ein Datum nach Ablauf der Frist aus, um einen Zeitplan mit Erinnerungen für den Teilnehmer und Eskalationsbenachrichtigungen an den Manager einzurichten.

   ![](assets/set-reminders-andescalation.png)

   *Erinnerungen und Eskalationsdaten festlegen*

1. Wenn der Teilnehmer den Kurs auch nach der Eskalation an den Manager immer noch nicht abschließt, können Sie mit den Einstellungen zum Skip-Manager des Teilnehmers eskalieren. Klicken Sie auf ein Datum nach Ablauf der verlängerten Frist, wählen Sie die Wiederholung von Erinnerungen, die Anzahl der Tage für den Zeitplan und wählen Sie **Manager und Manager zum Überspringen von Levels** in der &quot; **Eskalation** Dropdown-Liste. Klicken Sie auf das blaue Häkchen, um die Benachrichtigungseinstellungen zu speichern.

   ![](assets/reminder-to-managerandskipmanager.png)

   *Benachrichtigungseinstellungen speichern*

## Häufig gestellte Fragen {#frequentlyaskedquestions}

+++Wie richte ich Erinnerungsbenachrichtigungen für die Instanz ein?

Klicken Sie in einer Instanz auf Benachrichtigungswarnungen. Es wird ein Kalender geöffnet, der die Frist angibt, die für den rot hervorgehobenen Kurs festgelegt wurde. Klicken Sie auf das hervorgehobene Datum, um die Erinnerungen für den Teilnehmer festzulegen. Legen Sie die Erinnerungen fest, wie in diesem [Abschnitt](user-notifications.md#Setupmultilevelescalationnotifications).
+++
