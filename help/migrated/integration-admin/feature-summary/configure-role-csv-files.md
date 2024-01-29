---
jcr-language: en_us
title: Verwalten benutzerdefinierter Rollen über CSV-Dateien
description: Der Integrationsadministrator kann seinem Konto mehrere benutzerdefinierte Rollen gleichzeitig per CSV hinzufügen und diese verschiedenen Benutzern zuweisen. Dieser Ansatz automatisiert den Prozess der Erstellung benutzerdefinierter Rollen.
contentowner: saghosh
source-git-commit: ab6737e8b43222a6538921b0628a504a5f15859d
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 0%

---



# Verwalten benutzerdefinierter Rollen über CSV-Dateien

Der Integrationsadministrator kann seinem Konto mehrere benutzerdefinierte Rollen gleichzeitig per CSV hinzufügen und diese verschiedenen Benutzern zuweisen. Dieser Ansatz automatisiert den Prozess der Erstellung benutzerdefinierter Rollen.

Sie können Rollen über die FTP- und Box-Connectors für Learning Manager konfigurieren.

Nachdem Sie sich bei Ihrem Box- oder ExaVault-Speicherkonto angemeldet haben, kann der Integrationsadministrator die folgenden CSV-Dateien zum Konto hinzufügen:

* role.csv
* user_role.csv

Laden Sie zunächst die CSV-Dateien herunter und ändern Sie die Werte entsprechend Ihren Anforderungen.

**role.csv**
[Beispieldatei: role.csv](assets/role.csv) [Beispieldatei: user_role.csv](assets/user-role.csv)

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
    <p>Legen Sie die Rolle in der CSV-Datei fest, die den Benutzern zugewiesen werden soll.</p></td>
   <td>
    <p>Vertriebsmitarbeiter</p></td>
  </tr>
  <tr>
   <td>
    <p>&lt;Entity&gt;</p></td>
   <td>
    <p>Identifizieren Sie den Zugriffstyp (VOLL, SCHREIBEN, REGISTRIEREN, BERICHT, KEIN) für jeden Entitätstyp wie KURS, KATALOG usw.</p></td>
   <td>
    <p>VOLL</p>
    <p>KEINE</p>
    <p>SCHREIBEN | BERICHT</p>
    <p>Spaltennamen entsprechen Entitätstypnamen wie Katalog, Kurs, Lernplan usw.</p>
    <p>In der CSV-Datei ist eine Spalte für jeden Entitätstyp vorhanden. Unternehmen, für die keine Genehmigung erteilt werden soll, sollten mit dem Wert NONE</p></td>
  </tr>
  <tr>
   <td>
    <p>Katalogbereichsspezifizierer</p></td>
   <td>
    <p>Einzelner Katalogname oder eine durch PIPE (|) getrennte Liste von Katalognamen, die den Umfang dieser Rolle bestimmen.</p></td>
   <td>
    <p>Vertriebskatalog | Allgemeiner Katalog</p></td>
  </tr>
  <tr>
   <td>
    <p>Bereichsangabe für Benutzergruppe</p></td>
   <td>
    <p>Name und Wert des Benutzergruppenattributs, die den Umfang der Benutzer dieser Rolle bestimmen.</p>
    <p>Die Geltungsbereiche finden Sie im folgenden Abschnitt.</p></td>
   <td>
    <p>location=London</p></td>
  </tr>
  <tr>
   <td>
    <p>Beschreibung</p></td>
   <td>
    <p>Optionale benutzerfreundliche Beschreibung, um den Zweck der Rolle und die spätere Referenz zu verstehen.</p></td>
   <td>
    <p>Vollständiger Autorenzugriff auf LOs im Verkaufskatalog</p></td>
  </tr>
 </tbody>
</table>

Alle Spalten außer Description sind obligatorisch.

## Umfang der Benutzergruppen definieren {#definescopeofusergroups}

Sie können auf folgende Weise Bereiche für Benutzergruppen für verschiedene Gruppentypen angeben:

* Name der Benutzergruppe wie vorhanden (z. B. &quot;Alle Autoren&quot;, &quot;Meine benutzerdefinierte Gruppe&quot;)
* Blattattribut und -wert (z. B. Department=HR)
* Profilgruppen für die Selbstregistrierung (Selbstregistrierung=Profilname)
* Externe Registrierungsprofilgruppen (ext_registration=profilename)
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
    <p>Wenn dem Benutzer bereits eine konfigurierbare Rolle zugewiesen wurde, wird die Rolle durch eine neue Rolle ersetzt, die in der CSV-Datei angegeben ist. Es wird kein Fehler gemeldet.</p></td>
  </tr>
  <tr>
   <td>
    <p>CustomRole</p></td>
   <td>
    <p>Name der konfigurierbaren Rolle, die dem Benutzer zugewiesen werden soll</p></td>
   <td>
    <p>Der Rollenname muss eine vorhandene Rolle sein, die in der CSV-Datei angegeben ist. Rollen, die vom Administrator über die Benutzeroberfläche erstellt wurden, können hier verwendet werden.</p></td>
  </tr>
 </tbody>
