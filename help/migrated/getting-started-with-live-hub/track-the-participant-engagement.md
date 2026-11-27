---
title: Teilnehmer-Interaktionen nachverfolgen
description: Erfahren Sie, wie Kursleiter die Echtzeit-Interaktionsanzeige für Teilnehmer im Live-Hub verwenden, um den Browserfokus, die Chat-Aktivität und die Teilnahme an Umfragen zu überwachen.
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: 5d89078fff50bbd3be1a2d01085efd568b8e0130
workflow-type: tm+mt
source-wordcount: '1408'
ht-degree: 0%
---

# Teilnehmer-Interaktionen nachverfolgen

Die Interaktion des Teilnehmers im Live-Hub gibt den Kursleitern eine Echtzeit-Ansicht der Teilnehmer- oder Teilnehmer-Interaktion während einer Live-Sitzung. Sie kombiniert den Browserfokus, die Chat-Aktivität und die Teilnahme an Umfragen in einer einzigen Interaktionsstufe, die als grüne, gelbe oder rote Anzeige angezeigt wird. Nutze die Funktion, um Flecken in der Aufmerksamkeit zu erkennen und deine Zustellung in Echtzeit anzupassen.

Die Teilnehmer-Interaktion zeigt die durchschnittliche Interaktionsstufe aller Teilnehmer im Hauptraum zu einem bestimmten Zeitpunkt an. Die Stufe wird aktualisiert, sobald ein Teilnehmer an der Sitzung teilnimmt.

Die Interaktion mit den Teilnehmern wird nur während einer Live-Sitzung berechnet und angezeigt.

>[!NOTE]
>
> Nur Kursleiter können die Interaktion der Teilnehmer sehen. Teilnehmer haben keinen Zugriff darauf.

## Berechnungen zur Interaktionsstufe verstehen

Die Interaktionsbewertung der Teilnehmer hilft Ihnen dabei, die Aufmerksamkeit der Teilnehmer während einer Live-Sitzung in Echtzeit zu überwachen. Dieses Verlobungskennzeichen oben auf dem Bildschirm zeigt die allgemeine Verlobungsstufe als **Niedrig**, **Mittel** oder **Hoch** an, sodass Sie die Bereitstellung Ihrer Sitzung anpassen und die Teilnahme nach Bedarf fördern können.

Der Indikator ist nur für Kursleiter im Hauptraum sichtbar.

![Indikator für die Engagement-Ebene](assets/engagement-level-indicator.png)
*Live-Hub-Oberfläche, auf der die Teilnehmerinteraktion in der oberen rechten Ecke angezeigt wird.*

## Wie wird die Interaktionspunktzahl berechnet?

Jeder Teilnehmer oder Teilnehmer hat eine Interaktionsbewertung von 0 bis 100, basierend auf den folgenden Faktoren:

- **Aufmerksamkeit für die Sitzung**: Wenn ein Teilnehmer oder Teilnehmer das Sitzungsfenster aktiv lässt, ist seine Interaktionsstufe standardmäßig auf Hoch festgelegt. Wenn sie zu einem anderen Fenster oder einer anderen Browserregisterkarte wechseln, sinkt ihre Interaktionsstufe auf &quot;Niedrig&quot;, es sei denn, sie nehmen weiterhin an Sitzungsaktivitäten teil.
- **Teilnahme an der Sitzung**: Aktivitäten wie Sprechen, Freigeben eines Bildschirms, Senden von Chat-Nachrichten, Antworten auf Umfragen oder Tests, Zeichnen auf dem Whiteboard, Heben einer Hand, Senden von Reaktionen und Klicken innerhalb der Sitzung erhöhen die Interaktionspunktzahl.

### Wie sich die Interaktionsergebnisse ändern

Der Interaktionspunkt der Teilnehmer ändert sich während einer Live-Sitzung basierend auf ihrer Aufmerksamkeit und ihrer Teilnahme. Die folgenden Bedingungen wirken sich darauf aus, wie die Interaktionspunktzahl berechnet wird:

- **Aktivitätsdauer**: Die meisten Teilnahmeaktivitäten erhöhen vorübergehend die Engagement-Punktzahl, wobei ihr Beitrag über etwa fünf Minuten allmählich abnimmt. Wenn ein Teilnehmer beispielsweise während einer Sitzung spricht und dann zu einem anderen Fenster wechselt, nimmt seine Interaktionsbewertung allmählich ab und nicht sofort
- **Bildschirmfreigabe**: Der Interaktionswert bleibt bei 100, während ein Teilnehmer oder ein Teilnehmer seinen Bildschirm freigibt.
- **Simultane Aktivitäten**: Wenn ein Teilnehmer oder ein Teilnehmer mehrere Aktivitäten gleichzeitig ausführt, wird nur die Aktivität mit dem höchsten Interaktionswert berücksichtigt. Die Punktzahlen aus einzelnen Aktivitäten werden nicht kombiniert, wodurch sichergestellt wird, dass der Interaktionswert 100 nicht überschreitet.
- **Mehrere Geräte**: Wenn ein Teilnehmer oder ein Teilnehmer von mehreren Geräten aus an der Sitzung teilnimmt, wird die höchste Interaktionspunktzahl auf diesen Geräten berücksichtigt.

