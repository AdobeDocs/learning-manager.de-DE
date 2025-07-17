---
title: Künftige Änderungen in Adobe Learning Manager
description: Hier erfahren Sie mehr über die neuen Funktionen, Verbesserungen und wichtigen Updates, die in Kürze in Adobe Learning Manager verfügbar sind. Informiert euch über neue Entwicklungen, damit ihr vorausplanen und die neuesten Verbesserungen optimal nutzen könnt.
exl-id: 4d2129c4-42d8-446f-8837-879b5c2f42bf
source-git-commit: ffb4883227f1e461df5fc4a025fef1ba1b8568c2
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 2%

---

# Künftige Änderungen in Adobe Learning Manager

Wir freuen uns, einige wichtige Neuerungen in Adobe Learning Manager mit den kommenden Versionen zu teilen. Diese Verbesserungen zielen auf die Optimierung von Administrator-Workflows, die Verbesserung der Genauigkeit von Datenberichten und die Stärkung rollenbasierter Kontrollen ab.

Diese Änderungen dienen dazu, den manuellen Aufwand zu reduzieren, die Automatisierung zu unterstützen und die Governance bei Schulungen zu verbessern.

## Abschlüsse mit Kursleiter im Teilnehmertranskript erfassen

### Zielgruppe

Administrator- und Automatisierungseigentümer

### Überblick

Wenn in Adobe Learning Manager inkrementelle Teilnehmertranskripte (LT) für Automatisierungs-Workflows verwendet werden, werden Abschlüsse, die mit einem Kursleiter nach dem Sitzungsdatum abgeschlossen wurden, nicht erfasst. Der Zeitstempel für den Abschluss gibt die ursprüngliche Sitzungsendzeit an (nicht die Zeit, zu der der Kursleiter den Abschluss markiert hat). Da diese Aktualisierungen außerhalb des eintägigen Änderungsfensters liegen, das für die inkrementelle LT-Generierung verwendet wird, werden die Anwesenheits- und Abschlussdaten der Teilnehmer aus den Berichten ausgeschlossen, was zu ungenauen oder unvollständigen Downstream-Berichten und potenziellen Compliance-Lücken führt.

### Was hat sich verändert

Teilnehmertranskriptberichte (LT) enthalten Abschlüsse, die von Kursleitern nach dem Sitzungsdatum markiert wurden. Dadurch wird sichergestellt, dass jede verzögerte Anwesenheitsmarkierung im Transkriptexport korrekt widergespiegelt wird.

Anwesenheitsstatus wie &quot;Mit Bestehen/Nicht Bestehen teilgenommen&quot; werden automatisch in inkrementellen LT-Exporten angezeigt.

### Neue Funktionen

* Neue Spalte: Abgeschlossenes Datum markieren (UTC-Zeitzone).
* &quot;Abschlussquelle&quot; ist auf Modulebene verfügbar.
* Kompatibel mit Connector-basierten oder Job API-generierten LT-Berichten.

![](assets/capture-instructor.png)

**Aktion erforderlich**

* Wenn die Automatisierung von der Spaltenposition abhängt, stellen Sie sicher, dass für die neue Spalte logische Konten vorhanden sind.
* Bei Verwendung von Spaltennamen sind keine Änderungen erforderlich.
* Nachgerüstete Vervollständigungen (manuelle Einfuhr) sind nicht enthalten.

## Links im Bericht zu Arbeitshilfen herunterladen

### Zielgruppe

Administrator, benutzerdefinierter Administrator und Eigentümer von Automatisierung

### Überblick

Der Bericht zu Arbeitshilfen enthält einen direkten Download-Link für jede Arbeitshilfe, sodass Sie schnell vom Bericht selbst aus darauf zugreifen können.

### Neue Funktionen

Der dritten Position im Bericht wurde eine neue Spalte hinzugefügt: **[!UICONTROL Arbeitshilfeverknüpfung]**. Es ist direkt mit der Arbeitshilfe verknüpft, wenn es sich um eine Datei handelt oder die vom Autor bereitgestellte externe URL angezeigt wird.

Benutzer mit Zugriff (Admin/Autoren und benutzerdefinierte Rollen) können die Arbeitshilfe über diesen Link herunterladen.

![](assets/download-links-for-job-aid.png)

### Wichtig

* Überprüfen automatisierter Workflows mit Arbeitshilfeberichten (mit der Jobs-API).
* Wenn das Skript auf der Spaltenposition basiert, aktualisieren Sie die Skripte entsprechend.
* Bei Verwendung von Spaltennamen ist keine Aktion erforderlich.

## Spalten &quot;Interne Benutzer-ID&quot; und &quot;Manager-E-Mail&quot; zum Benutzerbericht hinzugefügt

### Zielgruppe

Administratoren (und benutzerdefinierte Administratoren), die den **[!UICONTROL Benutzerbericht]** (**[!UICONTROL Admin]** > **[!UICONTROL Benutzer]** > **[!UICONTROL Intern]** > **[!UICONTROL Benutzerdaten exportieren]**) verwenden, die von der Administrator-Benutzeroberfläche heruntergeladen wurden.

### Überblick

Zur Unterstützung der Workflows für die Benutzeridentifizierung und -integration wurden dem Benutzerbericht zwei Spalten hinzugefügt: **[!UICONTROL Interne Benutzer-ID]** und **[!UICONTROL Manager-E-Mail]**, die über die Benutzeroberfläche exportiert wurden.

### Neue Funktionen

Der Benutzerbericht enthält die interne Benutzer-ID eines Benutzers und die E-Mail-Adresse des Managers, um sie den verschiedenen Tools oder API-Endpunkten eindeutig zuzuordnen.

### Wichtig

* Wenn Sie diesen Bericht in automatisierten Flows verwenden, sollte diese neu hinzugefügte Spalte in der Automatisierung berücksichtigt werden.
* Wenn Workflows nicht betroffen sind, sind keine Änderungen erforderlich.

## Berechtigungen für Ankündigungsbereiche für benutzerdefinierte Administratoren

### Zielgruppe

Benutzerdefinierte Administratoren

### Überblick

Benutzerdefinierte Administratoren können Ankündigungen nur für die Benutzergruppen oder Kataloge innerhalb ihres definierten Bereichs erstellen.

### Neue Funktionen

* Mit Bereichsregeln können benutzerdefinierte Administratoren Ankündigungen nur für bestimmte Benutzergruppen oder Kataloge erstellen.
* Beim Definieren einer benutzerdefinierten Rolle können Administratoren Ankündigungsberechtigungen mit dem Umfang für Benutzergruppen oder Kataloge zuweisen.
* Benutzerdefinierte Administratoren sind auf das Erstellen von Ankündigungen innerhalb ihres angegebenen Bereichs beschränkt.
* Der Benachrichtigungsankündigungsbericht für benutzerdefinierte Administratoren zeigt Teilnehmer nur innerhalb ihres zugewiesenen Bereichs an.

### Wichtig

* Das Format des Berichts bleibt unverändert. Wenn benutzerdefinierte Administratoren ihn von der Benutzeroberfläche herunterladen, unterliegt der Inhalt des Berichts ihrem Umfang.
* Es sind keine Änderungen erforderlich, wenn dieser Bericht nicht in einem automatisierten oder nachgelagerten Arbeitsablauf verwendet wird.

Eine kumulative Liste der neuen Funktionen und Änderungen an Adobe Learning Manager finden Sie im Artikel [Versionshinweise](https://experienceleague.adobe.com/de/docs/learning-manager/using/introduction/release-notes).
