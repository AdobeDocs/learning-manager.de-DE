---
jcr-language: en_us
title: Registrierung als externer Benutzer nicht möglich
description: Externe Teilnehmer können sich nicht bei einem Profil im Adobe Learning Manager registrieren.
contentowner: nluke
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---



# Registrierung als externer Benutzer nicht möglich

## Problem

Externe Teilnehmer können sich nicht bei einem Profil registrieren.

## Fehler

Die E-Mail-ID ist bereits registriert. Bitte verwenden Sie eine andere E-Mail.

![](assets/cp-register-profile.png)

*Fehlermeldung einer bereits registrierten E-Mail*

## Beschreibung

Es gibt Szenarien, in denen ein Benutzer sich nicht bei einem externen Profil registrieren kann. Der Benutzer erhält den oben genannten Fehler während der Registrierung.

## Ursache

Dieses Problem tritt in einem der folgenden Szenarien auf:

* Der Benutzer ist bereits bei einem anderen externen Profil registriert.
* Der Benutzer ist bereits ein interner Teilnehmer.
* Der Benutzer befindet sich in einem gelöschten Status.

## Lösung:

**Szenario 1:** Der Benutzer ist bereits bei einem anderen externen Profil registriert.

1. Melden Sie sich als Administrator an.
1. Unter **Verwalten** auf **[!UICONTROL Benutzer]** > **[!UICONTROL Extern]**.
1. Öffnen Sie das Profil, zu dem der Benutzer bereits gehört, indem Sie auf Verwendete Lizenzen klicken.

   ![](assets/cp-seats-used.png)

   *Benutzerprofil öffnen*

1. Wählen Sie den Benutzer aus und klicken Sie auf **[!UICONTROL Aktionen]** > **[!UICONTROL Profil ändern]**.

   ![](assets/cp-change-profile.png)

   *Benutzerprofil ändern*

   Daraufhin wird ein Fenster geöffnet, in dem Sie wie unten beschrieben ein neues Profil auswählen können.

   ![](assets/cp-select-profiles.png)

   *Benutzerprofil auswählen*

1. Klicken Sie nach der Auswahl auf **[!UICONTROL Ändern]**.

**Szenario 2:** Der Benutzer ist als interner Teilnehmer vorhanden.

1. Melden Sie sich als Administrator an.
1. Unter **Verwalten** auf **[!UICONTROL Benutzer]** > **[!UICONTROL Intern]**.
1. Klicken Sie, um ein Teilnehmerprofil zu öffnen, und klicken Sie auf das Symbol &quot;Bearbeiten&quot;.

   ![](assets/cp-internal-learner.png)

   *Öffnen Sie ein internes Teilnehmerprofil*

1. Ändern Sie die E-Mail-Adresse des Teilnehmers oder fügen Sie *_old* an die vorhandene E-Mail-Adresse senden. Dadurch wird die E-Mail-Adresse freigegeben.

   Beispiel: Wenn die E-Mail-Adresse des Teilnehmers *<abc@adobe.com>,* ändern in *<abc_old@adobe.com>*

1. Klicken **Speichern** , um die vorgenommenen Änderungen beizubehalten.

**Szenario 3**: Der Benutzer befindet sich in einem gelöschten Status.

1. Melden Sie sich als Administrator an.
1. Unter **Verwalten** auf **[!UICONTROL Benutzer]** > **[!UICONTROL Benutzerbereinigung]**.
1. Wählen Sie den Teilnehmer aus und klicken Sie auf das Symbol &quot;Bearbeiten&quot;.

   ![](assets/cp-deleted-learner.png)

   *E-Mail-Adresse des Benutzers bearbeiten*

1. Ändern Sie die E-Mail-Adresse des Teilnehmers oder fügen Sie *_old* an die vorhandene E-Mail-Adresse senden. Dadurch wird die E-Mail-Adresse freigegeben.

   Beispiel: Wenn die E-Mail-Adresse des Teilnehmers **<abc@adobe.com>**&#x200B;ändern Sie ihn in **<abc_old@adobe.com>**.