## Gesamtpunktzahl der Interaktion

Das Teilnehmer-Engagement-Abzeichen zeigt die allgemeine Engagement-Ebene basierend auf der durchschnittlichen Engagement-Punktzahl aller Teilnehmer im Hauptraum an, gerundet auf die nächste ganze Zahl.

Die folgenden Bedingungen gelten für die Berechnung der Gesamtpunktzahl des Projekts:
- **Kursleiter und Aufzeichnungsbots**: Kursleiter und Aufzeichnungsbots sind von der Berechnung der Gesamtpunktzahl für das Engagement ausgeschlossen. Aufzeichnungsbots werden nicht in der Teilnehmerliste angezeigt.
- **Arbeitsräume**: Teilnehmer oder Teilnehmer in Arbeitsräumen sind nicht in der Gesamtpunktzahl für das Engagement enthalten. Wenn Teilnehmer zwischen Hauptraum und Arbeitsraum wechseln, werden ihre individuellen Interaktionswerte zurückgesetzt und innerhalb von ein bis zwei Minuten neu berechnet.
- **Neue Teilnehmer**: Die Teilnehmer-Interaktionsbewertung wird etwa eine Minute nach dem Beitritt zur Sitzung verfügbar. Bis die Punktzahl verfügbar ist, wird der Teilnehmer oder Teilnehmer von der Berechnung der Gesamtpunktzahl für das Engagement ausgeschlossen.
- **Leerer Hauptraum**: Wenn keine Teilnehmer oder Teilnehmer im Hauptraum vorhanden sind, zeigt das Abzeichen die Beteiligung des Teilnehmers ohne eine Engagement-Stufe an.

## Identifizieren von Interaktionsstufen und Indikatoren

Das Teilnehmer-Engagement-Abzeichen zeigt eine der folgenden Interaktionsstufen basierend auf der Gesamtpunktzahl des Projekts an. Sie können diese Stufen verwenden, um die Aufmerksamkeit der Teilnehmer zu überwachen und die Bereitstellung der Sitzung nach Bedarf anzupassen.  Jede Stufe hat folgende Bedeutung:

| **Engagement** | **Ergebnis** | **Beschreibung** |
|----|----|----|
| Hoch | 61 bis 100 | Teilnehmer nehmen aktiv an der Sitzung teil. |
| Mittel | 31 bis 60 | Teilnehmer zeigen gelegentliche Interaktion mit mäßiger Teilnahme. |
| Niedrig | 0 bis 30 | Die Teilnehmer zeigen während der Sitzung nur minimale oder keine Interaktion oder einen reduzierten Fokus. |

>[!NOTE]
>
> - Die Interaktionspunktzahl gibt die Aufmerksamkeit der Teilnehmer während einer Sitzung an. Es misst weder Lernergebnisse noch die Leistung.
> 
> - Interaktionsergebnisse werden jede Minute berechnet. Es kann bis zu zwei Minuten dauern, bis Änderungen an der Interaktionsmarke angezeigt werden.

## Häufig gestellte Fragen

+++ Erkennt der Interaktionswert, ob ein Teilnehmer die Sitzung aktiv überwacht?

Anzahl Die Interaktionspunktzahl wird auf der Grundlage berechnet, ob das Sitzungsfenster aktiv ist und die Aktivitäten des Teilnehmers wie Sprechen, Senden von Chat-Nachrichten und Antworten auf Umfragen. Es werden keine Kamera-Videos, Eye-Tracking oder der Status der Mikrofonstummschaltung verwendet, um die Interaktion zu messen.

+++

+++ Was passiert, wenn ein Teilnehmer sich vom Sitzungsfenster entfernt?

Wenn ein Teilnehmer zu einer anderen Browserregisterkarte, einem anderen Fenster oder einer anderen Anwendung wechselt, wird das Sitzungsfenster nicht mehr als aktiv betrachtet. Auch wenn das Sitzungsfenster sichtbar bleibt, wird es als inaktiv betrachtet, wenn ein anderes Fenster im Fokus ist.

+++

+++ Tragen alle Beteiligungsaktivitäten in gleichem Maße zum Engagement Score bei?

Sprechen, Bildschirmfreigabe, Chat-Nachrichten senden, auf Umfragen oder Tests reagieren, auf dem Whiteboard zeichnen, die Hand heben und Reaktionen senden tragen gleichermaßen zur Interaktionsbewertung bei. Ein Klick innerhalb der Session trägt etwas weniger dazu bei.

+++

+++ Wie ändert sich der Interaktionswert nach einer Teilnahmeaktivität?

