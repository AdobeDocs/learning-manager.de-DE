---
title: Untertitel in Live Hub-Sitzungen
description: Erfahre, wie Untertitel gesprochene Inhalte in Echtzeit anzeigen, sodass Kursleiter und Teilnehmer die Schritte während der Live-Hub-Sitzungen nachvollziehen können.
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: 574ba5fd9ac9dc02130a39006574c9ca1ce6c1d1
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 4%
---

# Verstehen der Bilduntertitel

Untertitel werden während einer Live Hub-Sitzung automatisch erstellt und aktualisiert, sobald die Teilnehmer sprechen. Untertitel werden in einem dedizierten Anzeigebereich angezeigt und in der vom Kursleiter in den **Raumeinstellungen** ausgewählten Sprache angezeigt.

Sowohl Kursleiter als auch Teilnehmer können Untertitel anzeigen. Jeder Teilnehmer kann Untertitel unabhängig ein- oder ausblenden, ohne die Untertiteleinstellungen für andere Teilnehmer zu beeinflussen.

Nur Kursleiter können die Untertitelsprache ändern. Die Teilnehmer können Untertitel nur in der von den Kursleitern ausgewählten Sprache anzeigen. Die Teilnehmer können die Sprache der Untertitel nicht ändern.

## Wie der Live-Hub die Untertitelsprache bestimmt

Live Hub wählt die Untertitelsprache automatisch basierend auf der folgenden Prioritätsreihenfolge aus:

1. **Kurssprache:** Live Hub verwendet die Kurssprache, wenn sie für Untertitel unterstützt wird. Wenn die aktuelle Kursinstanz für einen mehrsprachigen Kurs eine Sprache verwendet, die keine Untertitel unterstützt, wählt Live Hub die Sprache der ersten Kursinstanz aus, die Untertitel unterstützt. Weitere Informationen finden Sie unter [Unterstützte Sprachen in ALM](../../migrated/languages-supported.md).
1. **Kontosprache:** Wenn die Kurssprache nicht unterstützt wird, überprüft Live Hub die Kontosprache und verwendet sie, falls unterstützt.

>[!NOTE]
>
>Wenn weder die Kurssprache noch die Kontosprache unterstützt wird, wählt Live Hub Englisch als Untertitelsprache aus. Außerdem sind die Untertitel standardmäßig deaktiviert und müssen manuell aktiviert werden.

## Unterstützte Sprachen für Bilduntertitel

Live Hub unterstützt Untertitel in den folgenden Sprachen:

* Englisch
* Französisch
* Deutsch
* Chinesisch
* Spanisch
* Italienisch
* Japanisch
* Portugiesisch
* Dänisch
* Niederländisch
* Finnisch
* Türkisch
* Koreanisch
* Norwegisch
* Schwedisch
* Russisch

## Wie funktionieren Untertitel?

In einer Live Hub-Sitzung werden automatisch Untertitel generiert. Untertitel werden in einem eigenen Bedienfeld angezeigt und aktualisiert sich kontinuierlich, während die Teilnehmer sprechen. Sowohl Kursleiter als auch Teilnehmer können Untertitel anzeigen.

Jeder Teilnehmer kann Untertitel nach Belieben ein- oder ausblenden. Änderungen an dieser Einstellung wirken sich nicht auf andere Teilnehmer aus.

![](assets/closed-captions-overview.png)
*Live-Hub-Oberfläche, die die Untertitel in der Sitzung anzeigt*

## Rollen und Berechtigungen

Die Funktion **Bilduntertitel** ist sowohl für Kursleiter als auch für Teilnehmer in einer Live Hub-Sitzung verfügbar. Die verfügbaren Aktionen variieren je nach Benutzerrolle.

| **Kursleiter** | **Teilnehmer** |
|---|---|
| [Untertitel anzeigen](../getting-started-with-live-hub/manage-closed-captions-as-an-instructor.md#display-closed-captions) | [Untertitel anzeigen](../getting-started-with-live-hub/manage-closed-captions-as-a-learner.md#display-closed-captions) |
| [Darstellung von Untertiteln ändern](../getting-started-with-live-hub/manage-closed-captions-as-an-instructor.md#change-the-appearance-of-closed-captions) | [Darstellung von Untertiteln ändern](../getting-started-with-live-hub/manage-closed-captions-as-a-learner.md#change-the-appearance-of-closed-captions) |
| [Untertitelsprache auswählen](../getting-started-with-live-hub/manage-closed-captions-as-an-instructor.md#select-the-caption-language) | |