---
description: Erfahren Sie, wie Sie aktive Felder in Adobe Learning Manager verwenden, um benutzerdefinierte Benutzerinformationen zu erfassen, zu organisieren und zu verwalten. Verbessern Sie Reporting, Filterung und Benutzersegmentierung mit flexiblen Feldkonfigurationen.
jcr-language: en_us
title: Aktive Felder in Adobe Learning Manager konfigurieren
exl-id: e68300d6-9f19-4e42-b485-c4bbbbcf5518
source-git-commit: 0dade561e53e46f879e22b53835b42d20b089b31
workflow-type: tm+mt
source-wordcount: '1012'
ht-degree: 0%

---

# Aktive Felder

Aktive Felder in Adobe Learning Manager sind benutzerdefinierte Benutzerattribute, mit deren Hilfe Administratoren Benutzer effizient organisieren und verwalten können. Sie ermöglichen es Ihnen, zusätzliche Informationen über Benutzer zu erfassen, z. B. Abteilung, Standort oder Stellenbezeichnung. Administratoren können diese Daten verwenden, um Benutzergruppen zu erstellen, Lernergebnisse zu personalisieren und Berichte effektiver zu filtern.

Benutzerattribute sind Informationselemente wie der Vorname, der Nachname und die E-Mail-Adresse eines Benutzers. Mithilfe dieser Attribute können Administratoren:

* Identifizieren von Benutzern
* Benutzer gruppieren
* Verwalten von Benutzerberechtigungen und Zugriffsbeschränkungen

Durch das Hinzufügen benutzerdefinierter Attribute zu Benutzerprofilen erfassen aktive Felder zusätzliche Informationen, die für Ihre Organisation relevant sind.

