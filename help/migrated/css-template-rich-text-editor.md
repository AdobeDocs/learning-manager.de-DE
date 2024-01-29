---
jcr-language: en_us
title: CSS-Vorlage für Rich-Text-Editor
description: CSS-Vorlage für Rich-Text-Editor
contentowner: saghosh
preview: true
source-git-commit: 9325abb9cda8c8a019c9d72c1944a8284f38f83e
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---



# CSS-Vorlage für Rich-Text-Editor

## Warum ist CSS erforderlich?

Rich Text besteht aus HTML-Markup. Wenn Sie das Markup unverändert rendern, wird der Standardstil des Browsers angewendet. Das passt oft nicht gut zu den Stilrichtlinien des Unternehmens. Ein CSS ist erforderlich, um die Richtlinien zu erfüllen.

## Standardstil

Das angehängte CSS-Stylesheet enthält den Stil, der vom Lern-Manager angewendet wird. Das Styling wurde unter Berücksichtigung der meisten Anwendungsfälle optimiert. Laden Sie die angehängte CSS-Datei herunter und importieren Sie sie entsprechend Ihren Konventionen und Ihrem Build-System in Ihre Webanwendung. Die definierten CSS-Klassen werden unter der ql-editor-Klasse mit einem Namensraum versehen und beeinträchtigen nicht die vorhandenen Stile.

## Stile anpassen

Der Standardstil erfüllt möglicherweise nicht alle Anforderungen. Die Anpassungen können durch Überschreiben des bereitgestellten CSS vorgenommen werden. Der gesamte Stil wird als Nachfahren-Selektoren unter ql-editor eingeschlossen. Die folgenden Klassen werden verwendet:

* **Einzug**: li.ql-indent-$number. $number variiert von 1 bis 9
* **Umfang**: ql-size-small, ql-size-large, ql-size-huge
* **Ausrichtung**: ql-align-center, ql-align-justify, ql-align-right
* **Farbe**: ql-color-$color. $color = weiß, rot, orange, gelb, grün, blau, lila
* **Hintergrund**: ql-bg-$color. $color = schwarz, rot, orange, gelb, grün, blau, lila
* **html-Tags**: p, ol, ul, pre, blockquote, h1, h2, h3, h4, h5, h6

[CSS-Datei, die für die Anpassung verwendet wird.](assets/ql-headless.css)
