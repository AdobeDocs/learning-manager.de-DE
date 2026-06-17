---
jcr-language: en_us
title: Verfügbare Datensätze im Report Builder
description: Ein Referenzhandbuch zu den in Adobe Learning Manager Report Builder verfügbaren Datensätzen, Feldern und abgeleiteten Feldern.
contentowner: mmanuel
source-git-commit: b21196a3121c88bf54f33aecc0f4649eceb3ddf6
workflow-type: tm+mt
source-wordcount: '1363'
ht-degree: 28%

---


# Verfügbare Datensätze im Report Builder

Der Report Builder organisiert alle verfügbaren Spalten in Datensätzen und benennt Gruppen zugehöriger Felder. In diesem Artikel werden die einzelnen Datensätze aufgelistet, ihr Inhalt beschrieben und es wird angegeben, welche Datensätze in einem einzigen Bericht zusammengefasst werden können.

**Datensätze in dieser Version**

**Datensatz**

**Inhalt**

**Schlüsselfelder**

**Benutzer**

Profildaten von Teilnehmern für aktive und gelöschte Teilnehmer

Name, E-Mail-Adresse, Benutzer-ID, Manager, aktive Felder, Status

**Transkript**

Anmelde- und Abschlussdatensätze

Registrierungsdatum, Abschlussdatum, Fortschritt %, Status, Punktzahl

**Lernobjekt**

Kurs, Lernpfad und Zertifizierungsmetadaten

LO-Name, LO-ID, Typ, Katalog, Katalogbeschriftung, Status

**Lernobjektinstanz**

Details auf Instanzebene für Kurse mit mehreren Instanzen

Instanzname, Instanz-ID, Registrierungslimit, Frist

**Katalog**

Katalogmetadaten und Schlüssel-Wert-Paare für Katalogbeschriftungen

Katalogname, Katalog-ID, Beschriftungsschlüssel, Beschriftungswert. **Katalogbeschriftungsspalten sind kundenkonfiguriert**. Sie werden nur angezeigt, wenn für Ihr Konto Katalogbeschriftungen eingerichtet sind. Die angezeigten Bezeichnungsnamen und -werte spiegeln Ihre eigene Konfiguration wider.

**Benutzergruppe**

Benutzergruppenmitgliedschaft und Hierarchie

Benutzergruppenname, Benutzergruppen-ID, übergeordnete Gruppe, Mitgliederanzahl

**Modulsitzung**

Sitzungsdetails für Klassenzimmer, virtuelle Klassenzimmer und E-Learning-Module

Sitzungs-ID, Sitzungsname, Kursleitername(n), Startzeit, Endzeit, Ort

Liste der Spalten in Datasets

Katalog

* Erstellungsdatum
* ID
* Name

Katalogbeschriftung

* Katalog
* ID
* Name
* Wert

Benutzerdefiniertes Feld (Lernobjekt)

* Lernobjektabschluss in %
* Lernobjekt-Zeitplaneinhaltung in %

Benutzerdefiniertes Feld (Benutzer)

* Benutzerabschluss in %
* Einhaltung des Benutzerzeitplans in %

Lernobjekt

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

Lernobjektinstanz

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

Modul

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

Transkript (Lernobjekt)

* Abschlussdatum
* Abschlussfrist
* Abschlussquelle
* Abschlussquelle – Benutzer-ID
* Abschlussquelle – Benutzername
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

Transkript (Modul)

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

Benutzer

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

Benutzergruppe

* Erstellungsdatum
* ID
* Mitgliederanzahl
* Name
* Status

Benutzergruppe (aktives Feld)

* Erstellungsdatum
* ID
* Mitgliederanzahl
* Name
* Status

Benutzergruppe (benutzerdefiniert)

* Erstellungsdatum
* ID
* Mitgliederanzahl
* Name
* Status

Benutzergruppe (direktes Team)

* Erstellungsdatum
* ID
* Mitgliederanzahl
* Name
* E-Mail-Adresse des Besitzers/der Besitzerin
* Besitzer-ID
* Name des Besitzers/der Besitzerin
* Eindeutige Besitzer-ID
* Status