>[!INFO]
>
>Sehen Sie sich diese Schulung der ALM Academy an, um zu erfahren, wie Sie aktive Felder hinzufügen, anpassen und konfigurieren können.<br>[![Schaltfläche](assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/7555741)</br>

## Aktive Felder hinzufügen

Aktive Felder gelten sowohl für interne als auch für externe Teilnehmer, sodass Organisationen benutzerdefinierte Benutzerattribute für alle Benutzer definieren und verwalten können.

So fügen Sie aktive Felder für interne Benutzer hinzu oder verwalten sie:

1. Wählen Sie auf der Administrator-Homepage **Benutzer** aus.

2. Wählen Sie **Aktive Felder** aus.

3. Geben Sie den Namen des aktiven Felds ein, und wählen Sie dann **Hinzufügen** aus. Der Vorgang zum Hinzufügen aktiver Felder für externe Teilnehmer ist derselbe wie für interne Teilnehmer.

   ![](assets/add-active-field-alm.png)
   _Feld zur Eingabe des Namens eines neuen benutzerdefinierten Attributs für Benutzer_

4. Wählen Sie **Speichern**.

## Benutzerdefinierte Werte zu aktiven Feldern hinzufügen

Aktive Felder können vordefinierte oder benutzerdefinierte Werte enthalten, die der Struktur Ihrer Organisation entsprechen. Durch das Hinzufügen benutzerdefinierter Werte können Sie Details erfassen, die für Ihre internen Benutzer spezifisch sind, z. B. Abteilungsnamen, Job-Stufen oder regionale Büros.

Hinzufügen benutzerdefinierter Werte für interne Benutzer:

1. Wählen Sie im Abschnitt **Aktives Feld** die Option **Werte anzeigen** aus.
2. Im Dialogfeld &quot;**Werte in benutzerdefinierten Feldern**&quot;:

   * Wählen Sie ein aktives Feld aus der Dropdown-Liste **Feld auswählen** aus.
   * Geben Sie die Werte des aktiven Felds in das Feld **Neuer Wert** ein.

   ![](assets/add-value-active-fields.png)
   _Dialogfeld zur Eingabe benutzerdefinierter Werte für ein bestimmtes aktives Feld_

3. Wählen Sie **Fertig** und anschließend **Speichern**, um die Änderungen zu übernehmen.

## Aktive Feldeinstellungen konfigurieren

Passen Sie aktive Felder an, um die Benutzerverwaltung und Berichterstellungsaufgaben zu unterstützen, und konfigurieren Sie die Eigenschaften aktiver Felder:

* **Gruppierbar**: Mit dieser Option können Sie Teilnehmer basierend auf den Werten aktiver Felder gruppieren.
* **Bericht**: Mit dieser Option können Sie eine Berichtsbenutzergruppe auf der Grundlage des aktiven Feldwerts erstellen und den Berichtsfilter für das Feld in Dashboard-Berichten aktivieren.
* **Für Teilnehmer konfigurierbar**: Mit dieser Option können Teilnehmer das Feld selbst konfigurieren.
* **Exportfähig**: Diese Option enthält das aktive Feld in exportierten Benutzergruppenberichten.
* **Mehrwertig**: Diese Option unterstützt mehrere Werte für das aktive Feld.

So konfigurieren Sie die Einstellungen für aktive Felder:

1. Wählen Sie die Registerkarte **Einstellungen** aus, und navigieren Sie dann zum Abschnitt **Benutzeranzeige**.

   ![](assets/settings-active-field.png)
   _Wählen Sie die Registerkarte &quot;Einstellungen&quot; aus, um die aktiven Felder anzupassen_

2. Wählen Sie je nach Bedarf eine oder beide Optionen.:

   * **Nur nicht ausgefüllte Felder bei der Teilnehmeranmeldung anzeigen:** Wenn diese Option ausgewählt ist, sehen die Teilnehmer nur die aktiven Felder, die sie noch nicht ausgefüllt haben. Dadurch werden sie aufgefordert, ihr Profil abzuschließen, um sicherzustellen, dass die Benutzerdaten korrekt und aktuell sind. Die Anzeige dieser Felder unterstützt vollständige Teilnehmerprofile und ermöglicht personalisierte Lernerlebnisse.
   * **Wenn diese Option deaktiviert ist, wird die Seite &quot;Profil abschließen&quot; den Benutzern nicht angezeigt:** Wenn diese Option deaktiviert ist, sehen die Teilnehmer die Seite **Profil abschließen** bei der Anmeldung nicht. Sie werden nicht aufgefordert, Profilinformationen zu aktualisieren oder auszufüllen und können direkt auf die Plattform zugreifen.

   ![](assets/user-display-alm.png)
   _Einstellungsschnittstelle, um zu steuern, wie und wann aktive Felder angezeigt werden_

3. Wählen Sie **Speichern**, um Ihre Änderungen zu übernehmen.

## Aktive Felder mit mehreren Werten

Mit aktiven Feldern mit mehreren Werten können Sie einem einzelnen Benutzerattribut mehrere Werte zuweisen, z. B. Standorte, Tätigkeitsbezeichnungen oder Projektteams. Auf diese Weise können detailliertere und flexiblere Benutzerinformationen erfasst werden.

Sie können bis zu drei mehrwertige aktive Felder pro Konto konfigurieren. Diese stehen sowohl internen als auch externen Benutzern zur Verfügung. Nachdem ein Feld als mehrwertig festgelegt wurde, kann diese Einstellung nicht mehr geändert werden.

So weisen Sie einem aktiven Feld mehrere Werte zu:

1. Wählen Sie **Benutzer** und anschließend **Aktive Felder** aus.
2. Wählen Sie auf der Registerkarte **Einstellungen** die Option **Mehrwertig** aus.

![](assets/multi-values.png)
_Einstellungsschnittstelle, um zu steuern, wie und wann aktive Felder angezeigt werden_

Sie können mehrere Werte über die CSV-Datei oder über die Benutzeroberfläche hinzufügen. Sobald das Feld mit mehreren Werten in einer Benutzergruppe verwendet wurde, kann es nicht mehr in ein Feld mit einem einzelnen Wert geändert werden.

## Aktive Felder durch Hochladen einer CSV-Datei hinzufügen

Fügen Sie beim Hochladen von Benutzern über CSV aktive Felder hinzu, indem Sie entsprechende Kopfzeilen für jedes definierte Feld hinzufügen. Administratoren können mithilfe einer CSV-Datei mehrere Benutzer gleichzeitig hochladen. Die CSV-Datei sollte die neuen aktiven Felder enthalten, die die zu importierenden Benutzer definieren. Stellen Sie sicher, dass die Header-Namen in der Datei genau mit den im System eingerichteten aktiven Feldern übereinstimmen, damit die Daten korrekt zugeordnet werden. Laden Sie die CSV-Datei aus dem Abschnitt **Benutzer** hoch.

In diesem [Artikel](/help/migrated/administrators/feature-summary/add-users-user-groups.md) finden Sie weitere Informationen zum Massenhinzufügen von Benutzern.

## Beschränken von Werten für CSV-Felder

Mit der Option **Auswahl** einschränken in **Werte in benutzerdefinierten Feldern** wird gesteuert, ob Benutzer, die Daten über CSV-Dateien importieren, nur aus vordefinierten Werten für benutzerdefinierte Felder auswählen können. Wenn diese Option aktiviert ist, müssen Benutzer aus der festgelegten Werteliste auswählen, um Datenkonsistenz zu gewährleisten und neue oder unerwartete Einträge zu verhindern. Wenn diese Option deaktiviert ist, können Benutzer jeden Wert eingeben, was mehr Flexibilität, aber weniger Kontrolle über die Datengenauigkeit bietet.

![](assets/restrict-active.png)
_Kontrollkästchen zum Aktivieren der Werteinschränkung während des CSV-Uploads_

## Verwalten fehlender aktiver Felder beim CSV-Benutzerimport

In einigen Fällen ziehen Administratoren es den Teilnehmern vor, bestimmte aktive Felder manuell auszufüllen, wenn sie sich bei Adobe Learning Manager anmelden. Dies wird für Benutzer unterstützt, die über eine CSV-Datei importiert wurden. Im [Artikel](/help/migrated/administrators/feature-summary/add-users-user-groups.md) erfahren Sie, wie Sie mehrere Benutzer gleichzeitig hinzufügen.

Wenn eine CSV-Datei nicht alle aktiven Felder enthält, muss der Administrator die fehlenden Werte nach dem Import manuell eingeben.

Standardmäßig muss jedes aktive Feld einem entsprechenden Feld in der Quell-CSV zugeordnet werden. Wenn Sie jedoch keiner Spalte in der CSV-Datei ein bestimmtes aktives Feld zuordnen möchten, können Sie den Wert **DontImportFromSource** sowohl während des Box- als auch des FTP-Importvorgangs aus der Dropdownliste auswählen. Diese Option ist beim Importieren von Benutzern über FTP- oder Box-Connectors verfügbar. Weitere Informationen zu den Konnektoren finden Sie in diesem [Artikel](https://experienceleague.adobe.com/de/docs/learning-manager/using/integration/connectors).
