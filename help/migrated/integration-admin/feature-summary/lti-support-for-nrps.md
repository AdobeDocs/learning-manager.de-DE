---
description: Erfahren Sie, wie Adobe Learning Manager mithilfe von NRPS benutzerdefinierte Teilnehmerattribute von einer LTI 1.3-Plattform in Teilnehmerprofile als aktive Felder synchronisiert
jcr-language: en_us
title: LTI-Unterstützung für NRPS
exl-id: 4c972319-b8ce-4f2d-9ccb-1b93c6cc6ac0
source-git-commit: 92be9eb8ece6d083efe595894a492540cd96eead
workflow-type: tm+mt
source-wordcount: '1845'
ht-degree: 0%
---

# LTI-Unterstützung für NRPS

## Übersicht

Adobe Learning Manager unterstützt die NRPS-Spezifikation (Names and Role Provisioning Services), wenn es als LTI 1.3-Tool (Learning Tools Interoperability) fungiert. Wenn ein Teilnehmer den Lern-Manager von einem externen Lern-Management-System (der Plattform) aus startet, ruft der Lern-Manager den Mitgliedschaftsdatensatz des Teilnehmers von der Plattform ab. Anschließend werden die benutzerdefinierten Attribute in diesem Datensatz, z. B. Abteilungs- oder Mitarbeiter-ID, in das Profil des Teilnehmers als aktive Felder kopiert.

## Anwendungsszenarien

* **Teilnehmerprofile automatisch anreichern.** Bringen Sie Attribute wie Abteilungen, Mitarbeiter-ID oder benutzerdefinierte Metadaten von Ihrer Plattform in Learning Manager ein, ohne manuelle Dateneingabe oder separate Importe durchzuführen.
* **Analysieren Sie, woher die Teilnehmer kommen.** Erfassen Sie Standortattribute wie Land und Stadt, um ein Bild der Regionen zu erstellen, aus denen Ihre Teilnehmer stammen. Verwenden Sie die resultierenden Profilfelder für die Analyse im Lern-Manager.
* **Profildaten mit der Quellplattform abstimmen.** Die Plattform bleibt die Quelle der Wahrheit. Der Lern-Manager aktualisiert die Werte jedes Mal, wenn ein Teilnehmer gestartet wird.
* **Unterstützung mehrerer Plattformen in einem Konto.** Durch Namespacepräfixe werden Attribute von verschiedenen Plattformen getrennt gehalten, selbst wenn die Plattformen denselben Attributnamen verwenden.

Mit der benutzerdefinierten NRPS-Feldsynchronisation führt der Lern-Manager beim Start Folgendes durch:

1. Erkennt, dass die Plattform NRPS unterstützt.
2. Fordert das Starten des Teilnehmerdatensatzes von der Plattform aus an.
3. Extrahiert die benutzerdefinierten Attribute aus diesem Datensatz.
4. Schreibt die Attribute als aktive Felder in das Profil des Teilnehmers. Jeder Feldname hat ein Präfix `<namespace>`, sodass Attribute von verschiedenen Plattformen nicht kollidieren.
5. Learning Manager verwendet das OAuth 2.0-Clientanmeldeinformationen-Token, das bereits für Zuweisungs- und Bewertungsdienste (AGS) verwendet wird. Sie müssen keinen neuen Tokenendpunkt konfigurieren.

>[!NOTE]
>
>NRPS ist eine optionale Spezifikation in LTI Advantage. Die Unterstützung für NRPS und für benutzerdefinierte Attribute variiert je nach Plattform. Stellen Sie sicher, dass Ihre Plattform NRPS 2.0 legt, bevor Sie diese Funktion verwenden möchten.

## Wichtigste Funktionen

