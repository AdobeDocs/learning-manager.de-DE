---
description: Erfahren Sie, wie Sie den Marketo Engage-Connector mit Adobe Learning Manager integrieren
jcr-language: en_us
title: Marketo Engage-Connector
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 3%

---


# Marketo Engage-Connector in Adobe Learning Manager

## Einführung

Mit dem Marketo Engage-Connector kann Adobe Learning Manager nahtlos in Marketo Engage, eine Marketing-Automatisierungsplattform, integriert werden. Diese Integration hilft Marketing-Experten dabei, die Verhaltensdaten von Teilnehmern aus Adobe Learning Manager zu verfolgen und darauf zu reagieren, indem sie sie mit der Marketo-Datenbank synchronisieren.

Der Marketo Engage-Connector ermöglicht eine nahtlose Datensynchronisierung zwischen den beiden Systemen und ermöglicht Marketern die Verwendung von Lernaktivitätsdaten zur Erstellung zielgerichteter Marketingkampagnen.

Mit dem Marketo Engage-Connector können Sie:

- Leads in der Marketo Engage-Datenbank automatisch hinzufügen oder aktualisieren, wenn Anwender zu Adobe Learning Manager hinzugefügt werden.
- Synchronisieren Sie das Lernverhalten von Benutzern wie Kursregistrierungen, Abschlüsse, Qualifikationszuweisungen und Qualifikationsabschlüsse als benutzerdefinierte Objekte in Marketo.
- Erstellen Sie mithilfe dieser Daten dynamische Kampagnen in Marketo, die Funktionen wie **Smart Lists** nutzen.

Diese Integration hilft Marketing-Experten, Zielgruppen basierend auf ihrer Lernerfahrung innerhalb von Adobe Learning Manager anzusprechen.

## Wichtigste Funktionen

- Automatisierte Lead-Erstellung und -Aktualisierung auf Basis von Adobe Learning Manager-Anwendern.
- Exportieren Sie Lernaktivitäten (Registrierungen, Abschlüsse, Erfolge von Kenntnissen) als benutzerdefinierte Objekte in Marketo.
- Planen oder lösen Sie Exporte bei Bedarf aus.
- Unterstützung für vereinheitlichte Berichte, einschließlich:
   - Benutzerbericht
   - Teilnehmertranskript
   - Benutzerkenntnisbericht

## Voraussetzungen

Stellen Sie vor der Integration sicher, dass Ihr Marketo-Konto die Schemaerstellung über APIs unterstützt.

Sie benötigen die folgenden Details, um die Verbindung herzustellen:

- **Verbindungsname**
- **Client-ID**
- **Client-Geheimnis**
- **Marketo Engage-Domäne**

>[!NOTE]
>
>Sie können die Client-ID und den Client-Schlüssel aus der Marketo Engage-App unter **LaunchPoint** und die Domäne aus dem Abschnitt **Webdienste** abrufen.

## Connector einrichten

Einrichten des Marketo Engage-Connectors:

1. Melden Sie sich bei Adobe Learning Manager als Integrationsadministrator an.
2. Bewegen Sie den Mauszeiger über die Kachel **Marketo Engage** und wählen Sie **Verbinden** aus.

   ![](assets/marketo-engage-connector1.png)
   _Wählen Sie &quot;Verbinden&quot; aus, um den Marketo Engage-Connector zu konfigurieren_

3. Geben Sie die erforderlichen Anmeldeinformationen ein

   - Verbindungsname
   - Client-ID
   - Client-Geheimnis
   - Marketo Engage-Domäne

   ![](assets/marketo-engage-connector2.png)
   _Geben Sie die erforderlichen Details für den Marketo Engage-Connector ein._

4. Wählen Sie **Verbindung** aus, um die Verbindung herzustellen.

## Events und Kampagnen-Trigger.

Sie können Datenexporte nach Marketo Engage auf Grundlage der folgenden Ereignisse auslösen:

- Ein neuer Benutzer wird zu Adobe Learning Manager hinzugefügt.
- Ein Benutzer wird für einen Kurs registriert.
- Ein Benutzer schließt einen Kurs ab.
- Ein Benutzer wird für Kenntnisse registriert.
- Ein Benutzer schließt Kenntnisse ab.

Diese Ereignisse können **on demand** oder **auf terminierter Basis exportiert werden**.

## Spaltenzuordnung

Marketo verwendet zwei Datenbanken:

- **Lead-Datenbank** - für Benutzerdatensätze (Leads)
- **Benutzerdefinierte Objektdatenbank** - für benutzerdefinierte Aktivitäts- und Ereignisdatensätze

So ordnen Sie Felder zwischen Adobe Learning Manager und Marketo zu:

1. Die Felder **Benutzerbericht** aus Adobe Learning Manager werden in einer Spalte angezeigt.
2. Die entsprechenden **Marketo-Felder** sind in der Spalte nebenan aufgelistet.
3. Ordnen Sie die entsprechenden Felder aus dem Lern-Manager der Marketo zu, um Leads zu erstellen und zu aktualisieren.
4. Nach der Zuordnung werden alle exportierten Benutzer als Leads in der Marketo-Lead-Datenbank angezeigt.

Den exportierten Berichten im Abschnitt **Benutzerdefinierte Marketo-Objekte** wird &quot;cp_&quot; vorangestellt.

## Unterstützte Exportereignisse

Sie können die folgenden benutzerbezogenen Ereignisse in Ihre Marketo Engage-Instanz exportieren:

- Neuer Benutzer hinzugefügt
- Benutzermetadaten wurden aktualisiert
- Benutzeraktivität aktualisiert
- Schulungsregistrierung
- Selbstregistrierung
- Qualifikationsabschluss

Diese Exporte helfen dabei, Interaktionen zu fördern und Outreach-Kampagnen mithilfe von Lernaktivitätsdaten zu personalisieren.
