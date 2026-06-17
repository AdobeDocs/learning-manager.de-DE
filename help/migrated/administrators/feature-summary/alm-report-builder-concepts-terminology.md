---
jcr-language: en_us
title: Report Builder - Begriffe und Terminologie
description: Informieren Sie sich über die wichtigsten Konzepte von Report Builder, einschließlich Datasets, Spalten, Gruppierung, Filtern und Aggregaten, bevor Sie Ihren ersten Bericht erstellen.
contentowner: mmanuel
source-git-commit: b4540c4c23ad496c8fff01095be6715d18aa0512
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 0%

---


# Report Builder: Konzepte und Terminologie

## Vorlagen und Berichte

**Vorlagen** sind vordefinierte Berichtskonfigurationen, die von Adobe Learning Manager bereitgestellt werden. Sie wurden für allgemeine Anwendungsfälle, die Verfolgung von Registrierung und Abschluss, Compliance-Berichte und die Leistung von Kursleitern entwickelt und können sofort heruntergeladen werden. Vorlagen sind schreibgeschützt. Sie können sie nicht bearbeiten oder überschreiben.
2![](assets/image003.png)

**Berichte** sind Ihre eigenen gespeicherten Konfigurationen. Sie können einen Bericht von Grund auf neu erstellen oder eine Vorlage duplizieren und die Kopie bearbeiten. Wenn Sie eine Vorlage duplizieren, wird die Kopie zu einem Bericht auf der Registerkarte Berichte .

Vorlagen und Berichte werden im Report Builder, jedoch unter separaten Registerkarten angezeigt.

## Datensätze

Ein Dataset ist eine benannte Gruppe von verwandten Spalten im Report Builder. Wenn Sie einem Bericht Spalten hinzufügen, wählen Sie aus diesen Datasets. Betrachten Sie jeden Datensatz als eine Tabelle mit Informationen zu einem Aspekt Ihrer Lerndaten.

Im Folgenden finden Sie ein Beispiel für Datensätze, die in Report Builder verfügbar sind:

* **Benutzer:** Teilnehmerprofildaten, einschließlich aktiver Felder
* **Transkript:** Registrierungs- und Abschlussdatensätze
* **Lernobjekt:** Kurs, Lernpfad und Zertifizierungsdaten
* **Lernobjektinstanz:** Details auf Instanzebene
* **Katalog:** Katalog- und Katalogbeschriftungsdaten
* **Benutzergruppe:** Benutzergruppenmitgliedschaft und -hierarchie
* **Modulsitzung:** Klassenzimmer- und virtuelle Sitzungsdaten, einschließlich Details zum E-Learning-Modul

>[!NOTE]
>
>Datensätze sind selektiv verknüpfbar. Nicht alle Kombinationen sind in einem einzigen Bericht verfügbar.

## Spalten und die Schaltfläche Hinzufügen

Jede hinzugefügte Spalte wird in der Berichtsarbeitsfläche als Zeile angezeigt und in der heruntergeladenen Datei als Spalte eingefügt. Sie können dieselbe Spalte mehrmals hinzufügen. Dies ist nützlich, wenn Sie zwei verschiedene Werte aus demselben Feld messen möchten. Beispielsweise können Sie die Spalte Status zweimal hinzufügen: einmal, um Registrierungen zu zählen, und einmal, um Teilnehmer in Bearbeitung zu zählen, wobei die Anzahl verwendet wird, wenn sie aggregiert wird.
![](assets/image005.png)

Sie können auch jede Spalte umbenennen, indem Sie einen Alias eingeben. Der Alias wird als Spaltenüberschrift im heruntergeladenen Bericht angezeigt.

## Gruppieren nach und Aggregation

&quot;Gruppieren nach&quot; fasst Ihre Daten nach einem ausgewählten Feld zusammen, anstatt einzelne Zeilen anzuzeigen. Wenn Sie beispielsweise nach Kursleiternamen gruppieren, erhalten Sie eine Zeile pro Kursleiter und nicht eine Zeile pro Registrierung.

Nach Standarddatenbankverhalten gruppieren: Wenn Sie group by auf eine Spalte anwenden, muss auf jede zweite Spalte im Bericht eine Aggregatfunktion angewendet werden. Einzelne Zeilendaten können nicht mit gruppierten Daten kombiniert werden. Verfügbare Aggregate **Funktionen** sind:

