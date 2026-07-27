---
description: Stellen Sie einen Kurs für mehrere Zielgruppen bereit, indem Sie basierend auf den Benutzergruppen, zu denen sie gehören, steuern, welche Module die einzelnen Teilnehmer sehen und welche erforderlich sind.
jcr-language: en_us
title: Adaptive Kurse in Adobe Learning Manager
contentowner: mmanuel
source-git-commit: 5d4ba4ccd3b32a6108b5c8101f48f12f27775e00
workflow-type: tm+mt
source-wordcount: '1964'
ht-degree: 0%

---


# Adaptive Kurse in Adobe Learning Manager

Mit adaptiven Kursen in Adobe Learning Manager können Sie einen Kurs für mehrere Zielgruppen bereitstellen, indem Sie steuern, welche Module die einzelnen Teilnehmer sehen und welche erforderlich sind, basierend auf den Benutzergruppen, denen sie angehören.

Anstatt separate Kurse für jede Rolle, Region oder jedes Compliance-Profil zu erstellen, stellt ein einzelner adaptiver Kurs dem richtigen Teilnehmer dynamisch die richtigen Inhalte zur Verfügung.

## Welche Probleme adaptive Kurse lösen

Unternehmen, die große, vielfältige Arbeitskräfte ausbilden, stehen vor einer gemeinsamen Herausforderung: Datenschutz, Berufsethik und Sicherheit am Arbeitsplatz müssen die Teilnehmer mit unterschiedlichen Rollen, Standorten oder Compliance-Verpflichtungen erreichen.

Dies führt zu Doppelarbeit: Autoren unterhalten mehrere, nahezu identische Kurse, Berichte sind fragmentiert, und wenn sich der Kerninhalt ändert, muss jede Kopie aktualisiert werden.

Ein adaptiver Kurs löst dies, indem er Autoren die Möglichkeit bietet, Sichtbarkeits- und Abschlussregeln auf Modulebene zu konfigurieren, die mit Benutzergruppen verknüpft sind. Ein Kurs erfüllt alle Zielgruppen gleichzeitig.

### Häufige Szenarien

- Ein Compliance-Kurs umfasst ein Kernmodul für alle Mitarbeiter sowie Addendum-Module, die speziell auf die Anforderungen der Rechtszuständigkeit zugeschnitten sind. Jeder Teilnehmer sieht nur die Addendums, die für seinen Standort gelten.
- Ein Kurs für Neueinstellungen zeigt verschiedene Module für Mitarbeiter, Manager und Auftragnehmer an. Jede Rolle sieht nur, was für sie relevant ist.
- Ein Sicherheitskurs fügt ein neues obligatorisches Modul Mitte des Jahres hinzu. Administratoren lösen einen Aktualisierungsabschluss aus, sodass alle zuvor abgeschlossenen Teilnehmer das neue Modul absolvieren müssen, um die Konformität zu wahren.

### Praxisbeispiel

Ein Unternehmen führt einen obligatorischen Compliance-Kurs für seine gesamte Belegschaft durch. Der Kurs umfasst sieben Module:

- Zwei Module gelten für alle Mitarbeiter.
- Zwei Module gelten nur für Personalleiter.
- Zwei Module gelten nur für einzelne Anbieter in technischen Rollen.
- Ein Modul gilt nur für leitende Direktoren und höher.

## Funktionsweise der Modulsichtbarkeit und des Abschlusses

Jedes Inhaltsmodul in einem adaptiven Kurs hat zwei Einstellungen:

**Sichtbar für:** Benutzergruppen, die das Modul sehen können. Teilnehmer in diesen Gruppen sehen das Modul im Kurs und können darauf zugreifen, aber es wird nicht auf den Abschluss angerechnet, es sei denn, sie sind auch in **Obligatorisch für**.

