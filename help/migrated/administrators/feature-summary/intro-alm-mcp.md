---
description: Erweitern Sie Adobe Learning Manager in Claude, ChatGPT Enterprise und benutzerdefinierte Agenten, sodass Teilnehmer Kurse finden, den Fortschritt verfolgen und Antworten erhalten können.
jcr-language: en_us
title: Adobe Learning Manager Model Context Protocol-Server
exl-id: 8d0a25a6-1301-4f68-8db7-e3b1d3ff6537
source-git-commit: 89aa1b5ab02eed8a61507ab162fcbbd384e6c5fc
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%
---

# Adobe Learning Manager Model Context Protocol-Server

Das Model Context Protocol (MCP) ist ein offener Standard, mit dem ein AI-Client externe Tools erkennen und aufrufen kann. Der Adobe Learning Manager MCP-Server legt die Adobe Learning Manager-Teilnehmer-Tools für jeden MCP-kompatiblen Client, z. B. einen benutzerdefinierten Enterprise-Agenten, Claude oder ChatGPT Enterprise. Teilnehmer erreichen ihre Schulung und ihren Fortschritt über den Client, den sie bereits verwenden, während die Lerninhalte und -datensätze in Adobe Learning Manager verbleiben.

## Funktionsweise

Ein Teilnehmer sendet eine Anfrage in natürlicher Sprache an einen AI-Client. Der Client wählt das relevanteste Teilnehmer-Tool aus und ruft den MCP-Server mit dem OAuth-Zugriffstoken des Teilnehmers auf. Adobe Learning Manager führt das Tool als dieser Teilnehmer aus und gibt das Ergebnis zurück. Der Client erstellt die endgültige Antwort.

Jeder Anruf trägt die Identität des Teilnehmers. Ein Teilnehmer kann daher nur die Inhalte und Datensätze abrufen, auf die er bereits zugreifen darf.

Der AI-Client ruft den MCP-Server auf, der jede Anforderung an das entsprechende Teilnehmer-Tool weiterleitet.

## Teilnehmerfunktionen

Teilnehmer arbeiten in der natürlichen Sprache im AI-Client, den sie bereits verwenden. Der Client interpretiert jede Anforderung, ruft das entsprechende Adobe Learning Manager-Teilnehmertool auf und gibt eine Antwort zurück, die darauf basiert, worauf der Teilnehmer zugreifen kann. Teilnehmer können:

* Entdecken Sie die Kurse, Zertifizierungen und Lernpfade, die für sie verfügbar sind.
* Verfolgen Sie ihre Registrierungen, Fortschritte und Fristen, einschließlich der Lernprogramme, die demnächst ablaufen.
* Erhalten Sie Antworten auf Lerninhalte.
* Generieren Sie anhand Ihrer Ziele einen personalisierten Lernpfad und speichern Sie ihn.

Die vollständige Liste finden Sie in der **Referenz zu den Teilnehmertools**.

## Kunden- und Partnerschulung

>[!IMPORTANT]
>
>Kunden, die eigene Enterprise-Agenten erstellen, können ebenfalls eine Verbindung zum Server herstellen. Eine Partnerorganisation kann ihren eigenen Kunden beispielsweise über ihren eigenen Support-Mitarbeiter Zugang zu Schulungen bieten.

Kunden- und Partnerschulungen sind eine primäre Nutzung des MCP-Servers. Unternehmen, die eigene KI-Agenten für Unternehmen entwickeln, können diese Agenten mit den Adobe Learning Manager-Lernprogrammen verbinden. Ihre Kunden und Partner lernen dann innerhalb des Assistenten, den sie bereits verwenden, ohne zu einem separaten Lernassistenten zu wechseln.

