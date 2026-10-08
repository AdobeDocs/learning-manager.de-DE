---
description: Erfahren Sie, wie Sie eine JSON-Datei mit einem benutzerdefinierten Thema in den Inhaltssetzer importieren und wie Sie sie als ein neues benutzerdefiniertes Thema speichern, das in Ihrem Bedienfeld "Kursthemen" verfügbar ist.
jcr-language: en_us
title: Importieren eines Designs
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%
---

# Importieren eines Designs

Importieren Sie eine angepasste JSON-Datei, um Ihre Änderungen als neues Design in den Inhaltsauslöser zu übernehmen.

1. Wählen Sie **Designs** in der Symbolleiste aus.

2. Wählen Sie **Importieren** aus den **Optionen für das Kursdesign** aus.
   ![](../assets/48_course_themes_import_button_updated.png)

3. Wählen Sie die angepasste JSON-Datei auf Ihrem Computer aus.

4. Wählen Sie **Als neu speichern**, um ein neues benutzerdefiniertes Design zu erstellen.

## Design-JSON-Strukturübersicht

Eine thematische JSON-Datei umfasst fünf Hauptbereiche:

| Abschnitt | Steuerelemente |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Metadaten (ID, Name, Version, Beschreibung, Autor, Quelle, isDefault) | Designidentität und Anzeigeinformationen |
| foundation.palette | Die 7 Kernfarbtoken (Vordergrund, Hintergrund, Akzent, Hintergrund, subtil, sekundär, textPrimary, textInverse), auf die im gesamten Design über var(—tokenName) verwiesen wird |
| foundation.fonts | Stapel für Überschriften und Fließtext |
| foundation.Abstand und foundation.radius | Skalierung von horizontalem/vertikalem Abstand und Token für Eckenradius |
| Elemente | Typografie und strukturelle Formatierung für jede Textrolle (Lektion, Titel, Thema, Block, Überschrift, Unterüberschrift, Frage, Beschriftung, Absatz, Schaltfläche, Beschriftung) und jede Komponente (Absatz, Bild, Block, Video, Bild, Raster, Akkordeon, Karussell, FlipCard, Registerkarten, Zeitleiste, Bewertung) |

Da die meisten Werte mit var(—tokenName) auf Palettentoken verweisen, werden beim Aktualisieren eines einzelnen Tokens (z. B. accent) Änderungen automatisch auf alle Elemente übertragen, die darauf verweisen. Sie müssen nicht nach einzelnen Farbwerten suchen.

