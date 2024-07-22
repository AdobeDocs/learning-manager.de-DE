---
description: Erstellen von Lernplänen für Administratoren in Learning Manager.
jcr-language: en_us
title: Lernpläne
contentowner: manochan
exl-id: 99e3d2f5-0bf0-4f4e-8874-8136af7c592a
source-git-commit: 2a841234cd829d2a477d44e9cca095370ee25e51
workflow-type: tm+mt
source-wordcount: '1621'
ht-degree: 62%

---

# Lernpläne

Erstellen von Lernplänen für Administratoren in Learning Manager.

## Übersicht {#overview}

Ein Lernplan ist eine Reihe von Regeln, die Teilnehmer zu bestimmten Schulungen auf der Grundlage bestimmter Kriterien registrieren.

Ein Lernplan ermöglicht es einem Administrator, Kurse, Lernprogramme oder Zertifizierungen automatisch zuzuweisen, basierend auf dem Auftreten bestimmter Ereignisse wie dem Einsteigen eines neuen Mitarbeiters oder der Änderung der Bezeichnung oder des Standorts des Mitarbeiters.

Wenn beispielsweise ein Mitarbeiter einer Organisation beitritt, wird das Programm zur Orientierung neuer Mitarbeiter dem Mitarbeiter automatisch zugewiesen. Wenn ein Mitarbeiter zum Manager befördert wird, wird dem Mitarbeiter automatisch ein neues Manager-Orientierungsprogramm zugewiesen.

Sie können Teilnehmer anhand eines vordefinierten Satzes von Ereignissen automatisch für beliebige Kurse und Lernprogramme registrieren. Sie können für die Teilnehmer Lernpläne erstellen, indem eine Anschluss-Lernaktivität automatisch zugewiesen wird, nachdem ein Teilnehmer eine Qualifikation, einen Kurs oder ein Lernprogramm abschließt.

## Lernpläne erstellen {#createlearningplans}

Um einen Lernplan zu erstellen, müssen Sie sich als Administrator anmelden.

1. Klicken Sie im linken Teilfenster auf **[!UICONTROL Lernpläne]**. Wenn bereits Ereignisse definiert sind, werden sie auf der Seite angezeigt. Wenn Sie jedoch die Lernplanfunktion zum ersten Mal einrichten, fahren Sie mit dem nächsten Schritt fort.
1. Klicken Sie oben rechts auf der Seite auf **[!UICONTROL Hinzufügen]**. Geben Sie im Dialogfeld **[!UICONTROL Lernplan hinzufügen]** den Namen des Lernplans ein, den ein Mitarbeiter annehmen muss.

   ![](assets/add-learning-plandialog.png)

1. Wählen Sie in der Dropdown-Liste **[!UICONTROL Tritt ein, wenn]** das gewünschte Ereignis aus. Die Optionen bestimmen, wann ein Teilnehmer den Kurs besucht. Wählen Sie nach Auswahl des Ereignistyps die entsprechende Schulung, Kurse, das Lernprogramm oder die Zertifizierung aus.

>[!NOTE]
>
> Sowohl Administratoren als auch Autoren können Ereignisse für die automatische Registrierung erstellen.


Die Ereignisse sind:

**1 - Neuer Teilnehmer wird hinzugefügt:** Wenn ein neuer Benutzer oder ein Mitarbeiter der Organisation beitritt.

![](assets/new-learner-is-added.png)

**2 - Teilnehmer wird einer Gruppe hinzugefügt:** Wenn ein neuer Benutzer oder ein Mitarbeiter einer Gruppe beitritt.  Geben Sie die Benutzergruppe aus der Dropdownliste, für die dieses Ereignis gilt, ein. Sie können mehrere Gruppen auswählen. Sie können dieses Ereignis allen vorhandenen Mitgliedern dieser Gruppen zuweisen, indem Sie die Option auswählen.

![](assets/learner-gets-addedtoagroup.png)

Dieser Lernplan ist speziell für Benutzer von ***Benutzerdefinierte Gruppe*** konzipiert. Geben Sie den Namen der Gruppe in das Feld ein und wählen Sie die Gruppe(n) mit der Voraussuchfunktion aus.

