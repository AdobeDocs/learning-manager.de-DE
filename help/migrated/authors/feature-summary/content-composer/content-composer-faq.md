---
description: Hier finden Sie Antworten auf häufig gestellte Fragen von Content Composer zur Gliederungsbearbeitung, zum Quizverhalten, zur Captivate-Kompatibilität, zur Veröffentlichung und zur Freigabe für Reviewer.
jcr-language: en_us
title: Häufige Fragen zu Adobe Learning Manager Content Composer
source-git-commit: 68d15fa96588b2569c9b1cdb480e2ba9f31a1cf6
workflow-type: tm+mt
source-wordcount: '1438'
ht-degree: 0%

---


# Häufige Fragen zu Adobe Learning Manager Content Composer

Hier erhalten Sie Antworten auf häufig gestellte Fragen zur Verwendung von Content Composer.

**Die Schaltfläche &quot;Gliederung generieren&quot; ist ausgegraut. Was kann ich tun?**

Alle drei **Brief**-Felder, **Titel**, **Teilnehmer** und **Ziel** müssen Inhalte enthalten, bevor **Gliederung generieren** aktiviert wird. Überprüfen Sie die Arbeitsfläche für alle Felder, in denen Platzhaltertext noch kursiv angezeigt wird, wie z. B. *Geben Sie hier das Teilnehmerprofil ein* oder *Geben Sie das Ziel dieses Kurses ein*. Füllen Sie das leere Feld aus, und die Schaltfläche wird sofort aktiviert.

**Ich kann die Gliederung nicht auswählen, um eine Lektion umzubenennen. Warum?**

Die Bearbeitung von Gliederungen ist in der aktuellen Beta-Version gesprächig. Sie können auf der Arbeitsfläche keine Lektion oder kein Thema auswählen, um sie umzubenennen oder neu zu ordnen. Geben Sie Ihre Änderung im Assistant-Chat-Bereich in einfacher Sprache ein.

Beispiele:

- &quot;Benennen Sie Lektion 1 in &#39;Wie Phishing funktioniert&#39; um&quot;

- &quot;Bewegen Sie Thema 1.3 zum ersten Thema in Lektion 2&quot;

- &quot;Löschen Sie Lektion 4, und verteilen Sie die Themen auf Lektion 3.&quot;

**Die generierte Gliederung stimmt nicht mit dem überein, was ich wollte. Was ist schief gegangen?**

Der Umriss spiegelt die Eingabeaufforderung und den Kurzbefehl wider. Wenn die Struktur nicht passt, sind die häufigsten Ursachen eine Eingabeaufforderung, die zu viele Themen gleichzeitig abdeckt, oder ein Lernziel, das die spezifischen Fähigkeiten oder Verhaltensweisen, die der Kurs entwickeln sollte, nicht benennt.

**Die AI hat einen wichtigen Abschnitt meiner hochgeladenen Datei übersprungen. Wie kann ich das beheben?**

Content Composer priorisiert Abschnitte der Quelldatei, die für Ihr Lernziel am relevantesten sind. Wenn ein Abschnitt übersprungen wurde, wurde er wahrscheinlich nicht im Ziel widergespiegelt.

So beheben Sie dieses Problem:

1. Kehren Sie zum Bereich &quot;**Brief**&quot; zurück und aktualisieren Sie das Ziel, das fehlende Thema explizit zu benennen.

2. Bitten Sie den Assistenten, die Gliederung neu zu generieren: &quot;Generieren Sie die Gliederung neu, und stellen Sie sicher, dass der Abschnitt zur Datenaufbewahrungsrichtlinie enthalten ist.&quot;

Sie können den fehlenden Inhalt auch manuell als neues Thema in die Konversation mit der Gliederung einfügen: &quot;Fügen Sie in Lektion 2 ein neues Thema mit dem Titel &#39;Datenaufbewahrungsrichtlinie&#39; hinzu.&quot;

**Kann ich Content Composer mit Adobe Captivate verwenden?**

Anzahl Content Composer und Adobe Captivate verwenden keinen gemeinsamen Roundtripping-Workflow. Sie können Content Composer-Projekte nicht auf dem Captivate öffnen und Sie können Captivate-Projekte nicht im Content Composer öffnen.

Eine von der Captivate exportierte MP4-Datei kann als **Video**-Komponente in den Inhaltskomposer eingefügt werden.

**Kann ich Content Composer für Compliance- oder regulierte Schulungen verwenden?**

Ja. Dies ist einer ihrer stärksten Fälle. Laden Sie Ihre Richtlinien- oder Verfahrensdokumente unter &quot;Quelldateien verwalten&quot; hoch und wählen Sie &quot;Ausgabe auf Inhalte in Dateien beschränken&quot;, damit die KI nur auf Grundlage der bereitgestellten Informationen generiert, anstatt sie mit allgemeinen Kenntnissen zu ergänzen.

**Warum werden die Wissensüberprüfungen nicht bewertet?**

