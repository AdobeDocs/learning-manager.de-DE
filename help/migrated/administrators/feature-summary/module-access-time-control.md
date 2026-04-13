---
description: Legen Sie ein Zeitfenster fest, in dem Teilnehmer ein Modul starten dürfen.
jcr-language: en_us
title: Modulzugriffszeitsteuerung
contentowner: mmanuel
source-git-commit: 6423fd5c0853705a28c6c67b6936d93e68cbca20
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 1%

---

# Modulzugriffszeitsteuerung

## Übersicht

Mithilfe der Erweiterung können Autoren und Administratoren in Adobe Learning Manager ein Zeitfenster definieren, in dem Teilnehmer ein Modul starten dürfen. Außerhalb des konfigurierten Start-/Endfensters bleibt das Modul in der Kursstruktur sichtbar, aber die Teilnehmer können es nicht initiieren.

Diese Funktion ist von entscheidender Bedeutung für Benutzer, die eine strengere Kontrolle darüber benötigen, wann bestimmte Inhalte verfügbar werden, oder die ihre Initiierung beenden sollten, z. B. in zeitgesteuerten Programmen, kontextbasierten Schulungen oder zeitabhängigen Übungen.

## Neue Funktionen

Autoren können jetzt auf Modulebene innerhalb eines Kurses ein Startdatum/-uhrzeit sowie ein Enddatum/-uhrzeit konfigurieren, das bestimmt, wann Teilnehmer dieses Modul starten dürfen. Innerhalb dieses Fensters verhält sich das Modul wie gewohnt. Vor der Startzeit oder nach der Endzeit sieht der Teilnehmer das Modul in der Kursübersicht, kann es aber nicht starten.
Die Konfiguration wird in der Benutzeroberfläche für die Kurserstellung als zusätzliche Planungssteuerung für bestimmte Modultypen angezeigt, z. B. zum Selbststudium vorgesehene Inhalte, Tests oder Aktivitäten. Administratoren können diese Steuerelemente verwenden, um Module zu erstellen, die in Phasen geöffnet werden, oder um späte Starts in Programmen zu verhindern, in denen Inhalte innerhalb eines definierten Zeitraums belegt werden müssen.

## Wichtigste Vorteile

Der Hauptvorteil besteht in der Möglichkeit, zu steuern, wann auf Module zugegriffen werden kann. Schulungsteams können die Modulverfügbarkeit mit Ereignissen aus der Praxis synchronisieren, z. B. neuen Produkteinführungen, gesetzlichen Fristen und internen Programmen. Dadurch wird sichergestellt, dass Teilnehmer erforderliche Inhalte abschließen, bevor sie auf spätere Module zugreifen können.
Beispiel: Die Kohorte 1 kann nur in Woche 2 auf Modul 2 zugreifen, während Modul 3 bis Woche 3 gesperrt bleibt. Dadurch müssen Inhalte nicht mehr manuell ein- und ausgeblendet werden und es müssen keine separaten Kursversionen erstellt werden.
Dies verbessert die Lernerfahrung der Teilnehmer: Anstatt auf Module zu schauen, auf die technisch zugegriffen werden kann, die aber zu diesem Zeitpunkt nicht sein sollten (oder bereits abgeschlossen sein sollten), sehen die Teilnehmer eine Kursstruktur, in der die Module, die sie beginnen dürfen, eindeutig mit dem beabsichtigten Zeitplan ausgerichtet sind.

## Anwendungsszenarien

**Kohortenbasiertes Aktivierungsprogramm**: In diesem Programm wird jede Woche ein neues Modul geöffnet. Der Inhalt für Woche 1 ist sofort verfügbar, während Woche 2 sichtbar ist, kann aber erst zu einem bestimmten Datum gestartet werden. Woche 3 folgt dem gleichen Absperrverfahren. Die Teilnehmer können den gesamten Lernpfad sehen, aber das System steuert, wann sie tatsächlich jeden Schritt beginnen können.
**Zeitgebundene Produkt- oder Kampagnentraining**: Marketing- oder Produktteams können ein Schulungsmodul erstellen, auf das nur zugegriffen werden darf, wenn eine Kampagne aktiv ist oder eine bestimmte Version eines Produkts noch verfügbar ist. Dieses festgelegte Startfenster stellt sicher, dass Teilnehmer kein Modul zu einer eingestellten Produktversion nach der angegebenen Endzeit beginnen.
**Bewertungs- oder Prüfungsumgebungen**: Organisationen können ein Modul (z. B. einen Test) für ein kurzes, gut definiertes Fenster öffnen (z. B. &quot;Sie können die Prüfung jederzeit zwischen 9:00 und 12:00 an einem bestimmten Datum beginnen&quot;). Die Teilnehmer können die Prüfung nicht außerhalb dieses Fensters beginnen, was eine faire Planung über Zeitzonen und Kohorten hinweg unterstützt.

## Einstellen der Modulzugriffszeit

1. Melden Sie sich bei Adobe Learning Manager als Autor an.
2. Wechseln Sie zum Abschnitt **Lernen** > **Kurse**. ALM zeigt eine Kursliste an.![alt-text](/help/migrated/administrators/feature-summary/assets/module-access-time1.png)
3. Wählen Sie den Kurs aus, für den Sie die Einschränkung festlegen möchten.
4. Wählen Sie **Instanzen** aus. ALM zeigt eine Liste von Instanzen an.
5. Wählen Sie im Instanzabschnitt, für den Sie die Zugriffsbeschränkung festlegen möchten, **Module** aus. Die Schaltfläche **Bearbeiten** wird angezeigt.![Alternativtext](/help/migrated/administrators/feature-summary/assets/module-access-time2.png) ![Alternativtext](/help/migrated/administrators/feature-summary/assets/module-access-time3.png)
6. Wählen Sie **Bearbeiten**. Die relevanten Abschnitte, die sich auf das Modul beziehen, öffnen sich zum Ende der Seite.![alt-text](/help/migrated/administrators/feature-summary/assets/module-access-time4.png)
7. Wählen Sie für jeden Abschnitt ein Von-Datum, eine Von-Uhrzeit, ein Bis-Datum und eine Bis-Uhrzeit aus.
8. Wählen Sie **Speichern**. ALM zeigt die Meldung &quot;Zuordnung erfolgreich gespeichert&quot; an.