**Erforderlich für:** Benutzergruppen, für die das Modul erforderlich ist, um den Kurs abzuschließen. Ein Modul, das unter **Obligatorisch für** aufgeführt ist, ist für diese Gruppen automatisch sichtbar. Sie müssen nicht dieselben Gruppen zu beiden Einstellungen hinzufügen.

Ein Modul befindet sich zu einem beliebigen Zeitpunkt in einem von drei Status für einen bestimmten Teilnehmer:

| Status | Wie es bestimmt wird | Zählt bis zum Abschluss? |
|---|---|---|
| Obligatorisch | Der Teilnehmer befindet sich in einer Benutzergruppe, die unter **Obligatorisch für** aufgeführt ist. | Ja - muss ausgefüllt werden |
| Optional | Teilnehmer befindet sich in einer Gruppe unter **Sichtbar für**, aber nicht **Erforderlich für** | Nein - sichtbar und zugänglich, aber nicht erforderlich |
| Ausgeblendet | Der Teilnehmer befindet sich unter keiner der Einstellungen in einer Gruppe. | Überhaupt nicht für den Teilnehmer sichtbar |

## Merkmale eines adaptiven Kurses

Das entscheidende Merkmal von adaptiven Kursen ist, dass der Kurs das Profil des Teilnehmers kontinuierlich auswertet, nicht nur bei der Registrierung.

Wenn sich die Benutzergruppe eines Teilnehmers ändert, während er registriert ist:

- Module, die nicht mehr unter ihrer neuen Benutzergruppe angezeigt werden, verschwinden sofort.
- Wenn ein neu sichtbares Modul für seine neue Benutzergruppe obligatorisch ist, wird es zu den Abschlussanforderungen hinzugefügt.
- Wenn ein zuvor obligatorisches Modul nicht mehr obligatorisch ist, wird es von seiner Abschlussanforderung entfernt.
- Zuvor abgeschlossene Module bleiben abgeschlossen. Eine Profiländerung setzt die bereits ausgeführte Arbeit nicht zurück.

### Automatische Aufhebung der Registrierung

Wenn bei einer Änderung der Benutzergruppe alle obligatorischen Module eines Teilnehmers entfernt werden, wird die Registrierung des Teilnehmers für den Kurs automatisch aufgehoben.

### Automatische Vervollständigung

Wenn bei einer Änderung der Benutzergruppe alle verbleibenden unvollständigen obligatorischen Module von einem Teilnehmer in Bearbeitung entfernt werden, wird der Kurs für diesen Teilnehmer automatisch abgeschlossen.

Wenn eine Profiländerung zu neuen obligatorischen Modulen führt, die der Teilnehmer nicht abgeschlossen hat, kann ein Administrator einen Aktualisierungsabschluss auslösen, um den vorhandenen Abschluss rückgängig zu machen und den Teilnehmer aufzufordern, die neuen Module abzuschließen.

## Was passt sich an und was bleibt gleich?

Adaptive Regeln gelten nur für **Inhaltsmodule**. Folgendes gilt für alle registrierten Teilnehmer unabhängig von der Benutzergruppe:

- **Vorbereitungsmodule:** Wird allen Teilnehmern angezeigt, bevor der Kerninhalt beginnt.
- **Testmodule:** Für alle Teilnehmer verfügbar; Wenn Sie einen Test abschließen, wird der Kurs unabhängig vom Status des Inhaltsmoduls abgeschlossen.
- **Voraussetzungen:** Wenn für einen Kurs Voraussetzungen konfiguriert sind, müssen alle Teilnehmer diese Voraussetzungen erfüllen, bevor sie sich registrieren können, unabhängig von ihrer Benutzergruppe. Voraussetzungen sind nicht adaptiv und können nicht auf bestimmte Benutzergruppen beschränkt werden.

Arbeitshilfen und Ressourcen, die mit dem Kurs verknüpft sind, sind ebenfalls nicht adaptiv. Sie sind für alle registrierten Teilnehmer sichtbar.