Wissensüberprüfungen in &quot;Inhaltszusammenstellung&quot; wurden zur Verbesserung des Lernfortschritts während einer Lektion entwickelt, nicht zur Bewertung. Sie geben dem Teilnehmer sofortiges Feedback, erstellen aber keinen Prüfungs- oder Abschlussbericht.

Nur Quizbewertungen am Ende der Lektion werden bewertet. Wenn Sie eine Bewertung benötigen, die zur Punktzahl eines Teilnehmers beiträgt, verwenden Sie das Quiz, nicht eine Komponente der Wissensüberprüfung.

**Die Quizfragen stimmen nicht mit den vom Kurs vermittelten Informationen überein. Wie kann ich das beheben?**

Der Content Composer verwendet KI zum Generieren von Quizfragen, und die KI-Ausgabe ist nicht deterministisch. Die Fragen spiegeln möglicherweise nicht immer genau das wider, was Sie erwarten. Überprüfen Sie alle Quizfragen, nachdem der Kurs generiert wurde, bearbeiten Sie alle Fragen, die angepasst werden müssen, direkt im Kurs-Editor und überprüfen Sie, ob der Inhalt vor der Veröffentlichung korrekt ist.

## Informationen zum Freigeben für Reviewer

**Was ist &quot;Zur Überprüfung freigeben&quot; in &quot;Inhaltszusammenstellung&quot;?**

Mit &quot;Für Review freigeben&quot; können Sie einen Kurs vor der Veröffentlichung an Reviewer weitergeben, um Feedback zu erhalten. Prüfer öffnen den Kurs in einem Browser, fügen Kommentare zu einer beliebigen Komponente hinzu und wiederholen das Quiz, ohne Content Composer installieren zu müssen oder ein Abonnement zu benötigen.

**Benötigen die Überprüfer eine Lizenz für den Inhaltsersteller?**

Anzahl Prüfer benötigen kein Content Composer-Abonnement oder keine Installation. Jeder Benutzer, der über den Überprüfungslink verfügt, kann den Kurs in seinem Browser öffnen.

**Benötigen die Überprüfer eine Adobe ID, um daran teilzunehmen?**

Ja. Um einen Kurs zu überprüfen, müssen Sie sich anmelden, daher ist eine Adobe ID erforderlich. Nach der Anmeldung können Reviewer den Kurs öffnen, Kommentare hinzufügen, das Quiz absolvieren und @mentions verwenden, um den Autor oder andere Reviewer mit Tags zu versehen.

**Können Überprüfer den Kursinhalt bearbeiten?**

Anzahl Der Überprüfungszugriff ist schreibgeschützt. Die Reviewer können Kommentare hinzufügen, beantworten, schließen und filtern, aber den Kurstext, die Bilder oder die Struktur nicht ändern.

Wo werden Überprüfungsdateien gespeichert? Überprüfungsdateien werden in der Cloud von Adobe gehostet. Autoren müssen den Dateispeicher nicht verwalten und Kursdateien nicht direkt an die Reviewer senden.

### Freigabe und Zugriff

**Wer kann auf einen Überprüfungslink zugreifen?**

Standardmäßig können nur Personen, die Sie per Name oder E-Mail einladen, auf das Projekt zugreifen. Überprüfen Sie dies im Abschnitt Wer hat Zugriff? des Bedienfelds &quot;Projekt freigeben&quot;, bevor Sie den Link senden.

**Kann ich externe Stakeholder einladen, die keine Adobe-Benutzer sind?**

Ja, Sie können jeden per E-Mail einladen. Sie benötigen jedoch ein Adobe-Konto, um sich anzumelden und den Kurs zu überprüfen.

**Kann ich Reviewer hinzufügen, nachdem der Review bereits gestartet wurde?**

Ja. Sie können das Bedienfeld &quot;Projekt freigeben&quot; jederzeit öffnen, Namen oder E-Mail-Adressen hinzufügen und zum Kommentieren einladen auswählen. Neue Prüfer erhalten sofort eine Einladung.

**Kann ich einen Prüfer nach der Freigabe entfernen?**

Ja. Suchen Sie im Bedienfeld Projekt freigeben unter Wer hat Zugriff auf den Reviewer und entfernen Sie ihn. Wenn sie versuchen, den Kurs mit einem zuvor freigegebenen Link zu öffnen, wird eine Meldung angezeigt, dass ihnen der Zugriff verweigert wurde.

**Was passiert, wenn ein Überprüfer den Zugriff verliert?**

Sie können auf dem Bildschirm Zugriff verweigert die Option Zugriff anfordern auswählen. Der Kurseigentümer erhält eine Benachrichtigung, dass der Zugriff wiederhergestellt werden muss.

### Kommentare und Feedback

Können Überprüfer einen bestimmten Teil des Kurses kommentieren?

