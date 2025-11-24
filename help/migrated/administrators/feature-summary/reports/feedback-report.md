---
description: Erfahren Sie, wie Sie den Feedbackbericht in Adobe Learning Manager aufrufen, herunterladen und interpretieren. Lernen Sie Berichtsspalten, Fragetypen, Antworten von Managern und Teilnehmern kennen und erfahren Sie, wie Feedback-Erkenntnisse die Bewertung von Schulungen und die kontinuierliche Verbesserung unterstützen.
jcr-language: en_us
title: Feedbackbericht in Adobe Learning Manager
source-git-commit: 6fceea6cc1f5fbe47e0dbb211cfb9e2de67957f6
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 8%

---


# Feedbackbericht

## Überblick

Der Feedbackbericht in Adobe Learning Manager erfasst sowohl Stufe 1 (Teilnehmer-Feedback) als auch Stufe 3 (Manager-Feedback), nachdem die Teilnehmer die Lernobjekte abgeschlossen haben. Dieser Bericht enthält eine strukturierte Übersicht über subjektive und objektive Antworten von Teilnehmern und ihren Managern.

Der Bericht verfolgt Teilnehmerdetails wie Name, E-Mail-Adresse, Feedback-Formularname, Version und Sprache und erfasst Antworten auf vom Administrator definierte Fragen. Außerdem wird die Auswahl des Teilnehmers für jede Frage aufgezeichnet (z. B. &quot;Stimme voll zu&quot;, &quot;Stimme zu&quot; oder &quot;Stimme nicht zu&quot;).

## Zweck und Vorteile

* Bietet verwertbare Einblicke zur Verbesserung der Kursqualität und der allgemeinen Lerneffektivität.
* Verfeinern Sie die Navigations-, Tempo- und Bereitstellungsmethoden basierend auf direktem Benutzer-Feedback.

## Anwendungsszenarien

* **Inhaltsprobleme schnell identifizieren**: Administratoren können niedrige Bewertungen oder wiederholte negative Kommentare erkennen und die Lernobjekte aktualisieren, ohne auf Support-Tickets oder Eskalationen warten zu müssen.
* **Die Wirksamkeit der Schulung messen**: Teams können das Feedback der Teilnehmer über mehrere Kurse oder Versionen hinweg vergleichen, um herauszufinden, welche Lernobjekte gut funktionieren und welche möglicherweise überarbeitet werden müssen.
* **Mit Feedbackformularen die Interaktion der Teilnehmer verfolgen**: Administratoren können sehen, wie viele Teilnehmer Fragen beantworten oder überspringen, und ihnen helfen, Feedbackformulare zu optimieren, um die Antwortqualität und die Abschlussraten zu verbessern.

## Feedbackbericht herunterladen

1. Melden Sie sich bei Adobe Learning Manager als Administrator an.
2. Wählen Sie im linken Navigationsmenü **[!UICONTROL Berichte]** aus.
   ![](assets/select-report.png)
   _Auf der Administrator-Startseite ist die Option &quot;Berichte&quot; für das Herunterladen von Berichten hervorgehoben._

3. Wählen Sie **[!UICONTROL Benutzerdefinierte Berichte]** in den Berichten aus, und wählen Sie dann **[!UICONTROL Excel-Berichte]** aus.
4. Wählen Sie **[!UICONTROL Feedbackbericht]** aus.
   ![](assets/select-feedback-report.png)
   Im Abschnitt _Benutzerdefinierte Berichte wird die Option angezeigt, Feedbackbericht auszuwählen, um auf Teilnehmer- und Manager-Feedbackdaten zuzugreifen_

5. Wählen Sie **[!UICONTROL Alle Schulungen]** oder **[!UICONTROL Ausgewählte Schulungen]** und den Datumsbereich aus. Wenn Sie die zweite Option auswählen, können Sie bis zu 10 Kurse oder Lernpfade hinzufügen und ihren Feedbackbericht generieren. Darüber hinaus können Sie den Bericht für bis zu ein Jahr generieren.
   ![](assets/feedback-report.png)
   _Konfigurieren Sie den Feedbackbericht, indem Sie den Schulungsbereich auswählen, den Datumsbereich festlegen und die Übersetzungsoption auswählen, bevor Sie_ herunterladen.