**3 - Teilnehmer wird aus einer Gruppe entfernt:** Das Ereignis wird ausgelöst, wenn ein Benutzer oder Teilnehmer aus einer Gruppe entfernt wird. Geben Sie die Benutzergruppe aus der Dropdownliste, für die dieses Ereignis gilt, ein. Sie können mehrere Gruppen auswählen.

![](assets/learner-removed-from-group.png)


**4 - Teilnehmer schließt einen Kurs/einen Lernpfad/eine Zertifizierung ab:** Das Ereignis wird ausgelöst, wenn Teilnehmer Lernobjekte wie Kurse, Lernprogramme usw. beenden. Wählen Sie das Lernobjekt, für das dieses Ereignis gilt. Wählen Sie den Abschlussstatus für das Ereignis. Optional können Sie außerdem die Benutzergruppe auswählen, zu der dieser Benutzer gehört. Wenn Sie die Anzahl der Tage nach dem Abschluss des Lernobjekt eingeben, wird dieses Ereignis ausgelöst. Wählen Sie die Option, wenn Sie dieses Ereignis vorhandenen Benutzern zuweisen möchten, die bereits das Lernobjekt abgeschlossen haben.

![](assets/learner-completealearningobject.png)

**5 - Der Teilnehmer schlägt ein Modul eines Kurses fehl:** Das Ereignis wird ausgelöst, wenn ein Teilnehmer ein Lernobjekt wie einen Kurs, ein Lernprogramm usw. ausfällt. Wählen Sie das Lernobjekt, für das dieses Ereignis gilt. Sie können auch die Benutzergruppe auswählen, zu der dieser Teilnehmer gehört.

![](assets/learner-fails-module.png)

**4 - Der Teilnehmer erreicht eine Qualifikationsstufe:** Geben Sie den Namen der Qualifikation ein und wählen Sie die Qualifikationsstufe aus. Sie können außerdem die Benutzergruppe auswählen, zu der dieser Benutzer gehört. Dies ist optional. Wenn Sie die Anzahl der Tage nach dem Erwerb der Kenntnisse eingeben, wird dieses Ereignis ausgelöst. Wählen Sie die Option, wenn Sie dieses Ereignis vorhandenen Teilnehmern zuweisen möchten, die bereits diese Qualifikation erzielt haben.

![](assets/learner-achievesaskilllevel.png)

Legen Sie außerdem die Anzahl der Tage fest, nach denen der Lernplan den Teilnehmern zugewiesen werden muss.

![](assets/assign-learning.png)

**5 - An einem bestimmten Datum:** Wenn die Ereignisse an einem bestimmten Datum auftreten müssen. Wählen Sie das Datum aus, an dem das Ereignis zugewiesen werden muss. Wählen Sie die Benutzergruppen, für die das Ereignis automatisch zugewiesen werden muss. Wählen Sie die Instanzen, die zugewiesen werden müssen, und geben Sie optional ein, nach wie vielen Tagen das Ereignis ausgelöst werden muss.

![](assets/on-a-specific-date.png)

1. Für alle Ereignisse können Sie die Instanz aus der Dropdownliste **[!UICONTROL Instanz wählen]** auswählen. Sie können für jedes Ereignis auch Instanzen des zugewiesenen Teilnehmers auswählen.

   ![](assets/choose-instance.png)

   In Learning Manager erstellt ein Lernplan seine eigene Instanz, Auto. Wenn Sie eine Gruppe auswählen, z. B. „Alle Teilnehmer“, werden standardmäßig alle Teilnehmer im Lernplan für die Instanz „Auto“ registriert.

   Wenn Sie den Lernplan speichern, wird die Instanz „Automatisch“ als Option in der Dropdown-Liste **[!UICONTROL Instanz auswählen]** im Abschnitt „Teilnehmer“ eines Kurses angezeigt.

1. Um den Lernplan zu speichern, klicken Sie auf **[!UICONTROL Speichern]**.

## Registrierung für Schulung widerrufen {#unenroll-training}

Beim Hinzufügen eines Lernplans kann ein Administrator die Registrierung von Benutzern für bestimmte Schulungen auf der Grundlage bestimmter Auslöser aufheben.

Klicken Sie in der Admin-App auf **[!UICONTROL Lernpläne]** > **[!UICONTROL Hinzufügen]**.

