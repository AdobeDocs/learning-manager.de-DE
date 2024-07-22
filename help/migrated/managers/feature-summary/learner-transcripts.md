---
description: Erfahren Sie, wie Sie Teilnehmertranskripte basierend auf Benutzern, Lernobjekten oder Kenntnissen in Learning Manager herunterladen.
jcr-language: en_us
title: Teilnehmertranskripte
exl-id: 8204aa1e-0e0d-4d9e-9dc0-6260667bf4e7
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '917'
ht-degree: 85%

---

# Teilnehmertranskripte

Erfahren Sie, wie Sie Teilnehmertranskripte basierend auf Benutzern, Lernobjekten oder Kenntnissen in Learning Manager herunterladen.

Mit Adobe Learning Manager können die Manager eines Unternehmens die Transkripte erstellen, die mit den Teilnehmenden verknüpft sind.

## Teilnehmertranskripte erstellen {#generatelearnertranscripts}

1. Um Teilnehmertranskripte zu generieren, klicken Sie auf **[!UICONTROL Berichte]** im linken Bereich in der Manageranmeldung.
1. Klicken Sie auf der Seite auf die Registerkarte **[!UICONTROL Meine Berichte]**.
1. Klicken Sie auf den Link **[!UICONTROL Teilnehmertranskripte]**.

   ![](assets/learner-transcripts.png)

   *Berichte für Teilnehmertranskripte erstellen*

1. Ein Dialogfeld „Teilnehmertranskripte“ wird angezeigt. Wählen Sie den Datumsbereich, für den Sie das Transkript benötigen.

   >[!NOTE]
   >
   >Standardmäßig ist das Anfangsdatum das Registrierungsdatum des Teilnehmers und das Enddatum immer das aktuelle Datum. Sie können nur das Startdatum ändern, ab dem Sie die Daten benötigen.

1. Wählen Sie die Namen der Teilnehmer im Feld &quot;Teilnehmer auswählen&quot; aus und klicken Sie auf **[!UICONTROL Generieren]**.

Sie können einen einzelnen Teilnehmer oder Gruppen von Teilnehmern auswählen. Klicken Sie auf „Weitere Teilnehmer hinzufügen“, um weitere Teilnehmer hinzuzufügen.

Transkripte werden auf Ihrem Computer als XLS-Dateien erstellt und heruntergeladen. Jede XLS-Datei enthält sieben Arbeitsblätter, deren Details im Folgenden beschrieben werden:

## Herunterladen des Teilnehmertranskripts basierend auf der Zeitzone {#lt-timezone}

Wie ein Administrator kann auch ein Manager die Spalten auswählen, die exportiert werden sollen. Darüber hinaus kann ein Manager das Teilnehmertranskript basierend auf der Zeitzone herunterladen, die er in den Profileinstellungen ausgewählt hat.

Wenn der Manager diese Option aktiviert, wird die auf der Seite mit den Profileinstellungen festgelegte Zeitzone ausgewählt (siehe unten).

>[!NOTE]
>
>Bei einem neuen Manager ist das Kontrollkästchen &quot;Zeitzone&quot; deaktiviert.

![](assets/image030.png)

*Teilnehmertranskripte für einen Zeitbereich herunterladen*

## Inhalt der Teilnehmertranskriptdatei {#learnertranscriptfilecontent}

Eine typische Teilnehmertranskriptdatei besteht aus sechs Excel-Arbeitsblättern in einer einzelnen Datei. Diese Arbeitsblätter enthalten einen Gesamtüberblick über die Daten, einschließlich die anzahl von Teilnehmern im Kurs, ihre Kenntnisse, den Wettbewerbsprozentwert basieren auf dem Kurs oder Teilnehmer und ein Kompatibilitäts-Dashboard. Im Folgenden finden Sie die Dashboards, die in den Teilnehmertranskripten verfügbar sind:

**Teilnehmertranskript**

Im Teilnehmertranskript-Arbeitsblatt werden zusammen mit Profildetails über den Teilnehmer, ein Lernobjekt mit Details zur Nutzung bereitgestellt, z. B. Registrierungsdatum, Startdatum, erreichte Stufe, erzielte Quizpunkzahl und so weiter. Wenn Kurse Teil eines Lernprogramms sind, werden sie separat aufgelistet, außer einzelne Kursnutzungsdetails.

**1 - Dashboard für Lernaktivitäten**