Ja. Prüfer wählen eine beliebige Kurskomponente aus (Textblock, Bild oder Quizfrage) und fügen direkt zu diesem Element einen Kommentar hinzu. Kommentare bleiben im Kontext mit der Komponente verknüpft, der sie hinzugefügt wurden.

**Können mehrere Prüfer gleichzeitig Kommentare abgeben?**

Ja. Alle Reviewer sehen die Kommentare des jeweils anderen im Bedienfeld &quot;Kommentare&quot; und können jeweils antworten, klären oder @mention.

**Kann ich Kommentare filtern, um ungelöstes Feedback zu finden?**

Ja. Verwenden Sie den Filter Geklärt im Bereich Kommentare , um nur ungelöste Kommentare anzuzeigen. Sie können auch nach Reviewern filtern, um Feedback von einer bestimmten Person anzuzeigen, oder nach Zeit, um die neuesten Kommentare zu finden.

**Wie kann ich einen anderen Überprüfer in einem Kommentar mit Tags versehen?**

Geben Sie @ gefolgt vom Namen oder der E-Mail-Adresse ein und wählen Sie sie aus der Dropdown-Liste aus. Benutzer mit Tags erhalten eine Benachrichtigung. Dazu muss sich der Reviewer mit einer Adobe ID anmelden.

#### Quiz und Teilnehmerzugriff

**Können Überprüfer das Quiz durchführen?**

Ja. Reviewer können das Quiz bis zur angegebenen Anzahl von Wiederholungsversuchen durchführen. Ihre Punktzahlen werden nicht aufgezeichnet und wirken sich nicht auf den Kurs oder die LMS-Berichterstattung aus.

**Was ist der Unterschied zwischen der Freigabe für die Überprüfung und der Freigabe für Teilnehmer?**

&quot;Zur Überprüfung freigeben&quot; bietet Zugriff auf den Kurs, wobei das Bedienfeld &quot;Kommentare&quot; aktiviert ist. Es ist für Kollegen und Stakeholder gedacht, die Feedback geben. &quot;Für Teilnehmer freigeben&quot; ermöglicht den Zugriff auf den Kurs ohne Kommentare - für Teilnehmer, die nicht über ein LMS registriert sind. Die Teilnehmerergebnisse werden auch nicht über einen direkten Link aufgezeichnet.

### Aktualisieren und Schließen einer Überprüfung

**Muss ich eine neue Überprüfung erstellen, nachdem ich Änderungen vorgenommen habe?**

Anzahl Die Review-URL bleibt nach dem Aktualisieren des Kurses gleich. Wählen Sie **Freigeben**, um die Reviewer zu benachrichtigen, dass eine aktualisierte Version verfügbar ist.

**Werden Prüfer benachrichtigt, wenn ich den Kurs aktualisiere?**
Reviewer sehen ein Benachrichtigungsbanner, wenn sie den Überprüfungslink nach einem Update öffnen. Sie können Erneut laden auswählen, um die neueste Version anzuzeigen.

**Verbleiben alte Kommentare nach einem Kursupdate?**

Ja. Vorhandene Kommentare bleiben über Updates hinweg erhalten. Reviewer und Autoren können weiterhin die Kommentare zur aktualisierten Version schließen.

**Was passiert mit einem Teilnehmer-Link, nachdem ich den Kurs aktualisiert habe?**

Über den vorhandenen Teilnehmer-Link wird weiterhin die vorherige Version angezeigt. Generieren Sie nach jedem Update einen neuen Link und geben Sie ihn für Teilnehmer frei, um sicherzustellen, dass sie auf die neuesten Inhalte zugreifen.

**Wie werden Projektaktualisierungen angezeigt?**

Wenn der Autor den Kurs aktualisiert, während Sie ihn überprüfen, wird eine Benachrichtigung angezeigt.

![](../assets/68_newer_version_available_reload_notification.png)

- Wählen Sie **Neu laden**, um die neueste Version zu laden, oder schließen Sie die Benachrichtigung ab, um mit der Überprüfung der aktuellen Version fortzufahren. Das erneute Laden ist sicher - Ihre vorhandenen Kommentare bleiben auch nach den Projektaktualisierungen erhalten, sodass Sie kein Feedback verlieren, das Sie bereits hinzugefügt haben.

## Quiz als Überprüfer testen

Als Überprüfer können Sie das Quiz bis zur angegebenen Anzahl von Malen versuchen, Ihre Ergebnisse werden jedoch nicht aufgezeichnet.

- Wählen Sie **QUIZ STARTEN**, um das Quiz zu starten.

  ![](../assets/66_final_quiz_start_screen_attempts_info.png)

- Nach Abschluss des Vorgangs werden die Ergebnisse angezeigt. Von hier aus können Sie Antworten überprüfen auswählen, um zu sehen, welche Fragen richtig oder falsch beantwortet wurden, oder Quiz wiederholen , um es erneut zu versuchen.

  ![](../assets/67_quiz_results_attempts_remaining_reviewer.png)




