---
description: Beim Hochladen einer CSV-Datei wird ein Fehler angezeigt. Lesen Sie weiter, um das Problem zu beheben.
jcr-language: en_us
title: CSV-Datei kann nicht hochgeladen werden
contentowner: saghosh
exl-id: 10458499-1038-4c62-971f-f950d383e970
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 71%

---

# CSV-Datei kann nicht hochgeladen werden

## Fehler: Daten werden abgeschnitten: Daten sind zu lang für die Spalte

Wenn Sie versuchen, eine CSV-Datei in Adobe Learning Manager hochzuladen, wird die folgende Fehlermeldung angezeigt.

![](assets/csv-upload-failed.png)

*Fehlermeldung, dass bei der CSV-Verarbeitung ein Fehler aufgetreten ist*

## Ursache

Der Fehler tritt auf, wenn die in der angegebenen Spalte vorhandenen Daten die für die Spalte definierte Zeichenbeschränkung überschreiten.

## Auflösung

* Öffnen Sie die CSV-Datei.
* Überprüfen Sie die Daten in der Spalte, die im Fehler erwähnt wird.
* Wenn ein großer Wert vorhanden ist (z. B. mehr als 60 Zeichen), ändern Sie den Wert, um die Daten zu korrigieren.

## Fehler: In der ersten Spalte der CSV-Datei wird ein Sonderzeichen angezeigt

Sie können keine CSV-Datei hochladen, da in der ersten Spalte beim Zuordnen der Spalten ein Sonderzeichen angezeigt wird.

![](assets/csv-2.png)

*Sonderzeichen in der Namensspalte*

## Ursache

Das Problem tritt auf, wenn die CSV-Datei in Excel im UTF-8-Format gespeichert wird. Wenn Sie eine CSV-Datei in Excel als UTF-8 speichern, wird sie im UTF-BOM-Format gespeichert. Sie können dies entweder mit Notepad++ oder beim Hochladen einer CSV-Datei in Learning-Manager beim Zuordnen der Spalten überprüfen. In der ersten Spalte wird dann ein Sonderzeichen angezeigt.

## Auflösung

* **A:** Speichern über Excel:

   1. Öffnen Sie die CSV-Datei in Excel.
   1. Speichern Sie die Datei als normale CSV-Datei.

* **B:** Speichern über Notepad oder Notepad++:

   * Öffnen Sie die CSV-Datei in Notepad oder Notepad++.
   * Speichern Sie die Datei in einem UTF-8-Format.

## Fehler: E-Mail-Adresse eines Benutzers, der bereits im System vorhanden ist

Sie können keine CSV-Datei hochladen, da bei der CSV-Verarbeitung ein Fehler aufgetreten ist. Die folgende Fehlermeldung wird angezeigt:

![](assets/csv-3.png)

*Fehlermeldung für einen doppelten Benutzer*

## Ursache

Dieses Problem tritt auf, wenn ein Benutzer im System bereits mit derselben E-Mail-Adresse oder UUID vorhanden ist.

## Auflösung

### Szenario 1

**Konten, für die UUID nicht aktiviert ist.**

In diesem Szenario gibt es zwei Ursachen für diesen Fehler:

1. Der Benutzer, den Sie hinzufügen möchten, ist ein Manager eines externen Profils. Um dieses Problem zu beheben, öffnen Sie das externe Profil, zu dem der Benutzer gehört, wählen Sie den Benutzer aus, klicken Sie auf **[!UICONTROL Aktionen]** > **[!UICONTROL Rolle zuweisen]** > **[!UICONTROL Manager]** und ändern Sie den Manager des Profils.
1. Der Benutzer, den Sie hinzufügen möchten, wurde gelöscht. In diesem Szenario können Sie den Benutzer erst dann mit derselben E-Mail-Adresse hinzufügen, wenn der Bereinigungsvorgang abgeschlossen ist. Fügen Sie den Benutzer als **&#x200B; mit &#x200B;** sekundären E-Mail-Adresse hinzu, um Zugriff auf die Plattform zu gewähren. Sobald der Bereinigungsprozess abgeschlossen ist, bearbeiten Sie den Benutzer und ändern Sie die E-Mail-Adresse in die richtige E-Mail-Adresse.

### Szenario 2

**UUID-fähige Konten.**

Bei UUID-fähigen Konten kann dieses Problem auftreten, wenn einem Benutzer eine UUID zugewiesen wurde, die bereits von einem anderen Benutzer im Konto verwendet wird, oder wenn der Benutzer eine andere E-Mail-Adresse hat.

Es sind beispielsweise zwei Benutzer, A und B, mit den E-Mail-Adressen &quot;<a@xyz.com>&quot; und &quot;<b@xyz.com>&quot; mit der UUID 1 bzw. 2 vorhanden.

Wenn Sie jetzt eine CSV-Datei hochladen, die 3 als UUID des Benutzers A und 2 als UUID des Benutzers B aufweist, wird ein Fehler angezeigt.

>[!TIP]
>
>Um dieses Problem zu beheben, **müssen dieselbe E-Mail-Adresse und UUID für den Benutzer in der CSV-Datei und im System vorhanden sein.**
