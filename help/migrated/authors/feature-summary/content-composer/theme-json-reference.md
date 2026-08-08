---
description: Eine vollständige Referenz für jede Eigenschaft im Content Composer-Design-JSON-Schema, einschließlich Paletten-Tokens, Schriften-Stacks, Radius- und Abstands-Tokens, Textrollenwerten, Komponenteneigenschaften und Bewertungsstilen.
jcr-language: en_us
title: Adobe Learning Manager Content Composer-Designreferenz für JSON-Eigenschaften
source-git-commit: ea6d296fa99686136ab08d756a20570a4681d704
workflow-type: tm+mt
source-wordcount: '1899'
ht-degree: 5%

---


# Adobe Learning Manager Content Composer-Designreferenz für JSON-Eigenschaften

Eine vollständige Referenz für jede Eigenschaft in einer Content Composer-Design-JSON-Datei mit Beschreibungen und Beispielwerten.

Felder der obersten Ebene, die das Design identifizieren und beschreiben.

## **Metadaten**

| **Eigenschaft** | **Typ** | **Beschreibung** | **Versatzwert** |
|--------------|----------|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| id | Zeichenfolge | Eindeutiger Designbezeichner. Kleinschreibung, nur Bindestriche, keine Leerzeichen oder Sonderzeichen. Wird intern verwendet, um auf das Design zu verweisen. | &quot;Schiefer&quot; |
| name | Zeichenfolge | Der im Bedienfeld &quot;Kursthemen&quot; angezeigte Anzeigename. | &quot;Schiefer&quot; |
| Version | Zeichenfolge | Semantische Versionsnummer. Verwenden Sie &quot;1.0.0&quot; für neue Designs. | &quot;1.0.0&quot; |
| Beschreibung | Zeichenfolge | Kurze Beschreibung des visuellen Charakters des Themas. | &quot;Ein warmes, authentisches Thema mit cremefarbenem Hintergrund, roten Adobe-Akzenten und dem Roboto Slab + Roboto-Typensystem&quot; |
| Autorin | Zeichenfolge | Name des Designerstellers oder des Teams. | &quot;Content Composer&quot; |
| Quelle | Zeichenfolge | Ursprung des Designs. &quot;Versendet&quot; für integrierte Designs. &quot;custom&quot; für von Benutzern erstellte Designs. | &quot;custom&quot; |
| isDefault | boolesch | Ob dieses Design automatisch auf neue Kurse angewendet wird. In den meisten Fällen auf &quot;false&quot; festgelegt. | falsch |

## **foundation.palette**

Die sieben Kernfarbtoken, die die Farbgrundlage des Themas bilden. Alle Elementwerte verweisen mithilfe von var(—tokenName) und nicht mithilfe hartkodierter Hexadezimalwerte auf diese Token.

| **Eigenschaft** | **Typ** | **Beschreibung** | **Versatzwert** |
|------------------|------------|---------------------------------------------------------------------------------------------------------------------------|-----------------|
| Vordergrund | Hexadezimalfarbe | Primäre Vordergrundfarbe für Text, Symbole und Benutzeroberflächenelemente, die auf dem Hintergrund platziert werden. | #1A1A1A |
| Hintergrund | Hexadezimalfarbe | Arbeitsfläche des Hauptkurses und Hintergrundfarbe der Folie. | #FAF7F2 |
| Betonung | Hexadezimalfarbe | Markenakzentfarbe für Schaltflächen, ausgewählte Status, Fortschrittsanzeigen, Unterrichtsüberschriften und interaktive Hervorhebungen. | #E8001C |
| backgroundSubtle | Hexadezimalfarbe | Sekundäre Hintergrundfarbe für Karten, Fenster, Navigation und Komponentenfüllungen. | #F0EBE1 |
| sekundär | Hexadezimalfarbe | Farbe von Begrenzungslinien, Trennlinien und inaktiven Benutzeroberflächenelementen. | #D9D3C9 |
| textPrimary | Hexadezimalfarbe | Primäre Textfarbe für alle Überschriften und Textkörper. | #1A1A1A |
| textInverse | Hexadezimalfarbe | Textfarbe für Inhalte, die auf dunklen oder akzentfarbenen Hintergründen platziert werden, wie z. B. Schaltflächenbeschriftungen auf der Akzentfarbe. | #FFFFFF |