6. Wählen Sie die Sprache aus, in die das L1-Feedback übersetzt werden soll. Objektive Fragen und ihre Antworten werden in die ausgewählte Sprache übersetzt, wenn diese Sprachversion explizit definiert ist. Im Bericht werden nur die subjektiven Fragen angezeigt, die explizit in der ausgewählten Sprache definiert sind.  Antworten auf subjektive Fragen werden in der ursprünglichen Antwortsprache gegeben.
7. Wählen Sie **[!UICONTROL Herunterladen]**, um den Bericht herunterzuladen.

## Was enthält der Feedbackbericht?

Im Folgenden sind die Standardspalten im Bericht auf Kontoebene aufgeführt:

| Spalte | Beschreibung |
|----|----|
| Typ des Feedbacks | Gibt an, ob das Feedback vom Teilnehmer (L1) oder vom Manager (L3) stammt. |
| Benutzername | Name des Teilnehmers, der die Schulung abgeschlossen hat |
| Benutzer-E-Mail | E-Mail-Adresse des Teilnehmers |
| Schulungs-ID | Eine vom System generierte eindeutige Kennung, die jedem Lernobjekt (Kurs, Zertifizierung oder Lernpfad) zugewiesen ist |
| Schulungsname | Name des Lernobjekts, für das Feedback gesendet wird |
| Schulungsinstanz | Instanzname der Schulung (für Mehrinstanzkurse) |
| Schulungstyp | Art der Schulung (Kurs, Zertifizierung, Lernpfad) |
| Typ des Feedbackformulars | Typ/Kategorie des verwendeten Feedbackformulars (z. B. gemischte Kurse, Kurse zum Selbststudium und Klassenzimmerkurse) |
| Feedbackformularname | Name des Feedbackformulars |
| Feedback-Version | Versionsnummer des Feedbackformulars |
| Aktueller Manager | Name des Managers des Teilnehmers |
| E-Mail-Adresse des aktuellen Managers | E-Mail-Adresse des Managers des Teilnehmers |
| Datum des Abschlusses | Das Datum, an dem der Teilnehmer die Schulung abgeschlossen hat |
| Datum des Feedbacks | Das Datum, an dem der Teilnehmer das Feedback gesendet hat |
| L1 Feedback Originalsprache | Die Sprache, in der der Teilnehmer das L1-Feedback ursprünglich gesendet hat |

Die folgenden Spalten werden im Bericht auf Kontoebene basierend auf den vier Arten von Fragen angezeigt, die dem Feedbackformular hinzugefügt wurden:

| Spalte | Beschreibung |
|---|---|
| Kurseffektivität | Die im Formular angezeigte vordefinierte Frage zur Kurseffektivität |
| Antwort auf die Kurseffektivität | Die Antwort des Teilnehmers auf die Frage nach der Kurseffektivität |
| NPS-Frage 1 | Frage zum ersten Net Promoter |
| NPS-Bereich 1 | Verwendeter Bewertungsmaßstab (z. B. 0 bis 10) |
| NPS-Antwort 1 | Bewertung des Teilnehmers für NPS Frage 1 |
| Likert Frage 1 | Erste Likert-Frage |
| Likert Antwort 1 | Antwort auf die Likert-Frage 1 |
| Textfrage 1 | Erste offene/Textfrage im Formular |
| Textantwort 1 | Antwort des Teilnehmers auf Textfrage 1 |
| L3 Likert Skalierungsfrage 1 | Misst die Leistung des Teilnehmers nach der Schulung anhand einer Ratingskala |
| L3 Likert Scale Response 1 | Antwort des Managers auf diese Likert-Frage |
| L3 Free Text Question 1 | Dem L3-Feedback-Formular für Manager wurde eine Freitext-Frage hinzugefügt. Diese kann optional oder obligatorisch konfiguriert werden. |
| L3 Free Text Response 1 | Die Antwort des Managers auf diese Freitext-Frage |

>[!NOTE]
>
>Der Bericht auf Kontoebene enthält auch alle aktiven Felder, die für Teilnehmer konfiguriert sind.

Die folgenden Spalten werden im Bericht auf Lernobjektebene angezeigt:

| Spalte | Beschreibung |
|---|---|
| Teilnehmer | Name des Teilnehmers |
| E-Mail | E-Mail-Adresse des Teilnehmers |
| Feedbackformularname | Name des Feedbackformulars |
| Feedback-Version | Versionsnummer des Feedbackformulars |
| Teilnehmersprache | Vom Teilnehmer gewählte Sprache |


