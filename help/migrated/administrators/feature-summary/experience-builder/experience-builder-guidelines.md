---
title: Richtlinien und Einschränkungen von Experience Builder in Adobe Learning Manager
description: Richtlinien und Einschränkungen von Experience Builder bieten Teilnehmern, die KI-gestützte Algorithmen verwenden, personalisierte Kurs- und Inhaltsvorschläge.
jcr-language: en-us
source-git-commit: b3124c47d56a50437cb284fe809828bcd4c4008d
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 0%

---


# Richtlinien und Einschränkungen von Experience Builder

Experience Builder ist ein leistungsstarkes Tool, mit dem Benutzer mühelos dynamische und ansprechende Webseiten erstellen können. Um optimale Leistung, Benutzerfreundlichkeit und Sicherheit zu gewährleisten, ist es wichtig, bestimmte Richtlinien und Empfehlungen zu befolgen, wenn Sie Seiten konfigurieren, Widgets verwenden und Layouts anpassen. Dieses Dokument bietet einen detaillierten Überblick über wichtige Hinweise und Punkte, die Benutzer bei der Arbeit mit Experience Builder berücksichtigen sollten.

Die hier beschriebenen Informationen umfassen wichtige Aspekte wie Seiten- und Widget-Konfigurationen, Anpassungsoptionen, die Handhabung von benutzerdefiniertem Code und Sicherheitserwägungen. Durch die Einhaltung dieser Empfehlungen können Benutzer die Effizienz ihrer Experience Builder-Projekte maximieren, typische Fehler vermeiden und sich nahtlos an Aktualisierungen und Änderungen anpassen.

## Seiten- und Widget-Konfiguration

### Maximale Seitenanzahl

In Experience Builder können Sie bis zu 1000 Seiten erstellen. Dies ist die Obergrenze, es wird jedoch empfohlen, Seiten strategisch zu planen, um unnötige Komplexität zu vermeiden.

### Widgets pro Seite

* **Hartes Limit**: Einer einzelnen Seite können maximal 25 Widgets hinzugefügt werden.
* **Empfohlenes Limit**: Für eine bessere Leistung wird empfohlen, nicht mehr als 10 Widgets pro Seite zu verwenden.
* **API-basierte Widgets**: Widgets, die von ALM-APIs abhängig sind (z. B. Kurse und Pfade, Kategorie, Eigenes Lernen, Soziales Lernen, Kalender, Konformität, Leaderboard), sollten auf 10 pro Seite beschränkt sein.
* **Unabhängige Widgets**: Widgets wie HTML und Inhaltsfeld, die nicht auf ALM-APIs basieren, können bis zu der festen Grenze von 25 Widgets verwendet werden.

### Widgets für einmalige Verwendung

Bestimmte Widgets wie Kalender, Soziales Lernen, Konformität und Leaderboard sollten nur einmal pro Seite verwendet werden. Wenn Sie sie mehrmals verwenden, kann dies zu Leistungsproblemen führen, insbesondere bei Widgets wie dem Kalender, die erhebliche Ressourcen erfordern, um Sitzungen zu laden.

### Richtlinien für die Größe von Widgets

Widgets wie Kalender, Leaderboard, Social und Konformität sollten in Layouts mit einer Mindestbreite von einem Drittel der Seite platziert werden. Einzelkarten-Widgets sind für diese Breite am besten geeignet, um eine optimale Anzeige zu gewährleisten. Widgets wie Kalender und Konformität (erweiterte Ansicht) wurden für Layouts mit halber Breite entwickelt, um eine bessere Benutzererfahrung zu bieten. Bei anderen Layoutgrößen werden Widgets entsprechend dem verfügbaren Platz angepasst, um die Benutzerfreundlichkeit zu gewährleisten.

Die Verwendung von Widgets innerhalb dieser empfohlenen Größenrichtlinien verbessert die allgemeine Benutzerinteraktion.

## Anpassungsrichtlinien

### Standardpixelabstände

**Vertikaler Abstand**: Der standardmäßige vertikale Abstand zwischen Widgets beträgt 80 Pixel.
**Horizontaler Abstand**: Der standardmäßige horizontale Abstand zwischen Widgets beträgt 20 Pixel.