Kenntnisse, Gamification-Punkte und Abzeichen werden basierend auf dem ersten Kursabschluss des Teilnehmers vergeben und sind nicht von Neuabschlüssen aufgrund von Profiländerungen betroffen.

>[!NOTE]
>
>Wenn ein adaptiver Kurs Teil eines extern freigegebenen LO höherer Ordnung ist, wird der adaptive Kurs als regulärer Kurs in das untergeordnete Konto kopiert.


## Verfügbarkeit der Funktionen

Die Funktion für adaptive Kurse wird durch ein zweistufiges Flag auf Kontoebene gesteuert. Wenden Sie sich an Ihr Adobe-Kontoteam, um diese Funktion für Ihr Konto zu aktivieren.

Sobald das Konto-Flag aktiviert ist:

- Ein Schalter **Fertigstellungs- und Sichtbarkeitsregeln** ist beim Erstellen oder Bearbeiten eines Kurses verfügbar.
- Durch Aktivieren des Umschalters wird das Bedienfeld für die adaptive Konfiguration aktiviert.

**Vorsicht:** Das Aktivieren des Flags für adaptive Funktionen ist **unumkehrbar**. Nachdem sie auf Kontoebene aktiviert wurde, kann sie nicht mehr deaktiviert werden.

## Katalogfreigabe

Adaptive Kurse können zu Katalogen innerhalb Ihres Kontos hinzugefügt werden. Wenn ein Katalog extern für ein Peer-Konto freigegeben wird, werden adaptive Kurse automatisch vom freigegebenen Inhalt ausgeschlossen.

>[!NOTE]
>
>Wenn ein Lernpfad oder eine Zertifizierung, die einen adaptiven Kurs enthält, extern freigegeben wird, sieht das empfangende Konto den Lernpfad oder die Zertifizierung in seinem Katalog, der darin enthaltene adaptive Kurs wird jedoch nicht angezeigt. Das Lernobjekt ist nicht vollständig ausgeschlossen. Nur die adaptive Kurskomponente wird aus der freigegebenen Version entfernt. Autoren im empfangenden Konto sollten sich bewusst sein, dass das freigegebene Lernobjekt möglicherweise weniger Module als die Quellversion hat.

>[!NOTE]
>
>Wenn ein adaptiver Kurs als Voraussetzung eines anderen Kurses konfiguriert ist und dieser übergeordnete Kurs über die Katalogfreigabe für ein empfangendes Konto freigegeben wird, wird der adaptive erforderliche Kurs nicht für das empfangende Konto freigegeben. Dies gilt unabhängig davon, ob die Voraussetzung direkt auf dem Kurs festgelegt wird oder über ein Lernobjekt höherer Ordnung, z. B. einen Lernpfad oder eine Zertifizierung.
>
>Im empfangenden Konto ist der übergeordnete Kurs verfügbar, aber die adaptive Voraussetzung fehlt. Teilnehmer im empfangenden Konto sind nicht von der fehlenden Voraussetzung betroffen, da die Abhängigkeit von der Voraussetzung für Inhalte, die über die Katalogfreigabe ohne die erforderlichen Voraussetzungen eingehen, nicht erzwungen wird.
>
>Konfigurieren Sie keine adaptiven Kurse als Voraussetzungen für Inhalte, die Sie extern freigeben möchten.

## Unterstützte Konfigurationen

| Konfiguration | Unterstützt? |
| --- | --- |
| Adaptiver Kurs in einem regulären Lernpfad | Ja (siehe Hinweis unten) |
| Adaptiver Kurs in einem flexiblen Lernpfad | Ja |
| Adaptiver Kurs in einem adaptiven Lernpfad | Nein |
| Adaptiver Kurs in einer Zertifizierung | Ja (nicht empfohlen für wiederkehrende Zertifizierungen) |
| Mehrfachregistrierung | Nein |
| Instanz-Switching | Ja |
| Katalogfreigabe (kontoübergreifend) | Nein |
| Sichtbarkeitsregeln für Vorbereitungs- oder Testmodule | Nein |
| Sichtbarkeitsregeln für Kerninhaltsmodule | Ja |
| Adaptiver Kurs in einem flexiblen Lernpfad | Ja |

