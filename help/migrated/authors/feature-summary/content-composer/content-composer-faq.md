---
description: Hier finden Sie Antworten auf die häufigsten Fragen von Content Composer, z. B., warum die Option "Gliederung erstellen" ausgegraut ist, wie Sie eine Lektion umbenennen können, warum Quizfragen sich falsch ausgerichtet fühlen und was zu tun ist, wenn Publish deaktiviert ist.
jcr-language: en_us
title: Häufige Fragen zu Adobe Learning Manager Content Composer
source-git-commit: ea6d296fa99686136ab08d756a20570a4681d704
workflow-type: tm+mt
source-wordcount: '584'
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
