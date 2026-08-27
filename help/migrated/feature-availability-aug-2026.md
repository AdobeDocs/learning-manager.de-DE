---
description: Erfahren Sie, welche App-Oberflächen neue Adobe Learning Manager-Funktionen für die Version von August 2026 unterstützen, einschließlich APIs, Mobilgeräte und AEM Widget
jcr-language: en_us
title: Funktionsverfügbarkeit in der Version Aug. 2026 von Adobe Learning Manager
exl-id: e134937c-630d-4285-9181-2eca114717f6
source-git-commit: bb95f74b775d279e94fad319380d451446256636
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 2%

---


# Funktionsverfügbarkeit in der Version Aug. 2026 von Adobe Learning Manager

## Zweck

Unternehmenskunden, die die Plattform über ihr eigenes Frontend (eine &quot;Headless&quot;-Implementierung) erstellen oder erweitern, fragen regelmäßig, ob eine neue oder geänderte Funktion tatsächlich außerhalb der Standard-Web-Benutzeroberfläche verwendet werden kann, über die Teilnehmer-API, die Admin-API, das AEM Widget oder eine andere Integrationsoberfläche.

Dieses Dokument bietet eine schnelle, narrative Antwort auf jede Funktion, die in dieser Version ausgeliefert wird. Für jede Funktion werden in diesem Dokument unterstützte Anwendungsoberflächen, Integrationsverfügbarkeit, Migrationsunterstützung und ggf. anwendbares Benachrichtigungsverhalten angegeben.

## Funktionsspezifische Verfügbarkeit

### Komponentenbasierter E-Mail-Generator

Dies ist eine phasenweise Aktivierung für verschiedene Konten, die sich nach der Funktionsversion anmelden - diese Konten von einem vorhandenen E-Mail-Editor zu einem neuen Editor zu migrieren. Nach der Aktivierung kann der Kunde den alten E-Mail-Editor nicht mehr verwenden. (Für die Aktivierung von Funktionen wenden Sie sich bitte an CSM/Support.)

* **Verfügbar auf:** Administrator-App. Administratoren und Autoren konfigurieren hier E-Mail-Layouts und -Vorlagen.
* **Nicht zutreffend:** Benutzeroberfläche für Teilnehmer, Headless API und AEM Widget, da Teilnehmer die resultierenden E-Mails einfach über ihren eigenen E-Mail-Client erhalten.
* **Benachrichtigungen:**
  * E-Mail-Benachrichtigungen werden weiterhin an Teilnehmer über unterstützte E-Mail-Clients hinweg gesendet.
  * Mit dieser Funktion wird kein neues plattforminternes Benachrichtigungsverhalten eingeführt.

### Externes Lernprogramm

* **Verfügbar für:** Native Web, Headless-API (Teilnehmer), Native Mobile Web und die Administrator-App.
* **Noch nicht verfügbar in:** Native Mobile App.
* **Job-API:** Nicht zutreffend.
* **Migration:** Noch nicht unterstützt.
* **Benachrichtigungen:**
  * Plattforminterne Benachrichtigungen stehen Teilnehmern und Managern zur Verfügung, wenn externe Lernaktivierungsanfragen gesendet werden oder wenn Anforderungen genehmigt oder abgelehnt werden.
  * E-Mail-Benachrichtigungen sind derzeit für diesen Arbeitsablauf nicht verfügbar.

### Inkrementeller Benutzerbericht

* **Nur verfügbar für:** Job-API. Stellt einen inkrementellen (Delta-)Export von Benutzerdaten für die Berichterstellung bereit.
* **Nicht zutreffend:**-Benutzeroberfläche, andere API-Oberflächen und Migrations-Tooling.

### Berichtsgenerator

* **Verfügbar auf:** Administrator-App.
* **Noch nicht verfügbar für:** Job-API. Ein Job-API-basierter Export ist für eine zukünftige Version geplant.
* **Migration:** Nicht zutreffend.
* **Benachrichtigungen:**
  * Benutzer erhalten plattforminterne Benachrichtigungen, wenn Berichtsdownloads bereit sind oder wenn die Berichterstellung fehlschlägt.
  * E-Mail-Benachrichtigungen sind nicht relevant.

### Hierarchische Inhaltsordner

* **Verfügbar auf:** Administrator-App und Autoren-App.
* **Migration:** wird unterstützt.
* **Job-API:** Nicht zutreffend. Es gibt heute keine dedizierte API-Oberfläche.

>[!NOTE]
>
>Benutzerdefinierte Rollenberechtigungen gelten nur auf der Stamm-/übergeordneten Ordnerebene, nicht für jeden Ordner in der Hierarchie.

### Agent für Einblicke

* **Verfügbar auf:** Administrator-App. Derzeit nur auf vollständige Administratoren beschränkt (keine benutzerdefinierten Rollen).
* **Admin-API:** Nicht verfügbar.
* **Job-API/Migration:** Nicht zutreffend.

### Lernpfad-Agent

* **Verfügbar für:** Natives Web und die Headless-API (Teilnehmer).
* **Noch nicht verfügbar in:** Native Mobile Web, Native Mobile App und AEM Widget.
* **Job-API/Migration:** Nicht zutreffend.

### AI Assistant (Teilnehmer)

* **Verfügbar für:** Natives Web, Headless-API (Teilnehmer) und Natives mobiles Web.
* **Noch nicht verfügbar für:** Native App und AEM Widget.
* **Job-API/Migration:** Nicht zutreffend.

>[!NOTE]
>
>Diese Funktion muss explizit aktiviert werden, bevor sie den Teilnehmern angezeigt wird.

### Live-Hub

* **Verfügbar für:** Native Web, Headless-API (Teilnehmer), Native Mobile Web und die Administrator-App.
* **Job-API:** Nicht zutreffend.
* **Migration:** Derzeit nicht unterstützt.

### Benutzerdefinierte Administratoren: Weitere benutzerdefinierte Rollen lesen/verwalten

* **Verfügbar auf:** Administrator-App. Ermöglicht es benutzerdefinierten Administratoren, andere benutzerdefinierte Administratorrollen anzuzeigen und zu verwalten.
* **Job-API/Migration:** Nicht zutreffend. Noch keine dedizierte API dafür.

### Leistungsübersicht

* **Verfügbar für:** Native Web, Headless-API (Teilnehmer), Native Mobile Web, Native Mobile App und die Administrator-App.
* **Noch nicht verfügbar auf:** AEM Widget.
* **Migration:** Derzeit nicht unterstützt.
* **Benachrichtigungen:**
  * Keine E-Mail-Benachrichtigungen.
  * Keine plattforminternen Benachrichtigungen.

### Kanäle

* **Verfügbar für:** Native Web und die Administrator-App. Derzeit in der Betaversion.
* **Noch nicht verfügbar für:** Headless-API (Teilnehmer), mobiles Web, mobile App, AEM Widget und Admin-API.
* **Job-API/Migration:** Nicht zutreffend.