Acme Inc. z. B. entwickelt einen eigenen KI-Assistenten für Unternehmen. Ein Partner von Acme Inc. besucht den Assistenten, um mehr über die Produkte von Acme Inc. zu erfahren. Der Assistent stellt über den MCP-Server eine Verbindung mit dem Konto von Acme Inc. Adobe Learning Manager her und gibt lernbezogene Antworten zurück. Der Partner verlässt nie die Acme Inc. Erfahrung.

Mit diesem Ansatz können Organisationen:

* Stellt Lernerlebnisse innerhalb der vorhandenen KI-Erlebnisse eines Partners bereit.
* Erweitern Sie benutzerdefinierte Unternehmensagenten mit den Lernwerkzeugen von Adobe Learning Manager.
* Integrieren Sie Lernen in Ihre eigenen Workflows.
* Integrieren Sie Lernen in das KI-Ökosystem des Unternehmens.

## Mitarbeiterschulung

Mitarbeiter, die bereits einen AI-Client verwenden, wie Claude, können ihre Lerninformationen dort abrufen. Beispielsweise kann ein Mitarbeiter zugewiesenes Lernen überprüfen, Anmeldungen überprüfen, Kurse zu einem Thema suchen oder nach einem Lernpfad fragen, ohne zu Adobe Learning Manager zu wechseln. Für Beispielanforderungen erfahren Sie mehr über [Beispielaufforderungen für Teilnehmer](/help/migrated/learners/feature-summary/sample-prompts-for-learners.md).

Mit diesem Ansatz können Mitarbeiter:

* Bleibe bei den Tools, die sie bereits einsetzen.
* Erreichen Sie Ihr Ziel, wo immer sie arbeiten.
* Verwenden Sie einen beliebigen MCP-kompatiblen AI-Client als Einstiegspunkt zu Adobe Learning Manager.
* Abrufen von Lerninformationen ohne Änderung des Kontexts

## Ein Server für beide Zielgruppen.

Kunden- und Partnerschulungen sowie Mitarbeiterschulungen verwenden dieselben Teilnehmer-Tools und denselben Server. Nur die Zielgruppe ändert sich. Wählen Sie den Ansatz, der zu Ihren Teilnehmern passt.

| **Zielgruppe** | **Beispiel** | **Wo die Teilnehmer arbeiten** |
|----|----|----|
| Extern | Kunden und Partner. | Der KI-Agent Ihres Unternehmens |
| interne | Mitarbeiter | Ein AI-Client für Unternehmen, z. B. Claude oder ChatGPT Enterprise |

## Rollen einrichten

Das Setup ist auf drei Rollen aufgeteilt.

* **Administrator:** Erstellt eine MCP-Clientanwendung in Adobe Learning Manager und verwaltet sie. Weitere Informationen über [Konfigurieren eines MCP-Servers](/help/migrated/administrators/feature-summary/configure-mcp-admin.md).
* **AI-Client-Administrator:** Fügt den Server dem Unternehmens-AI-Client der Organisation hinzu, z. B. Claude oder ChatGPT Enterprise.
* **Teilnehmer:** Wählt **Connect** im AI-Client aus, authentifiziert die Verbindung und stellt die Adobe Learning Manager-Kontodetails bereit.

## Sicherheit der Teilnehmeranfragen

Jeder Teilnehmer authentifiziert die Verbindung und stellt seine Adobe Learning Manager-Kontodetails bereit. Jede Anforderung wird als dieser Teilnehmer ausgeführt, sodass der AI-Client nur die Informationen zurückgibt, auf die der Teilnehmer in Adobe Learning Manager zugreifen kann. Der Server gewährt Teilnehmern keinen zusätzlichen Zugriff.

## Einschränkungen

* Der MCP-Server ist nur für Adobe Learning Manager Ultimate -Konten verfügbar.
* Die Verfügbarkeit von Tools hängt davon ab, was dein AI-Client unterstützt.
* Der Server behandelt jede Anforderung als neu. Multiturn-Unterhaltungen funktionieren nur, wenn Ihr AI-Client den Konversationskontext beibehält.