Der Beitrag der meisten Teilnahmeaktivitäten nimmt über etwa fünf Minuten allmählich ab. Wenn ein Teilnehmer beispielsweise in ein anderes Fenster wechselt und dann spricht, erhöht sich sein Interaktionswert beim nächsten Update auf 100. In den folgenden Minuten nimmt die Punktzahl allmählich auf 80, 60, 40 und 20 ab. Dort bleibt sie bestehen, bis der Teilnehmer zum Sitzungsfenster zurückkehrt oder erneut teilnimmt.

Ein Teilnehmer, der das Sitzungsfenster aktiv hält, hält ein hohes Maß an Interaktion aufrecht.

+++

+++ Sind die Teilnehmer an Arbeitsräumen in der Gesamtpunktzahl für das Engagement enthalten?

Anzahl Nur Teilnehmer im Hauptraum werden in die Berechnung der Gesamtpunktzahl für das Engagement einbezogen. Das Verlobungsabzeichen wird nicht angezeigt, wenn sich ein Kursleiter in einem Arbeitsraum befindet.

+++

+++ Warum nimmt die Gesamtpunktzahl der Interaktion nach Ende der Arbeitsräume ab?

Wenn Teilnehmer aus Arbeitsräumen in den Hauptraum wechseln, werden ihre individuellen Interaktionsergebnisse zurückgesetzt und innerhalb von ein bis zwei Minuten neu berechnet. Dadurch kann die Gesamtpunktzahl der Interaktion vorübergehend verringert werden.

+++

+++ Wie wird die Interaktionsbewertung berechnet, wenn ein Teilnehmer von mehreren Geräten aus teilnimmt?

Wenn ein Teilnehmer von mehreren Geräten aus an der Sitzung teilnimmt, wird die höchste Interaktionspunktzahl für diese Geräte berücksichtigt. Eine inaktive Sitzung auf einem Gerät verringert nicht die Interaktionspunktzahl, die auf einem anderen aktiven Gerät aufgezeichnet wurde.

+++

+++ Warum dauert die Aktualisierung der Verlobungsabzeichen bis zu zwei Minuten?

Der Interaktionswert jedes Teilnehmers wird einmal pro Minute berechnet. Die Gesamtpunktzahl der Interaktion wird dann jede Minute aktualisiert, sodass Änderungen bis zu zwei Minuten dauern können, bis sie auf dem Interaktionsabzeichen angezeigt werden.

+++

+++ Was können Kursleiter tun, wenn das Verlobungsabzeichen &quot;Niedrig&quot; anzeigt?

Eine niedrige Interaktionsstufe zeigt an, dass die meisten Teilnehmer das Sitzungsfenster verlassen haben und nicht aktiv teilnehmen. Die Kursleiter können Umfragen, Tests, Chat-Beiträge oder Diskussionsfragen verwenden, um die Teilnahme zu fördern und die Aufmerksamkeit der Teilnehmer auf die Sitzung zu lenken.

+++

+++ Können Kursleiter Interaktionswerte verwenden, um die Anwesenheit zu verfolgen oder Teilnehmer zu bewerten?

Interaktionspunkten bieten einen allgemeinen Hinweis auf die Aufmerksamkeit und Aktivität der Teilnehmer während einer Sitzung. Ein Teilnehmer kann ein hohes Maß an Interaktion beibehalten, indem er das Sitzungsfenster aktiv hält, auch ohne aktiv teilzunehmen oder das Lernen zu demonstrieren. Deshalb sind Interaktionswerte möglicherweise nicht geeignet, die Leistung der Teilnehmer zu bewerten oder die Anwesenheit zu verfolgen.

+++

+++ Können die Teilnehmer ihre Interaktionswerte anzeigen?

Anzahl Das Verlobungsabzeichen ist nur für Kursleiter sichtbar.

+++

+++ Können Kursleiter die Interaktionsergebnisse der einzelnen Teilnehmer anzeigen?

Anzahl Das Verknüpfungssymbol zeigt nur die Gesamtpunktzahl des Projekts für den Hauptraum an. Einzelne Teilnehmerpunktzahlen sind nicht verfügbar.

+++

+++ Können Kursleiter die Verfolgung von Interaktionen deaktivieren?

Anzahl Die Interaktionsverfolgung ist immer aktiviert und kann nicht deaktiviert werden.

+++

+++ Sind Interaktionsergebnisse in Berichten oder im Sitzungsverlauf verfügbar?

Anzahl Die Verlobungsmarke zeigt nur die aktuelle Gesamtpunktzahl der Verlobung an. Interaktionsergebnisse werden nicht gespeichert oder in den Berichten oder im Sitzungsverlauf nicht berücksichtigt.

+++

+++ Können Co-Kursleiter das Verlobungsabzeichen anzeigen?

Ja. Co-Kursleiter können das Verlobungsabzeichen auch während einer Sitzung anzeigen.

+++

+++ Wie werden die Ergebnisse der Interaktion auf Mobilgeräten berechnet?

Die Teilnehmer können über mobile Browser auf Live Hub-Sitzungen zugreifen. Die Interaktionsergebnisse werden anhand derselben Kriterien wie in Desktop-Browsern berechnet.

+++