Benutzergruppe (integriert)

* Erstellungsdatum
* ID
* Mitgliederanzahl
* Name
* Status

Benutzergruppe (Team)

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

**Wie Datasets zusammenkommen**

Nicht jedes Datensatzpaar kann in einem einzigen Bericht kombiniert werden. Datensätze müssen eine logische Beziehung im Datenmodell von Adobe Learning Manager gemeinsam nutzen, um verknüpfbar zu sein. Wenn Sie die erste Spalte hinzufügen, filtert der Report Builder die verbleibenden Datensätze so, dass nur kompatible Datensätze angezeigt werden. Wenn ein Datensatz ausgegraut angezeigt wird, kann er nicht direkt mit den bereits ausgewählten Spalten verknüpft werden.

Das bedeutet, dass der Datensatz nicht mit den bereits ausgewählten Spalten verknüpft werden kann. Dies ist eine harte Einschränkung im Datenmodell. Die beiden Datasets haben keinen kompatiblen Verknüpfungspfad.

Ein gängiges Beispiel ist das abgeleitete Feld **Compliance %**. Wenn Kompatibilität % ausgewählt ist, sind die Datensätze **Transkript**, **Modul Transkript** und **LO-Instanz** deaktiviert. Compliance % wird auf Benutzer- oder Benutzergruppenebene anhand von Lernobjekten und Katalogen berechnet. Es soll nur zusammen mit **Benutzer**, **Benutzergruppe**, **Lernobjekt** und **Katalog** Spalten und Filtern verwendet werden.

Wenn Sie einen deaktivierten Datensatz verwenden möchten, heben Sie die Auswahl der Spalten auf, die den Konflikt verursachen, und fügen Sie dann den benötigten Datensatz hinzu.

Die folgenden Verknüpfungsbeziehungen werden aus dem Datenmodell des Report Builders abgeleitet. Wenn Sie diese verstehen, können Sie vor dem Erstellen eines Berichts besser planen, welche Datensätze kombiniert werden sollen.

**Hub-Datensätze**

Zwei Datensätze fungieren als zentrale Hubs. Die meisten anderen Datensätze stellen eine Verbindung her:

* **Registrierung** (Registrierungsdatensatz), die primäre Faktentabelle. Es stellt eine direkte Verbindung zu **Benutzer** (dem Teilnehmer, der sich registriert hat), **Lernobjekt** (dem, bei dem er sich registriert hat) und über das Lernobjekt zu **Modulsitzung**, **Katalog**, **Katalogbeschriftung** und **LO-Instanz** her.
* **Modultranskript** (moduleTranscript-Datensatz) — die Fortschrittstabelle auf Modulebene. Es stellt eine Verbindung zu **Benutzer** und zu **Modulsitzung** her, die wiederum mit **Lernobjekt** verknüpft ist.

Die meisten Berichte, die Teilnehmer-, Kurs- und Abschlussdaten kombinieren, werden über einen dieser beiden Hubs erstellt.

**Pfade nach Anwendungsfall verbinden**

**So kombinieren Sie diese Datensätze**

**Der Verknüpfungspfad**

**Benutzer** + **Registrierung**

Registrierung → Benutzer (über Teilnehmer-ID)

**Registrierung** + **Lernobjekt**

Registrierung → Lernobjekt (über LO-ID)

**Lernobjekt** + **Katalog**

Lernobjekt → LO-Katalog → Katalog

**Lernobjekt** + **Katalogbeschriftung**

Lernobjekt → LO-Katalogbeschriftungen

**Lernobjekt** + **LO-Instanz**

LO-Instanz → Lernobjekt

**Modulsitzung** + **Lernobjekt**

Modulsitzung → Lernobjekt (über Sitzungskurs)

**Modulsitzung** + **Benutzer** (Kursleiter)

Modulsitzung → Benutzer (über Kursleiter-Alias FK)

**Benutzer** + **Benutzergruppe**