## **foundation.fonts**

Zwei Schriftstapel, die über alle Textrollen in dem Design angewendet werden. Verweisen Sie mit var(—font-heading) oder var(—font-body) auf Elementwerte.

| **Eigenschaft** | **Typ** | **Beschreibung** | **Versatzwert** |
|--------------|-------------------|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| Rubrik | Zeichenkette für Schriftarten | Schriftfamilie für Unterrichtstitel, Thementitel und Anzeigeüberschriften. Schließen Sie websichere Fallbacks ein. | &quot;Roboto Slab, Georgia, &#39;Times New Roman&#39;, Serif&quot; |
| body | Zeichenkette für Schriftarten | Schriftfamilie für Absatztext, Beschriftungen, Quizfragen und UI-Beschriftungen. Schließen Sie websichere Fallbacks ein. | &quot;Roboto, -apple-system, BlinkMacSystemFont, &#39;Segoe UI&#39;, sans-serif&quot; |

## **foundation.spacing**

Als Grundlinie verwendete Token für horizontale und vertikale Abstände. Komponenten werden mithilfe der Multiplikatoren horizontalSpacingScale und vertikalSpacingScale skaliert.

| **Pfad** | **Typ** | **Beschreibung** | **Versatzwert** |
|---------------|----------|-------------------------------------|-----------------|
| horizontal.xs | px-Wert | Kleinste horizontale Abstandseinheit | 4px |
| horizontal.s | px-Wert | Kleine horizontale Abstandseinheit | 8px |
| horizontal.m | px-Wert | Mittlere horizontale Abstandseinheit | 12px |
| horizontal.l | px-Wert | Große horizontale Abstandseinheit | 16px |
| horizontal.xl | px-Wert | Extra große horizontale Abstandseinheit | 24px |
| vertical.xs | px-Wert | Kleinste vertikale Abstandseinheit | 4px |
| vertical.s | px-Wert | Kleine vertikale Abstandseinheit | 8px |
| vertical.m | px-Wert | Mittlere vertikale Abstandseinheit | 16px |
| vertical.l | px-Wert | Große vertikale Abstandseinheit | 24px |
| vertical.xl | px-Wert | Extra große vertikale Abstandseinheit | 32px |

## **foundation.radius**

Randradiustoken, die die Eckenrundung für Komponenten und Karten steuern.

| **Eigenschaft** | **Typ** | **Beschreibung** | **Versatzwert** |
|--------------|----------|---------------------------------------------------------|-----------------|
| Keine | px-Wert | Keine Rundung - scharfe Ecken. Immer 0px. | 0px |
| s | px-Wert | Kleiner Radius für subtile Eckenabrundungen. | 4px |
| m | px-Wert | Mittlerer Radius für Standardkarten- und Bauteilrundungen. | 8px |
| l | px-Wert | Großer Radius für markante Rundungen. | 16px |
| voll | px-Wert | Volle Pille oder Kreisform. Immer 9999px. | 9999px |

## **foundation.logo**

| **Eigenschaft** | **Typ** | **Beschreibung** | **Versatzwert** |
|--------------|----------------|----------------------------------------------------------------------------------------------|-----------------|
| Logo | Zeichenfolge oder Null | URL oder Dateipfad für das Logobild, das in der Kopfzeile des Kurses angezeigt wird. Für kein Logo auf null setzen. | null |

## **elements.text**

Typografieeigenschaften für jede benannte Textrolle im Kurs. Alle Rollen haben dieselbe Gruppe von Eigenschaften.

### **Textrollen**

