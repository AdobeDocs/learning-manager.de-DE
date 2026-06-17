---
jcr-language: en_us
title: Report Builder - Häufig gestellte Fragen
description: Hier erhalten Sie Antworten auf häufig gestellte Fragen zu Adobe Learning Manager Report Builder.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 0%

---


# Report Builder - Häufig gestellte Fragen


**Was ist der Unterschied zwischen einer Vorlage und einem Bericht?**

Vorlagen sind vordefinierte Berichtskonfigurationen, die von Adobe Learning Manager bereitgestellt werden. Sie wurden für gängige Anwendungsfälle entwickelt und können sofort heruntergeladen werden. Sie sind schreibgeschützt. Du kannst sie nicht bearbeiten. Berichte sind Ihre eigenen gespeicherten Konfigurationen. Erstelle ein Template von Grund auf neu, oder dupliziere eine Vorlage, und bearbeite die Kopie. Berichte werden auf der Registerkarte **Berichte** angezeigt. Vorlagen werden auf der Registerkarte **Vorlagen** angezeigt.

**Kann ich eine Vorlage direkt bearbeiten?**

Anzahl Vorlagen sind schreibgeschützt. Um eine Vorlage anzupassen, wählen Sie **Duplizieren** aus, um eine bearbeitbare Kopie zu erstellen. Ihre Änderungen werden als neuer Bericht auf der Registerkarte **Berichte** gespeichert und wirken sich nicht auf die ursprüngliche Vorlage aus.

Doppelte Zeilen werden angezeigt, wenn ein Feld in den Daten eine 1:n-Beziehung zum Hauptdatensatz hat. Übliche Ursachen sind Sitzungen mit mehreren Kursleitern (eine Zeile pro Kursleiter pro Sitzung) und Lernobjekte mit mehreren Autoren. Um dies zu beheben, fügen Sie das Feld mit mehreren Werten, z. B. **Kursleiternamen** oder **Autorenname**, als Spalte hinzu.

**Warum ändert sich die Zeilenreihenfolge zwischen zwei Downloads desselben Berichts?**

Die Berichterstellung verwendet ein verteiltes Abfragesystem. Ohne explizite Sortierung hängt die Zeilenreihenfolge davon ab, welcher Abfrageknoten zuerst Ergebnisse zurückgibt, was sich zwischen den Ausführungen unterscheiden kann. Wenden Sie mindestens eine Sortierung auf Ihren Bericht an, um eine konsistente Ausgabe über mehrere Downloads hinweg zu gewährleisten.

**Warum werden Datumsangaben in UTC angezeigt?**

Report Builder gibt in dieser Version Datumswerte in UTC zurück. Die konfigurierte Zeitzone Ihres Kontos wird in einer zukünftigen Version auf Datumsfelder angewendet. Berücksichtigen Sie bei der Analyse datumsbasierter Daten den UTC-Offset, der für die primäre Zeitzone Ihres Kontos relevant ist.

**Wie lange dauert es, bis neue Registrierungs- oder Abschlussdaten angezeigt werden?**

Report Builder wird aus der Adobe Learning Manager-Datenbank abgerufen, die eine maximale Latenz von etwa 15 Minuten aufweist, nachdem ein Ereignis im System aufgetreten ist. Wenn Sie gerade eine Registrierung oder einen Abschluss aufgezeichnet haben und diese nicht in Ihrem Bericht angezeigt wird, warten Sie mindestens 15 Minuten und laden Sie sie erneut herunter.

**Gibt es eine Beschränkung für Zeilen oder Spalten in einem Bericht?**

Berichte sind auf ca. 1 Million Zeilen beschränkt. Die Anzahl der Spalten in dieser Version ist nicht begrenzt. Wenn Ihr Bericht mehr als 1 Million Zeilen erfordert, wenden Sie Filter an, um den Bereich einzugrenzen.

**Kann ich Report Builder-Daten über eine API oder Automatisierung abrufen?**

Der automatisierte API-Zugriff auf Report Builder-Berichte ist für eine zukünftige Version geplant. In der aktuellen Version werden Berichte manuell über die Report Builder-Benutzeroberfläche heruntergeladen oder regelmäßig über die Abonnementfunktion empfangen.
