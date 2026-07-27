---
jcr-language: en_us
title: Verfügbare Datensätze im Report Builder
description: Ein Referenzhandbuch zu den in Adobe Learning Manager Report Builder verfügbaren Datensätzen, Feldern und abgeleiteten Feldern.
contentowner: mmanuel
source-git-commit: 8823a5481bc3b34266f7ec36a8f3c26cb923e1ce
workflow-type: tm+mt
source-wordcount: '1410'
ht-degree: 27%

---


# Verfügbare Datensätze im Report Builder

## Übersicht

Der Report Builder organisiert alle verfügbaren Spalten in Datensätzen und benennt Gruppen zugehöriger Felder. In diesem Artikel werden die einzelnen Datensätze aufgelistet, ihr Inhalt beschrieben und es wird angegeben, welche Datensätze in einem einzigen Bericht zusammengefasst werden können.

## **Verfügbare Datasets**

Die Angaben in der Tabelle sind nicht vollständig. Im Abschnitt **Liste der Spalten in Datasets** finden Sie eine vollständige Auflistung aller Spalten in Datasets.

| **Dataset** | **Inhalt** | **Schlüsselfelder** |
|----------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Benutzer** | Profildaten von Teilnehmern für aktive und gelöschte Teilnehmer | Name, E-Mail-Adresse, Benutzer-ID, Manager, aktive Felder, Status |
| **Transkript (Lernobjekt) und Transkript (Modul)** | Anmelde- und Abschlussdatensätze | Registrierungsdatum, Abschlussdatum, Fortschritt in Prozent, Status |
| **Lernobjekt** | Kurs, Lernpfad und Zertifizierungsmetadaten | Lernobjektname, Lernobjekt-ID, Typ, Katalog, Katalogbeschriftung, Status |
| **Lernobjektinstanz** | Details auf Instanzebene für Kurse mit mehreren Instanzen | Instanzname, Instanz-ID, Registrierungslimit, Frist |
| **Katalog** | Katalogmetadaten und Schlüssel-Wert-Paare für Katalogbeschriftungen | Autorennamen, Erstellungsdatum, Dauer, Format. **Katalogbeschriftungsspalten sind kundenkonfiguriert**. Sie werden nur angezeigt, wenn für Ihr Konto Katalogbeschriftungen eingerichtet sind. Die angezeigten Bezeichnungsnamen und -werte spiegeln Ihre eigene Konfiguration wider. |
| **Benutzergruppe** | Benutzergruppenmitgliedschaft und Hierarchie | Erstellungsdatum, Anzahl der Mitglieder, Name, Status |
| **Modul** | Sitzungsdetails für Klassenzimmer, virtuelle Klassenzimmer und E-Learning-Module | Modul-ID, Kursleitername(n), Startzeit, Endzeit, Ort |


>[!NOTE]
>
>Bei Kursen, die von einem anderen Konto durch Katalogfreigabe erworben wurden, gibt die Spalte **Autorennamen** im Lernobjektdataset den ursprünglichen Autorennamen aus dem Quellkonto zurück. Dies unterscheidet sich von der standardmäßigen ALM-Admin-Oberfläche und den festen Berichten, in denen erworbene Kurse stattdessen &quot;externer Autor&quot; anzeigen. Dieses Verhalten ist spezifisch für Report Builder und gilt nur für Peer-Konten (Empfangskonten).

## Liste der Spalten in Datasets

### Katalog

* Erstellungsdatum
* ID

* Name

### Katalogbeschriftung

* ID
* Name
* Wert

### Benutzerdefiniertes Feld (Lernobjekt)

* Lernobjektabschluss in %
* Lernobjekt-Zeitplaneinhaltung in %

### Benutzerdefiniertes Feld (Benutzer)

* Benutzerabschluss in %
* Einhaltung des Benutzerzeitplans in %

### Lernobjekt