In den folgenden Abschnitten werden die Auslöser aufgeführt, in denen die Option **[!UICONTROL Registrierung für Schulung widerrufen]** hinzugefügt wurde.

![](assets/unenroll-courses.png)

## Teilnehmer wird aus einer Gruppe entfernt {#learnergetsremovedfromagroup}

1. Fügen Sie eine oder mehrere Benutzergruppen hinzu. Wenn mehrere Gruppen ausgewählt sind, wird der Plan ausgelöst, wenn ein Teilnehmer aus einer der genannten Gruppen entfernt wird.
1. Wählen Sie die Aktion &quot;**[!UICONTROL Registrierung für Schulung widerrufen]**&quot;.

   1. Der Administrator kann die Schulungen auswählen, für die die Registrierung des Benutzers widerrufen wird, wenn er aus der Benutzergruppe entfernt wird.
   1. Das Instanz- und Abschlussdatum gelten in diesem Szenario nicht.

![](assets/image038.png)

## Teilnehmer hat eine Schulung abgeschlossen {#learnercompletesatraining}

1. Fügen Sie eine oder mehrere Benutzergruppen hinzu. Wenn mehrere Gruppen ausgewählt sind, wird der Plan ausgelöst, wenn ein Teilnehmer die angegebene Schulung abschließt.
1. Wählen Sie die Aktion &quot;**[!UICONTROL Registrierung für Schulung widerrufen]**&quot;.

   1. Der Administrator kann die Schulungen auswählen, für die die Registrierung des Benutzers widerrufen wird, wenn er der Benutzergruppe hinzugefügt wird.
   1. Das Instanz- und das Abschlussdatum gelten in diesem Fall nicht.

![](assets/image040.png)

## Lernende/r besteht ein Modul eines Kurses nicht

1. Fügen Sie eine oder mehrere Benutzergruppen hinzu. Wenn mehrere Gruppen ausgewählt sind, wird der Plan ausgelöst, wenn ein Teilnehmer die angegebene Schulung nicht besteht.
1. Wählen Sie die Aktion &quot;**[!UICONTROL Registrierung für Schulung widerrufen]**&quot;.

   1. Der Administrator kann die Schulungen auswählen, für die die Registrierung des Benutzers widerrufen wird, wenn er der Benutzergruppe hinzugefügt wird.
   1. Das Instanz- und das Abschlussdatum gelten in diesem Fall nicht.

## Teilnehmer wird zu einer Gruppe hinzugefügt {#learnergetsaddedtoagroup}

1. Fügen Sie eine oder mehrere Benutzergruppen hinzu. Wenn mehrere Gruppen ausgewählt sind, wird der Plan ausgelöst, wenn ein Teilnehmer einer der genannten Gruppen hinzugefügt wird.
1. Wählen Sie die Aktion „Registrierung für Schulung widerrufen“.

   1. Der Administrator kann die Schulungen auswählen, für die die Registrierung des Benutzers widerrufen wird, wenn er der Benutzergruppe hinzugefügt wird.
   1. Das Instanz- und das Abschlussdatum gelten in diesem Fall nicht.

![](assets/image043.png)

## Teilnehmer erreicht Kenntnisstufe {#learnerachievesaskilllevel}

1. Geben Sie die zu erreichende Kenntnis an.
1. Fügen Sie eine oder mehrere Benutzergruppen hinzu. Wenn mehrere Gruppen ausgewählt sind, wird der Plan ausgelöst, wenn ein Teilnehmer die ausgewählte Kenntnis erworben hat.

![](assets/image045.png)

## An einem bestimmten Datum {#onaspecificdate}

1. Wählen Sie das Datum aus, an dem die Registrierung des Teilnehmers widerrufen werden soll.
1. Fügen Sie eine oder mehrere Benutzergruppen hinzu. Wenn mehrere Gruppen ausgewählt sind, wird der Plan am Tag ausgelöst und die Registrierung der Benutzer widerrufen, die Teil der ausgewählten Gruppen sind.
1. Wählen Sie die Aktion „Registrierung für Schulung widerrufen“.

   1. Der Administrator kann die Schulungen auswählen, für die die Registrierung des Benutzers am angegebenen Datum widerrufen wird.
   1. Das Instanz- und das Abschlussdatum gelten in diesem Fall nicht.

![](assets/image047.png)

