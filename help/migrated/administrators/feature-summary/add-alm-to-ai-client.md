---
description: Fügen Sie den Adobe Learning Manager MCP-Server Ihrem AI-Client für Unternehmen wie Claude oder ChatGPT Enterprise hinzu, damit die Teilnehmer eine Verbindung herstellen können.
jcr-language: en_us
title: Hinzufügen von Adobe Learning Manager zu Ihrem AI-Client für Unternehmen
exl-id: d893efb7-dc0d-4a3a-88d6-b315340e5daa
source-git-commit: 05691364449234a4782e2de5d4752c7b277f5fd4
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%
---

# Hinzufügen von Adobe Learning Manager zu Ihrem AI-Client für Unternehmen

Sie benötigen Administratorrechte in Ihrem AI-Client. Rufen Sie zuerst die MCP-Endpunkt-URL, die Client-ID und den geheimen Schlüssel von Ihrem Adobe Learning Manager-Administrator ab. Weitere Informationen finden Sie unter **Konfigurieren eines Model Context Protocol-Servers**.

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
>KI-Client-Oberflächen ändern sich oft. Wenn diese Schritte nicht mit Ihrem Client übereinstimmen, lesen Sie in der Dokumentation Ihres AI-Client-Anbieters nach, wie Sie eine Remote-Verbindung hinzufügen.

## Fehlerbehebung

**Die Teilnehmer sehen die Verbindung nicht.** Vergewissern Sie sich, dass die Verbindung für den Arbeitsbereich oder die Gruppe des Teilnehmers aktiviert ist.

**Die Autorisierung schlägt fehl, wenn ein Teilnehmer Connect auswählt.** Überprüfen Sie, ob die Client-ID und der geheime Schlüssel mit den Werten auf der Seite **Client-Anmeldeinformationen** des Servers in Adobe Learning Manager übereinstimmen.
