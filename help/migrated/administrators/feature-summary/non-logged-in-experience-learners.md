---
title: Nicht angemeldete Benutzer für Teilnehmer
description: Das native Adobe Learning Manager-Portal unterstützt einen nicht protokollierten Zugriff auf die Schulungswebsite. Wenn dieser Modus aktiviert ist, können Teilnehmer die Schulungswebsite entdecken und darauf zugreifen und verschiedene verfügbare Kurse und Inhalte auschecken. Das nicht angemeldete Erlebnis ermöglicht es Teilnehmern, Kurse zu durchsuchen, ohne bei einem Portal angemeldet zu sein.
source-git-commit: aef2dfe9d6f49dcccaf1f71b57ffa25a3075efe8
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# Nicht angemeldete Benutzer für Teilnehmer

Das native Adobe Learning Manager-Portal unterstützt einen nicht protokollierten Zugriff auf die Schulungswebsite. Wenn dieser Modus aktiviert ist, können Teilnehmer die Schulungswebsite entdecken und darauf zugreifen und verschiedene verfügbare Kurse und Inhalte auschecken.

Das nicht angemeldete Erlebnis ermöglicht es Teilnehmern, Kurse zu durchsuchen, ohne bei einem Portal angemeldet zu sein.

Damit die nicht angemeldete Startseite aktiviert wird, muss der Integrationsadministrator die Option [Trainingsdaten-Connector](/help/migrated/integration-admin/feature-summary/connectors.md#training-data-access).

Die Schulung kann dann aus dem Connector exportiert werden.

>[!NOTE]
>
>Stellen Sie sicher, dass die Option Nativer Lern-Manager ausgewählt ist.

Der Administrator kann die Startseite ändern und konfigurieren, die für nicht angemeldete Benutzer vorgesehen ist.

## Starten der Optionen für die Startseite

Wählen Sie auf der Startseite des Adobe-Lern-Managers **Branding**. Wählen Sie dann im linken Bereich Nicht angemeldete Startseite aus.

![Startseitenoptionen](assets/non-logged-in-homepage.png)

*Wählen Sie die Option Nicht angemeldete Startseite aus.*

## Banner hinzufügen

Füge ein Banner für jede Marketing-Ankündigung oder das aktuelle Thema hinzu. Auswählen **Banner hinzufügen**.

![Spruchband](assets/add-banner-image.png)

*Banner hinzufügen*

Navigieren Sie zum Speicherort des Bildes, das als Banner verwendet werden soll. Geben Sie dann einen Link als Aktionsschaltfläche auf dem Bannerbild an.

## Kategorien hinzufügen

Diese Komponente kann verwendet werden, um den Katalog nach Tags, Kenntnissen und Katalog zu filtern. Dieser Abschnitt enthält eine Kopfzeile und eine Beschreibung für jede Kategorie. Wenn der Benutzer auf die Schaltfläche klickt, wird er zur Katalogseite mit den angewendeten Filtern weitergeleitet.

Auswählen **[!UICONTROL Kategorie hinzufügen]**. Geben Sie dann die Details für die Kategorie ein.

![Kategorie hinzufügen](assets/add-category.png)

*Kategorien hinzufügen.*

Speichern Sie die Kategorie. Die Kategorie wird dem Abschnitt hinzugefügt.

## Katalog hinzufügen

Fügen Sie einen Katalog für nicht angemeldete Benutzer hinzu, damit sie die gesamte Schulung auf der Plattform durchsuchen können.

![Katalog hinzufügen](assets/add-catalog.png)

*Katalog hinzufügen*

Alle exportierten Schulungen sind vorhanden.

## Nicht unterstützte Funktionen

* Arbeitshilfen werden nicht exportiert. Die Teilnehmer können sie jedoch nach der Anmeldung sehen.
* Sortieren nach in der Katalogkomponente.
* Standardeinstellung für die Anzeige in der Admin-App (Einstellungen > Allgemein > Listenansicht)
* Sternebewertung/Wirksamkeit.
* Einstellungen für das Kartensymbol.
* Relevante Einstellung der Kenntnisse und Tags.
* Teilnehmer-App-Ansicht, die katalogweise angezeigt wird.
* Schulungsübersichtsseiten - Wenn Sie auf die Karte klicken, werden Sie zur Anmeldung weitergeleitet, woraufhin ein Benutzer zur Schulungsübersichtsseite/Instanzseite weitergeleitet wird.
* Alle aktivierten Kataloge werden angezeigt. Jeder Teilnehmer, der keinen Zugriff auf einen Katalog hat, kann den Katalog und die Schulung nicht sehen, nachdem er sich angemeldet hat.
