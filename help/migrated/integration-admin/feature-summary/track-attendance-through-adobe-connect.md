---
description: Erfahren Sie, wie Adobe Learning Manager Teilnehmer als anwesend markiert, wenn sie eine Adobe Connect-Sitzungsaufzeichnung ohne manuelle Aktualisierungen ansehen
jcr-language: en_us
title: Anwesenheit über Aufnahmeansichten von Adobe Connect verfolgen
exl-id: f4cb951e-3cb1-4caf-b6b8-aec86b32f782
source-git-commit: 90b45cb128b74ecb33a89bf42ef4d6e960101ff0
workflow-type: tm+mt
source-wordcount: '1654'
ht-degree: 1%
---

# Anwesenheit über Aufnahmeansichten von Adobe Connect verfolgen

## Übersicht

Adobe Learning Manager kann die Teilnahme an virtuellen Klassenzimmersitzungen von Adobe Connect über Aufnahmeansichten verfolgen. Wenn ein Teilnehmer eine Live-Sitzung vermisst, die Aufzeichnung in Adobe Connect jedoch lange genug ansieht, markiert der Lernmanager den Teilnehmer als anwesend. Der Teilnehmer schließt dann das Sitzungsmodul ab und kann zum Abschluss des Lernobjekts wechseln, zu dem die Sitzung gehört.

Vor dieser Funktion hatte der Learning Manager keine Möglichkeit, die Anwesenheit von Teilnehmern aufzuzeichnen, die eine Connect-Aufzeichnung angesehen haben. Ein Teilnehmer, der eine Live-Sitzung verpasst hat, konnte sie nicht abschließen, und ein Kursleiter musste einspringen und die Anwesenheit manuell markieren. Diese Funktion entfernt diesen manuellen Schritt. Adobe Connect meldet, wer welche Aufzeichnung und wie lange verfolgt hat, und Learning Manager vergleicht die Überwachungszeit mit den für das Konto festgelegten Abschlusskriterien.

Sobald der Teilnehmer die Abschlusskriterien für die aufgezeichnete Sitzung erfüllt, werden die Teilnehmer in der Admin-App markiert.

Die E-Mail-ID des Teilnehmers sollte in Adobe Learning Manager und Adobe Connect gleich sein, da Adobe Learning Manager den Teilnehmer mit derselben E-Mail-ID zu Adobe Connect umleitet.
Die Standardsynchronisierungsfrequenz und das kürzeste Intervall, das der Integrationsadministrator festlegen kann, betragen eine Stunde.


## Wer macht was?

| Rolle | Aktivitäten. |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Teilnehmer | Öffnet die Sitzungsaufzeichnung und überwacht sie, nachdem die Live-Sitzung versäumt wurde. |
| Der Kursleiter | Startet die Aufzeichnung während der Live-Sitzung, sodass eine Aufzeichnung und ein Transkript vorhanden sind. |
| Integrations-Admin | Konfiguriert das Adobe Connect-Konto, das die Anwesenheitssynchronisation verwendet, und legt den Synchronisierungszeitplan fest oder aktiviert oder deaktiviert ihn. |
| Autor oder Zustellungsverwalter | Plant die Sitzungen des virtuellen Klassenzimmers und verwendet bei Mehrtagesprogrammen einen dauerhaften Raum über Tage hinweg wieder. |
| Adobe Connect | Es erfasst die E-Mail-Adresse jedes Teilnehmers und die Überwachungszeit für die Aufzeichnung und legt die Liste der Aufzeichnungsanzeiger über eine API. |

Jede Rolle spielt eine eigene Rolle bei der aufzeichnungsbasierten Teilnahme.

## Glossar

| Begriff | Bedeutung |
|---------------------------------|--------------------------------------------------------------------------------------------------------|
| Virtuelle Klassenzimmersitzung | Eine auf Adobe Connect gehostete Sitzung im virtuellen Klassenzimmer. |
| Von einem Kursleiter geführte virtuelle Schulung | Von einem Kursleiter durchzuführende Schulungen in virtuellen Klassenzimmern |
| Lernobjekt | Ein Kurs, der beispielsweise das Sitzungsmodul enthält. |
| Dauerhafter Raum | Ein Adobe Connect-Raum, der für mehrere Sitzungen wiederverwendet werden kann, z. B. an Tag 1, Tag 2 und Tag 3. |
| Abschlusskriterien | Der Prozentsatz der Aufzeichnung, den ein Teilnehmer überwachen muss, um für das Modul als abgeschlossen markiert zu werden. |