* Autorennamen
* Datum der automatischen Deaktivierung
* Anzahl der Abschlüsse
* Erstellungsdatum
* Dauer (Minuten)
* Anzahl der Registrierungen
* Registrierungstyp
* Format
* ID
* Instanzenwechsel aktiviert
* Letztes Abschlussdatum
* Datum der letzten Veröffentlichung
* Mehrfacheinschreibung aktiviert
* Name
* Voraussetzungen durchgesetzt
* Preis
* Punkte für Kenntnisse
* Kenntnisstufen
* Name der Kenntnisse
* Durchschnittliche Sternebewertung
* Anzahl der Sternebewertungen
* Anzahl Begonnen
* Status
* Tags
* Typ
* Eindeutige ID

### Lernobjektinstanz

* Abschlussfrist
* Erstellungsdatum
* Registrierungsfrist
* ID
* Letztes Abschlussdatum
* Lernobjekt-ID
* Name
* Status
* Typ
* Frist für die Aufhebung der Registrierung

### Modul

* Endzeit für Zugriff
* Startzeit für Zugriff
* Kurs-ID
* Kursinstanz-ID
* Dauer (Minuten)
* Endzeit
* Anzahl der Registrierungen
* ID
* Kursleiternamen
* Standort
* Standortinformationen
* Standortregion
* Standort-URL
* Modul-ID
* Name
* Maximale Anzahl Lizenzen
* Startzeit
* Typ
* Limit für Warteliste

### Transkript (Lernobjekt)

* Abschlussdatum
* Abschlussfrist
* Abschlussquelle
* Abschlussquelle * Benutzer-ID
* Vervollständigungsquelle * Benutzername
* Registrierungsdatum
* Registrierungsquelle
* Registrierungsstatus
* Lernobjekt-ID
* Lernobjektname
* Lernobjektinstanz-ID
* Überfällig
* Eltern-Lernobjekt-ID
* Bestanden am
* Fortschritt in Prozent
* Stammzertifizierungs-ID
* Anfangsdatum
* Status
* Verbrachte Zeit (Minuten)
* Höchste Punktzahl des Benutzers/der Benutzerin
* Benutzer-ID
* Aktuelle Punktzahl des Benutzers/der Benutzerin

### Transkript (Modul)

* Abschlussdatum
* Kurs-ID
* Modul-ID
* Modulname
* Bestanden am
* Fortschritt in Prozent
* Gesamtpunktzahl für Quizmodul
* Anfangsdatum
* Status
* Verbrachte Zeit (Minuten)
* Benutzer-E-Mail
* Höchste Punktzahl des Benutzers/der Benutzerin
* Benutzer-ID
* Aktuelle Punktzahl des Benutzers/der Benutzerin
* Benutzername

### Benutzer

* Adobe ID
* Inhaltssprache
* Erstellungsdatum
* Löschdatum
* Anzahl direkter Team-Mitglieder
* E-Mail
* ID
* Sprache der Benutzeroberfläche
* Ist Admin
* Ist Autor/Autorin
* Ist benutzerdefinierte Rolle
* Ist Kursleiter/-leiterin
* Ist Integrations-Admin
* Ist Teilnehmer/Teilnehmerin
* Ist Manager/Managerin
* Ist Root-Benutzer/-Benutzerin
* Datum des letzten Zugriffs
* E-Mail-Adresse des Managers
* Manager-ID
* Managername
* Eindeutige Manager-ID
* Name
* Rollen
* Quelle
* Status
* Anzahl der Team-Mitglieder
* Zeitzone
* Typ
* Eindeutige ID

### Benutzergruppe

* Erstellungsdatum
* ID
* Mitgliederanzahl
* Name
* Status

### Benutzergruppe (aktives Feld)

* Erstellungsdatum
* ID
* Mitgliederanzahl
* Name
* Status

### Benutzergruppe (benutzerdefiniert)

* Erstellungsdatum
* ID
* Mitgliederanzahl
* Name
* Status

### Benutzergruppe (direktes Team)

* Erstellungsdatum
* ID
* Mitgliederanzahl
* Name
* E-Mail-Adresse des Besitzers/der Besitzerin
* Besitzer-ID
* Name des Besitzers/der Besitzerin
* Eindeutige Besitzer-ID
* Status