* **Anzahl:** Gesamtzahl der Zeilen
* **Anzahl, wenn:** Anzahl der Zeilen, bei denen das Feld einem von Ihnen angegebenen Wert entspricht
* **Summe:** Summe eines numerischen **Felds**
* **Min:** niedrigster Wert in einem numerischen Feld
* **Max.:** der höchste Wert in einem numerischen Feld
* **Durchschnitt:** Mittelwert eines numerischen Felds

Wenn Sie Pivot-Tabellen in Excel verwendet haben, funktioniert group by auf Spaltenebene genauso.

## Filter

Filter beschränken, welche Zeilen in Ihrem Bericht angezeigt werden. Sie können mehrere Filter anwenden und sie mit UND- oder ODER-Logik kombinieren.

Filteroperatoren hängen vom Datentyp der Spalte ab:

* **Zeichenfolgenfelder:** Enthält, ist gleich, beginnt mit (Type-Ahead-Suche für erkannte Werte verfügbar)
* **Numerische Felder:** Größer, kleiner, gleich, zwischen
* **Datumsfelder:** Entspricht dem Vorher-, Nachher-, Zwischen- und relativen Bereich (zum Beispiel letzte 90 Tage)
* **Enum (list)-Felder:** ist in, ist nicht in (Werteauswahl für Mehrfachauswahl)

## UND/ODER-Logik und verschachtelte Filtergruppen

Mehrere Filter verwenden standardmäßig die UND-Logik. Alle Bedingungen müssen &quot;true&quot; sein, damit eine Zeile angezeigt wird. Sie können den Operator zwischen zwei beliebigen Filtern in OR ändern. Sie können Filter auch gruppieren, indem Sie Als Gruppe hinzufügen verwenden, um eine Klammer zu erstellen. Filter innerhalb der Gruppe werden gemeinsam ausgewertet, bevor sie mit Filtern außerhalb der Gruppe kombiniert werden.

So können Sie Bedingungen wie die folgenden erstellen:

(Katalog = Sicherheit ODER Katalog = Hygiene) UND Fertigstellungstermin ist in den letzten 90 Tagen.

Sie können Gruppen innerhalb anderer Gruppen verschachteln, um komplexe mehrstufige Logik zu unterstützen.

## Paginierung

Sie können nach einer oder mehreren Spalten sortieren. Die erste Spalte, nach der sortiert wird, ist die primäre Sortierung. Zusätzliche Sortierungen gelten innerhalb der Zeiten in der primären Spalte.

Wenden Sie immer mindestens eine Sortierung an, wenn Sie eine konsistente Ausgabe benötigen. Da die Berichterstellung über ein verteiltes System ausgeführt wird, ist die Zeilenreihenfolge zwischen zwei Downloads desselben Berichts nicht gewährleistet, es sei denn, die Sortierung wird angewendet.

## Trend-Daten und Snapshot-Daten

Jeder Bericht, der einen Trendaggregator verwendet, z. B. monatlich oder wöchentlich, spiegelt die aktuellen Snapshot-Daten nach Datum gruppiert wider. Sie spiegelt nicht den historischen Zustand der Daten zu jedem früheren Datum wider.

Beispielsweise zeigt ein Trend zur Registrierung, der nach Monaten gruppiert ist, wie viele Registrierungen es heute gibt, verteilt auf die Monate, in denen sie erstellt wurden. Es werden keine Teilnehmer berücksichtigt, die später die Registrierung aufgehoben oder Benutzergruppen geändert haben. Diese Änderungen werden nicht rückwirkend auf die vergangenen Monate angewendet.

## Gelöschte Teilnehmer und aktive Felder

Report Builder unterstützt die Aufnahme gelöschter Teilnehmer in Berichte und das Abrufen ihrer aktiven Feldwerte. Verwenden Sie die Spalte **Löschdatum** im Dataset **Benutzer**, um den Bericht zu erstellen.

## Best Practices

* Lesen Sie die verfügbaren Datensätze, bevor Sie einen Bericht von Grund auf neu erstellen. Wenn Sie wissen, welcher Datensatz die benötigten Felder enthält, sparen Sie viel Konfigurationszeit.
* Wenden Sie die Sortierung an, bevor Sie einen geplanten Bericht abonnieren. Dies gewährleistet eine konsistente Reihenfolge der Zeilen bei jeder Auslieferung.
* Wenn Sie unerwartete doppelte Zeilen sehen, überprüfen Sie, ob Ihr Bericht ein Feld enthält, das mehrere Werte pro Zeile enthalten kann, z. B. den Namen eines Kursleiters für eine Sitzung mit mehreren Kursleitern.