| **Rolle** | **Angewendet auf** |
|--------------|------------------------------------------------------------------------------|
| lessonTitle | Haupttitel auf der Folie zum Öffnen einer Lektion |
| topicTitle | Überschrift am Anfang jeder Themenfolie |
| blockHeading | Überschriften in Inhaltskomponenten wie Akkordeonkopfzeilen und Kartentitel |
| Unterposition | Sekundäre Überschriften innerhalb einer Themenfolie |
| Frage | Fragentext zu Quiz- und Wissensüberprüfung |
| Bildtitel | Untertitel unter Bildern und Medienblöcken |
| Absatz | Textkörper in Inhaltsfolien |
| buttonLabel | Text auf Schaltflächen und Call-to-Action-Elementen |

### **Freigegebene Texteigenschaften**

Die folgenden Eigenschaften gelten für jede oben aufgeführte Textrolle.

| **Eigenschaft** | **Typ** | **Akzeptierte Werte** | **Beschreibung** |
|--------------------|-----------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| fontFamily | CSS var oder font stack | var(—font-heading), var(—font-body) oder eine vollständige Zeichenfolge für den Schriftenstapel | Schriftfamilie für diese Textrolle. |
| fontSize | px-Wert | Beliebiger Pixelwert | Schriftgröße: |
| fontWeight | Zeichenfolge | Nur &quot;fett&quot; oder &quot;normal&quot;: Numerische Werte werden nicht unterstützt. | Schriftstärke. |
| fontStyle | Zeichenfolge | &quot;normal&quot; oder &quot;kursiv&quot; | Schriftschnitt. |
| Farbe | CSS var oder hex | Beliebiges Paletten-Token über var(—tokenName) oder einen direkten Hexadezimalwert | Textfarbe: |
| textAlign | Zeichenfolge | &quot;left&quot;, &quot;center&quot; oder &quot;right&quot; | Horizontale Textausrichtung. |
| letterSpacing | Zeichenfolge | &quot;normal&quot;, einen px-Wert oder einen em-Wert | Abstand zwischen Zeichen. |
| lineHeight | Zeichenfolge | Ein prozentualer oder einheitlicher Wert | Line-Height. |
| textDecoration | Zeichenfolge | &quot;none&quot;, &quot;underline&quot; oder &quot;line-through&quot; | Textdekoration |
| textTransform | Zeichenfolge | &quot;none&quot;, &quot;uppercase&quot;, &quot;lowercase&quot; oder &quot;capitalize&quot; | Groß-/Kleinschreibung in Text. |
| paddingInlineStart | px-Wert | Beliebiger Pixelwert | Auf den Textblock angewendeter linker Abstand. |
| paragraphSpacing | px-Wert | Beliebiger Pixelwert | Unter jedem Absatz innerhalb des Textblocks wird ein Leerzeichen eingefügt. |

### **Werte für Textrolle - Design erstellen**

| **Rolle** | **fontFamily** | **fontSize** | **fontWeight** | **fontStyle** | **color** | **textAlign** | **letterSpacing** | **lineHeight** | **textTransform** |
|--------------|---------------------|--------------|----------------|---------------|--------------------|---------------|-------------------|----------------|-------------------|
| lessonTitle | var(—font-heading) | 48px | kühn | normal | var(—textPrimary) | Mittelpunkt | -0,01em | 130% | Keine |
| topicTitle | var(—font-heading) | 40px | normal | normal | var(—textPrimary) | linken | 0 | 135% | Keine |
| blockHeading | var(—font-heading) | 24px | kühn | normal | var(—textPrimary) | linken | 0 | 140% | Keine |
| Unterposition | var(—font-body) | 20px | kühn | normal | var(—textPrimary) | linken | 0,01em | 150% | Keine |
| Frage | var(—font-heading) | 24px | normal | normal | var(—textPrimary) | linken | 0 | 150% | Keine |
| Bildtitel | var(—font-body) | 13px | normal | normal | var(—textPrimary) | linken | 0,02em | 170% | Keine |
| Absatz | var(—font-body) | 16px | normal | normal | var(—textPrimary) | linken | 0,01em | 190% | Keine |
| buttonLabel | var(—font-body) | 14px | kühn | normal | var(—textInverse) | Mittelpunkt | 0,06em | 125% | Großbuchstabe |

## **Elemente - Strukturoberflächen**

Eigenschaften, die den Hintergrund und den Rahmen der festen Layout-Oberflächen des Kurses steuern.