Benutzergruppenmitgliedschaft → Benutzer + Benutzergruppe

**Lernobjekt** + **Benutzer** (Autor)

LO Autor → Benutzer (über Autor Alias FK)

**Benutzer** + **Aktive Felder**

Benutzer-aktive Felder → Benutzer (über Benutzer-ID)

**Aliasbeziehungen**

Einige Felder im Datenmodell verbinden sich mit der Entität **Benutzer** über eine benannte Rolle und nicht über eine direkte Teilnehmer-ID. Dies sind verzerrte Fremdschlüssel. Sie verweisen auf dieselbe Benutzertabelle, stellen aber eine andere Rolle dar:

* **Kursleiter**: Modulsitzung tritt dem Benutzer als Kursleiter der Sitzung bei
* **Autor**: LO-Autor tritt dem Benutzer als Autor des Lernobjekts bei
* **Manager**: Der Benutzer tritt sich selbst bei, um den Manager des Teilnehmers zu repräsentieren
* **Abgeschlossen von**: Die Registrierung und das Modultranskript enthalten jeweils eine separate &quot;completed by&quot;-Benutzerreferenz

Aus diesem Grund kann ein einziger Bericht sowohl den Namen eines Teilnehmers als auch den Namen seines Kursleiters anzeigen. Beide stammen aus der Entität &quot;Benutzer&quot; über unterschiedliche Verknüpfungspfade.

**Datasettypen für Benutzergruppen**

Die Kategorie **Benutzergruppe** enthält mehrere unterschiedliche Datensatzansichten, die jeweils einen anderen Gruppentyp abdecken:

**Datensatz**

**Gruppentyp**

**Benutzergruppe** (Benutzergruppe)

Alle Benutzergruppen. Verwenden Sie dies als primären Benutzergruppendatensatz.

**Active Field User Group** (active_field_user_group)

Gruppen basierend auf aktiven Feldwerten (z. B. Region, Abteilung)

**Team-Benutzergruppe** (team_user_group)

Manager-hierarchiebasierte Gruppen

**Benutzerdefinierte Benutzergruppe** (benutzerdefinierte_Benutzergruppe)

Manuell konfigurierte benutzerdefinierte Gruppen

**Integrierte Benutzergruppe** (integrierte_Benutzergruppe)

Systemdefinierte Gruppen

Die ansichtsbasierten Benutzergruppendatensätze (**Aktives Feld**, **Team**, **Benutzerdefiniert**, **Integriert**) verfügen nicht über direkte Fremdschlüsselbeziehungen im Schema, sondern sind SQL-Ansichten. Dies bedeutet, dass sie über lockerere Join-Einschränkungen verfügen als der **Benutzergruppe**-Kerndatensatz. Verwenden Sie den **Benutzergruppe**-Kerndatensatz, wenn Sie Benutzergruppendaten mit Registrierungs- oder Transkriptdaten verbinden, um die zuverlässigsten Ergebnisse zu erzielen.

**Abgeleitete Felder**

Abgeleitete Felder sind vorberechnete Spalten, die vom Report Builder berechnet werden. Sie werden getrennt von den Standardspalten in der Spaltenauswahl aufgeführt.

**Abgeleitetes Feld**

**Was berechnet wird**

**Erforderliche Datensätze**

**Compliance %**

Prozentsatz der erforderlichen Teilnehmer, die Kurse mit Compliance-Tags absolviert haben

Benutzergruppe, Lernobjekt, Transkript

**Abschluss %**

Abschlüsse aufgeteilt nach Anmeldungen × 100

Transkript oder Lernobjekt

**Anzahl registrierter Benutzer**

Gesamtzahl der registrierten Teilnehmer für ein Lernobjekt

Lernobjekt

**Anzahl der Abschlüsse**

Abschlüsse für ein Lernobjekt insgesamt

Lernobjekt

**Startzahl**

Teilnehmer, die begonnen, aber nicht abgeschlossen haben

Lernobjekt

**Mitgliederzahl**

Anzahl der Benutzer in einer Benutzergruppe

Benutzergruppe
