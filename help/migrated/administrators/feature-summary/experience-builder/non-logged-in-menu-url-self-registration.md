---
description: Hier erfahren Sie, wie Sie eine nicht angemeldete Menü-URL für jedes Selbstregistrierungsprofil freigeben, damit externe Benutzer dem richtigen Profil in Adobe Learning Manager beitreten.
jcr-language: en_us
title: Nicht-angemeldete Menü-URL für Selbstregistrierung verwenden
exl-id: c4b3f1f5-a785-45ab-b820-621dae16526d
source-git-commit: 8cf3817fc740f8a0219ca6b4f3fe6c637633c955
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 0%
---

# Nicht-angemeldete Menü-URL für Selbstregistrierung verwenden

Mit Selbstregistrierungsprofilen können externe Benutzer, z. B. Partner oder Mitglieder mehrerer Organisationen, ihre eigenen Konten in Adobe Learning Manager erstellen. Sie können jetzt eine nicht angemeldete Menü-URL für jedes Selbstregistrierungsprofil freigeben. Das Menü ist in Experience Builder integriert.

Wenn Benutzer **Registrieren** auf einer Seite auswählen, die über diese URL erreicht wird, fügt Adobe Learning Manager sie dem Profil hinzu, zu dem die URL gehört. Dadurch können Sie Benutzer aus verschiedenen Organisationen, z. B. verschiedenen Agenturen oder Partnerunternehmen, in separaten Profilen speichern.

Früher wurden dem in **Branding** ausgewählten Profil immer neue Benutzer durch eine URL für eine nicht angemeldete Seite hinzugefügt. Durch die URL des nicht angemeldeten Menüs wird diese Einschränkung aufgehoben: Jedes Profil hat eine eigene URL, und alle URLs öffnen dieselbe Zielseite.

## Vorbereitung

1. Erstellen Sie das nicht angemeldete Menü in Experience Builder und wählen Sie die Landingpage in **Branding** aus. Alle Profil-URLs öffnen diese Landingpage.

1. Erstellen Sie das Selbstregistrierungsprofil in **Benutzer** > **Extern**. Jedes Profil verfügt über eine eigene Gruppen-ID und einen eigenen Zugriffsschlüssel, die Benutzer registrieren müssen.

## Anmelde-URL für ein Profil kopieren

1. Wählen Sie **Benutzer** > **Extern** und anschließend **Selbstregistrierung** aus.

1. Wählen Sie in der Spalte **URL der Landingpage, die kopiert werden soll** die Option **Nicht angemeldet** für ein Profil aus.

   ![Die zu kopierende Landingpage-URL für ein Selbstregistrierungsprofil](assets/Use-a-non-logged-in-menu-URL-for-self-registration-image1.png "Die zu kopierende Landingpage-URL")

1. Kopieren Sie die URL und geben Sie sie für die Benutzer frei, die Sie einladen möchten.

Die zu kopierende **Landingpage-URL** enthält folgende Optionen:

* **Registrierung**: Die Standardregistrierungs-URL
* **Startseite (veraltet), für die keine Anmeldung erfolgt ist**: Die URL für die ältere, nicht angemeldete Startseite
* **Menü ohne Anmeldung**: Die URL für das nicht angemeldete Menü in Experience Builder

## Was Benutzer sehen

1. Der Benutzer öffnet die URL und landet auf der nicht angemeldeten Landingpage, die Sie unter **Branding** ausgewählt haben.

1. Der Benutzer wählt &quot;**Registrieren**&quot; aus und gibt die Gruppen-ID und den Zugriffsschlüssel für das Profil ein.

1. Der Benutzer gibt seinen Namen, seine E-Mail-Adresse und sein Kennwort ein und schließt dann die Registrierung ab.

Adobe Learning Manager fügt den Benutzer dem Profil hinzu, zu dem die URL gehört. Sie können den neuen Benutzer unter diesem Profil in **Benutzer** > **Extern** sehen.

>[!NOTE]
>
>Jede Profil-URL zeigt dieselbe Landingpage an. Nur das Profil, dem Benutzer hinzugefügt werden, unterscheidet sich.

## Begrüßungs-E-Mail mit der URL senden

1. Wählen Sie **Benutzer** > **Extern** und wählen Sie das Selbstregistrierungsprofil aus.

1. Wählen Sie in der Liste **URL der Landingpage, die kopiert werden soll** die URL aus, die Sie in die E-Mail aufnehmen möchten.

   ![URL-Liste der Landingpage mit den E-Mail- und Kopiersymbolen](assets/Use-a-non-logged-in-menu-URL-for-self-registration-image2.png "URL-Liste der Landingpage")

1. Wählen Sie das E-Mail-Symbol aus, um die E-Mail zu senden. Alternativ können Sie auf das Symbol &quot;Kopieren&quot; klicken, um die URL zu kopieren.

Adobe Learning Manager sendet die E-Mail mit der Vorlage **Profil erstellt (Externe/Partner)**. Die E-Mail enthält die von Ihnen ausgewählte eindeutige URL, die Lizenzbeschränkung für das Profil und das URL-Ablaufdatum. Geben Sie die URL für die Benutzer frei, die Sie einladen möchten.

## Wechsel von der alten, nicht angemeldeten Startseite

Frühere Versionen dieser Liste zeigten die Option **Nicht angemeldet**. Sie heißt jetzt **Nicht angemeldete Homepage (veraltet)**.

Die ältere nicht angemeldete Startseite wird in einer zukünftigen Version veraltet sein. Wenn Sie sie verwenden, wechseln Sie zum nicht angemeldeten Menü in Experience Builder, um dieselbe Funktion beizubehalten.