| **Element** | **Eigenschaft** | **Typ** | **Beschreibung** | **Versatzwert** |
|--------------|--------------|-------------------|---------------------------------------------------|----------------------------|
| Leinwand | Hintergrund | CSS-Variable | Hintergrundfarbe der Arbeitsfläche des Hauptkurses | var(—background) |
| Kopfzeile | Hintergrund | CSS-Variable | Hintergrundfarbe der Kurskopfzeile | var(—background) |
| Kopfzeile | Einfassung | CSS-Rahmenzeichenfolge | Unterer Rand der Kopfzeile des Kurses | 1px solid var(—secondary) |
| Fußzeile | Hintergrund | CSS-Variable | Hintergrundfarbe der Fußzeilenleiste für Kurse | var(—background) |
| Fußzeile | Einfassung | CSS-Rahmenzeichenfolge | Oberer Rand der Fußzeilenleiste des Kurses | 1px solid var(—secondary) |
| lessonHeader | Hintergrund | CSS-Variable | Hintergrundfarbe des Kopfzeilenbereichs des Unterrichtstitels | var(—accent) |
| Thema | Hintergrund | CSS-Variable | Hintergrundfarbe jeder Themenfolie | var(—background) |
| Thema | Einfassung | CSS-Rahmenzeichenfolge | Rahmen um den Themenfoliencontainer | 1px solid var(—secondary) |
| Navigation | Hintergrund | CSS-Variable | Hintergrundfarbe des Lektionsnavigationsbereichs | var(—backgroundSubtle) |
| Navigation | Einfassung | CSS-Rahmenzeichenfolge | Rahmen im Lektionsnavigationsbereich | 1px solid var(—secondary) |
| Knopf | Hintergrund | CSS-Variable | Hintergrundfarbe der Schaltflächen für primäre Aktionen | var(—accent) |
| Seitenumbruch | Hintergrund | CSS-Variable | Hintergrundfarbe des Paginierungssteuerelements | var(—backgroundSubtle) |

## **Elemente - freigegebene Komponenteneigenschaften**

Diese Eigenschaften werden für alle Inhaltsblockkomponenten angezeigt: paragraphBlock, videoBlock, imageGrid, accordion, carousel, flipCard und timeline.

| **Eigenschaft** | **Typ** | **Beschreibung** |
|------------------------|-------------------|---------------------------------------------------------------------------------------------------|
| Hintergrund | CSS var oder color | Äußerer Hintergrund des Komponentenblocks. Typisch &quot;transparent&quot;. |
| cardBackgroundColor | CSS var oder color | Hintergrundfüllung einzelner Karten innerhalb der Komponente. |
| cardBorder | CSS-Rahmenzeichenfolge | Auf jede Karte angewendeter Rahmen. Vollständige CSS-Kurzschrift, z. B. &quot;1px solid var(—secondary)&quot;. |
| cardShadowOffset | Zeichenfolge | X- und Y-Versatz des Kartenschattens, zum Beispiel &quot;0px 2px 6px&quot;. |
| cardShadowColor | CSS var oder color | Farbe des Kartenschattens. |
| cardShadowOpacity | Prozentzeichenfolge | Deckkraft des Kartenschattens. Setzen Sie den Wert auf &quot;0 %&quot;, um den Schatten zu entfernen. |
| horizontalSpacingScale | Ziffernfolge | Auf horizontale Abstandstoken angewendeter Multiplikator für diese Komponente. Bei &quot;1&quot; wird der Standardabstand verwendet. |
| verticalSpacingScale | Ziffernfolge | Auf Token für vertikale Abstände angewendeter Multiplikator für diese Komponente. Bei &quot;1&quot; wird der Standardabstand verwendet. |
| radiusScale | Ziffernfolge | Der auf die Radius-Token für diese Komponente angewendete Multiplikator. Bei &quot;1&quot; wird der Standardradius verwendet. |
| nestedAccentColor | CSS var oder color | Akzentfarbe für verschachtelte Elemente innerhalb der Komponente. Gilt nur für paragraphBlock. |

### **Werte für freigegebene Komponenten - Design verschieben**

