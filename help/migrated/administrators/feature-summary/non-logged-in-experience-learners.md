---
title: Oberfläche für nicht angemeldete Teilnehmer
description: Das native Adobe Learning Manager-Portal unterstützt einen nicht protokollierten Zugriff auf die Schulungswebsite. Wenn dieser Modus aktiviert ist, können Teilnehmer die Schulungswebsite entdecken und darauf zugreifen und verschiedene verfügbare Kurse und Inhalte auschecken. Auf der Oberfläche ohne Anmeldung können Teilnehmer Kurse durchsuchen, ohne bei einem Portal angemeldet zu sein.
exl-id: 12260cca-d2d2-4e7c-991d-9b09690d4c0a
source-git-commit: 664b9c867fc767e11d4d91e3be9ae172e7e85035
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 39%

---

# Oberfläche für nicht angemeldete Teilnehmer

Das native Adobe Learning Manager-Portal unterstützt einen nicht protokollierten Zugriff auf die Schulungswebsite. Wenn dieser Modus aktiviert ist, können Teilnehmer die Schulungswebsite entdecken und darauf zugreifen und verschiedene verfügbare Kurse und Inhalte auschecken.

Auf der Oberfläche ohne Anmeldung können Teilnehmer Kurse durchsuchen, ohne bei einem Portal angemeldet zu sein.

Damit die Startseite ohne Anmeldung aktiviert wird, muss der Integrationsadministrator die Option [Schulungsdaten-Connector](/help/migrated/integration-admin/feature-summary/connectors.md#training-data-access) aktivieren und konfigurieren.

Die Schulung kann dann aus dem Connector exportiert werden.

>[!NOTE]
>
>Stellen Sie sicher, dass die Option Nativer Lern-Manager ausgewählt ist.

Der Administrator kann die Startseite ändern und konfigurieren, die für nicht angemeldete Benutzer vorgesehen ist.

## Teilnehmer-APIs

Adobe Learning Manager - Mit Teilnehmer-APIs können Sie ein benutzerdefiniertes Lernerlebnis für Ihre Benutzer erstellen. Die Verwendung dieser APIs erfordert ein gültiges Benutzertoken und darf nur für Arbeitsabläufe mit einem vollständig lizenzierten/registrierten Teilnehmer verwendet werden.

>[!IMPORTANT]
>
>Sie dürfen nicht, wie es der Fall ist, für irgendeine Art von Datenabruf verwendet werden, um nicht angemeldete Benutzer/freigegebene Benutzer oder andere solche Fälle zu unterstützen. Wenn Sie ein Headless- oder AEM-basiertes, nicht angemeldetes Erlebnis erstellen möchten, wenden Sie sich bitte an uns. Wir werden Ihnen den richtigen Ansatz auf der Grundlage Ihrer Anforderungen vorschlagen.

Die nicht angemeldeten Nutzungsszenarien erfordern eine besondere Behandlung.

**Wenden Sie sich an das Lösungsarchitekturteam, falls Sie Fragen zur geeigneten Verwendung dieser APIs haben, und vergewissern Sie sich, dass ein Lösungsarchitekt eine Lösung vor der Bereitstellung überprüft hat**.

## Starten der Optionen für die Startseite

Wählen Sie auf der Adobe Learning Manager-Homepage **Branding** aus. Wählen Sie dann im linken Bereich Nicht angemeldete Startseite aus.

![Homepage-Optionen](assets/non-logged-in-homepage.png)

*Wählen Sie die Option &quot;Nicht angemeldete Homepage&quot; aus*

## Hinzufügen eines Banners

Fügen Sie ein Banner hinzu, um Marketing-Ankündigungen anzuzeigen oder das Trendthema des Tages vorzustellen. Wählen Sie **Banner hinzufügen**.

![Banner](assets/add-banner-image.png)

*Banner hinzufügen*

Navigieren Sie zum Speicherort des Bildes, das als Banner verwendet werden soll. Geben Sie dann einen Link als Aktionsschaltfläche auf dem Bannerbild an.

## Kategorien hinzufügen

Diese Komponente kann verwendet werden, um den Katalog nach Tags, Kenntnissen und Katalog zu filtern. Dieser Abschnitt enthält einen Titel und eine Beschreibung für jede Kategorie. Durch Klicken wird der Benutzer zu der Katalogseite mit den angewendeten Filtern weitergeleitet.

Wählen Sie **[!UICONTROL Kategorie hinzufügen]**. Geben Sie dann die Details für die Kategorie ein.

![Kategorie hinzufügen](assets/add-category.png)

*Kategorien hinzufügen*

Speichern Sie die Kategorie. Die Kategorie wird dem Abschnitt hinzugefügt.

## Hinzufügen eines Katalogs

Fügen Sie einen Katalog für nicht angemeldete Benutzer hinzu, damit sie die gesamte Schulung auf der Plattform durchsuchen können.

![Katalog hinzufügen](assets/add-catalog.png)

*Katalog hinzufügen*

Alle exportierten Schulungen werden aufgeführt.

## Nicht unterstützte Funktionen

* Arbeitshilfen werden nicht exportiert. Die Teilnehmer können sie jedoch nach der Anmeldung sehen.
* Sortieren nach in der Katalogkomponente.
* Standardeinstellung für die Anzeige in der Admin-App (Einstellungen > Allgemein > Listenansicht)
* Sternebewertung/Wirksamkeit.
* Einstellungen für das Kartensymbol.
* Einstellungen für relevante Kenntnisse und Tags.
* Teilnehmer-App-Ansicht, die katalogweise angezeigt wird.
* Schulungsübersichtsseiten: Wenn ein Benutzer auf die Karte klickt, wird er zur Registrierung und anschließend zur Schulungsübersichtsseite/Instanzseite weitergeleitet.
* Alle aktivierten Kataloge werden angezeigt. Ein Teilnehmer, der keinen Zugriff auf einen Katalog besitzt, kann den Katalog und die darin enthaltene Schulung nach der Anmeldung nicht anzeigen.
* Bei der nativen Option werden Änderungen an einem Kurs oder Lernpfad nur nach 24 Stunden statt in Echtzeit widergespiegelt, während sie für das Premium-Angebot nach mindestens 3 Stunden widergespiegelt werden.