## Lernplan bearbeiten {#editalearningplan}

Nach dem Erstellen eines Lernplans kann der Administrator den Lernplan jederzeit bearbeiten/aktualisieren. Wählen Sie zum Bearbeiten den Namen des Lernplans aus und ändern Sie die Werte im daraufhin angezeigten Popup-Dialogfeld &quot;**[!UICONTROL Lernplan bearbeiten]**&quot;.  Wählen Sie **[!UICONTROL Speichern]**.

>[!NOTE]
>
>Sie können die Option &quot;**[!UICONTROL Tritt auf, wenn &quot;]**&quot; im Popup &quot;**[!UICONTROL Lernplan bearbeiten&quot; &quot;]**&quot; nicht ändern.


## Lernplan aktivieren {#enablealearningplan}

Standardmäßig sind alle neuen Lernpläne, die Sie erstellt haben, deaktiviert. Sie müssen einen Plan aktivieren, dem ein Teilnehmer zugewiesen werden soll. Wenn Sie das Kontrollkästchen **[!UICONTROL Aktuelle Teilnehmer]** aktivieren, wird das Ereignis von selbst aktiviert.

Um einen Lernplan zu aktivieren,

1. Wählen Sie aus der Liste der Lernpläne den Plan aus, den Sie aktivieren möchten.

   ![](assets/list-of-learningplans.png)

1. Klicken Sie oben rechts auf der Seite auf **[!UICONTROL Aktionen]** > **[!UICONTROL Aktivieren]**. Dies aktiviert den Lernplan.

## Lernplan löschen {#deletealearningplan}

Um einen Lernplan zu löschen,

1. Wählen Sie in der Liste der Lernpläne den Plan aus, den Sie löschen möchten.
1. Klicken Sie oben rechts auf der Seite auf **[!UICONTROL Aktionen]** > **[!UICONTROL Löschen]**.

## Lernplan deaktivieren {#disablealearningplan}

Um einen Lernplan zu deaktivieren,

1. Klicken Sie auf die Registerkarte **[!UICONTROL Aktiviert]**.
1. Wählen Sie in der Liste der Lernpläne den Plan aus, den Sie deaktivieren möchten.
1. Klicken Sie oben rechts auf der Seite auf **[!UICONTROL Aktionen]** > **[!UICONTROL Deaktivieren]**. Dadurch wird der Plan auf die Registerkarte **[!UICONTROL Deaktiviert]** verschoben.

## Lernplan filtern {#filteralearningplan}

Sie können Lernpläne nach der Art des Ereignisses filtern, das beim Erstellen eines Lernplans verwendet wurde. Klicken Sie auf **[!UICONTROL Typ]** und wählen Sie eine beliebige Option aus, um Lernpläne anzuzeigen, die der Auswahl entsprechen.

![](assets/filter-a-learningplan.png)

## Häufig gestellte Fragen {#frequentlyaskedquestions}

1. Wie richte ich den Learning Manager ein, um die automatische Registrierung für die Aufnahme neuer Mitarbeiter zu konfigurieren?

   Wählen Sie in der Dropdownliste **[!UICONTROL Tritt auf, wenn]** die Option **[!UICONTROL Neuer Teilnehmer hinzugefügt]** aus. Ordnen Sie dann die Lernobjekte, die Instanz und das Abschlussdatum für den Teilnehmer zu. Sowohl Administratoren als auch Autoren können Ereignisse für die automatische Registrierung erstellen. Aktivieren Sie das Ereignis, nachdem Sie es erstellt haben.

1. Wie richte ich einen Lernplan/eine automatische Registrierung für den Unterricht und den virtuellen Unterrichtskurs ein?

   Es wird empfohlen, die Kursinstanz mit den erforderlichen Sitzungsdetails einzurichten. Richten Sie dann einen Lernplan ein und ordnen Sie ihn der bereits erstellten Kursinstanz zu.

1. Wie kann ich die Liste der Teilnehmer anzeigen, die bei einem bestimmten Lernplan registriert sind?

   Wenn die Instanz &quot;Auto&quot; erstellt wird, klicken Sie auf **[!UICONTROL Kurs]** > **[!UICONTROL Teilnehmer]** und wählen Sie die gewünschte Instanz aus der Dropdown-Liste **[!UICONTROL Instanz]** aus.
