---
description: Erstellen, Bearbeiten und Löschen eines Model Context Protocol-Servers in Adobe Learning Manager, damit Teilnehmer ihre Lerninhalte von AI-Clients aus abrufen können
jcr-language: en_us
title: Konfigurieren eines Model Context Protocol-Servers
exl-id: 3130c36d-e63e-4cd6-b0ed-561371b9b261
source-git-commit: 05691364449234a4782e2de5d4752c7b277f5fd4
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 1%
---

# Konfigurieren eines Model Context Protocol-Servers

Als Administrator erstellen Sie einen Server, kopieren dessen Anmeldeinformationen und geben diese an den AI-Client-Administrator weiter, der die Verbindung abschließt. Sie können einen Server jederzeit erneut aufrufen, um ihn zu bearbeiten, seine Tools zu aktualisieren, seine Anmeldeinformationen zu kopieren, seinen Status zu ändern oder ihn zu löschen.

## Erstellen des MCP-Servers

1. Melden Sie sich bei Adobe Learning Manager als Administrator an.
2. Wechseln Sie zu **AI in Learning** \> **MCP Servers**.
3. Wählen Sie **Neuer MCP-Server** aus.
4. Geben Sie die Serverdetails einschließlich einer Beschreibung ein.

   * **Servername:** Geben Sie einen Namen mit bis zu 50 Zeichen ein.
   * **Beschreibung:** Geben Sie eine kurze Beschreibung mit bis zu 150 Zeichen ein.
   * **URL:** Geben Sie die URL Ihres Unternehmens oder Ihrer Anwendung ein.
   * **Domänen umleiten:** Geben Sie die Domäne jedes AI-Clients ein, der eine Verbindung herstellen wird, z. B. [http://\*.chatgpt.com](https://encoded-592c9deb-987b-4562-aa3c-9fa3d37d83e9.uri/http%3a%2f%2f*.chatgpt.com) oder [http://\*.claude.ai](https://encoded-592c9deb-987b-4562-aa3c-9fa3d37d83e9.uri/http%3a%2f%2f*.claude.ai). Dieses Feld ist erforderlich.

     ![](/help/migrated/administrators/feature-summary/assets/configure-mcp-admin1.png)

5. Wählen Sie **Weiter**.
6. Überprüfen Sie auf der Seite **Verfügbare Tools** die vom Server gelegt Teilnehmertools. Bereitstellen detaillierter, kontextbezogener und zweckorientierter Beschreibungen für MCP-Tools Gut geschriebene Toolbeschreibungen helfen MCP-kompatiblen Clients dabei, die entsprechenden Tools genauer zu erkennen und aufzurufen. Hierzu zählen der Zweck des Tools, unterstützte Aufgaben, erwartete Eingaben und typische Anwendungsfälle. Klare und präzise Beschreibungen verbessern die Werkzeugauswahl und die allgemeine Benutzererfahrung, wenn Teilnehmer mit KI-Assistenten interagieren.

   ![](assets/configure-mcp-admin2.png)

   Wählen Sie **Ansicht** für jedes Tool aus, um die Anweisungen anzuzeigen, um zu bestimmen, wann das Tool ausgewählt ist und wie das Tool reagiert.

   ![](assets/configure-mcp-admin3.png)

7. Wählen Sie im linken Navigationsbereich **Client-Anmeldeinformationen** aus.
8. Kopieren Sie die **MCP-Endpunkt-URL**, **Client-ID** und den **geheimen Schlüssel**. Wählen Sie **Kopieren** neben jedem Wert.

   ![](assets/configure-mcp-admin4.png)

9. Wählen Sie **Schließen**.

>[!NOTE]
>
>Der Server bietet schreibgeschützten Zugriff auf Benutzer mit der Teilnehmerrolle.

Geben Sie die Endpunkt-URL, die Client-ID und den geheimen Schlüssel an Ihren AI-Client-Administrator weiter.

## Bearbeiten einer Werkzeugbeschreibung

Eine Toolbeschreibung weist den AI-Client an, wann das Tool ausgewählt werden soll und wie das Tool reagiert. Sie können auch Beispielaufforderungen hinzufügen. Gut geschriebene Toolbeschreibungen helfen MCP-kompatiblen Clients dabei, die entsprechenden Tools genauer zu erkennen und aufzurufen. Hierzu zählen der Zweck des Tools, unterstützte Aufgaben, erwartete Eingaben und typische Anwendungsfälle.

1. Wählen Sie auf der Seite **Verfügbare Tools** das Menü **Aktionen** für ein Tool aus.
2. Wählen Sie **MCP-Tool-Konfiguration** \> **Bearbeiten** aus.

   ![](assets/configure-mcp-admin5.png)

3. Aktualisieren Sie im Dialogfeld **Edit tool** **Instructions/Description**.

   ![](assets/configure-mcp-admin6.png)

4. Bearbeiten Sie unter **Beispielaufforderungen** die Aufforderungen. Um eine Eingabeaufforderung hinzuzufügen, wählen Sie **Ein weiteres Beispiel hinzufügen**.
5. Wählen Sie **Speichern**.

Um ein Tool auf seinen ursprünglichen Wortlaut zurückzusetzen, wählen Sie das Menü **Aktionen** für das Tool aus und wählen dann **MCP-Tool-Konfiguration** \> **Zurücksetzen**.

## MCP-Server bearbeiten

1. Wählen Sie **AI in Learning** \> **MCP-Server** aus.
2. Wählen Sie den Servernamen aus.
3. Wählen Sie **Bearbeiten**.
4. Aktualisieren Sie die Felder auf der Seite **Anwendungsdetails** und speichern Sie dann Ihre Änderungen.

## MCP-Server löschen

1. Wählen Sie **AI in Learning** \> **MCP-Server** aus.
2. Wählen Sie in der Zeile für den Server das Menü **Aktionen** aus.
3. Wählen Sie **Löschen** aus.
4. Wählen Sie im Bestätigungsdialogfeld **Löschen** aus.

>[!WARNING]
>
>Durch das Löschen eines Servers wird der Zugriff auf alle zugehörigen Tools für verbundene KI-Anwendungen entfernt. Aktive Sitzungen funktionieren möglicherweise nicht mehr sofort und Sie können den Löschvorgang nicht mehr rückgängig machen.

## Fehlerbehebung

**Werkzeugänderungen werden nicht sofort angezeigt.**
Änderungen an Werkzeugbeschreibungen werden erst nach einer Weile wirksam. Warten Sie und versuchen Sie es erneut.

**Ein AI-Client funktioniert nicht mehr, nachdem ein Server gelöscht wurde.**
Erstellen Sie einen neuen Server und geben Sie die neuen Anmeldeinformationen an Ihren AI-Client-Administrator weiter.

**Der AI-Client verwendet das falsche Tool.**
Prüfen Sie alle von Ihnen geänderten Werkzeugbeschreibungen. Verwenden Sie **Zurücksetzen**, um den ursprünglichen Wortlaut wiederherzustellen.

## Best Practices

* Behalten Sie die ursprünglichen Werkzeugbeschreibungen bei, es sei denn, Sie haben einen bestimmten Grund, sie zu ändern.
* Schreiben Sie klare, spezifische Werkzeugbeschreibungen und Beispielaufforderungen, wenn Sie sie bearbeiten.
* Speichern Sie den geheimen Schlüssel sicher und geben Sie ihn nur an Ihren AI-Client-Administrator weiter.
* Erstellen Sie für jede AI-Anwendung einen separaten Server, damit Sie einen löschen können, ohne die anderen zu beeinträchtigen.
* Vergewissern Sie sich, dass keine AI-Anwendung von einem Server abhängig ist, bevor Sie ihn löschen.
