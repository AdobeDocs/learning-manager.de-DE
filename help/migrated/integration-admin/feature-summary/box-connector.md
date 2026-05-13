---
description: Box-Connector in Adobe Learning Manager
jcr-language: en_us
title: Box-Connector
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '894'
ht-degree: 1%

---


# Box-Connector in Adobe Learning Manager

## Einführung

Der **Box-Connector** in Adobe Learning Manager ermöglicht eine nahtlose Integration mit externen Systemen, indem der Import und Export von Benutzer- und Lerndaten über CSV-Dateien automatisiert wird. Externe Systeme können CSV-Dateien in festgelegten Ordnern im von Adobe Learning Manager verwalteten Box-Konto ablegen, wo sie automatisch auf der Grundlage eines definierten Zeitplans verarbeitet werden.

Mit diesem Connector können Administratoren:

- Importieren Sie interne Benutzer aus CSV-Dateien.
- Exportieren Sie Benutzerkenntnisdaten und Teilnehmertranskripte in externe Systeme.
- Importieren Sie xAPI-Aktivitätsanweisungen aus unterstützten Drittanbietersystemen.

Der Connector unterstützt Attributzuordnung, geplante Synchronisierung und On-Demand-Ausführung, sodass Organisationen aktuelle Benutzer- und Lerndaten plattformübergreifend verwalten können.

## Box-Connector konfigurieren

So richten Sie den Box-Connector in Adobe Learning Manager ein:

1. Melden Sie sich bei Adobe Learning Manager als Integrationsadministrator an.
2. Bewegen Sie den Mauszeiger über die Kachel **Box**.
3. Wählen Sie **Verbinden**.

   ![](assets/box-connector1.png)
   _Verbinden auswählen, um den Box-Connector zu konfigurierenVerbinden, um den Box-Connector zu konfigurieren_

4. Geben Sie die E-Mail-Adresse der Person ein, die das Adobe Learning Manager Box-Konto für Ihr Unternehmen verwaltet.
5. Wählen Sie **Verbinden**.



### Konto aktivieren

1. Adobe Learning Manager sendet einen Link zum Zurücksetzen des Kennworts an die angegebene E-Mail-ID.
2. Der Benutzer muss das Kennwort zurücksetzen, bevor er zum ersten Mal auf das Box-Konto zugreifen kann.

>[!NOTE]
>
>Pro Adobe Learning Manager-Konto kann nur ein Box-Konto konfiguriert werden.

Wählen Sie auf der Seite **Übersicht** eine der folgenden Aktionen aus:

- **Interne Verwendung importieren**
- **xAPI-Aktivitätsbericht importieren**
- **Benutzerkenntnisse exportieren**
- **Teilnehmertranskript exportieren**
- **xAPI-Aktivitätsbericht exportieren**

Sobald die Verbindung hergestellt ist, kann der Box-Connector Daten zwischen Adobe Learning Manager und Ihren externen Systemen synchronisieren.

## Interne Benutzer importieren

Die Benutzerimportfunktion ermöglicht die automatische Synchronisation von Mitarbeiterdaten aus HR-Systemen und anderen externen Quellen in Adobe Learning Manager.

### Attribute zuordnen

Durch Attributzuordnung wird die Verbindung zwischen Ihren externen Daten und der unterstützten Datenstruktur von Adobe Learning Manager erstellt, wodurch sichergestellt wird, dass die Daten in die richtigen Felder gelangen. Dieser Schritt ist obligatorisch.

Zuordnen von Attributen:

