---
description: Lesen Sie den Artikel zum Konfigurieren von E-Mail-Vorlagen für die Ereignisse, die sich auf alle Lernobjekte beziehen.
jcr-language: en_us
title: E-Mail-Vorlagen
exl-id: 3b17f889-52be-4073-ab91-7c76dd79f1d2
source-git-commit: 6862dc1958a34a369f0e0e7218f28151a47beb3b
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 72%

---

# E-Mail-Vorlagen

Lesen Sie den Artikel zum Konfigurieren von E-Mail-Vorlagen für die Ereignisse, die sich auf alle Lernobjekte beziehen.

Learning Manager verschickt E-Mail-Benachrichtigungen ereignisgesteuert an mehrere Benutzerrollen.

Als Autor können Sie E-Mail-Vorlagen anpassen, indem Sie Inhalte hinzufügen oder modifizieren und Benachrichtigungen an Benutzer für verschiedene Ereignisse, die von Teilnehmern, Managern und Autoraktivitäten ausgelöst wurden, senden. Beispielsweise können Sie eine E-Mail senden, wenn sich ein Teilnehmer bei Ihren Kurs anmeldet. Bei Anmeldung erhält der Teilnehmer die kurzspezifische E-Mail automatisch.

Die Administratoren können auch festlegen, dass bei bestimmten Ereignissen keine E-Mail-Benachrichtigungen gesendet werden.

## Konfigurieren von E-Mail-Benachrichtigungen {#settingemailnotifications}

1. Wählen Sie in der Autoren-App das Lernobjekt aus, für das Sie die E-Mail-Vorlage konfigurieren möchten. Beispiel: Kurse.

1. Klicken Sie auf der Lernobjektseite auf den Kurs, die Zertifizierung oder das Lernprogramm, für den/die/das Sie die E-Mail-Vorlage konfigurieren möchten.

1. Wählen Sie auf der Lernobjektdetailseite **E-Mail-Vorlagen** > **Alle Vorlagen**. E-Mail-Vorlagen sind verfügbar für **Standardinstanz** und **Aktueller Kurs**. Sie können zwischen ihnen wechseln, indem Sie das Dropdown-Menü in der oberen rechten Ecke verwenden.

   Sie können die Liste der Vorlagen sehen, die für das von Ihnen gewählte Lernobjekt verfügbar sind.

   ![](assets/email-templates-forlearningprograms.png)
   *Vorlagenliste*

1. Klicken Sie auf den Namen eines Ereignisses, um die Vorlage im Vorschaumodus anzuzeigen.

   ![](assets/preview-the-emailtemplateforyourlearningobject.png)

   *Vorschau der Vorlage anzeigen*

   Sie können die Vorlagen ändern, indem Sie in ihrem Hauptteil auf den Text klicken. Sie können in den Text Variablen einfügen, indem Sie auf die entsprechenden Symbole klicken (siehe Abbildung). Um die Namen der Symbole anzuzeigen, zeigen Sie mit der Maus darauf.

   ![](assets/insert-variable.png)
   *Einfügen von Variablen*

   Folgende Variablen stehen zur Verfügung:

   * LPName
   * LPCompletionDeadline
   * LearnerName
   * LearnerEmail
   * CourseName
   * CourseDescription
   * CourseCompletionDeadline
   * CourseSkillDetails
   * CourseBadge

   Sie können den Inhalt der Benachrichtigungen zurücksetzen, indem Sie über der Vorlage auf den Link „Original wiederherstellen“ klicken.

   Wie Sie oben in der Vorlage sehen, können Sie die Vorlage je nach Typ der E-Mail-Benachrichtigung für mehrere Rollen (Manager, Teilnehmer usw.) anpassen.

1. Klicken Sie am unteren Rand der Seite „Vorlagen“ auf „Speichern“.
1. Klicken Sie auf der Seite mit der E-Mail-Vorlage auf die Kreisschaltfläche „Ja/Nein“, um die Benachrichtigung zu senden bzw. zu deaktivieren.

![](assets/email-notification-e1437624109719.png)
*E-Mail-Benachrichtigung aktivieren oder deaktivieren*

Wenn der Kreis in der Benachrichtigungsschaltfläche für den Namen eines Ereignisses bei „Ja“ steht und die Schaltfläche blau dargestellt wird, ist die Benachrichtigung aktiviert. Wenn sie grau dargestellt wird und der Kreis bei „Nein“ steht, ist die Benachrichtigung deaktiviert.

Wenn Sie eine E-Mail-Vorlage auf Kursebene konfigurieren, erhält diese Vorrang über die Einstellungen auf Administratorebene für diesen Kurs.

## Einstellungen für E-Mail-Vorlagen

Der Autor kann in den E-Mail-Vorlageneinstellungen Folgendes einrichten:

* **Email Banner**: Ermöglicht Ihnen, das E-Mail-Banner zu ändern.

* **E-Mail-Signatur**: Ermöglicht Ihnen, die E-Mail-Signatur hinzuzufügen oder zu bearbeiten.