>[!NOTE]
>
>Beim Herunterladen des **Anwesenheitsberichts für eine PDF**-Sitzung in einem adaptiven Kurs, der Teil eines Flex-Lernpfads ist, werden Teilnehmer auf Warteliste im Abschnitt &quot;Aktiv&quot; der PDF angezeigt. Die Benutzeroberfläche des Lernpfads verfügt nicht über einen dedizierten Wartelistenabschnitt, sodass im PDF-Export kein separates Wartelistenbucket vorhanden ist. Um Teilnehmer auf der Warteliste genau zu identifizieren, überprüfen Sie **Administrator > [Adaptiver Kurs] > Warteliste**, bevor Sie die Anwesenheit markieren.

Die Spalte &quot;**Eingebettet in**&quot; im Wartelistenbericht identifiziert die Instanzen des Flex-Lernpfads, die diesen adaptiven Kurs als Komponente enthalten. Es werden der Name des Lernpfads und die Lernobjekt-ID angezeigt. Es ist nicht dazu gedacht, einzelne Registrierungspfade für Teilnehmer anzuzeigen. Bei adaptiven Kursen, die in einem untergeordneten Lernpfad verschachtelt sind, der sich selbst in einem übergeordneten Lernpfad befindet, wird in dieser Spalte nur der direkte übergeordnete Lernpfad angezeigt.

Wenn der adaptive Kurs Teil einer **wiederkehrenden Zertifizierung** ist, gilt der Abschluss der Aktualisierung nur für die Registrierung des Teilnehmers im Stammzertifizierungszyklus. Nachfolgende wiederkehrende Zyklen enthalten eine separate Instanz des adaptiven Kurses, die nicht von der Aktualisierung betroffen ist. Teilnehmer, die in einem wiederkehrenden Zyklus registriert sind, sehen keine Modulaktualisierungen oder lassen ihre Abschlüsse rückgängig machen. Wenn Ihr Unternehmen adaptive Kurse in wiederkehrenden Zertifizierungen verwendet, teilen Sie dem Administrator diese Einschränkung mit, bevor Sie den Abschluss der Aktualisierung auslösen.

>[!NOTE]
>
>Wenn ein adaptiver Kurs in einen **geordneten** Lernpfad aufgenommen wird, können Teilnehmer, die keine sichtbaren Module im adaptiven Kurs haben, diesen Kurs nicht abschließen, da ihre Benutzergruppe nicht mit den Sichtbarkeitsregeln eines Moduls übereinstimmt. In einem geordneten Lernpfad wird dadurch verhindert, dass auf alle nachfolgenden Elemente zugegriffen werden kann. Um dies zu vermeiden, stellen Sie sicher, dass jeder Teilnehmer, der sich für den Lernpfad registriert, zu mindestens einer Benutzergruppe gehört, die für mindestens ein Modul in einem adaptiven Kurs im Pfad sichtbar ist.

Betten Sie außerdem keinen Lernpfad ein, der einen adaptiven Kurs enthält, in einen (verschachtelten) Lernpfad höherer Ordnung ein. Wenn in dieser Konfiguration ein Teilnehmer keine sichtbaren oder obligatorischen Module im adaptiven Kurs hat, reagiert der eingebettete Player möglicherweise nicht mehr und verhindert die Navigation durch den verbleibenden Inhalt. Dieses Verhalten wird in einer zukünftigen Version behoben.

