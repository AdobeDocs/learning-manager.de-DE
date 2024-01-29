---
jcr-language: en_us
title: Kurs kann im Learning Manager nicht gesucht werden
description: Ein Teilnehmer kann einen Kurs im Lern-Manager nicht suchen.
contentowner: nluke
source-git-commit: 8b29ac996962e7ce8fbda51f3421c9a5f248fcf6
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---



# Kurs kann im Learning Manager nicht gesucht werden

## Problem

Ein Teilnehmer kann einen Kurs im Lern-Manager nicht suchen.

## Szenario 1: Die Registrierung erfolgt über ein höheres Lernobjekt

### Zusammenfassung

Es gibt Szenarien, in denen ein Teilnehmer einen Kurs sucht und der Kurs nicht aufgeführt wird. Wenn sich der Teilnehmer jedoch für ein Lernprogramm/eine Zertifizierung registriert hat, kann der Teilnehmer den Kurs innerhalb des Lernobjekts anzeigen.

### Warum passiert das?

Wenn sich ein Teilnehmer im Lern-Manager über ein Lernprogramm/eine Zertifizierung registriert, erfolgt die Registrierung für diesen Kurs über das Lernprogramm/die Zertifizierung.

Daher kann der Teilnehmer nicht nach eigenständigen Kursen suchen, die unter **Eigenes Lernen**.

Der Teilnehmer kann die Kurse jedoch nicht innerhalb des Lernprogramms/der Zertifizierung anzeigen.

## Szenario 2: Der Teilnehmer hat keinen Zugriff auf den Katalog, der den Kurs enthält.

### Zusammenfassung

Ein Teilnehmer kann keine Kurse im Katalog oder im Lern-Dashboard suchen.

### Warum passiert das?

Dieses Problem tritt in folgenden Fällen auf:

* Der Teilnehmer ist kein Teil des Katalogs, der den Kurs enthält. **ODER**
* Der Kurs ist nicht Teil des Katalogs, auf den der Teilnehmer Zugriff hat.

### Auflösung

1. Melden Sie sich als Administrator an.

1. Klicken **[!UICONTROL Katalog]** und navigieren Sie zu dem Katalog, der den Kurs enthält.
1. Klicken **[!UICONTROL Intern freigeben]** oder **[!UICONTROL Inhalt]** (je nach dem oben genannten Szenario).

   ![](assets/cp-share-internally.png)

   *Teilen Sie den Katalog intern*

1. Überprüfen Sie die folgenden Szenarien:

   * Teilnehmer ist nicht Teil des Katalogs

     Klicken Sie auf **[!UICONTROL Hinzufügen]** und fügen Sie die Benutzergruppe hinzu, zu der der Benutzer gehört. Klicken **[!UICONTROL Speichern]**.

     ![](assets/cp-add-user-group.png)

     *Benutzergruppe hinzufügen*

   * Der Kurs ist nicht Teil des Katalogs

     Klicken Sie im Abschnitt Inhalt auf **[!UICONTROL Inhalt hinzufügen]** und wählen Sie den Kurs aus, den Sie dem Katalog hinzufügen müssen.

     ![](assets/cp-add-content.png)

     *Inhalte zum Kurs hinzufügen*