## Anwendungsszenarien

### Ein Teilnehmer vermisst eine Live-Sitzung

Ein Teilnehmer kann nicht an der virtuellen Live-Klassenzimmersitzung teilnehmen. Später öffnet der Teilnehmer die Sitzung im Learning Manager und sieht sich die Aufzeichnung an. Sobald die Überwachungszeit die Abschlusskriterien erfüllt, markiert der Lern-Manager den Teilnehmer als anwesend und der Teilnehmer schließt das Modul ab, ohne den Kursleiter um Hilfe zu bitten.

### Ein Teilnehmer, der nur teilweise sieht

Ein Teilnehmer öffnet die Aufzeichnung, sieht aber weniger als die erforderliche Freigabe. Die Abschlusskriterien sind nicht erfüllt, sodass der Lernmanager den Teilnehmer nicht als anwesend markiert.

### Mehrtägige Sitzungen in einem dauerhaften Raum

Ein Autor oder Liefermanager plant die Sitzungen für Tag 1, Tag 2 und Tag 3 im selben dauerhaften Connect-Raum. Sie können den Raumnamen sehen und wiederverwenden, ohne sich bei Adobe Connect anzumelden.

## Wichtigste Funktionen

| Funktion | Zweck |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Automatische Anwesenheit | Markiert einen Teilnehmer als anwesend in einer Connect-basierten virtuellen Klassenzimmersitzung, wenn der Teilnehmer die Aufzeichnung lange genug ansieht, um den vorgeschriebenen Schwellenwert zu erreichen. |
| Zeit von Connect aus ansehen | Verwendet die Teilnehmer-E-Mail und die Aufzeichnung der Überwachungszeit, die Adobe Connect erfasst. |
| Schwellenwert für Abschlusskriterien | Markiert den Teilnehmer als abgeschlossen für das Modul, wenn die Überwachungszeit den in den Abschlusskriterien festgelegten Prozentsatz erreicht. |
| Nur tatsächliche Überwachungszeit | Zählt die Zeit, die ein Teilnehmer wirklich gesehen hat. Durch Ziehen der Suchleiste wird keine Überwachungszeit hinzugefügt. |
| Geplante Synchronisierung | Führt eine Back-End-Pipeline in einem Zeitplan aus, den der Integrationsadministrator steuert, und kann aktiviert oder deaktiviert werden. |
| Dauerhafte Raumsichtbarkeit | Zeigt den Namen des Connect-Raums auf Instanzebene an, sodass Autoren einen dauerhaften Raum über Tage hinweg wiederverwenden können. |

## Anwesenheitsverfolgung

*Von einem Teilnehmer, der die Aufzeichnung öffnet, zu Learning Manager, der das Modul als abgeschlossen markiert.*

### Durchgehender Textfluss

1. Der Kursleiter hostet die Live-Sitzung im virtuellen Klassenzimmer auf Adobe Connect und beginnt die Aufzeichnung. Die Aufzeichnung und das Transkript werden nach der Sitzung verfügbar.

1. Ein Teilnehmer, der die Sitzung versäumt hat, wählt die Aufzeichnung aus, um sie anzuzeigen. Adobe Connect verfolgt die Ansicht automatisch.

1. Adobe Connect erfasst die E-Mail-Adresse des Teilnehmers und die Zeit, die der Teilnehmer tatsächlich aufgezeichnet hat.

1. Im konfigurierten Zeitplan ruft eine Back-End-SnapLogic-Pipeline die Adobe Connect API auf und ruft die Liste der Aufzeichnungsanzeiger für einen bestimmten Rahmen ab. Die Pipeline verwendet das Adobe Connect-Konto, das in Integrationsadministrator eingerichtet wurde.

1. Learning Manager ordnet jeden Viewer dem entsprechenden Kurs und Modul zu.

1. Der Lern-Manager vergleicht die Gesamtüberwachungszeit des Teilnehmers mit den Abschlusskriterien.

