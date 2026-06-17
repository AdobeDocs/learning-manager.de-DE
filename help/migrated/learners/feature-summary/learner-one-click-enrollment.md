---
description: Mit einer Anmeldung mit einem Klick können Teilnehmer auf einen beliebigen Deep-Link zu einem von Administratoren freigegebenen Modul klicken und sofort auf den Inhalt zugreifen, ohne mehrere Schritte durchlaufen zu müssen, um auf "Registrieren" zu klicken und dann den Kurs zu starten. Dadurch sparen Sie Zeit und der Kurszugriff wird verbessert.
jcr-language: en_us
title: Registrierung mit einem Klick in Adobe Learning Manager verwenden
contentowner: mmanuel
source-git-commit: 87971737d1d9838d8b29035b5b9bf718742da1eb
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 1%

---


# Registrierung mit einem Klick für Adobe Learning Manager

Erhalten Sie den Deep-Link von Ihrem Administrator per E-Mail, Chat oder über eine andere Messaging-Plattform, um sich für ein Schulungsmodul oder einen Kurs zu registrieren. Wählen Sie den Link aus, um sich sofort zu registrieren und das Modul ohne zusätzliche Schritte zu starten.

## Registrieren Sie einen Teilnehmer und leiten Sie ihn zum Kurs weiter.

Beachten Sie die folgenden Szenarien und die entsprechenden Aktionen. Wenn Sie als Teilnehmer auf den Deep-Link klicken, der an Sie gesendet wurde, geschieht je nach Szenario, in dem Sie sich befinden, eine der folgenden Aktionen:

| SN | Szenario | Aktion |
| --- | --- | --- |
| 1 | Kurs mit einem Modul und ungeordnet | Sie werden automatisch registriert und der Player wird geöffnet. Sie müssen auf &quot;Abspielen&quot; klicken, um das Video abzuspielen. |
| 2 | Kurs mit mehreren Modulen und ungeordnet | Sie werden automatisch registriert und landen auf dem bestimmten Modul, mit dem der Deep-Link verknüpft ist. Sie müssen auf &quot;Abspielen&quot; klicken, um das Video abzuspielen. |
| 3 | Kurs mit mehreren Modulen und Bestellung | Sie gelangen auf die Übersichtsseite mit einer Meldung, die besagt, dass Sie die vorhergehenden Kurse abschließen müssen, bevor Sie den aktuellen beginnen, falls Sie die vorhergehenden nicht abgeschlossen haben. In diesem Fall werden Sie automatisch registriert und landen auf dem ersten Modul des Kurses. |
| 4 | Der Kurs hat Voraussetzungen | Wenn die Voraussetzungen erfüllt sind, können Sie das Modul im Player starten. Drücken Sie die Taste Abspielen , um das Video abzuspielen. Wenn sie nicht abgeschlossen sind, wird die folgende Meldung angezeigt: &quot;Vorausgesetzte Kurse können nicht übersprungen werden. Bitte füllen Sie alle erforderlichen Kurse aus, bevor Sie mit diesem Kurs beginnen. |
| 5 | Kurs mit Warteliste | Sie werden registriert. Sie gelangen auf die Kursübersichtsseite und werden der Warteliste hinzugefügt. Außerdem wird eine Meldung angezeigt, dass der Kurs auf der Warteliste steht. |
| 6 | Wenn Sie bereits für den Kurs registriert sind, für den ein Deep Link generiert wird. | Sie landen auf dem Modul und der Player wird gestartet. Drücken Sie die Taste Abspielen , um das Video abzuspielen. |

## Authentifizierungsstatus und Deep-Link-Verhalten

Zusätzlich zu den oben genannten Szenarien gibt es zwei weitere Benutzerverhalten, die sich auf den Authentifizierungsstatus (angemeldet und abgemeldet) beziehen.

* Wenn Sie auf einen Deep-Link klicken und nicht bei Adobe Learning Manager angemeldet sind, werden Sie zur Anmeldeseite weitergeleitet. Melden Sie sich an, und der Deep-Link leitet Sie zum entsprechenden Modul weiter.

* Wenn Sie auf einen Deep-Link klicken und bei Adobe Learning Manager angemeldet sind, werden Sie direkt zum Modul weitergeleitet.

## Immersive Unterstützung für Mobilgeräte und Web

Die folgenden Szenarien gelten sowohl für die Mobil- als auch für die Webversion von Adobe Learning Manager.

* Wenn Sie nicht über die Desktopversion von Adobe Learning Manager verfügen und einen Deep-Link erhalten, werden Sie durch Auswahl des Links auf die Anmeldeseite von Adobe Learning Manager in Ihrem Browser weitergeleitet, wenn Sie nicht bei der Web- oder Mobilversion angemeldet sind.
* Wenn Sie nicht über die Desktopversion von Adobe Learning Manager verfügen und einen Deep-Link erhalten, werden Sie durch Auswahl des Links direkt zum Adobe Learning Manager-Modul in Ihrem Browser weitergeleitet, sofern Sie bereits in der Web- oder mobilen Version angemeldet sind.

## Automatische Wiedergabe mit Browsereinschränkung

Wenn Sie auf einen Deep-Link klicken, werden Sie zu einem Modul oder einer Anmeldeseite weitergeleitet, wenn Sie nicht angemeldet sind. Wenn es sich bei dem Modul um ein Video handelt, wird das Video vom Player nicht automatisch abgespielt. In allen Fällen verhindert der Browser, dass der Player das Video automatisch abspielt. Sie müssen die Taste &quot;Manuell abspielen&quot; drücken, um das Video abzuspielen.
