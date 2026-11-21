---
description: Fügen Sie den Adobe Learning Manager-Server als benutzerdefinierte Verbindung zu Ihrem eigenen Claude-Konto hinzu, melden Sie sich an und fragen Sie nach Ihren Lerninhalten
jcr-language: en_us
title: Adobe Learning Manager zu Claude als Teilnehmer hinzufügen
exl-id: 31c00b29-4919-48b7-9993-ed3ac358ba5e
source-git-commit: 05691364449234a4782e2de5d4752c7b277f5fd4
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%
---

# Adobe Learning Manager zu Claude als Teilnehmer hinzufügen

Führen Sie diese Schritte nur aus, wenn Ihr Unternehmen die Verbindung noch nicht für Sie hinzugefügt hat. Wenn Sie eine Adobe Learning Manager-Verbindung in Claude sehen, wählen Sie stattdessen **Connect** aus.

## Verbindung in Claude hinzufügen

1. Wechseln Sie in Claude zu **Anpassen** \> **Verbindungen**.
2. Wählen Sie **Hinzufügen** (**+**) aus, und wählen Sie dann **Benutzerdefinierte Verbindung hinzufügen** aus.
3. Geben Sie einen **Namen** ein, z. B. Adobe Learning Manager.
4. Geben Sie die MCP-Endpunkt-URL in **URL des Remote-MCP-Servers** ein.
5. Wählen Sie **Weiter**.
6. Halten Sie unter **Authentifizierung** **Jetzt anmelden**.
7. Wählen Sie unter **OAuth-Client** die Option **Einen eigenen OAuth-Client verwenden** aus.
8. Geben Sie die Client-ID in **Client-ID** ein.
9. Geben Sie den geheimen Schlüssel in **Clientschlüssel** ein.
10. Wählen Sie **Hinzufügen** aus.
11. Melden Sie sich beim Öffnen der Anmeldeseite bei Adobe Learning Manager an.

Nachdem Sie sich angemeldet haben, wird die Verbindung als verbunden angezeigt. Stellen Sie eine Frage zum Lernen. Für Ideen sehen Sie **Beispielaufforderungen für Teilnehmer**.

>[!IMPORTANT]
>
>Claude bezeichnet das Feld &quot;Client-Geheimnis&quot; als optional, aber Adobe Learning Manager erfordert es. Wenn Sie das Feld leer lassen oder einen falschen Wert eingeben, schlägt die Anmeldung fehl und die Meldung &quot;Autorisierung fehlgeschlagen&quot; wird angezeigt.

>[!NOTE]
>
>Ihre Anforderungen werden mit Ihren eigenen Berechtigungen ausgeführt. Claude kann nur sehen, was du in Adobe Learning Manager siehst.

## Anderes Adobe Learning Manager-Konto verwenden

Wenn in deinem Browser bereits eine Adobe Learning Manager-Sitzung aktiv ist, stellt Claude eine Verbindung zu diesem Konto her, ohne nach Anmeldedaten zu fragen. Um die Verbindung als anderer Benutzer herzustellen, melden Sie sich zuerst bei Adobe Learning Manager ab oder verwenden Sie ein privates Browserfenster.

## Andere KI-Kunden

Für ChatGPT oder einen anderen Client unterscheiden sich die Schritte. Informationen zum Hinzufügen einer benutzerdefinierten Verbindung finden Sie in der Dokumentation Ihres AI-Clients. Verwenden Sie dabei die gleichen drei Werte von Ihrem Administrator.

## Fehlerbehebung

**Bei der Anmeldung wird eine nicht registrierte Umleitungsnachricht angezeigt.** Ihr Administrator muss die Claude-Domäne zu **Domänen umleiten** für den Server hinzufügen. Bitten Sie Ihren Administrator, <https://claude.ai> hinzuzufügen, und versuchen Sie es erneut.

**Claude sagt, Autorisierung fehlgeschlagen.** Überprüfen Sie den geheimen Schlüssel auf zusätzliche Leerzeichen oder einen falschen Wert. Kopieren Sie es erneut von Ihrem Administrator, entfernen Sie die Verbindung und fügen Sie sie erneut hinzu.

**Sie haben eine Verbindung als falscher Benutzer hergestellt.** Trennen Sie die Verbindung, melden Sie sich von Adobe Learning Manager ab und stellen Sie die Verbindung erneut in einem privaten Browserfenster her.

**Claude fordert Sie auf, sich erneut anzumelden.** Ihre Sitzung ist abgelaufen oder Ihr Zugriff wurde widerrufen. Wählen Sie **Verbinden** aus, um sich erneut anzumelden.
