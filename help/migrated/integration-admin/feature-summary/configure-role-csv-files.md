---
jcr-language: en_us
title: Verwalten benutzerdefinierter Rollen über CSV-Dateien
description: Der Integrationsadministrator kann seinem Konto mehrere benutzerdefinierte Rollen gleichzeitig über CSV hinzufügen und diese verschiedenen Benutzern zuweisen. Dieser Ansatz automatisiert den Prozess der Erstellung von benutzerdefinierte Rollen.
contentowner: saghosh
exl-id: fce2f457-2834-491a-8331-64086f5a51b5
source-git-commit: f328076016d8c41455cad71f00d1dc9a1531e007
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 81%

---

# Verwalten benutzerdefinierter Rollen über CSV-Dateien

Der Integrationsadministrator kann seinem Konto mehrere benutzerdefinierte Rollen gleichzeitig über CSV hinzufügen und diese verschiedenen Benutzern zuweisen. Dieser Ansatz automatisiert den Prozess der Erstellung von benutzerdefinierte Rollen.

Sie können Rollen über die FTP- und Box-Connectors von Learning Manager konfigurieren.

Nachdem Sie sich bei Ihrem Box-Speicherkonto angemeldet haben, kann der Integrationsadministrator die folgenden CSV-Dateien zum Konto hinzufügen:

* user.csv
* role.csv
* user_role.csv

Laden Sie zunächst die CSV-Dateien herunter und ändern Sie die Werte entsprechend Ihren Anforderungen.

* Beispieldatei: [role.csv](assets/role.csv)
* Beispieldatei: [user_role.csv](assets/user_role.csv)

**role.csv**

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Spaltenname</b></p></td>
   <td>
    <p><b>Beschreibung</b></p></td>
   <td>
    <p><b>Beispielwerte</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Name</p></td>
   <td>
    <p>Identifizieren Sie die Rolle in CSV, die Benutzern zugewiesen werden soll.</p></td>
   <td>
    <p>Vertriebs-Autor</p></td>
  </tr>
  <tr>
   <td>
    <p>&lt;Entity&gt;</p></td>
   <td>
    <p>Identifizieren Sie den Zugriffstyp (VOLL, SCHREIBEN, REGISTRIEREN, BERICHT, KEIN) für jeden Entitätstyp wie KURS, KATALOG usw.</p></td>
   <td>
    <p>FULL</p>
    <p>NONE</p>
    <p>WRITE | REPORT</p>
    <p>Spaltennamen entsprechen Entitätstypnamen wie Katalog, Kurs, Lernplan usw.</p>
    <p>In der CSV ist eine Spalte für jeden Entitätstyp vorhanden. Entitäten, für die keine Berechtigung erteilt werden soll, sollten mit dem Wert NONE (KEINE) eingeschlossen werden</p></td>
  </tr>
  <tr>
   <td>
    <p>Katalogbereich-Angabe</p></td>
   <td>
    <p>Einfacher Katalogname oder durch PIPE (senkrechten Strich) (|) getrennte Liste der Katalognamen, die den Umfang dieser Rolle bestimmen.</p></td>
   <td>
    <p>Verkaufskatalog | Gesamtkatalog</p></td>
  </tr>
  <tr>
   <td>
    <p>Bereichsangabe für Benutzergruppe</p></td>
   <td>
    <p>Name und Wert des Benutzergruppenattributs, die den Bereich der Benutzer dieser Rolle bestimmen.</p>
    <p>Informationen zu den Bereichen finden Sie im folgenden Abschnitt.</p></td>
   <td>
    <p>Ort = London</p></td>
  </tr>
  <tr>
   <td>
    <p>Beschreibung</p></td>
   <td>
    <p>Optionale benutzerfreundliche Beschreibung, um den Zweck der Rolle und die spätere Bezugnahme besser zu verstehen.</p></td>
   <td>
    <p>Vollständiger Autorenzugriff auf LOs im Verkaufskatalog</p></td>
  </tr>
 </tbody>
</table>

Alle Spalten mit Ausnahme der Beschreibung sind obligatorisch.

## Definieren Sie den Umfang der Benutzergruppen {#definescopeofusergroups}

Sie können auf folgende Weise Bereiche für Benutzergruppen für verschiedene Arten von Gruppen angeben:

* Name der Benutzergruppe wie er ist (z. B. Alle Autoren, Meine benutzerdefinierte Gruppe)
* Blattattribut und -wert (z. B. Abteilung = HR)
* Selbstregistrierungsprofilgruppen (self_registration = profilename)
* Externe Registrierungsprofilgruppen (ext_registration = profilename)
* Das Team eines Managers mit direktem Bericht (manager_direct=`<emailid>`)
* Die vollständige Organisation eines Managers (manager_org=`<emailid>`)

