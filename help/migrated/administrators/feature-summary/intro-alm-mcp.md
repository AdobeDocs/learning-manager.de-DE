---
description: Ermöglichen Sie es Teilnehmern, Kurse zu entdecken, den Fortschritt zu verfolgen und Antworten auf Adobe Learning Manager-Inhalte in Claude, ChatGPT Enterprise und benutzerdefinierten Mitarbeitern zu erhalten.
jcr-language: en_us
title: Adobe Learning Manager Model Context Protocol-Server
exl-id: 8d0a25a6-1301-4f68-8db7-e3b1d3ff6537
source-git-commit: 05691364449234a4782e2de5d4752c7b277f5fd4
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%
---

# Adobe Learning Manager Model Context Protocol-Server

## Übersicht

Das Model Context Protocol (MCP) ist eine Standardmethode für einen AI-Client, um eine Verbindung zu Tools herzustellen. Der Adobe Learning Manager MCP-Server bringt das Lernen dorthin, wo die Teilnehmer bereits arbeiten. Die Adobe Learning Manager-Teilnehmer-Tools werden allen AI-Clients gelegt, die MCP unterstützen, z. B. einem benutzerdefinierten Unternehmens-Agent, Claude oder ChatGPT. Teilnehmer können dann innerhalb desselben Clients auf ihre Schulungen und ihren Fortschritt zugreifen, während der Inhalt in Adobe Learning Manager bleibt.

## Teilnehmerfunktionen

Teilnehmer arbeiten in der natürlichen Sprache im AI-Client, den sie bereits verwenden. Der Client interpretiert jede Anforderung, ruft das entsprechende Adobe Learning Manager-Teilnehmertool auf und gibt eine Antwort zurück, die darauf basiert, worauf der Teilnehmer zugreifen kann. Teilnehmer können:

* Entdecken Sie die Kurse, Zertifizierungen und Lernpfade, die für sie verfügbar sind.
* Verfolgen Sie ihre Registrierungen, Fortschritte und Fristen, einschließlich der Lernprogramme, die demnächst ablaufen.
* Erhalten Sie Antworten auf Lerninhalte.
* Generieren Sie anhand Ihrer Ziele einen personalisierten Lernpfad und speichern Sie ihn.
Die vollständige Liste finden Sie in der **Referenz zu den Teilnehmertools**.

Der AI-Client ruft den MCP-Server auf, der jede Anforderung an das entsprechende Teilnehmer-Tool weiterleitet.

Die vollständige Liste finden Sie in der **Referenz zu den Teilnehmertools**.

## Kunden- und Partnerschulung

Kunden- und Partnerschulungen sind eine primäre Nutzung des MCP-Servers. Unternehmen, die eigene KI-Agenten für Unternehmen entwickeln, können diese Agenten mit den Adobe Learning Manager-Lernprogrammen verbinden. Ihre Kunden und Partner lernen dann innerhalb des Assistenten, den sie bereits verwenden, ohne zu einem separaten Lernassistenten zu wechseln.

Acme Inc. z. B. entwickelt einen eigenen KI-Assistenten für Unternehmen. Ein Partner von Acme Inc. besucht die Umgebung von Lenovo, um mehr über die Lenovo-Produkte zu erfahren. Der Acme-Mitarbeiter stellt über den MCP-Server eine Verbindung zu seinem Adobe Learning Manager-Konto her und gibt lernbezogene Antworten zurück, sodass der Partner das Acme-Erlebnis nie verlässt.

Mit diesem Ansatz können Organisationen:

* Bieten Sie Lernerlebnisse innerhalb der vorhandenen KI-Erfahrung eines Partners.
* Lassen Sie die Teilnehmer-Tools von Adobe Learning Manager von benutzerdefinierten Unternehmensagenten verwenden.
* Baue das Lernen in ihre eigenen Workflows ein.
* Integrieren Sie Lernen in das KI-Ökosystem des Unternehmens.

## Mitarbeiterschulung

Mitarbeiter, die bereits einen AI-Client verwenden, wie Claude, können ihre Lerninformationen dort abrufen. Beispielsweise kann ein Mitarbeiter zugewiesenes Lernen überprüfen, Anmeldungen überprüfen, Kurse zu einem Thema suchen oder nach einem Lernpfad fragen, ohne zu Adobe Learning Manager zu wechseln. Beispielanforderungen finden Sie unter [Beispielanforderungen für Teilnehmer](https://word-edit.officeapps.live.com/docs/sample-prompts-adobe-learning-manager-learners).

Mit diesem Ansatz können Mitarbeiter:

* Bleibe bei den Tools, die sie bereits einsetzen.
* Erreichen Sie Ihr Ziel, wo immer sie arbeiten.
* Verwenden Sie einen beliebigen AI-Client, der MCP unterstützt, als Einstiegspunkt zu Adobe Learning Manager.
* Erhalten Sie Lerninformationen, ohne den Kontext zu ändern.

## Ein Server für beide Zielgruppen.

Kunden- und Partnerschulungen sowie Mitarbeiterschulungen verwenden dieselben Teilnehmer-Tools und denselben Server. Nur die Zielgruppe ändert sich. Wählen Sie den Ansatz, der zu Ihren Teilnehmern passt.

| **Zielgruppe** | **Beispiel** | **Wo die Teilnehmer arbeiten** |
|----|----|----|
| Extern | Kunden und Partner. | Der KI-Agent Ihres Unternehmens |
| interne | Mitarbeiter | Ein AI-Client für Unternehmen, z. B. Claude oder ChatGPT Enterprise |

## Rollen einrichten

Die Einrichtung ist auf drei Rollen aufgeteilt.

* **Administrator:** Erstellt eine MCP-Clientanwendung in Adobe Learning Manager und verwaltet sie. Siehe [MCP-Server konfigurieren](https://word-edit.officeapps.live.com/docs/configure-model-context-protocol-server-adobe-learning-manager).
* **AI-Client-Administrator:** Fügt den Server dem Unternehmens-AI-Client der Organisation hinzu, z. B. Claude oder ChatGPT Enterprise.
* **Teilnehmer:** Wählt **Connect** im AI-Client aus, authentifiziert die Verbindung und stellt die Adobe Learning Manager-Kontodetails bereit.

## Sicherheit der Teilnehmeranfragen

Jeder Teilnehmer authentifiziert die Verbindung und stellt seine Adobe Learning Manager-Kontodetails bereit. Die Anforderung wird als dieser Teilnehmer ausgeführt, sodass der AI-Client nur die Informationen zurückgibt, auf die der Teilnehmer in Adobe Learning Manager zugreifen kann. Der Server gibt Teilnehmern keinen zusätzlichen Zugriff.

## Einschränkungen für MCP in diesem Update

* Die Verfügbarkeit von Tools hängt davon ab, was dein AI-Client unterstützt.
* Jede Anforderung wird als neu behandelt. Multi-Turn-Konversationen funktionieren nur, wenn euer AI-Client die Konversation kontextbezogen hält.