| **Komponente** | **cardBackgroundColor** | **cardBorder** | **cardShadowOpacity** |
|----------------|-----------------------------|----------------------------|---------------------------|
| paragraphBlock | var(—backgroundSubtle) | 1px solid var(—secondary) | 8% |
| videoBlock | var(—backgroundSubtle) | 1px solid var(—secondary) | 8% |
| imageGrid | var(—backgroundSubtle) | 1px solid var(—accent) | 8% |
| Akkordeon | var(—backgroundSubtle) | 1px solid var(—secondary) | 8% |
| Karussell | var(—backgroundSubtle) | 1px solid var(—secondary) | 8% |
| flipCard | var(—backgroundSubtle) | 1px solid var(—secondary) | 8% |
| Timeline | var(—backgroundSubtle) | 1px solid var(—secondary) | 8% |

## **Elemente - komponentenspezifische Eigenschaften**

Eigenschaften, die für einzelne Komponententypen spezifisch sind.

| **Komponente** | **Eigenschaft** | **Typ** | **Beschreibung** | **Versatzwert** |
|----------------|--------------------------|----------|------------------------------------------------------------------|-------------------------|
| paragraphBlock | nestedAccentColor | CSS-Variable | Akzentfarbe für verschachtelte Elemente innerhalb des Absatzblocks | var(—accent) |
| flipCard | cardFrontBackgroundColor | CSS-Variable | Hintergrundfarbe der Vorderseite der Flipkarte | var(—backgroundSubtle) |
| flipCard | cardBackBackgroundColor | CSS-Variable | Hintergrundfarbe der Rückseite der Flipkarte - die Einblendfarbe | var(—accent) |
| flipCard | arrowColor | CSS-Variable | Farbe des Pfeilsymbols für die Spiegelung | var(—textInverse) |
| Tabulatoren | activeBg | CSS-Variable | Hintergrundfarbe der aktuell ausgewählten Registerkarte | var(—accent) |
| Tabulatoren | inactiveBg | CSS-Variable | Hintergrundfarbe nicht ausgewählter Registerkarten | var(—backgroundSubtle) |
| Tabulatoren | containerBg | CSS-Variable | Hintergrundfarbe des Containers für die Registerkartenleiste | var(—backgroundSubtle) |
| Timeline | trackColor | CSS-Variable | Farbe der Verbindungslinie zwischen Zeitleistenknoten | var(—secondary) |
| Timeline | progressCompletedBg | CSS-Variable | Füllfarbe abgeschlossener Zeitleisten-Fortschrittsmarkierungen | var(—accent) |
| Timeline | progressCurrentBorder | CSS-Variable | Rahmenfarbe der aktuellen Zeitleisten-Fortschrittsmarke | var(—accent) |
| Timeline | progressUnachedBg | CSS-Variable | Füllfarbe der Zeitleistenmarken noch nicht erreicht | var(—secondary) |
| Timeline | progressUnachedBorder | CSS-Variable | Rahmenfarbe der Zeitleistenmarken noch nicht erreicht | var(—backgroundSubtle) |

## **elements.assessment**

Eigenschaften für Quiz- und Wissensüberprüfungskomponenten.