**user_role.csv**

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Spaltenname</b></p></td>
   <td>
    <p><b>Beschreibung</b></p></td>
   <td>
    <p><b>Kommentar</b></p></td>
  </tr>
  <tr>
   <td>
    <p>ID</p></td>
   <td>
    <p>E-Mail-ID des Benutzers, dem eine konfigurierbare Rolle zugewiesen werden soll.</p></td>
   <td>
    <p>Wenn dem Benutzer bereits eine konfigurierbare Rolle zugewiesen wurde, wird die Rolle durch eine neue Rolle ersetzt, die in der CSV angegeben ist. Es wird kein Fehler gemeldet.</p></td>
  </tr>
  <tr>
   <td>
    <p>CustomRole</p></td>
   <td>
    <p>Name der konfigurierbaren Rolle, die dem Benutzer zugewiesen werden soll</p></td>
   <td>
    <p>Der Rollenname muss eine vorhandene Rolle sein, wie in der CSV angegeben. Hier können vom Administrator über die Benutzeroberfläche erstellte Rollen verwendet werden.</p></td>
  </tr>
 </tbody>
</table>

**Umfassende Funktionen**

Wenn für eine der folgenden Funktionen (Funktionen auf Kontoebene) die Berechtigung „Vollständig“ zugewiesen wird, werden der Benutzergruppenbereich und der Katalogbereich automatisch als VOLLSTÄNDIG betrachtet, da der Benutzer keinen eingeschränkten Zugriff auf diese Funktionen haben kann.

Wenn in der CSV Katalognamen oder Benutzergruppennamen angegeben sind, werden diese mit der Berechtigung FULL überschrieben.

* Ankündigungen
* Kenntnisse
* Gamification
* Benutzer
* Lernpläne
* E-Mail-Vorlagen

## Hinzufügen der Rollen-CSVs zum Konto {#addtherolecsvsintheaccount}

Wählen Sie in Ihrem Box-Konto **Importieren > Benutzer > Intern** und laden Sie die Dateien „role.csv“ und „user_role.csv“ hoch.

* Die Dateien role.csv und user_role.csv müssen in den Ordner kopiert werden **Importieren** > **Anwender** > **intern** > **Benutzerrolle**.
* Die Datei &quot;user.csv&quot; muss in den Ordner kopiert werden **Importieren** > **Anwender** > **intern**.

Beide CSV müssen nur über Box hochgeladen werden und können nicht über die Benutzeroberfläche hochgeladen werden.

>[!NOTE]
>
>Die CSV-Datei des Benutzers ist obligatorisch. Die CSVs der benutzerdefinierten Rolle sind jedoch optional. Alle vorhandenen Dateien werden verarbeitet, andere werden übersprungen.

Die mit der CSV-Datei erstellten benutzerdefinierten Rollen sind für Administratoren in der Benutzeroberfläche nicht sichtbar. Diese Rollen werden nicht durch Rollen in Beziehung gesetzt oder beeinflusst, die von der Benutzeroberfläche erstellt wurden (oder später erstellt werden sollen).

Von einer CSV-Datei erstellte benutzerdefinierte Rollen können vollständig über die CSV-Datei selbst verwaltet werden. Dazu gehören das Hinzufügen, Ändern und Löschen von Rollen.

Zugewiesene Rollen können durch Entfernen von Zuordnungseinträgen aus user_role csv widerrufen werden. Zuweisungen über die Admin-Benutzeroberfläche sind davon jedoch nicht betroffen.

Aktualisieren Sie die CSV-Dateien, um eine benutzerdefinierte Rolle zuzuweisen und zu widerrufen.

## Synchronisation von benutzerdefinierte Rollen {#synchronizationofcustomroles}

Nachdem der Integrationsadministrator die rollenbasierten CSVs in den Connector-Speicher hochgeladen hat, kann der Administrator die Synchronisierung mit den CSVs aktivieren. Jedes Mal, wenn eine benutzerdefinierte Rolle in den CSVs aktualisiert, hinzugefügt oder gelöscht wird, kann der Administrator die Informationen in den Dateien synchronisieren und die Liste der Rollen auf den neuesten Stand bringen.

Klicken Sie auf der Seite Erste Schritte im Bereich Administrator auf **[!UICONTROL Einstellungen]** > **[!UICONTROL Datenquellen]**.

Aktivieren Sie im Abschnitt „Synchronisierungseinstellungen“ die Option **[!UICONTROL Automatische Synchronisierung aktivieren]**.

![](assets/sync-settings.png)

*Wählen Sie die Option Automatische Synchronisierung aktivieren .*

Wenn Sie diese Option auswählen, können Sie die Zeit für die Synchronisierung genau zu der Zeit planen, die Sie im Feld „Synchronisierungszeit“ angegeben haben. Wenn Sie die Synchronisierungszeit auf 00:00 Uhr festlegen, werden die benutzerdefinierte Rolle jeden Tag genau zur angegebenen Zeit aktualisiert.

Wenn Sie die Daten bei Bedarf synchronisieren möchten, klicken Sie auf **[!UICONTROL Jetzt synchronisieren]**.

## Einschränkungen beim Konfigurieren von Rollen {#constraintswhileconfiguringroles}

In jedem Konto muss der Name einer Rolle eindeutig sein. Daher darf eine über die Benutzeroberfläche oder CSV erstellte Rolle nicht denselben Namen haben wie eine andere Rolle, die bereits von der Benutzeroberfläche oder CSV erstellt wurde.

In ähnlicher Weise kann einem Benutzer über die Admin-Benutzeroberfläche keine konfigurierbare Rolle zugewiesen werden, die über CSV erstellt wurde, da diese Rollen nicht verfügbar sind.

Die Benutzerzuweisung CSV kann jedoch zum Zuweisen von Rollen verwendet werden, die von der Benutzeroberfläche erstellt wurden.
