---
jcr-language: en_us
title: Häufige Fragen (Report Builder)
description: Hier erhalten Sie Antworten auf häufig gestellte Fragen zu Adobe Learning Manager Report Builder.
contentowner: mmanuel
source-git-commit: 8823a5481bc3b34266f7ec36a8f3c26cb923e1ce
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---


# Häufige Fragen (Report Builder)

**Was ist der Unterschied zwischen einer Vorlage und einem Bericht?**

Vorlagen sind vordefinierte Berichtskonfigurationen, die von Adobe Learning Manager bereitgestellt werden. Sie wurden für gängige Anwendungsfälle entwickelt und können sofort heruntergeladen werden. Sie sind schreibgeschützt. Du kannst sie nicht bearbeiten. Berichte sind Ihre eigenen gespeicherten Konfigurationen. Erstelle ein Template von Grund auf neu, oder dupliziere eine Vorlage, und bearbeite die Kopie. Berichte werden auf der Registerkarte **Berichte** angezeigt. Vorlagen werden auf der Registerkarte **Vorlagen** angezeigt.

**Kann ich eine Vorlage direkt bearbeiten?**

Anzahl Vorlagen sind schreibgeschützt. Um eine Vorlage anzupassen, wählen Sie **Duplizieren** aus, um eine bearbeitbare Kopie zu erstellen. Ihre Änderungen werden als neuer Bericht auf der Registerkarte **Berichte** gespeichert und wirken sich nicht auf die ursprüngliche Vorlage aus.

Doppelte Zeilen werden angezeigt, wenn ein Feld in den Daten eine 1:n-Beziehung zum Hauptdatensatz hat. Übliche Ursachen sind Sitzungen mit mehreren Kursleitern (eine Zeile pro Kursleiter pro Sitzung) und Lernobjekte mit mehreren Autoren. Um dies zu beheben, fügen Sie das Feld mit mehreren Werten, z. B. **Kursleiternamen** oder **Autorenname**, als Spalte hinzu.

**Warum werden Datumsangaben in UTC angezeigt?**

Report Builder gibt in dieser Version Datumswerte in UTC zurück. Die konfigurierte Zeitzone Ihres Kontos wird in einer zukünftigen Version auf Datumsfelder angewendet. Berücksichtigen Sie bei der Analyse datumsbasierter Daten den UTC-Offset, der für die primäre Zeitzone Ihres Kontos relevant ist.

**Wie lange dauert es, bis neue Registrierungs- oder Abschlussdaten angezeigt werden?**

Report Builder wird aus der Adobe Learning Manager-Datenbank abgerufen, die eine maximale Latenz von etwa 15 Minuten aufweist, nachdem ein Ereignis im System aufgetreten ist. Wenn Sie gerade eine Registrierung oder einen Abschluss aufgezeichnet haben und diese nicht in Ihrem Bericht angezeigt wird, warten Sie mindestens 15 Minuten und laden Sie sie erneut herunter.

**Gibt es eine Beschränkung für Zeilen oder Spalten in einem Bericht?**

Berichte sind auf ca. 1 Million Zeilen beschränkt. Die Anzahl der Spalten in dieser Version ist nicht begrenzt. Wenn Ihr Bericht mehr als 1 Million Zeilen erfordert, wenden Sie Filter an, um den Bereich einzugrenzen.

**Gibt es eine Dateigrößenbeschränkung beim Exportieren von Berichten von Report Builder?**

Derzeit werden exportierte Berichtsdateien, die größer als 5 GB sind, im Report Builder nicht unterstützt. Wenn Ihr Bericht diese Größe voraussichtlich überschreitet, sollten Sie zusätzliche Filter anwenden oder die Anzahl der Zeilen reduzieren, damit der Export unter 5 GB bleibt.

**Kann ich Report Builder-Daten über eine API oder Automatisierung abrufen?**

Der automatisierte API-Zugriff auf Report Builder-Berichte ist für eine zukünftige Version geplant. In der aktuellen Version werden Berichte manuell über die Report Builder-Benutzeroberfläche heruntergeladen oder regelmäßig über die Abonnementfunktion empfangen.