### Benutzerdefiniertes CSS

Benutzer können die Standardabstände und andere visuelle Eigenschaften mit benutzerdefiniertem CSS überschreiben.

Schritte zur Anpassung:

* Inspect der Seitenelemente zur Identifizierung von CSS-Klassen.
* Übernehmen Sie Änderungen auf globaler Ebene, Widget-Ebene oder Seitenebene.

Um beispielsweise den vertikalen Abstand zwischen Widgets zu reduzieren, ändern Sie die CSS-Eigenschaft für die entsprechende Klasse.

## Menüpositionierung

Menüs können oben oder links auf der Seite positioniert werden. Weitere Anpassungen können mit benutzerdefiniertem CSS vorgenommen werden.

## Funktionsspezifische Empfehlungen

### Social-Learning- und Gamification-Widgets

* Wenn diese Funktionen deaktiviert sind, müssen Administratoren die entsprechenden Widgets manuell von Seiten entfernen.
* Seiten sollten neu gestaltet werden, um sicherzustellen, dass sie nach der Deaktivierung dieser Funktionen funktionell und optisch intakt bleiben.

## Verarbeiten von benutzerdefiniertem Code

### Auswirkungen von Updates

* Bestehender benutzerdefinierter Code (HTML, CSS, JS), der in das Backend injiziert wurde, funktioniert nach Aktualisierungen von Experience Builder möglicherweise nicht wie erwartet.
* Benutzer müssen ihren Code umschreiben, um ihn an Änderungen der Benutzeroberfläche anzupassen, z. B. an aktualisierten Klassennamen.

### Frontend-Unterstützung

* Fügen Sie benutzerdefinierten Code mithilfe von HTML-Widgets oder CSS/JS-Blöcken auf Kontoebene direkt im Administratorportal hinzu.

### Haftungsausschluss

* Benutzerdefinierter Code funktioniert in zukünftigen Versionen möglicherweise nicht wie erwartet und erfordert Anpassungen. Sei darauf vorbereitet, ihren Code nach jeder Veröffentlichung zu aktualisieren.

## Allgemeine Empfehlungen

### Überlegungen zur Performance

* Vermeiden Sie das Überschreiten der empfohlenen Widget-Grenzwerte, um Leistungseinbußen zu vermeiden.
* Wenn Sie ressourcenintensive Widgets (z. B. einen Kalender) mehrmals auf einer Seite verwenden, kann sich dies erheblich auf die Ladezeiten der Seite auswirken.

### Sicherheitsüberlegungen

* **HTML-Widgets**: Sie müssen sicherstellen, dass der Code Sicherheitsprobleme wie XSS-Angriffe (Cross-Site Scripting) behandelt, da diese außerhalb des Gültigkeitsbereichs des Steuerelements von Experience Builder liegen.
* **Benutzerdefinierte Fußzeile**: Stellen Sie beim Anpassen der Fußzeile mithilfe von HTML oder CSS sicher, dass der Code den Best Practices für die Sicherheit entspricht.

### Umbruch von Änderungen

Aktualisierungen von Experience Builder können wichtige Änderungen bei Anpassungen mit sich bringen. Sie müssen:

* Passen Sie den Code an neue Benutzeroberflächenelemente an.
* Testen Sie die Anpassungen nach jedem Update.

## Weitere Hinweise

### Benutzerdefinierte CSS-Implementierung

* Sie können Seitenelemente auswerten, CSS-Klassen kopieren und die gewünschten Eigenschaften anwenden, um Layouts global, auf Widget- oder auf Seitenebene anzupassen.

### Widget-IDs und Seiten-IDs

Jedes Widget und jede Seite verfügen über eindeutige IDs, die für zielgerichtete CSS-Änderungen verwendet werden können. Dies ermöglicht Anpassungen auf verschiedenen Ebenen:

* Globale Ebene: Wenden Sie CSS-Änderungen auf alle Seiten an.
* Widget-Ebene: Wenden Sie CSS-Änderungen auf bestimmte Widgets an.
* Seitenebene: Wenden Sie CSS-Änderungen auf alle Widgets innerhalb einer bestimmten Seite an.










