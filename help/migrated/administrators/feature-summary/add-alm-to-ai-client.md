---
description: Registrieren Sie den Adobe Learning Manager MCP-Server als Verbindung im AI-Client Ihres Unternehmens, damit sich die Teilnehmer in Ihrem Unternehmen verbinden und ihren Lernfortschritt abfragen können.
jcr-language: en_us
title: Hinzufügen von Adobe Learning Manager zu Ihrem AI-Client für Unternehmen
exl-id: d893efb7-dc0d-4a3a-88d6-b315340e5daa
source-git-commit: 89aa1b5ab02eed8a61507ab162fcbbd384e6c5fc
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%
---

# Hinzufügen von Adobe Learning Manager zu Ihrem AI-Client für Unternehmen

## Übersicht

Sie benötigen Administratorrechte in Ihrem AI-Client. Rufen Sie zunächst die MCP-Endpunkt-URL, die Client-ID und den geheimen Schlüssel von Ihrem Adobe Learning Manager-Administrator ab. Weitere Informationen über [Konfigurieren eines Model Context Protocol-Servers](/help/migrated/administrators/feature-summary/configure-mcp-admin.md).

## Verbindung hinzufügen

1. Melden Sie sich bei Ihrem AI-Client für Unternehmen als Administrator an.
2. Öffnen Sie die Administratoreinstellungen für Verbindungen.
3. Fügen Sie eine benutzerdefinierte Verbindung hinzu, die das Model Context Protocol verwendet.
4. Geben Sie die Adobe Learning Manager MCP-Endpunkt-URL ein.
5. Geben Sie die Client-ID und den geheimen Schlüssel von Ihrem Adobe Learning Manager-Administrator ein.
6. Speichern Sie die Verbindung.
7. Stellen Sie die Verbindung für Ihre Teilnehmer zur Verfügung.

>[!NOTE]
>
>KI-Client-Schnittstellen ändern sich häufig. Wenn diese Schritte nicht mit Ihrem Client übereinstimmen, lesen Sie in der Dokumentation Ihres AI-Client-Anbieters nach, wie eine Remote-Verbindung hinzugefügt wird.

## Fehlerbehebung

**Die Teilnehmer sehen die Verbindung nicht.**
Vergewissern Sie sich, dass die Verbindung für den Arbeitsbereich oder die Gruppe des Teilnehmers aktiviert ist.

**Die Autorisierung schlägt fehl, wenn ein Teilnehmer Connect auswählt.**
Überprüfen Sie, ob die Client-ID und der geheime Schlüssel mit den Werten auf der Seite **Client-Anmeldeinformationen** des Servers in Adobe Learning Manager übereinstimmen.