* **Support für NRPS-Ansprüche:** Learning Manager überprüft jeden LTI 1.3-Start auf den NRPS-Anspruch. Wenn kein Anspruch besteht, wird der Start normalerweise ohne Fehler und ohne Auswirkungen auf den Teilnehmer fortgesetzt.
  * Dieser Anspruch enthält die folgenden Informationen:
    * **Endpunkt der Mitgliedschaft:** `context_memberships_url ` identifiziert die Dienst-URL für den Kurs oder den Lernkontext, aus dem der Teilnehmer ALM gestartet hat.
    * **Unterstützte Versionen:** `service_versions` listet die an diesem Endpunkt verfügbaren NRPS-Versionen auf.
      Diese Funktion unterstützt NRPS 2.0.
  * **Infrastruktur für gemeinsam genutzte Token:** Learning Manager fügt der vorhandenen AGS-Tokenanforderung den NRPS-Bereich hinzu und verwendet den vorhandenen Cache für das Token pro Registrierung erneut.
* **Benutzerdefinierte Parameter mit Teilnehmerprofilen synchronisieren**
  * **Aktive Felder mit Namespacepräfix:** Jedes benutzerdefinierte Attribut ist einem aktiven Feld mit dem Namen `<namespace>_<field_name>` zugeordnet.
  * **Automatische Felderstellung:** Wenn kein entsprechendes aktives Feld vorhanden ist, erstellt der Lern-Manager ein Feld mit dem Typ **Text** und dem Status **Aktiv**.
  * **Plattform als Quelle der Wahrheit:** Der Learning Manager überschreibt vorhandene Profilwerte mit den neuesten Werten von der Plattform. Teilnehmer und Administratoren können diese Felder nicht bearbeiten.
  * **Nicht blockierendes Verhalten:** NRPS-Fehler hindern Teilnehmer nicht daran, Lerninhalte zu starten.
  * **Mehrere Quellen für benutzerdefinierte Attribute:** Learning Manager können benutzerdefinierte Attribute vom NRPS-Endpunkt und von benutzerdefinierten Parametern im LTI-Starttoken lesen. Erfahren Sie mehr über [benutzerdefinierte Attribute im Starttoken ](#custom-attributes-in-the-launch-token).

## Unterstützte Konfigurationen

| Element | Support |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| Lern-Manager-Rolle | LTI 1.3-Tool |
| LTI-Version | LTI 1,3 |
| NRPS-Dienstversion | 2.0 |
| Plattformen (spezifikationskonformes benutzerdefiniertes Feldformat) | Moodle, D2L Brightspace, Blackboard (Anthologie), Sakai |
| Benutzerdefinierter Feldtyp | Text |
| Auslöser | Jede LTI 1.3-Einführung |

Die Plattformunterstützung hängt vom benutzerdefinierten Feldserialisierungsmuster ab, das im NRPS-Mitgliederdatensatz verwendet wird. Es können mehrere Muster gleichzeitig vorhanden sein, aber Learning Manager verarbeitet nur die Muster, die in der aktiven Version unterstützt werden.

## Funktionsweise

### Launch Flow

1. Ein Teilnehmer startet den Learning Manager von der Plattform aus.
2. Der Learning Manager liest die NRPS-Angabe im LTI 1.3-Starttoken. Wenn der Anspruch NRPS-Dienstversion 2.0 auflistet, speichert der Learning Manager die `context_memberships_url` für die Sitzung und für den LTI-Kontext (Kurs).
3. Der Lern-Manager fordert ein Zugriffstoken an, das den NRPS-Bereich &quot;`https://purl.imsglobal.org/spec/lti-nrps/scope/contextmembership.readonly`&quot; enthält.
4. Der Lern-Manager ruft `context_memberships_url?rlid=<lti_user_id>` mit dem Bearer-Token auf, um den Startteilnehmerdatensatz abzurufen. Wenn die Plattform den `rlid`-Filter ignoriert und die vollständige Liste zurückgibt, findet Learning Manager den Teilnehmer bis `user_id`.
5. Learning Manager extrahiert die benutzerdefinierten Felder aus dem Datensatz.
6. Der Lern-Manager ordnet jedes benutzerdefinierte Feld einem aktiven Feld zu und schreibt die Werte in das Profil des Teilnehmers.
7. Alternativ unterstützt ALM auch das Extrahieren benutzerdefinierter Parameter, die während des Starts des Tools mit dem Teilnehmerprofil synchronisiert werden sollen, wenn die benutzerdefinierten Parameter mit dem ALM-identifizierbaren Feld &quot;`ALMfield`&quot; vorab festgelegt sind.

### Benutzerdefiniertes Feldformat

Die NRPS 2.0-Spezifikation definiert benutzerdefinierte Daten als `message`-Array im Memberdatensatz. Der Lern-Manager liest die benutzerdefinierten Daten aus dem benutzerdefinierten LTI-Anspruch innerhalb dieses Arrays. In dieser Version unterstützt der Lern-Manager die spezifikationskompatible Muster-S-Darstellung.

```json
{
  "user_id": "abc123",
  "message": [
    {
      "https://purl.imsglobal.org/spec/lti/claim/custom": {
        "department": "Engineering",
        "employee_id": "E4567"
      }
    }
  ]
}
```

### Benutzerdefinierte Attribute im Starttoken

Plattformen können auch benutzerdefinierte Attribute als benutzerdefinierte Parameter im LTI-Starttoken senden. Learning Manager sammelt Attribute sowohl vom Starttoken als auch vom NRPS-Endpunkt und speichert sie im Teilnehmerprofil.

Bei Attributen im Starttoken muss der Parametername mit dem Präfix `almfield-` beginnen, das Learning Manager benötigt. Ohne das Präfix kann der Lern-Manager diese Parameter nicht von anderen benutzerdefinierten Parametern unterscheiden und importiert sie nicht. Attribute, die vom NRPS-Endpunkt abgerufen werden, benötigen dieses Präfix nicht. Dieses Präfix ist nur erforderlich, wenn benutzerdefinierte Parameter in das Starttoken für ALM importiert werden, um das Feld zu identifizieren, das mit aktiven Feldern für Teilnehmer synchronisiert werden soll.

>[!NOTE]
>
>Bestätigen Sie das genau erforderliche Präfix mit Ihrem Learning Manager-Mitarbeiter, bevor Sie benutzerdefinierte Parameter auf der Plattform konfigurieren.

### Aktive Feldbenennung und -zuordnung

Der Lern-Manager erstellt den aktiven Feldnamen &quot;`<namespace>_<field_name>`&quot;. Das Feld `department` im Namespace `https://purl.imsglobal.org/spec/lti/claim/custom` wird beispielsweise zu `https://purl.imsglobal.org/spec/lti/claim/custom_department`.

Learning Manager wendet die folgenden Regeln an:

* **Namenslänge:** Wenn der Name die Zeichenbeschränkung des aktiven Feldnamens überschreitet, verkürzt der Lern-Manager zuerst den Namespaceteil und behält den Feldnamen bei.
* **Namenskonflikte:** Nach dem Kürzen sucht Learning Manager nach Konflikten mit vorhandenen aktiven Feldern aus einer anderen Quelle. Bei einem Konflikt wird die Kürzungslänge angepasst, bis ein eindeutiger Name gefunden wird. Wenn kein eindeutiger Name gefunden wird, wird das Feld übersprungen und ein Fehler wird protokolliert.
* **Zuordnung:** Bei der Zuordnung von Feldnamen wird die Groß-/Kleinschreibung nicht berücksichtigt.
* **Vorhandenes und aktiviertes Feld:** Learning Manager schreibt den Wert in das Profil des Teilnehmers.
* **Vorhandenes und deaktiviertes Feld:** Learning Manager überspringt das Feld, ohne einen Fehler zu protokollieren.
* **Kein vorhandenes Feld:** Der Lern-Manager erstellt ein **Text**-Feld mit dem Status **Aktiv**.

### Schreiben von Werten in das Profil

* Bei jedem Start, bei dem Learning Manager NRPS-Daten abruft, werden alle aufgelösten benutzerdefinierten Feldwerte in das Profil des startenden Teilnehmers geschrieben. Andere Teilnehmerprofile werden nicht geändert.
* Wenn ein Feld bereits einen Wert aufweist, wird dieser vom Learning Manager mit dem neuesten Wert aus der Plattform überschrieben.
* Wenn der Plattformwert leer oder null ist, behält Learning Manager den vorhandenen Profilwert bei.
* Wenn ein Feld nicht geschrieben wird, wird weder der Start noch der Schreibvorgang für andere Felder blockiert.
* Learning Manager wendet die Feldaktualisierungen nach Möglichkeit in derselben Starttransaktion an.
* Teilnehmer können Felder, die auf NRPS basieren, auf ihrer Profilseite nicht bearbeiten, und Administratoren können diese Werte nicht im Namen eines Teilnehmers bearbeiten.

## Einrichten der benutzerdefinierten NRPS-Feldsynchronisation

### Voraussetzungen

* Ihre Plattform ist beim Learning Manager als LTI 1.3-Tool registriert. Diese Funktion unterstützt LTI 1.1 oder LTI 1.2 nicht.
* Ihre Plattform unterstützt die NRPS-Dienstversion 2.0 und legt benutzerdefinierte Attribute im spezifikationskompatiblen `message`-Format.
* Das LTI-Starttoken enthält den `namesroleservice`-Anspruch.
* Der Anspruch stellt `context_memberships_url` bereit, das den kursspezifischen NRPS-Endpunkt identifiziert.
* Der `service_versions`-Wert im Anspruch enthält `2.0`.
* Sie haben Administratorzugriff auf die Toolregistrierung der Plattform.

### Gewähren des NRPS-Geltungsbereichs für Learning Manager

Für neue Registrierungen, die den NRPS-Bereich enthalten, ist keine zusätzliche Konfiguration im Learning Manager erforderlich.

Neue Registrierungen, die den NRPS-Umfang enthalten, funktionieren ohne weitere Änderungen im Learning Manager. Bei einer bestehenden Registrierung muss der Plattformadministrator die Toolregistrierung auf der Plattformseite aktualisieren.

>[!NOTE]
>
>Sie müssen den Tokenendpunkt, die Client-ID oder den privaten Schlüssel im Lern-Manager nicht ändern. Die vorhandene AGS-Konfiguration wird wiederverwendet. Wenn die Plattform den NRPS-Geltungsbereich nicht gewährt, überspringt der Learning Manager NRPS, ohne den AGS oder den Start zu beeinträchtigen.

### Leg der Teilnehmerattribute auf der Plattform

Die Plattform steuert, welche Teilnehmerattribute sie freigibt. Die genauen Schritte hängen von der Plattform ab. Beispiel: In Moodle:

1. Fügen Sie Learning Manager als externes Tool mit LTI 1.3 hinzu.
2. Aktivieren Sie die Datenschutzeinstellungen, die es der Plattform ermöglichen, Teilnehmerinformationen mit dem Tool zu teilen.
3. Definieren Sie die benutzerdefinierten Attribute, die gesendet werden sollen. Sie können Plattformvariablen oder vordefinierte Werte verwenden.
4. Wenn Sie Attribute auch als benutzerdefinierte Parameter im Starttoken senden, fügen Sie jedem Parameternamen das Präfix hinzu, das Learning Manager benötigt.

>[!NOTE]
>
>Es werden nur die Attribute gelegt, die für den Nutzungsfall des Lernprogramms erforderlich sind. Learning Manager behandelt die Plattform als Quelle der Wahrheit und bietet in dieser Version keine separaten Einwilligungs- oder Datenschutzkontrollen an.

### Synchronisation überprüfen

1. Starten Sie den Lern-Manager von der Plattform aus als Testteilnehmer.
2. Vergewissern Sie sich, dass der Start normal abgeschlossen wird.
3. Öffnen Sie in der Learning Manager-Admin-App die Seite Aktive Felder.
4. Vergewissern Sie sich, dass die Felder mit dem Namespacepräfix mit dem Typ **Text** und dem Status **Aktiv** angezeigt werden.
5. Öffnen Sie das Profil des Testteilnehmers und bestätigen Sie, dass die Werte mit der Plattform übereinstimmen.
6. Vergewissern Sie sich, dass Felder, die auf NRPS basieren, schreibgeschützt sind. Weder der Teilnehmer noch ein Administrator können die synchronisierten Werte manuell bearbeiten.
7. Starten Sie den Kurs erneut, nachdem Sie einen nicht leeren Quellwert geändert haben, und überprüfen Sie, ob Learning Manager den vorhandenen Profilwert mit dem neuesten NRPS-Wert überschreibt.

>[!TIP]
>
>Wenn ein Feld vorhanden, aber deaktiviert ist, schreibt der Lern-Manager nicht darauf. Aktivieren Sie das Feld, wenn es ausgefüllt werden soll.

## Fehlerbehandlung und -protokollierung

Der Learning Manager blockiert einen Teilnehmer nie aufgrund eines NRPS-Problems. Es versucht es nicht noch einmal. Der Fehler wird protokolliert und die NRPS-Synchronisierung für diesen Start wird übersprungen. Der nächste Start versucht es erneut.

| Bedingung | Ergebnis |
|------------------------------------------------------------------|-------------------------------------------------------|
| NRPS-Anspruch fehlt im Starttoken. | NRPS wird übersprungen. Der Launch wird fortgesetzt. |
| Es ist nur NRPS-Dienstversion 1.0 vorhanden. | NRPS wird übersprungen. Der Launch wird fortgesetzt. |
| Die Tokenanforderung schlägt fehl oder die Plattform gewährt den NRPS-Bereich nicht. | NRPS wird übersprungen. AGS und der Start sind davon nicht betroffen. |
| NRPS-Aufruf schlägt fehl (Timeout, 4xx oder 5xx) | Der Fehler wird protokolliert. Der Launch wird fortgesetzt. |
| Teilnehmer wird in der NRPS-Antwort nicht gefunden | Die Feldsynchronisation wird übersprungen. Der Launch wird fortgesetzt. |
| Keine benutzerdefinierten Felder in der NRPS-Antwort | Die Feldsynchronisierung wird ohne Fehler übersprungen. |
| Ein Feldnamenkonflikt kann nicht gelöst werden | Das Feld wird übersprungen und ein Fehler wird protokolliert. |
| Fehler beim Schreiben eines einzelnen Felds. | Andere Felder sind noch geschrieben. Der Launch wird fortgesetzt. |

Jeder Protokolleintrag enthält den Zeitstempel, die ID der Plattformregistrierung, die Teilnehmer-ID und den Fehlergrund. Systemadministratoren von Learning Manager können auf die Protokolle zugreifen.

## Hinweise

* Nur der Datensatz des startenden Teilnehmers wird synchronisiert. Learning Manager synchronisiert nicht die vollständige Kursliste.
* Es wird nur NRPS-Dienstversion 2.0 unterstützt.
* Alle synchronisierten Felder haben den Typ **Text**. Learning Manager schließt keine Typen aus Werten ab. Die Feldtypen &quot;Anzahl&quot;, &quot;Datum&quot; und &quot;Boolesche Wert&quot; werden nicht unterstützt.
* Learning Manager fungiert als LTI-Tool. Es fungiert nicht als NRPS-Plattform und stellt anderen Tools keinen Endpunkt für die Liste zur Verfügung.
* Die Synchronisierung benutzerdefinierter Felder erfolgt während des LTI-Starts.
