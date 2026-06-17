---
jcr-language: en_us
title: Nutzung des virtuellen Coaches überwachen
description: Überwachen Sie, wie Virtual Coach von Ihrem Konto verwendet wird.
contentowner: mmanuel
source-git-commit: 87971737d1d9838d8b29035b5b9bf718742da1eb
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 2%

---


# Nutzung des virtuellen Coaches überwachen

Zeigen Sie Nutzungsdaten des virtuellen Coaches an, verfolgen Sie die Nutzung von MAU-Krediten (Monthly Active User) und greifen Sie in Adobe Learning Manager auf die Leistungsberichte der Teilnehmer zu.

## Virtual Coach für Ihr Konto aktivieren

Virtual Coach ist als Add-on für Adobe Learning Manager verfügbar. Nach dem Kauf generiert die Bereitstellung einen Aktivierungsschlüssel, der per E-Mail an den Kontoadministrator gesendet wird.

1. Melden Sie sich bei Adobe Learning Manager als Administrator an.
2. Navigieren Sie im linken Navigationsbereich zur Seite **Abrechnung**.
3. Geben Sie im Abschnitt **Virtueller Coach** den Aktivierungsschlüssel ein, den Sie per E-Mail erhalten haben.
4. Wählen Sie **Anwenden**. Virtual Coach ist für Ihr Konto aktiviert.
   ![](assets/virtual-coach-037.png)

Nach der Aktivierung erhalten Sie eine In-App-Benachrichtigung, die bestätigt, dass die Funktion live ist. Vier Beispielszenarien werden automatisch zur Inhaltsbibliothek hinzugefügt, damit die Autoren sofort beginnen können.

>[!NOTE]
>
>Der Aktivierungsschlüssel wird bei der Bereitstellung automatisch generiert und per E-Mail freigegeben. Wenn Sie nicht über den Aktivierungsschlüssel verfügen, wenden Sie sich an Ihren Adobe Learning Manager Customer Success Manager (CSM).

## MAU-Guthaben anzeigen

Monatliche MAU-Credits (Active User) zählen die Anzahl der eindeutigen Teilnehmer, die den virtuellen Coach jeden Monat verwenden.

1. Navigieren Sie zur Seite **Abrechnung**.
2. Wählen Sie im Abschnitt **Virtueller Coach** die Option **Nutzungsdetails anzeigen**.
3. Verwenden Sie die Dropdown-Liste **Zeitraum auswählen**, um den Datumsbereich auszuwählen, den Sie überprüfen möchten.
   ![](assets/virtual-coach-038.png)

   In der Tabelle **Gesamtnutzung** wird Folgendes angezeigt:

   a. **Verfügbar:** Insgesamt erworbene MAU-Credits\
   b. **Verwendet:** Credits bis dato belegt\
   c. **Verbleibend:** Credits für den Rest der Vertragslaufzeit verfügbar

   Die Tabelle **Monatliche Nutzung** zeigt die Anzahl der eindeutigen aktiven Teilnehmer nach Kalendermonat an.

4. Wählen Sie **Detaillierten Bericht herunterladen**, um die vollständigen Nutzungsdaten zu exportieren.

## Wie MAU-Credits verbraucht werden

Ein MAU-Kredit wird verbraucht, wenn ein Teilnehmer eine virtuelle Coach-Sitzung in einem Kalendermonat abschließt. Zusätzliche Sitzungen desselben Teilnehmers im selben Monat verbrauchen keine zusätzlichen Credits.

| Szenario | MAUs belegt |
|----------|--------------|
| Ein Teilnehmer hat im Januar 5 Sitzungen abgeschlossen | 1 |
| Derselbe Teilnehmer verwendet den virtuellen Coach im Januar und Februar | 2 (1 pro Monat) |
| 100 Teilnehmer schließen im Januar jede Sitzung ab. | 100 |

