---
description: Erfahren Sie, wie Learning Manager-Administratoren Virtual Coach aktivieren, die Nutzung von MAU-Credits überwachen und Berichte zur Teilnehmerleistung herunterladen.
jcr-language: en_us
title: Nutzung und Abrechnung von Virtual Coach verwalten
exl-id: 1f8f6465-51c3-4670-a1c7-9a7dfb091452
source-git-commit: 449f25df93867bf4d5ec11af057f8da7c405a09f
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%
---

# Nutzung und Abrechnung von Virtual Coach verwalten

Aktivieren Sie &quot;Virtueller Coach&quot;, überwachen Sie die Nutzung von MAU-Credits (Monthly Active User) und laden Sie als Adobe Learning Manager-Administrator Leistungsberichte von Teilnehmern herunter.

## Virtual Coach für Ihr Konto aktivieren {#activatevirtualcoach}

Virtual Coach ist als Add-on für Adobe Learning Manager verfügbar. Nach dem Kauf generiert die Bereitstellung einen Aktivierungsschlüssel, der per E-Mail an den Kontoadministrator gesendet wird.

1. Melden Sie sich bei Adobe Learning Manager als Administrator an.
2. Navigieren Sie im linken Navigationsbereich zur Seite **Abrechnung**.
3. Geben Sie im Abschnitt **Virtueller Coach** den Aktivierungsschlüssel ein, den Sie per E-Mail erhalten haben.

   ![](/help/migrated/administrators/feature-summary/assets/virtual_coach12.png)
   *Geben Sie Ihren Aktivierungsschlüssel im Abschnitt &quot;Virtueller Coach&quot; der Abrechnungsseite ein, um die Funktion zu aktivieren.*

4. Wählen Sie **Anwenden**. Virtual Coach ist für Ihr Konto aktiviert.

Nach der Aktivierung erhalten Sie eine In-App-Benachrichtigung, die bestätigt, dass die Funktion live ist. Vier Beispiele für Rollenspielszenarien werden der **Inhaltsbibliothek** automatisch hinzugefügt, sodass die Autoren sofort beginnen können.

>[!NOTE]
>
>Der Aktivierungsschlüssel wird bei der Bereitstellung automatisch generiert und per E-Mail freigegeben. Wenn Sie nicht über den Aktivierungsschlüssel verfügen, wenden Sie sich an Ihren Adobe Learning Manager Customer Success Manager.

## MAU-Kreditsaldo anzeigen

Monatliche MAU-Credits (Active User) zählen die Anzahl der eindeutigen Teilnehmer, die den virtuellen Coach jeden Monat verwenden.

1. Navigieren Sie zur Seite **Abrechnung**.
2. Wählen Sie im Abschnitt **Virtueller Coach** die Option **Nutzungsdetails anzeigen**.

   ![](/help/migrated/administrators/feature-summary/assets/virtual-coach22.png)

3. Verwenden Sie die Dropdown-Liste **Zeitraum auswählen**, um den Datumsbereich auszuwählen, den Sie überprüfen möchten.

   In der Tabelle **Gesamtnutzung** wird Folgendes angezeigt:

   - **Verfügbar**: erworbene MAU-Credits insgesamt.
   - **Verwendet**: Credits, die bisher verbraucht wurden.
   - **Verbleibend**: Credits, die für den Rest der Vertragslaufzeit verfügbar sind.

   Die Tabelle **Monatliche Nutzung** zeigt die Anzahl der eindeutigen aktiven Teilnehmer nach Kalendermonat an.

   ![](/help/migrated/administrators/feature-summary/assets/virtual-coach23.png)

4. Wählen Sie **Detaillierten Bericht herunterladen**, um die vollständigen Nutzungsdaten zu exportieren.

   ![](/help/migrated/administrators/feature-summary/assets/virtual-coach-report-mau-billing-5.png)

## Wie MAU-Credits verbraucht werden

Ein MAU-Kredit wird verbraucht, wenn ein Teilnehmer eine virtuelle Coach-Sitzung in einem Kalendermonat startet. Zusätzliche Sitzungen desselben Teilnehmers im selben Monat verbrauchen keine zusätzlichen Credits. Nicht genutzte Credits verfallen am Ende der Vertragslaufzeit und werden nicht übertragen.

| Szenario | MAUs belegt |
|---|---|
| Ein Teilnehmer hat im Januar 5 Sitzungen abgeschlossen | 1 |
| Derselbe Teilnehmer verwendet den virtuellen Coach im Januar und Februar | 2 (1 pro Monat) |
| 100 Teilnehmer schließen im Januar jede Sitzung ab. | 100 |

*MAU-Credits werden pro eindeutigem Teilnehmer und Kalendermonat gezählt, unabhängig davon, wie viele Sitzungen jeder Teilnehmer startet.*

**Beispiel: Einzelner Teilnehmer, mehrere Sitzungen.** Sarah startet im Januar fünf virtuelle Coach-Sitzungen. Sie gilt als einmalige Benutzerin für den Monat, daher wird 1 MAU unabhängig davon, wie oft sie übt, konsumiert.

**Beispiel: derselbe Teilnehmer, mehrere Monate.** Sarah verwendet Virtual Coach sowohl im Januar (3 Sessions) als auch im Februar (2 Sessions). Jeder Kalendermonat zählt separat, sodass 2 MAUs verbraucht werden - 1 für Januar und 1 für Februar.

**Beispiel: Mehrere Teilnehmer, im selben Monat.** 100 Vertriebsmitarbeiter starten im Januar jeweils eine virtuelle Coach-Sitzung. Jeder einzelne Teilnehmer zählt für diesen Monat als eine MAU, sodass 100 MAUs verbraucht werden.

**Beispiel: Teamtraining im Laufe der Zeit.** Ihr Team mit 50 Mitarbeitern nutzt das ganze Jahr über Virtual Coach. In einem Monat, in dem nur fünf der 50 Übungen durchgeführt werden, werden fünf MAUs für diesen Monat verbraucht; in einem Monat, in dem alle 50 Teilnehmer erneut üben, 0 zusätzliche MAUs, die über das hinausgehen, was bereits für wiederkehrende Teilnehmer in diesem Monat belegt wurde, da jeder Teilnehmer nur einmal pro Kalendermonat gezählt wird, unabhängig davon, wie oft er darin übt.

Navigieren Sie zu [Virtual Coach-Berichte](/help/migrated/administrators/feature-summary/virtual-coach/virtual-coach-reports.md), um mehr über Virtual Coach-Berichte zu erfahren.
