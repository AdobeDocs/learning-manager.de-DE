---
description: Erfahren Sie, wie Sie eine benutzerdefinierte Design-JSON-Datei in den Inhaltskomposer importieren und sie als ein neues benutzerdefiniertes Design speichern, das in Ihrem Bedienfeld "Kursthemen" verfügbar ist.
jcr-language: en_us
title: Importieren eines Designs
source-git-commit: f8687710f5b73e8b7cf8d56057cac25483f38cdc
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# Importieren eines Designs

Importieren Sie eine benutzerdefinierte JSON-Datei, um Ihre Änderungen als neues Design in Content Composer anzuwenden.

1. Wählen Sie **Designs** in der Symbolleiste aus.

2. Wählen Sie **Importieren** aus den **Optionen für das Kursdesign** aus.
   ![](../assets/48_course_themes_import_button_updated.png)

3. Wählen Sie die benutzerdefinierte JSON-Datei auf Ihrem Computer aus.

4. Wählen Sie **Als neu speichern**, um ein neues benutzerdefiniertes Design zu erstellen.

## Design-JSON-Strukturübersicht

Eine Design-JSON-Datei umfasst fünf Hauptbereiche:

| Abschnitt | Steuerelemente |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Metadaten (ID, Name, Version, Beschreibung, Autor, Quelle, isDefault) | Designidentität und Anzeigeinformationen |
| foundation.palette | Die 7 Kernfarbtoken (Vordergrund, Hintergrund, Akzent, Hintergrund, subtil, sekundär, textPrimary, textInverse), auf die im gesamten Design über var(—tokenName) verwiesen wird |
| foundation.fonts | Überschriften- und Textkörperschriftstapel |
| foundation.spacing und foundation.radius | Skalierung von horizontalen/vertikalen Abständen und Token mit Eckenradius |
| Elemente | Typografie und strukturelle Formatierung für jede Textrolle (Lektion, Titel, Thema, Block, Überschrift, Unterüberschrift, Frage, Beschriftung, Absatz, Schaltfläche, Beschriftung) und jede Komponente (Absatz, Bild, Block, Video, Bild, Raster, Akkordeon, Karussell, FlipCard, Registerkarten, Zeitleiste, Bewertung) |

Da die meisten Werte mit var(—tokenName) auf Palettentoken verweisen, werden beim Aktualisieren eines einzelnen Tokens (z. B. accent) Änderungen automatisch auf alle Elemente übertragen, die darauf verweisen. Sie müssen nicht nach einzelnen Farbwerten suchen.