| **Eigenschaft** | **Typ** | **Beschreibung** | **Versatzwert** |
|----------------------------|----------------|------------------------------------------------------------------------------|-------------------------|
| Hintergrund | CSS-Variable | Äußerer Hintergrund des Bewertungsblocks | durchsichtig |
| optionTextColor | CSS-Variable | Textfarbe der Beschriftungen der Antwortoptionen | var(—textPrimary) |
| optionIndicatorColor | CSS-Variable | Farbe des Optionsfelds oder des Kontrollkästchenindikators | var(—accent) |
| optionSelectedColor | CSS-Variable | Auf den Indikator der ausgewählten Option angewendete Farbe | var(—accent) |
| optionCheckmarkColor | CSS-Variable | Farbe des Häkchensymbols bei einer ausgewählten Option | var(—textInverse) |
| optionBackgroundColor | CSS-Variable | Hintergrundfarbe jeder Antwortoption | var(—background) |
| optionHoverBackgroundColor | CSS-Variable | Hintergrundfarbe einer Antwortoption beim Bewegen des Mauszeigers | var(—backgroundSubtle) |
| buttonBackgroundColor | CSS-Variable | Hintergrundfarbe der Schaltfläche &quot;Antwort senden&quot; oder &quot;Antwort prüfen&quot; | var(—accent) |
| buttonTextColor | CSS-Variable | Textfarbe der Beschriftung der Schaltfläche &quot;Senden&quot; oder &quot;Antwort prüfen&quot; | var(—textInverse) |
| buttonHoverBackgroundColor | CSS-Variable | Hintergrundfarbe der Schaltfläche beim Hovern | var(—accent) |
| feedbackCorrectColor | Hexadezimalfarbe | Hintergrundfarbe des richtigen Bedienfelds für das Antwortfeedback | #D7F7E1 |
| feedbackIncorrectColor | Hexadezimalfarbe | Hintergrundfarbe des Bereichs für falsches Antwortfeedback | #FFEBE8 |
| feedbackTextColor | Hexadezimalfarbe | Textfarbe im Feedbackfenster | #111111 |
| optionBorderCorrectColor | Hexadezimalfarbe | Rahmenfarbe für die richtige Antwortoption, nachdem die Antwort angezeigt wurde | #079355 |
| optionBorderIncorrectColor | Hexadezimalfarbe | Rahmenfarbe einer falsch ausgewählten Option, nachdem die Antwort angezeigt wurde | #D73220 |
| horizontalSpacingScale | Ziffernfolge | Multiplikator für horizontalen Abstand innerhalb der Bewertungskomponente | &quot;1&quot; |
| verticalSpacingScale | Ziffernfolge | Multiplikator für den vertikalen Abstand innerhalb der Bewertungskomponente | &quot;1&quot; |
| radiusScale | Ziffernfolge | Multiplikator für den Rahmenradius innerhalb der Bewertungskomponente | &quot;1&quot; |

## **Palettentoken var() reference**

Verwenden Sie diese var()-Ausdrücke in Elementwerten, um Paletten-Token zu referenzieren. Durch das Aktualisieren eines Paletten-Tokens werden automatisch alle Elemente aktualisiert, die es verwenden.

| **Ausdruck** | **Verweise** |
|-------------------------|-------------------------------------|
| var(—vordergrund) | foundation.palette.vordergrund |
| var(—background) | foundation.palette.background |
| var(—accent) | foundation.palette.accent |
| var(—backgroundSubtle) | foundation.palette.backgroundSubtle |
| var(—secondary) | foundation.palette.secondary |
| var(—textPrimary) | foundation.palette.textPrimary |
| var(—textInverse) | foundation.palette.textInverse |
| var(—font-heading) | foundation.fonts.heading |
| var(—font-body) | foundation.fonts.body |

## Beispiel für ein Design-JSON

