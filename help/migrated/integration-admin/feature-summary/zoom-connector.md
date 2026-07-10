---
description: Erfahren Sie, wie Sie den Zoom-Connector mit Adobe Learning Manager integrieren
jcr-language: en_us
title: Zoom-Connector
contentowner: mmanuel
source-git-commit: 481eed24a5ac72329228c8d27b625d443bd637ce
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 1%

---


# Zoom-Connector in Adobe Learning Manager

## Einführung

Der Zoom-Connector in Adobe Learning Manager ermöglicht die nahtlose Integration in Zoom, um Live-Sitzungen im virtuellen Klassenzimmer bereitzustellen. Mit dieser Integration können Kursleiter Zoom-Meetings direkt über den Lernmanager hosten, Teilnehmer registrieren und die Anwesenheit und den Abschluss verfolgen. Teilnehmer erhalten automatisch Einladungen und können über ihre Adobe Learning Manager-Konten an Sitzungen teilnehmen. Nach der Sitzung werden die Anwesenheits- und Leistungsdaten wieder mit Adobe Learning Manager synchronisiert, um Berichte und Nachverfolgung zu erstellen.

## Einrichten des Zoom-Connectors

So konfigurieren Sie den Zoom-Connector:

1. Melden Sie sich bei Adobe Learning Manager als Integrationsadministrator an.
2. Bewegen Sie den Mauszeiger über die Kachel **Zoom**.

   ![](assets/zoom-connector1.png)
   _Zoom-Connector in Adobe Learning Manager konfigurieren_

3. Wählen Sie **Verbinden**. Die Einrichtungsseite des Zoom-Connectors wird geöffnet.
4. Geben Sie die folgenden Kontodetails in die entsprechenden Felder ein. Sie können diese Anmeldedaten von Ihrem Zoom-Kontoadministrator erhalten:

   * Verbindungsname
   * Konto-ID zoomen
   * Client-ID
   * Client-Geheimnis
   * E-Mail-Adresse des Super-Administrators

   ![](assets/zoom-connector2.png)
   _Geben Sie die Konfigurationsdetails zum Einrichten des Zoom-Connectors ein_

5. Wählen Sie **Verbinden**, um die Integration einzurichten.

>[!NOTE]
>
>Wenn Sie den Connector aktivieren, müssen **Teilnehmer dieselbe E-Mail-Adresse** für ihre Zoom- und Adobe Learning Manager-Konten verwenden, um sicherzustellen, dass die Benutzerdaten ordnungsgemäß synchronisiert werden.

## Zoom-Kurse erstellen

Sobald die Verbindung hergestellt ist:

1. Melden Sie sich als **Autor** an und erstellen Sie einen neuen Kurs für virtuelle Klassenzimmer.
2. Wählen Sie während der Kurserstellung **Zoom** als Konferenzsystem aus.
3. Weisen Sie dem Kurs Teilnehmer über Administratoren, Manager oder durch Selbsteinschreibung zu.
4. Nach der Registrierung erhalten die Teilnehmer eine E-Mail mit Kursdetails.
5. Teilnehmer können sich bei ihrem Adobe Learning Manager-Konto anmelden, um auf den Kurs zuzugreifen und an der Zoom-Sitzung teilzunehmen.

## Anwesenheit und Abschluss verfolgen

Nach dem Ende der virtuellen Sitzung:

* Adobe Learning Manager erhält automatisch den Abschlussstatus von Zoom.
* Administratoren können Anwesenheits- und Bewertungsberichte in Adobe Learning Manager anzeigen, um die Teilnahme und Leistung der Teilnehmer zu verfolgen.

## Erstellen einer Zoom-OAuth-Anwendung von Server zu Server

Um den Zoom-Connector mit Adobe Learning Manager verwenden zu können, müssen Sie eine Zoom Server-to-Server OAuth-App erstellen und die erforderlichen Geltungsbereiche konfigurieren.

### Erforderliche OAuth-Geltungsbereiche

Stellen Sie beim Erstellen der Anwendung in Zoom sicher, dass die folgenden Bereiche ausgewählt sind:

```
| Scope Description | Zoom Scope |
|---|---|
| View all user meetings | meeting:read:admin |
| View and manage all user meetings | meeting:write:admin |
| View report data | report:read:admin |
| View all user information | user:read:admin |
| Manage users | user:write:admin |
| Add a meeting registrant | meeting:write:registrant:admin |
| List all meeting registrants | meeting:read:list_registrants:admin |
| Manage sub-account meetings | meeting:write:meeting:master |
| View meeting participants report | report:read:list_meeting_participants:admin |
```