1. Wählen Sie auf der Seite des Box-Connectors **Interne Benutzer** aus.
2. Wählen Sie **Spaltenzuordnung** aus.
3. Auf der Seite **Attribute zuordnen**:
   - Links werden die erforderlichen Felder in Adobe Learning Manager angezeigt.
   - Auf der rechten Seite werden die CSV-Spaltennamen angezeigt. Zunächst enthält diese Seite leere Dropdown-Menüs.
   - Wählen Sie **Wählen Sie CSV** aus, um eine CSV-Beispieldatei hochzuladen. Dadurch wird die Dropdown-Liste auf der rechten Seite mit den Spaltennamen aus Ihrer CSV-Datei gefüllt. Lesen Sie [diesen Artikel](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/migration-manual#csv), um Beispiel-CSVs abzurufen.
   - Ordnen Sie jedes Adobe Learning Manager-Feld der entsprechenden CSV-Spalte zu.

   ![](assets/box-connector2.png)
   _Oberfläche für die Attributzuordnung, die links Adobe Learning Manager-Felder und rechts die Dropdown-Listen für CSV-Spalten anzeigt_

4. Wählen Sie **Speichern**, um die Zuordnung abzuschließen.

Nach dem Speichern wird das konfigurierte Konto als Datenquelle in der Administrator-App angezeigt. Administratoren können dann einen Import planen oder eine manuelle Synchronisierung auslösen.

### Importieren von xAPI-Anweisungen

Der Import von xAPI-Anweisungen ermöglicht eine detaillierte Verfolgung der Lernaktivitäten, indem externe Lerndaten in Adobe Learning Manager importiert werden.

_Quelle konfigurieren_

Die xAPI-Quellkonfiguration stellt die Verbindung zwischen externen Lernsystemen und der Aktivitätsverfolgung von Adobe Learning Manager her.

So konfigurieren Sie eine Quelle:

1. Navigieren Sie zum xAPI-Konfigurationsabschnitt.
2. Wählen Sie **Neue Konfiguration hinzufügen** in der Konfigurationsliste aus.
3. Geben Sie **Name** und **Quelldateiname** ein.
   - Name: Beschreibende Kennung für diese xAPI-Quelle (z. B. LMS-Integration oder externes Schulungssystem).
   - Quelldateiname: Exakter Dateiname, der in Ihren Box-Ordner hochgeladen wird (muss genau übereinstimmen, einschließlich Dateierweiterung).

   ![](assets/box-connector3.png)
   _Konfigurationsformular, das das Namensfeld und das Quelldateinamensfeld anzeigt_

4. Wählen Sie **Speichern** aus, um die Basiskonfiguration zu erstellen.

_Filter hinzufügen (optional)_

Mit Filtern können Sie xAPI-Anweisungen basierend auf bestimmten Kriterien selektiv importieren.

So fügen Sie einen Filter für die Quelle hinzu:

1. Wählen Sie im linken Fensterbereich **Filter** aus.
2. Wählen Sie **Neuen Filter hinzufügen**.
3. Konfigurieren Sie Folgendes:
   - **Name:** Beschreibender Name für die Filterregel.
   - **Bedingung:** Vergleichsoperator (gleich, enthält, größer als usw.).

   ![](assets/box-connector4.png)
   _Dialogfeld zur Filtererstellung mit Feldern für Name und Bedingungen_

4. Wählen Sie **Neuen Filter hinzufügen**, um weitere Filter hinzuzufügen.
5. Wählen Sie **Speichern** oder **Löschen** nach Bedarf in der Spalte **Aktionen** aus.
6. Wählen Sie nach dem Hinzufügen der Filter **Speichern** aus.

## Import planen

Automatisierte Planung stellt eine konsistente Datensynchronisierung ohne manuelle Eingriffe sicher und sorgt für die Aufrechterhaltung aktueller Lernaktivitäts-Datensätze.

So planen Sie den Import:

1. Wählen Sie im linken Fensterbereich **Zeitplan konfigurieren** aus.

   ![](assets/box-connector5.png)
   _Konfigurationsseite für Zeitplan mit den Aktivierungsoptionen und Zeitsteuerelementen_

2. Wählen Sie **Import von xAPI-Anweisungen über diese Verbindung aktivieren**.
3. Wählen Sie **Zeitplan aktivieren**, um automatische Importe einzurichten.
4. Legen Sie die folgenden Zeitplanparameter fest:

   - **Startdatum:** Wann der geplante Import beginnen soll.
   - **Uhrzeit:** Tageszeit für die Ausführung des Imports.
   - **Wiederholen nach:** Wie oft Importe ausgeführt werden sollen (tägliche, wöchentliche, benutzerdefinierte Intervalle).
5. Wählen Sie **Speichern**.

## On demand ausführen (optional)

On-Demand-Ausführung ermöglicht sofortigen Datenimport außerhalb regulärer geplanter Vorgänge.

Wann On-Demand-Importe verwendet werden:

- Testen neuer Konfigurationen vor der Planung.
- Verarbeitung dringender oder zeitkritischer Datenaktualisierungen.
- Einmalige Datenmigrationen oder Korrekturen.
- Fehlerbehebung bei Importproblemen.

So importieren Sie xAPI-Anweisungen manuell:

1. Wählen Sie im linken Fensterbereich **On Demand** aus.
2. Wählen Sie **Ausführen**.

## Ausführungsstatus anzeigen

Die Statusüberwachung ermöglicht die proaktive Verwaltung von Importvorgängen und die schnelle Erkennung von Problemen.

Anzeigen des Ausführungsstatus

1. Wählen Sie **Ausführungsstatus** aus, um eine Liste aller Importausführungen anzuzeigen.
2. Die Statusseite zeigt Folgendes an:

   - **Startdatum:** Als der Importvorgang begann
   - **Dauer:** Für die Verarbeitung erforderliche Gesamtzeit
   - **Typ des Imports:** Ob der Import geplant war oder On-Demand.
   - **Aktueller Status:** Echtzeit-Statusinformationen
      - **Wird ausgeführt:** Import wird derzeit ausgeführt
      - **Abgeschlossen:** Erfolgreicher Abschluss mit Datensatzzählern
      - **Fehler:** Fehler mit Diagnoseinformationen