</table>

**Vollständiger Umfang**

Wenn für eine der folgenden Funktionen (Funktionen auf Kontoebene) eine vollständige Berechtigung zugewiesen wird, werden der Benutzergruppenumfang und der Katalogumfang automatisch als VOLLSTÄNDIG betrachtet, da der Benutzer keinen eingeschränkten Zugriff auf diese Funktionen haben kann.

Wenn Katalognamen oder Benutzergruppennamen in der CSV-Datei angegeben werden, werden sie mit der Berechtigung &quot;VOLL&quot; überschrieben.

* Ankündigungen
* Kenntnisse
* Gamification
* Benutzer
* Lernpläne
* E-Mail-Vorlagen

## Rollen-CSVs zum Konto hinzufügen {#addtherolecsvsintheaccount}

Wählen Sie in Ihrem Box-Konto **Importieren > Benutzer > intern**, und laden Sie die Dateien &quot;role.csv&quot; und &quot;user_role.csv&quot; hoch.

* Die CSVs der benutzerdefinierten Rolle müssen in den Ordner &quot;import->user->internal->user_role&quot; kopiert werden.
* Die Benutzer-CSV muss in den Ordner &quot;import->user->internal&quot; kopiert werden.

Beide CSV müssen nur über Box oder FTP hochgeladen werden und können nicht über die Benutzeroberfläche hochgeladen werden.

>[!NOTE]
>
>Die CSV-Datei des Benutzers ist obligatorisch. Die CSVs der benutzerdefinierten Rolle sind jedoch optional. Alle vorhandenen Dateien werden verarbeitet, andere werden übersprungen.

Die benutzerdefinierten Rollen, die mit der CSV-Datei erstellt wurden, sind für Administratoren in der Benutzeroberfläche nicht sichtbar. Diese Rollen sind nicht von Rollen abhängig, die von der Benutzeroberfläche erstellt (oder später erstellt) werden, oder werden von ihnen beeinflusst.

Von einer CSV-Datei erstellte benutzerdefinierte Rollen können vollständig über die CSV-Datei selbst verwaltet werden. Dazu gehören das Hinzufügen, Ändern und Löschen von Rollen.

Zugewiesene Rollen können widerrufen werden, indem Zuweisungseinträge aus der CSV-Datei &quot;user_role&quot; entfernt werden. Zuweisungen über die Admin-Benutzeroberfläche sind davon jedoch nicht betroffen.

Um eine benutzerdefinierte Rolle zuzuweisen und zu widerrufen, aktualisieren Sie die CSV-Dateien.

## Synchronisierung benutzerdefinierter Rollen {#synchronizationofcustomroles}

Nachdem der Integrationsadministrator die rollenbasierten CSVs im Connector-Speicher hochgeladen hat, kann der Administrator die Synchronisierung mit den CSVs aktivieren. Jedes Mal, wenn eine benutzerdefinierte Rolle in den CSVs aktualisiert, hinzugefügt oder gelöscht wird, kann der Administrator die Informationen in den Dateien synchronisieren und die Liste der Rollen auf den aktuellen Stand bringen.

Klicken Sie auf der Seite Erste Schritte im Bereich Administrator auf **[!UICONTROL Einstellungen]** > **[!UICONTROL Datenquellen]**.

Aktivieren Sie im Abschnitt Synchronisationseinstellungen die Option **[!UICONTROL Automatische Synchronisierung aktivieren]**.

![](assets/sync-settings.png)

*Wählen Sie die Option Automatische Synchronisierung aktivieren .*

Wenn Sie diese Option auswählen, können Sie die Zeit für die Synchronisierung genau zu dem Zeitpunkt planen, den Sie im Feld &quot;Synchronisierungszeit&quot; angeben. Wenn Sie die Synchronisierungszeit als 12:00 Uhr angeben, werden die benutzerdefinierten Rollen täglich genau zu der angegebenen Zeit aktualisiert.

Wenn Sie die Daten bei Bedarf synchronisieren möchten, klicken Sie auf **[!UICONTROL Jetzt synchronisieren]**.

## Einschränkungen beim Konfigurieren von Rollen {#constraintswhileconfiguringroles}

In jedem Konto muss der Name einer Rolle eindeutig sein. Daher darf eine über die Benutzeroberfläche oder CSV erstellte Rolle nicht denselben Namen wie eine andere Rolle haben, die bereits von der Benutzeroberfläche oder CSV erstellt wurde.

In ähnlichen Zeilen kann einem Benutzer in der Admin-Benutzeroberfläche keine konfigurierbare Rolle zugewiesen werden, die über CSV erstellt wurde, da diese Rollen nicht verfügbar sind.

Die Benutzerzuweisungs-CSV kann jedoch verwendet werden, um Rollen zuzuweisen, die von der Benutzeroberfläche erstellt wurden.