```
{
  "id": "slate",
  "name": "Slate",
  "version": "1.0.0",
  "description": "A warm, authoritative theme with cream background, Adobe red accents, and the Roboto Slab + Roboto type system",
  "author": "Content Composer",
  "source": "custom",
  "isDefault": false,
  "foundation": {
    "palette": {
      "foreground": "#1A1A1A",
      "background": "#FAF7F2",
      "accent": "#E8001C",
      "backgroundSubtle": "#F0EBE1",
      "secondary": "#D9D3C9",
      "textPrimary": "#1A1A1A",
      "textInverse": "#FFFFFF"
    },
    "fonts": {
      "heading": "Roboto Slab, Georgia, 'Times New Roman', serif",
      "body": "Roboto, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    },
    "spacing": {
      "horizontal": {
        "xs": "4px",
        "s": "8px",
        "m": "12px",
        "l": "16px",
        "xl": "24px"
      },
      "vertical": {
        "xs": "4px",
        "s": "8px",
        "m": "16px",
        "l": "24px",
        "xl": "32px"
      }
    },
    "radius": {
      "none": "0px",
      "s": "4px",
      "m": "8px",
      "l": "16px",
      "full": "9999px"
    },
    "logo": null
  },
  "elements": {
    "text": {
      "lessonTitle": {
        "fontFamily": "var(--font-heading)",
        "fontSize": "48px",
        "fontWeight": "bold",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "center",
        "letterSpacing": "-0.01em",
        "lineHeight": "130%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "topicTitle": {
        "fontFamily": "var(--font-heading)",
        "fontSize": "40px",
        "fontWeight": "normal",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0",
        "lineHeight": "135%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "blockHeading": {
        "fontFamily": "var(--font-heading)",
        "fontSize": "24px",
        "fontWeight": "bold",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0",
        "lineHeight": "140%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "subheading": {
        "fontFamily": "var(--font-body)",
        "fontSize": "20px",
        "fontWeight": "bold",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0.01em",
        "lineHeight": "150%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "question": {
        "fontFamily": "var(--font-heading)",
        "fontSize": "24px",
        "fontWeight": "normal",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0",
        "lineHeight": "150%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "caption": {
        "fontFamily": "var(--font-body)",
        "fontSize": "13px",
        "fontWeight": "normal",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0.02em",
        "lineHeight": "170%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "paragraph": {
        "fontFamily": "var(--font-body)",
        "fontSize": "16px",
        "fontWeight": "normal",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0.01em",
        "lineHeight": "190%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "buttonLabel": {
        "fontFamily": "var(--font-body)",
        "fontSize": "14px",
        "fontWeight": "bold",
        "fontStyle": "normal",
        "color": "var(--textInverse)",
        "textAlign": "center",
        "letterSpacing": "0.06em",
        "lineHeight": "125%",
        "textDecoration": "none",
        "textTransform": "uppercase",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      }
    },
    "canvas": {
      "background": "var(--background)"
    },
    "header": {
      "background": "var(--background)",
      "border": "1px solid var(--secondary)"
    },
    "footer": {
      "background": "var(--background)",
      "border": "1px solid var(--secondary)"
    },
    "lessonHeader": {
      "background": "var(--accent)"
    },
    "topic": {
      "background": "var(--background)",
      "border": "1px solid var(--secondary)"
    },
    "navigation": {
      "background": "var(--backgroundSubtle)",
      "border": "1px solid var(--secondary)"
    },
    "button": {
      "background": "var(--accent)"
    },
    "pagination": {
      "background": "var(--backgroundSubtle)",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "paragraphBlock": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "nestedAccentColor": "var(--accent)",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "imageBlock": {
      "background": "transparent",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "videoBlock": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "imageGrid": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--accent)",
      "cardShadowOffset": "0px 2px 8px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "accordion": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "carousel": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "flipCard": {
      "background": "transparent",
      "cardFrontBackgroundColor": "var(--backgroundSubtle)",
      "cardBackBackgroundColor": "var(--accent)",
      "arrowColor": "var(--textInverse)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "tabs": {
      "background": "transparent",
      "activeBg": "var(--accent)",
      "inactiveBg": "var(--backgroundSubtle)",
      "containerBg": "var(--backgroundSubtle)",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "timeline": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "trackColor": "var(--secondary)",
      "progressCompletedBg": "var(--accent)",
      "progressCurrentBorder": "var(--accent)",
      "progressUnreachedBg": "var(--secondary)",
      "progressUnreachedBorder": "var(--backgroundSubtle)",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "assessment": {
      "background": "transparent",
      "optionTextColor": "var(--textPrimary)",
      "optionIndicatorColor": "var(--accent)",
      "optionSelectedColor": "var(--accent)",
      "optionCheckmarkColor": "var(--textInverse)",
      "optionBackgroundColor": "var(--background)",
      "optionHoverBackgroundColor": "var(--backgroundSubtle)",
      "buttonBackgroundColor": "var(--accent)",
      "buttonTextColor": "var(--textInverse)",
      "buttonHoverBackgroundColor": "var(--accent)",
      "feedbackCorrectColor": "#D7F7E1",
      "feedbackIncorrectColor": "#FFEBE8",
      "feedbackTextColor": "#111111",
      "optionBorderCorrectColor": "#079355",
      "optionBorderIncorrectColor": "#D73220",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    }
  }
}
```