In diesem LO-spezifischen Dashboard können Sie die Anzahl der Teilnehmer für einen Kurs, jedes Lernprogramm oder jede Zertifizierung anzeigen. Sie können das Arbeitsblatt zum Fortschritt für Teilnehmer für ein bestimmtes Lernobjekt anzeigen. Dieses Blatt zeigt Daten wie die Anzahl der Teilnehmer, die den Kurs oder das Lernprogramm abgeschlossen haben, Teilnehmer, die noch nicht fertig sind und die Ablaufdaten für die Teilnehmer.

Der Fortschritt der Benutzer für den jeweiligen Kurs wird anhand der Eingabefelder berechnet, in denen Sie das Fälligkeitsdatum und Prozent-Schwellenwerte für den Fortschritt angeben. Wenn Sie beispielsweise in den Eingabefeldern Werte von 7 Tagen und 70 % angeben, wird der Fortschritt für Kurse angezeigt, die in 7 Tagen fällig sind und von denen bereits mehr als 70 % absolviert sind. Sie können auch den Zeitraum für dieses Blatt ändern, wobei die geänderten Daten automatisch in diesem Dashboard angezeigt werden.

**2 - Dashboard für Lernaktivitäten**

Dieses Lern-Dashboard zeigt Daten für einen bestimmten Benutzer. Über dieses Dashboard können Sie Kurse, Lernprogramme oder Zertifizierungen sehen, bei denen sich ein bestimmter Benutzer registriert hat. Die Tabelle enthält außerdem Daten zu Lernobjekten, welche die Benutzer abgeschlossen haben, zu laufenden Lernobjekten und zu bevorstehenden Terminen für den Benutzer.

Der Fortschritt der Benutzer für den jeweiligen Kurs wird anhand Ihrer Eingaben berechnet, d. h. der Werte für Fälligkeitsdatum und prozentualen Fortschritt. Wenn Sie beispielsweise in den Eingabefeldern Werte von 7 Tagen und 70 % angeben, wird der Fortschrift der Benutzer für verschiedene Kurse angezeigt, die in 7 Tagen fällig sind und von denen bereits mehr als 70 % absolviert sind.

**Kenntnisse**

Auf dem Blatt „Kenntnisse“ finden Sie Kenntnisnahme, Kenntnisstufe, erforderliche Punkte, erzielte Punktzahl, abgeschlossener Prozentwert und andere Profildetails. Nachfolgend sehen Sie ein Beispiel für eine Momentaufnahme als Referenz.

**Dashboard für Kenntnisse**

In diesem Dashboard können Sie sehen, ob Ihr Unternehmen mit diversen Kenntnissen ausgestattet ist. Für bestimmte Kenntnisse können Sie überprüfen, wie viele Benutzer diese Kenntnisse besitzen sollten und wie viele sie tatsächlich besitzen. Außerdem gibt dieses Dashboard an, welche Benutzer ihre Kenntnisse möglicherweise auffrischen müssen. Dieser Wert wird anhand des Werts berechnet, den Sie in das Eingabefeld eingeben. Wenn Sie beispielsweise einen Wert von 50 Tagen eingeben, liefert das Dashboard Daten zu Benutzern, deren Kenntnisse möglicherweise nach 50 Tagen aufgefrischt werden müssen.

Dieses Dashboard für Kenntnisse ist stärker benutzerspezifisch. Sie können einen bestimmten Benutzer oder mehrere Benutzer filtern und ihre Kenntnisstufe als Dashboard anzeigen. Mit diesem Blatt können Manager und Administratoren verfolgen, wie viele Kenntnisse jeder Teilnehmer hat im Vergleich dazu, wie viele Kenntnisse jeder Teilnehmer haben sollte. Das Dashboard „Kenntnisse“ gibt auch Aufschluss darüber, welche Teilnehmer ihre Kenntnisse auffrischen müssen. Die Auffrischungsliste der Teilnehmer wird anhand der Anzahl von Tagen berechnet, die Sie in das Eingabefeld eingeben.

**Kompatibilitäts-Dashboard**

Das Kompatibilitäts-Dashboard besteht aus zwei Teilen - Kompatibilitätsbericht pro Benutzer und Kompatibilitätsbericht pro Schulungen. Für den benutzerbasierten Bericht können Sie das Kompatibilitäts-Dashboard verwenden, um Benutzer nachzuverfolgen, die bevorstehende Termine für wichtige Kompatibilitätsinitiativen haben. Für den schulungsbasierten Bericht können Sie nach Lernprogramm oder Zertifizierung filtern.

Für beide Kompatibilitätsberichte können Sie nach dem Fälligkeitsdatum filtern, um die entsprechenden Daten anzuzeigen.