1. Wenn die Überwachungszeit die Kriterien erfüllt, markiert der Lern-Manager den Teilnehmer als abgeschlossen für das Modul. Im Backend zeichnet Learning Manager dies auf, indem die CSV-Datei für die Benutzerkursstufe aufgefüllt wird.

>[!NOTE]
>
>Adobe Connect überträgt keine Daten an Learning Manager. Learning Manager ruft sie auf der Ebene der Adobe Connect-Instanzen ab, zum Beispiel &quot;diese fünf Benutzer haben sich diese sechs Aufzeichnungen in den letzten 24 Stunden angesehen&quot;. Die Anwesenheit wird daher nach dem nächsten Pipeline-Lauf aktualisiert, nicht in dem Moment, in dem der Teilnehmer die Anzeige beendet.

### Abschlusskriterien und Überwachungszeit

Der Teilnehmer muss mindestens den Prozentsatz der Aufzeichnung überwachen, den die Abschlusskriterien definieren. Beachten Sie die folgenden Regeln:

* Der Prozentsatz gilt für die Aufzeichnungsdauer, nicht für die geplante Sitzungsdauer. Wenn eine 15-minütige Sitzung nur für 5 Minuten aufgezeichnet wird, richtet sich die erforderliche Zeit nach den 5 Minuten. Adobe Connect gibt die Aufnahmedauer an.

* Der Prozentsatz wird auf der Seite &quot;Lernmanager&quot; festgelegt. Dies ist eine gemeinsame Einstellung für das gesamte Konto, nicht eine Einstellung für jede Instanz. Die gleiche Einstellung wurde bereits für Live-Sitzungen angewendet, z. B. wenn eine Beteiligung von 80 % erforderlich ist.

* Adobe Connect zeichnet auf, wie lange der Teilnehmer das Video tatsächlich gesehen hat. Das Springen mit der Suchleiste zählt nicht, und Learning Manager verarbeitet die Überwachungszeit, die Connect vergeht.

| Abschlusskriterien | Aufzeichnungslänge | Benötigte Überwachungszeit | Ergebnis |
|-------------------------|------------------------------------|-----------------------|-------------------------------------------------------------|
| 50% | 5 Minuten | 2,5 Minuten | Nach 2,5 Minuten als abgeschlossen markiert. |
| 50% | 5 Minuten (Sitzung war 15 Minuten) | 2,5 Minuten | Basierend auf der 5-minütigen Aufzeichnung, nicht auf der 15-minütigen Sitzung. |
| 0% | Beliebig | Keine über das Öffnen hinaus | Das Öffnen der Aufzeichnung reicht aus. |

### Berechtigungsfenster

Der Lern-Manager wendet die aufzeichnungsbasierte Anwesenheit nur bis zum Abschlussdatum des Lernobjekts an. Wenn das Lernobjekt kein Abschlussdatum hat, verwendet der Lern-Manager das Abschlussdatum des übergeordneten Lernobjekts.

### Synchronisierung planen

Der Integrations-Admin steuert, wie oft die Pipeline ausgeführt wird. Der Zeitplan kann unter anderem stündlich oder wöchentlich sein, und der Integrationsadministrator kann den Zeitplan ein- oder ausschalten. Für jeden Run wird das gleiche Adobe Connect-Konto verwendet.

### Änderungen

* Wenn ein Benutzer den dauerhaften Raum hinzufügt, der für Tag 1 erstellt wurde, gewährt ihm Learning Manager Zugriff auf diesen Raum. Sie können dann denselben Raum Sitzungen an anderen Tagen hinzufügen.
* Der Learning Manager zeigt den Namen des Connect-Raums auf Instanzebene in den Sitzungsdetails neben der **URL für virtuelle Klassenzimmer** an.
* Für die Standardinstanz zeigt der Lern-Manager den Raum an, der während der Kurserstellung eingerichtet wurde.

### Einschränkungen und Überlegungen

* Die Teilnahme erfolgt nicht in Echtzeit, da Learning Manager Daten nach einem Zeitplan abruft.
* Die Funktion gilt nur für Connect-basierte virtuelle Klassenzimmersitzungen.
* Es muss eine Aufzeichnung vorhanden sein, daher muss der Kursleiter die Aufzeichnung während der Live-Sitzung starten.
* Teilnehmer werden über die E-Mail-Adresse abgeglichen, die Adobe Connect erfasst.
* Durch Ziehen der Suchleiste wird keine Überwachungszeit hinzugefügt.
* Die aufzeichnungsbasierte Anwesenheit endet am Abschlussdatum des Lernobjekts oder des übergeordneten Lernobjekts.