_MAU-Credits werden pro eindeutigem Teilnehmer und Kalendermonat gezählt, unabhängig davon, wie viele Sitzungen jeder Teilnehmer abschließt._

Nicht genutzte Credits verfallen am Ende der Vertragslaufzeit und werden nicht übertragen.

### Beispiel 1: Einzelner Teilnehmer, mehrere Sitzungen

Szenario: Sarah absolviert fünf virtuelle Coach-Sitzungen im Januar.

* Sessions im Januar: 5
* Verwendete MAUs: 1
* Grund: Sarah wird für den Monat Januar als einmalige Benutzerin gezählt, unabhängig davon, wie oft sie übt.

### Beispiel 2: Derselbe Teilnehmer, mehrere Monate

Szenario: Sarah nutzt sowohl im Januar als auch im Februar Virtual Coach.

* Sessions im Januar: 3
* Sessions im Februar: 2
* Verwendete MAUs: 2 (1 für Januar + 1 für Februar)
* Grund: Jeder Kalendermonat zählt separat.

### Beispiel 3: Mehrere Teilnehmer im selben Monat

Szenario: 100 Vertriebsmitarbeiter führen im Januar jeweils eine virtuelle Coach-Sitzung durch.

* Sitzungen insgesamt: 100
* Verwendete MAUs: 100
* Grund: Jeder einzelne Teilnehmer zählt als eine MAU für diesen Monat.

### Beispiel 4: Teamtraining im Zeitverlauf

Szenario: Ihr Team mit 50 Mitarbeitern nutzt das ganze Jahr über Virtual Coach.

| Monat | Aktive Teilnehmer | Diesen Monat verbrauchte MAUs | Kumulative MAUs |
|------|----------------|--------------------------|-----------------|
| Jahrbuch | 0 | 0 | 0 |
| Februar | 5 (5 Personen übten nicht) | 5 | 5 |
| März | 0 (alle 50 geübten Gewinne) | 0 | 45 |
| April | 0 | 0 | 75 |

## Virtuelle Coach-Berichte anzeigen

Der Abschnitt **Verwalten** > **Berichte** Abschnitt > **AI-Berichte** enthält Nutzungsdaten und Leistungsdaten für alle Virtual Coach-Aktivitäten in Ihrer Organisation. Unter der Überschrift **Virtueller Coach** sind zwei Berichte verfügbar.

Alle Berichte werden im CSV-Format exportiert. Die Berichterstellung kann je nach Datengröße einige Minuten dauern.

### Übersicht über die Teilnehmernutzung

Enthält monatliche Nutzungsdaten für alle Teilnehmer. Verwenden Sie diesen Bericht, um zu verfolgen, wie viele Teilnehmer den virtuellen Coach jeden Monat verwenden, die MAU-Kreditaufnahme zu überwachen und Interaktionstrends im Zeitverlauf zu ermitteln.

### Sitzungsdetails

Enthält Daten auf Sitzungsebene für alle Teilnehmer der letzten 90 Tage. Verwenden Sie diesen Bericht, um die einzelnen Sitzungsergebnisse, den Themenbereich und die Stilmetriken für Ihre Teilnehmerpopulation zu überprüfen und Kompetenzlücken zu identifizieren, die möglicherweise zusätzlicher Schulungen oder Inhalte bedürfen.

## Abrufen und Herunterladen von Berichten

1. Melden Sie sich bei Adobe Learning Manager als Administrator an.
2. Wählen Sie im linken Navigationsbereich **Berichte** aus.
3. Wählen Sie **AI-Berichte** aus.
4. Wählen Sie im Abschnitt **Virtueller Coach** den Bericht aus, den Sie herunterladen möchten, **Übersicht zur Teilnehmernutzung** oder **Sitzungsdetails**.
   ![](assets/virtual-coach-039.png)
5. Wählen Sie den Datumsbereich aus, wenn Sie dazu aufgefordert werden, und wählen Sie dann **Weiter**.
6. Der Bericht wird automatisch als CSV-Datei heruntergeladen.