>[!NOTE]
>
>Wenn ein Teilnehmer automatisch die Registrierung für einen adaptiven Kurs in einem **regulären** Lernpfad aufhebt, bleibt der übergeordnete Lernpfad in einem registrierten Status, da durch eine Änderung der Benutzergruppe alle sichtbaren Module entfernt wurden. Die Registrierung für den Lernpfad wird nicht automatisch aufgehoben. Der Teilnehmer sieht den Lernpfad als in seinem Transkript registriert an, obwohl der darin enthaltene adaptive Kurs nicht mehr zugänglich ist. Wenn Ihr Anwendungsfall erfordert, dass der übergeordnete Lernpfad auch die Registrierung aufhebt, wenn der adaptive Kurs dies tut, sollten Sie einen **adaptiven Lernpfad** anstelle eines regulären Lernpfads verwenden, um den adaptiven Kurs zu enthalten.

## Adaptive Kurse für Ihr Konto aktivieren

Aktivieren Sie adaptives Lernen, damit Autoren Kurse erstellen können, die verschiedenen Teilnehmern je nach Benutzergruppenmitgliedschaft verschiedene Module anzeigen.

## Bevor Sie

- **Permanent:** Nach der Aktivierung kann Adaptive Learning für das Konto nicht mehr deaktiviert werden.
- **Betrifft sowohl Kurse als auch Lernpfade gleichzeitig:** Das gleiche Flag, das adaptive Kurse aktiviert, aktiviert auch adaptive Lernpfade.
- **Vorhandene Kurse bleiben unverändert:** Nur neu erstellte Kurse können adaptiv gestaltet werden. Kein vorhandener regulärer Kurs wird automatisch konvertiert.
- **Autoren sehen die Option sofort:** Sobald Sie speichern, wird der adaptive Kurstyp im Authoring-Workflow angezeigt.
- **Zwei-Ebenen-Bereitstellung:** Wenn Ihr Konto für adaptives Lernen bereitgestellt wurde, wird die Option aktiviert und gesperrt. Sie kann nicht über die Benutzeroberfläche geändert werden. Wenn das Konto nicht bereitgestellt wurde, ist die Einstellung überhaupt nicht sichtbar. Wenden Sie sich an Adobe, um die Bereitstellung anzufordern.

## Adaptive Kurse aktivieren

1. Melden Sie sich bei Adobe Learning Manager als Administrator an.
2. Wählen Sie im linken Navigationsbereich **Einstellungen** aus.
3. Wählen Sie **Allgemein** aus.
4. Navigieren Sie zum Abschnitt **Sichtbarkeit und Abschlussregeln**. Wenn das adaptive Lernen für Ihre Organisation aktiviert wurde, wird die Option wie folgt als gesperrt angezeigt:

![](assets/image_0001.png)

Adaptives Lernen ist jetzt für Ihr Konto aktiv. Autoren können adaptive Kurse und adaptive Lernpfade sofort erstellen.

## Was ändert sich nach der Aktivierung?

Nach der Aktivierung des adaptiven Lernens:

- Autoren sehen beim Erstellen eines Kurses zusätzlich zum vorhandenen regulären Kurstyp eine **Option zur Inhaltssichtbarkeit und zu den Abschlussregeln**.
- Jedes Inhaltsmodul in einem adaptiven Kurs kann mit **Optional** und **Obligatorisch** Regeln für Benutzergruppen konfiguriert werden.
- Teilnehmer, die für einen adaptiven Kurs registriert sind, sehen nur die Module, die ihre Benutzergruppen sichtbar machen.
- Alle bestehenden regulären Kurse bleiben unverändert.

## Fehlerbehebung

- **Der Abschnitt Sichtbarkeit und Abschlussregeln ist in Einstellungen nicht sichtbar:** Das Feature muss am Backend bereitgestellt werden, bevor der Schalter angezeigt wird. Wenden Sie sich an Ihren Adobe-Kundenbetreuer oder den Adobe-Support, um Zugriff anzufordern.
- **Der Umschalter ist bereits aktiviert und wird gesperrt angezeigt:** Adaptives Lernen wurde aktiviert, als Ihr Konto bereitgestellt wurde. Es sind keine Maßnahmen erforderlich. Autoren können bereits adaptive Kurse erstellen.