### Zu beachtende Punkte

* Die Überwachungszeit muss größer oder gleich dem vorgeschriebenen Prozentsatz sein (z. B. 50 % von 5 Minuten beträgt 2,5 Minuten). Die Überwachungszeit addiert sich nicht, wenn der Teilnehmer die Sitzung wiederholt überwacht, aber immer noch kurz vor der vorgeschriebenen Überwachungszeit ist. Die Überwachungszeit addiert sich jedoch, selbst wenn der Teilnehmer die Sitzung zu verschiedenen Zeitpunkten in Teilen beobachtet und die Schwellenwertkriterien erfüllt. Wenn ein Teilnehmer beispielsweise eine Minute der Sitzung am Tag 1 und dann am nächsten Tag weitere 1,5 Minuten der Sitzung vom Punkt an betrachtet, an dem er gegangen ist, wird die Überwachungszeit addiert. Dies geschieht auf der Adobe Connect-Seite.

* Abschlusskriterien können auf Kursebene und auf Kontoebene konfiguriert werden. Der Effekt ist derselbe wie bei der Live-Session-Teilnahme.

* Die Standardsynchronisierungsfrequenz und das kürzeste Intervall, das der Integrationsadministrator festlegen kann, betragen eine Stunde.

* Die E-Mail-ID des Teilnehmers sollte in Adobe Learning Manager und Adobe Connect gleich sein, da Adobe Learning Manager den Teilnehmer mit derselben E-Mail-ID zu Adobe Connect umleitet.

### Häufig gestellte Fragen

**Q. Muss der Teilnehmer an der Live-Sitzung teilnehmen?**
**A.** Nein. Ein Teilnehmer, der die Live-Sitzung vermisst, kann weiterhin als anwesend markiert werden, indem er die Aufzeichnung lange genug ansieht.

**Q. Wie viel von der Aufzeichnung muss der Teilnehmer ansehen?**
**A.** Der Prozentsatz in den Abschlusskriterien, der auf die Aufzeichnungsdauer angewendet wird. Beispielsweise benötigt eine 5-minütige Aufnahme bei 50 % mindestens 2,5 Minuten Überwachungszeit.

**Q. Zählt das Überspringen der Aufzeichnung?**
**A.** Nein. Adobe Connect zeichnet die Zeit auf, die der Teilnehmer tatsächlich gesehen hat. Daher zählt das Ziehen der Suchleiste nicht.

**Q. Wird die Teilnahme markiert, sobald der Teilnehmer die Anzeige beendet hat?**
**A.** Nein. Der Learning Manager ruft Viewer-Daten planmäßig aus Adobe Connect ab, sodass die Anwesenheit nach dem nächsten Pipeline-Lauf aktualisiert wird.

**Q. Sendet Adobe Connect die Daten an Learning Manager?**
**A.** Nein. Learning Manager ruft sie ab. Es ist ein Pull-Mechanismus auf der Ebene der Adobe Connect-Instanz, kein Push.

**Q. Woher weiß der Lern-Manager, welcher Teilnehmer es gesehen hat?**
**A.** Adobe Connect erfasst die E-Mail-Adresse des Teilnehmers und die Überwachungszeit der Aufzeichnung. Learning Manager ordnet dies dem Kurs und dem Modul zu.

**Q. Wer steuert, wie oft die Synchronisation ausgeführt wird?**
**A.** Der Integrationsadministrator legt den Zeitplan fest und kann ihn aktivieren oder deaktivieren.

**Q. Ist der Fertigstellungsprozentsatz für jede Instanz festgelegt?**
**A.** Nein. Dies ist eine gemeinsame Einstellung im gesamten Konto.

**Q. Kann sich eine mehrtägige Sitzung einen Connect-Raum teilen?**
**A.** Ja. Autoren können den dauerhaften Raum, der für Tag 1 erstellt wurde, in den Sitzungen für andere Tage wiederverwenden, und der Name des Raums wird auf Instanzebene im Lern-Manager angezeigt.
