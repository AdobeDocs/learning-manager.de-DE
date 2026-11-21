---
jcr-language: en_us
title: Warteliste und Verwaltung der Anwesenheit
description: Administratoren können die Anwesenheit und Wartelisten von Kursteilnehmern verwalten.
contentowner: manochan
exl-id: 257ed196-d6a7-4d6c-bd90-33d658f6ba55
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: 38dba6765ff013e446ab1f6098e9f1df0c24d0f9
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 38%
---
# Warteliste und Verwaltung der Anwesenheit

Administratoren können die Anwesenheit und Wartelisten von Kursteilnehmern verwalten.

## Verwaltung der Warteliste {#waitlistmanagement}

Teilnehmer werden auf eine Warteliste für einen Klassenzimmerkurs gesetzt, wenn die Lizenzen basierend auf der Reihenfolge ihrer Registrierung begrenzt sind. Wenn alle für eine Benutzergruppe reservierten Lizenzen gefüllt sind, werden weitere Mitglieder dieser Gruppe auf die Warteliste der Gruppe gesetzt. Teilnehmer außerhalb der Benutzergruppen werden in die **Warteliste öffnen** platziert.

Administratoren können die Warteliste überprüfen und Teilnehmer auf der Warteliste verwalten. Adobe Learning Manager kann Teilnehmer auf der Warteliste auch automatisch bewerben, wenn eine Lizenz verfügbar wird.

So verwalten Sie Teilnehmer auf Warteliste:

1. Wählen Sie im linken Teilfenster **Kurse** aus.
1. Wählen Sie den Namen eines Klassenzimmerkurses aus den verfügbaren Kursen aus.

   Es wird eine neue Seite mit ausführlichen Kursinformationen angezeigt.

1. Wählen Sie **Warteliste** im linken Bereich der Kursdetailseite aus.

   Die Wartelistenseite wird mit dem folgenden **Wartelistenstatus** geöffnet:

   * **Sitzplatzbeschränkung:** Die Gesamtzahl der für die Sitzung verfügbaren Lizenzen.
   * **Ausgefüllt:** Anzahl der derzeit belegten Plätze.
   * **In Warteliste:** Anzahl der Teilnehmer, die auf die Registrierung warten.

1. Wählen Sie die folgenden Registerkarten auf der Seite **Warteliste** aus:

   1. **Warteliste nach Benutzergruppe**: Führt die Teilnehmer auf der Warteliste unter jeder Benutzergruppe auf.

   >[!NOTE]
   >
   >Diese Registerkarte wird nur angezeigt, wenn die Einstellung **Gruppenregistrierung** aktiviert ist.

   1. **Warteliste öffnen**: Listet die Teilnehmer auf der Warteliste auf, die nicht für eine Benutzergruppe reserviert sind.

   ![Seite &quot;Warteliste&quot; zeigt die Registerkarte &quot;Warteliste nach Benutzergruppe&quot; an](assets/waitlist-by-user-group-tab.png "Seite &quot;Warteliste&quot; zeigt die Registerkarte &quot;Warteliste nach Benutzergruppe&quot; an")

1. Wählen Sie neben einem Teilnehmer eine der folgenden Aktionen aus:

   | **Aktion** | **Beschreibung** |
   |---|---|
   | **Bestätigen** | Registriert den Teilnehmer auf der Warteliste für die Sitzung und entfernt ihn aus der Warteliste. |
   | **Registrierung aufheben** | Entfernt den Teilnehmer aus der Warteliste und aktualisiert die Positionen der verbleibenden Teilnehmer auf der Warteliste. |

## Verwaltung der Anwesenheit {#attendancemanagement}

Diese Funktion ist nur für Präsenzkurse und Kurse im virtuellen Klassenzimmer verfügbar. Sie können die Anwesenheit mit den unten angeführten Schritten erfassen:

1. Klicken Sie auf „Kurse“ im linken Bereich, nachdem Sie sich als Administrator angemeldet haben.
1. Klicken Sie in der Liste der verfügbaren Kurse auf den Namen des gewünschten Präsenzkurses/Moduls. Eine neue Seite mit genauen Informationen über den Kurs erscheint.
1. Klicken Sie auf die Registerkarte „Anwesenheit“, wählen Sie die Teilnehmer aus und klicken Sie auf „Speichern“, um deren Anwesenheit zu vermerken.

>[!NOTE]
>
>Wenn ein Kurs mehrere Module umfasst und der Teilnehmer nur eines davon abgeschlossen hat, können Sie ein einzelnes Modul auswählen und auf &quot;Speichern&quot; klicken. Wenn der Teilnehmer alle Module eines Kurses abgeschlossen hat, können Sie auf die Option „Alle auswählen“ und dann auf „Speichern“ klicken.

Die Anwesenheit für eine Adobe Connect-basierte virtuelle Klassenzimmersitzung wird automatisch 2-3 Stunden nach der Sitzung vermerkt. Der Abschluss des virtuellen Klassenzimmer-Kurses des Teilnehmers wird erst vermerkt, nachdem die Teilnahme vermerkt wurde.
