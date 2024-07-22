---
jcr-language: en_us
title: Suche nach Kurs in Learning Manager nicht möglich
description: Ein Teilnehmer kann in Learning Manager einen Kurs nicht finden.
contentowner: nluke
exl-id: 702aacb7-a0b9-48fb-8a3d-425bfea63f65
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 55%

---

# Suche nach Kurs in Learning Manager nicht möglich

## Problem

Ein Teilnehmer kann in Learning Manager einen Kurs nicht finden.

## Szenario 1: Die Registrierung erfolgt über ein höheres Lernobjekt

### Zusammenfassung 

Es gibt Szenarien, in denen ein Teilnehmer einen Kurs sucht und der Kurs nicht aufgeführt wird. Wenn sich der Teilnehmer jedoch für ein Lernprogramm/eine Zertifizierung registriert hat, kann der Teilnehmer den Kurs innerhalb des Lernobjekts anzeigen.

### Warum passiert das?

Wenn sich ein Teilnehmer im Lern-Manager über ein Lernprogramm/eine Zertifizierung registriert, erfolgt die Registrierung für diesen Kurs über das Lernprogramm/die Zertifizierung.

Daher kann der Teilnehmer unter **Eigenes Lernen** nicht nach eigenständigen Kursen suchen.

Der Teilnehmer kann die Kurse jedoch nicht innerhalb des Lernprogramms/der Zertifizierung anzeigen.

## Szenario 2: Der Teilnehmer hat keinen Zugriff auf den Katalog, der den Kurs enthält.

### Zusammenfassung 

Ein Teilnehmer kann keine Kurse im Katalog oder im Lern-Dashboard suchen.

### Warum passiert das?

Dieses Problem tritt in folgenden Situationen auf:

* Der Teilnehmer ist kein Teil des Katalogs, der den Kurs enthält. **ODER**
* Der Kurs ist nicht Teil des Katalogs, auf den der Teilnehmer zugreifen kann.

### Auflösung

1. Melden Sie sich als Administrator an.

1. Klicken Sie auf **[!UICONTROL Katalog]** und navigieren Sie zu dem Katalog, der den Kurs enthält.
1. Klicken Sie auf **[!UICONTROL Intern freigeben]** oder **[!UICONTROL Inhalt]** (in Abhängigkeit des oben genannten Szenarios).

   ![](assets/cp-share-internally.png)

   *Katalog intern freigeben*

1. Überprüfen Sie die folgenden Szenarien:

   * Teilnehmer ist nicht Teil des Katalogs

     Um den Katalog freizugeben, klicken Sie auf **[!UICONTROL Hinzufügen]** und fügen Sie die Benutzergruppe hinzu, zu der der Benutzer gehört. Klicken Sie auf **[!UICONTROL Speichern]**.

     ![](assets/cp-add-user-group.png)

     *Benutzergruppe hinzufügen*

   * Der Kurs ist nicht Teil des Katalogs

     Klicken Sie im Abschnitt &quot;Inhalt&quot; auf **[!UICONTROL Inhalt hinzufügen]** und wählen Sie den Kurs aus, den Sie dem Katalog hinzufügen müssen.

     ![](assets/cp-add-content.png)

     *Inhalte zum Kurs hinzufügen*
