---
description: Erfahren Sie, was die Teilnehmer mit dem Adobe Learning Manager Model Context Protocol-Server tun können und welche MCP-Tools die einzelnen Funktionen unterstützen.
jcr-language: en_us
title: Teilnehmer-Tools für den Model Context Protocol-Server
exl-id: 4509b984-d0ba-4b7e-a0bb-803aa235fd1e
source-git-commit: 05691364449234a4782e2de5d4752c7b277f5fd4
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 2%
---

# Teilnehmer-Tools für den Model Context Protocol-Server

Jede Funktion wird als angemeldeter Teilnehmer ausgeführt, nachdem der Teilnehmer eine Verbindung hergestellt hat. Eine Anforderung gibt nur den Inhalt zurück, auf den dieser Teilnehmer in Adobe Learning Manager zugreifen kann. Weitere Informationen finden Sie unter [Verbinden Ihres AI-Clients](/help/migrated/learners/feature-summary/connect-ai-client-to-alm-learner.md).

## Teilnehmerfunktionen

| **Funktion** | **Welche Möglichkeiten Teilnehmer haben** | **Beispielanforderung** |
|----|----|----|
| Lerninhalte suchen | Kurse, Zertifizierungen und Lernpfade finden | Welche Führungskurse gibt es? |
| Registrierungen anzeigen | Anmeldungen und ordnungsgemäße Lerninhalte prüfen | Welche meiner Kurse laufen demnächst ab? |
| Lernfragen stellen | Antworten auf Fragen zu Lerninhalten | Was bedeutet Management von Lieferkettenrisiken in FedRAMP? |
| Lernpfade generieren | Erstellen personalisierter Lernpfade | Helfen Sie mir, Kurse zu finden, die Kenntnisse im Projektmanagement erweitern. |
| Speichern von Lernpfaden | Generierte Lernpfade speichern | Speichern Sie diesen Lernpfad. |

## Unterstützte MCP-Werkzeuge

Der Teilnehmer-Assistent-MCP-Server legt die folgenden Tools für Teilnehmer.

| **MCP-Tool** | **Zweck** | **Unterstützt die Funktion** |
|----|----|----|
| Suchen | Verfügbare Lerninhalte suchen | Lerninhalte suchen |
| Registrierung abrufen | Registrierungsinformationen für Teilnehmer abrufen | Registrierungen anzeigen |
| Antwort-Agent | Beantworten von Fragen mithilfe von Lerninhalten | Lernfragen stellen |
| Benutzer abrufen | Identifizieren des angemeldeten Teilnehmers für jede Anforderung | Alle Funktionen |
| Lernobjekt abrufen | Abrufen von Details zu einem Lernobjekt, z. B. Beschreibung und Dauer | Lerninhalte suchen, Registrierungen anzeigen |
| Lernpfad generieren | Erstellen empfohlener Lernpfade | Lernpfade generieren |
| Lernpfad speichern | Generierte Lernpfade speichern | Speichern von Lernpfaden |

>[!IMPORTANT]
>
>Tool-Namen werden als Referenz angezeigt und können je nach Client-Implementierung variieren.