### Benutzergruppe (integriert)

* Erstellungsdatum
* ID
* Mitgliederanzahl
* Name
* Status

### Benutzergruppe (Team)

* Erstellungsdatum
* ID
* Mitgliederanzahl
* Beschreibung
* Name
* E-Mail-Adresse des Besitzers/der Besitzerin
* Besitzer-ID
* Name des Besitzers/der Besitzerin
* Besitzerstatus
* Eindeutige Besitzer-ID
* Status

## Zusammenführung von Datensätzen

Nicht jedes Datensatzpaar kann in einem einzigen Bericht kombiniert werden. Datensätze müssen eine logische Beziehung im Datenmodell von Adobe Learning Manager gemeinsam nutzen, um verknüpfbar zu sein. Wenn Sie die erste Spalte hinzufügen, filtert der Report Builder die verbleibenden Datensätze so, dass nur kompatible Datensätze angezeigt werden. Wenn ein Datensatz ausgegraut angezeigt wird, kann er nicht direkt mit den bereits ausgewählten Spalten verknüpft werden.

Das bedeutet, dass der Datensatz nicht mit den bereits ausgewählten Spalten verknüpft werden kann. Dies ist eine harte Einschränkung im Datenmodell. Die beiden Datasets haben keinen kompatiblen Verknüpfungspfad.

Ein gängiges Beispiel ist das abgeleitete Feld **Compliance %**. Wenn Kompatibilität % ausgewählt ist, sind die Datensätze **Transkript**, **Modul Transkript** und **LO-Instanz** deaktiviert. Compliance % wird auf Benutzer- oder Benutzergruppenebene anhand von Lernobjekten und Katalogen berechnet. Es soll nur zusammen mit **Benutzer**, **Benutzergruppe**, **Lernobjekt** und **Katalog** Spalten und Filtern verwendet werden.

Wenn Sie einen deaktivierten Datensatz verwenden möchten, heben Sie die Auswahl der Spalten auf, die den Konflikt verursachen, und fügen Sie dann den benötigten Datensatz hinzu.

>[!NOTE]
>
>Wenn ein generierter Bericht Kursdaten, aber keine Lernpfaddaten enthält, überprüfen Sie, ob Sie dem Lernobjektdataset mit dem Moduldataset beigetreten sind. Module sind direkt mit Kursen verknüpft, jedoch nicht direkt mit Lernpfaden. Wenn Modulfelder enthalten sind, gibt der Report Builder möglicherweise nur Kursdatensätze zurück und filtert Lernpfade heraus. Um einen Bericht zu Lernpfaden zu erstellen, vermeiden Sie das Hinzufügen von Modulfeldern, es sei denn, der Bericht ist speziell zur Analyse von Moduldaten auf Kursebene vorgesehen.

Die folgenden Verknüpfungsbeziehungen werden aus dem Datenmodell des Report Builders abgeleitet. Wenn Sie diese verstehen, können Sie vor dem Erstellen eines Berichts besser planen, welche Datensätze kombiniert werden sollen.

### Hub-Datensätze

Zwei Datensätze fungieren als zentrale Hubs. Die meisten anderen Datensätze stellen eine Verbindung her:

* **Registrierung** (Registrierungsdatensatz), die primäre Faktentabelle. Es stellt eine direkte Verbindung zu **Benutzer** (dem Teilnehmer, der sich registriert hat), **Lernobjekt** (dem, bei dem er sich registriert hat) und über das Lernobjekt zu **Modul**, **Katalog**, **Katalogbeschriftung** und **LO-Instanz** her.
* **Modultranskript** (moduleTranscript-Datensatz): die Fortschrittstabelle auf Modulebene. Es stellt eine Verbindung zu **Benutzer** und zu **Modul** her, das wiederum mit **Lernobjekt** verknüpft ist.

Die meisten Berichte, die Teilnehmer-, Kurs- und Abschlussdaten kombinieren, werden über einen dieser beiden Hubs erstellt.

