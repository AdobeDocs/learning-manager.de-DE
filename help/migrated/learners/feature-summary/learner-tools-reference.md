---
description: Erfahren Sie, was die Teilnehmer mit dem Adobe Learning Manager Model Context Protocol-Server tun können und welche Tools die einzelnen Funktionen unterstützen.
jcr-language: en_us
title: Teilnehmer-Tools für den Model Context Protocol-Server
exl-id: 4509b984-d0ba-4b7e-a0bb-803aa235fd1e
source-git-commit: 89aa1b5ab02eed8a61507ab162fcbbd384e6c5fc
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%
---

# Teilnehmer-Tools für den Model Context Protocol-Server

## Übersicht

Jede Funktion wird als angemeldeter Teilnehmer ausgeführt, nachdem der Teilnehmer eine Verbindung hergestellt hat. Eine Anforderung gibt nur den Inhalt zurück, auf den dieser Teilnehmer in Adobe Learning Manager zugreifen kann. Weitere Informationen über [Verbinden Ihres AI-Clients](/help/migrated/learners/feature-summary/connect-ai-client-to-alm-learner.md).

## Teilnehmerfunktionen

| **Funktion** | **Welche Möglichkeiten Teilnehmer haben** | **Beispielanforderung** |
|----|----|----|
| Lerninhalte suchen | Kurse, Zertifizierungen und Lernpfade finden | Welche Führungskurse gibt es? |
| Registrierungen anzeigen | Anmeldungen und ordnungsgemäße Lerninhalte prüfen | Welche meiner Kurse laufen demnächst ab? |
| Lernfragen stellen | Antworten auf Fragen zu Lerninhalten | Was bedeutet Management von Lieferkettenrisiken in FedRAMP? |
| Lernpfade generieren | Erstellen personalisierter Lernpfade | Helfen Sie mir, Kurse zu finden, die Kenntnisse im Projektmanagement erweitern. |
| Speichern von Lernpfaden | Generierte Lernpfade speichern | Speichern Sie diesen Lernpfad. |

## Unterstützte MCP-Werkzeuge

Der Adobe Learning Manager MCP-Server legt die folgenden Teilnehmerwerkzeuge.

| **Toolname** | **Beschreibung** |
|----|----|
| search_learning_items | Suchen Sie im Katalog nach Kursen, Lernpfaden, Zertifizierungen, Arbeitshilfen, Abzeichen, Kenntnissen, Katalogen und Tags. Filtern Sie nach Teilnehmerstatus, Kenntnissen, Tag, Katalog, Bereitstellungsformat, Preis und Sprache. Verwenden Sie für Themenfragen &quot;answer_learning_content_question&quot;. Beispiel: &quot;Python-Anfängerkurse.&quot; |
| list_my_learning_enrollments | Listen Sie die registrierten, laufenden und abgeschlossenen Kurse, Lernpfade, Zertifizierungen und Arbeitshilfen des Teilnehmers mit Status, Fortschritt und Termin auf. Filtern Sie nach Lernobjekttyp oder Abschlussstatus. Die Ergebnisse zeigen zuerst die letzten Registrierungen an. Beispiel: &quot;Was ist bald fällig?&quot; |
| get_learning_object | Erhalten Sie die vollständigen Details eines Kurses, eines Lernpfads, einer Zertifizierung oder einer Arbeitshilfe nach ID, optional mit Instanzen, Kenntnissen und Sub-Lernobjekten. Rufen Sie die ID aus search_learning_items oder list_my_learning_enrollments ab. |
| get_my_learning_profile | Rufen Sie das Profil des Teilnehmers ab, einschließlich Konto- und Managerdetails. Verwenden Sie für Registrierungen und den Fortschritt list_my_learning_enrollments. |
| answer_learning_content_question | Beantworten Sie Fragen zu Lerninhalten, die auf dem Lern-Material basieren und in den Quell-Lernobjekten zitiert werden. Fassen Sie ein Lernobjekt zusammen, oder vergleichen Sie zwei nebeneinander, um die Abdeckung, die Tiefe, die Voraussetzungen und die Zielgruppe zu ermitteln. Um Inhalte zu suchen oder aufzulisten, verwenden Sie search_learning_items oder list_my_learning_enrollments. Beispiel: &quot;Erläutern Sie TCP und UDP, wie in meinem Netzwerkkurs beschrieben.&quot; |
| personalized_learning_path | Empfehlen Sie Kurse, die den Zielen, Themen und Bedürfnissen eines Teilnehmers entsprechen. Speichern Sie einen genehmigten Pfad im Konto des Teilnehmers. Listen Sie gespeicherte Pfade auf, oder rufen Sie Details und Kurse eines Pfades nach ID ab. |

>[!IMPORTANT]
>
>Tool-Namen werden als Referenz angezeigt und können je nach Client-Implementierung variieren.