### Aliasing-Beziehungen

Einige Felder im Datenmodell verbinden sich mit der Entität **Benutzer** über eine benannte Rolle und nicht über eine direkte Teilnehmer-ID. Dies sind verzerrte Fremdschlüssel. Sie verweisen auf dieselbe Benutzertabelle, stellen aber eine andere Rolle dar:

* **Kursleiter**: Modul tritt dem Benutzer als Kursleiter der Sitzung bei
* **Autor**: Lernobjektautor tritt dem Benutzer als Autor des Lernobjekts bei
* **Manager**: Der Benutzer tritt sich selbst bei, um den Manager des Teilnehmers zu repräsentieren
* **Abgeschlossen von**: Die Registrierung und das Modultranskript enthalten jeweils eine separate &quot;completed by&quot;-Benutzerreferenz

Aus diesem Grund kann ein einziger Bericht sowohl den Namen eines Teilnehmers als auch den Namen seines Kursleiters anzeigen. Beide stammen aus der Entität &quot;Benutzer&quot; über unterschiedliche Verknüpfungspfade.

### Datasettypen der Benutzergruppe

Die Kategorie **Benutzergruppe** enthält mehrere unterschiedliche Datensatzansichten, die jeweils einen anderen Gruppentyp abdecken:

| **Datensatz** | **Gruppentyp** |
|---------------------------------------------------------|---------------------------------------------------------------|
| **Benutzergruppe** (Benutzergruppe) | Alle Benutzergruppen. Verwenden Sie dies als primären Benutzergruppendatensatz. |
| **Benutzergruppe (aktives Feld)** (aktive_Feldbenutzergruppe) | Gruppen basierend auf aktiven Feldwerten (z. B. Region, Abteilung) |
| **Benutzergruppe (Team)** (team_user_group) | Manager-hierarchiebasierte Gruppen |
| **Benutzergruppe (Benutzerdefiniert)** (benutzerdefinierte_Benutzergruppe) | Manuell konfigurierte benutzerdefinierte Gruppen |
| **Benutzergruppe (integriert)** (integrierte_Benutzergruppe) | Systemdefinierte Gruppen |

Die ansichtsbasierten Benutzergruppendatensätze (**Aktives Feld**, **Team**, **Benutzerdefiniert**, **Integriert**) verfügen nicht über direkte Fremdschlüsselbeziehungen im Schema, sondern sind SQL-Ansichten. Dies bedeutet, dass sie über lockerere Join-Einschränkungen verfügen als der **Benutzergruppe**-Kerndatensatz. Verwenden Sie den **Benutzergruppe**-Kerndatensatz, wenn Sie Benutzergruppendaten mit Registrierungs- oder Transkriptdaten verbinden, um die zuverlässigsten Ergebnisse zu erzielen.

## Abgeleitete Felder

Abgeleitete Felder sind vorberechnete Spalten, die vom Report Builder berechnet werden. Sie werden getrennt von den Standardspalten in der Spaltenauswahl aufgeführt.

| **Abgeleitetes Feld** | **Was berechnet wird** | **Erforderliche Datensätze** |
|-------------------------|-------------------------------------------------------------------------|-----------------------------------------|
| **Compliance %** | Prozentsatz der erforderlichen Teilnehmer, die Kurse mit Compliance-Tags absolviert haben | Benutzergruppe, Lernobjekt, Transkript |
| **Abschluss %** | Abschlüsse geteilt durch Registrierungen x 100 | Transkript oder Lernobjekt |
| **Anzahl registrierter Benutzer** | Gesamtzahl der registrierten Teilnehmer für ein Lernobjekt | Lernobjekt |
| **Anzahl der Abschlüsse** | Abschlüsse für ein Lernobjekt insgesamt | Lernobjekt |
| **Startzahl** | Teilnehmer, die begonnen, aber nicht abgeschlossen haben | Lernobjekt |
| **Anzahl der Mitglieder** | Anzahl der Benutzer in einer Benutzergruppe | Benutzergruppe |
