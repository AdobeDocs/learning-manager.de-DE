---
description: Wie Abrechnungspläne bestimmen, ob Konten lizenzierte Lizenzen gemeinsam nutzen können, und was geschieht mit der gemeinsamen Nutzung von Beziehungen, wenn sich ein Abo ändert?
jcr-language: en_us
title: Tiering - Sitzfreigabe
exl-id: 42b4cba4-1e44-40d8-aa57-ce2a855be258
source-git-commit: 34d4e6fb6583eed0dd3a46126c28284c58210078
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%
---

# Freigabe von Lizenzen und Kontoabonnements in Adobe Learning Manager

Über die Freigabe von Lizenzen kann ein Konto einen Teil seiner lizenzierten Lizenzen für ein anderes Konto freigeben, sodass Teilnehmer im Empfängerkonto über Lizenzen im Freigabekonto auf Adobe Learning Manager zugreifen können. Welche Konten Lizenzen gemeinsam nutzen können und mit wem, hängt vom Abrechnungsplan ab, auf dem jedes Konto basiert.

## Welche Abos unterstützen die gemeinsame Nutzung von Lizenzen?

Die Freigabe von Lizenzen ist für Konten im **Ultimate**-Plan verfügbar. Konten im **Prime**-Abo können keine Lizenzen mit einem anderen Konto teilen und keine freigegebenen Lizenzen von einem anderen Konto erhalten.

Konten, die mit Kreditkarte belastet werden, sind standardmäßig im Prime-Abo enthalten und können daher nicht an der gemeinsamen Nutzung der Lizenzen teilnehmen.

Testkonten sind die eine Ausnahme: Ein Testkonto kann freigegebene Lizenzen von einem Ultimate -Konto erhalten. Während eine aktive Freigabebeziehung besteht, hat das Testkonto Zugriff auf die Ultimative-Level-Funktion.

## Sichtbarkeit von Peer-Konten festlegen

Die Einstellung für das Peer-Konto wird in der Admin-App des Kontos angezeigt, das diese Funktion verwendet.

>[!NOTE]
>
>Wenn Ihr Konto Lizenzen mit zusätzlichen Konten teilt, die über das Konto hinausgehen, von dem Sie Lizenzen erhalten, z. B. wenn Ihr Konto den gemeinsamen Zugriff zusammen mit einem dritten Konto übergibt, muss jedes Konto in dieser Kette zum Teilen im Ultimativen Plan enthalten sein, damit die Freigabe von Anfang bis Ende fortgesetzt werden kann.

## Kontokombinationen, die die Freigabe von Lizenzen unterstützen

Die folgende Tabelle zeigt, ob die gemeinsame Nutzung von Lizenzen zwischen verschiedenen Kombinationen von Kontoabonnements möglich ist.

| Freigabekonto (übergeordnetes Konto) | Empfangskonto (untergeordnetes Konto) | Freigabe unterstützt? |
|---|---|---|
| Prime (beliebige) | Beliebig | Nein, die Freigabe von Lizenzen ist auf Konten mit dem Ultimate-Abo beschränkt |
| ultimativ | ultimativ | Ja |
| ultimativ | Prime- | Nein, Plankonflikt |
| ultimativ | Ein Kreditkartenkonto | Nein, Abonnementkonflikt, da Konten mit Kreditkartenabrechnung im Prime-Abo enthalten sind |
| ultimativ | Test | Ja, das Testkonto erhält Ultimativen Zugriff, während die Beziehung aktiv ist |

>[!NOTE]
>
>Einige zusätzliche Einschränkungen für die gemeinsame Nutzung von Lizenzen zwischen bestimmten Kontokonfigurationen können unabhängig vom Abo-Typ gelten, z. B. basierend darauf, wie das Abonnement eines Kontos ursprünglich eingerichtet wurde. Wenn Sie keine Freigabebeziehung zwischen zwei Ultimate-Konten herstellen können, wenden Sie sich an den Adobe-Support, um Ihre Kontokonfiguration zu bestätigen.

## Was passiert mit der Freigabe von Lizenzen, wenn ein Abo geändert wird?

Die Berechtigung zur Freigabe von Lizenzen wird bei der Verlängerung bewertet. Wenn sich der Plan eines Kontos in einer Weise ändert, die sich auf eine vorhandene Freigabebeziehung auswirkt, geschieht Folgendes:

* Wenn das Abo eines freigebenden (übergeordneten) Kontos bei der Verlängerung von Ultimate auf Prime geändert wird, enden die bestehenden Beziehungen zur Freigabe von Lizenzen.
* Wenn das empfangende Konto über ein eigenes, unabhängiges Abonnement verfügt, ist dieses Abonnement hiervon nicht betroffen. nur die Freigabebeziehung selbst wird beendet.
* Wenn es sich bei dem empfangenden Konto um ein Testkonto handelt, das auf dem Ultimativen Zugriff des übergeordneten Kontos basiert, wird es auf den Zugriff auf Prime-Ebene zurückgesetzt, sobald die Freigabebeziehung beendet ist.

Diese Änderungen werden bei der nächsten Verlängerung des Kontos für bestehende ALM-Konten wirksam, nicht sofort während einer aktiven Vertragslaufzeit. Diese gelten jedoch nicht für neue Konten, die erstellt werden, nachdem die Tiering-Funktion live gegangen ist.

>[!NOTE]
>
>Konten, die mit Kreditkarte belastet werden und derzeit über Zugriff auf die höchste Stufe verfügen, wechseln ab der nächsten Verlängerung zum Prime-Abo. Wenn ein solches Konto zu diesem Zeitpunkt über aktive Beziehungen zur gemeinsamen Nutzung von Lizenzen verfügt, enden diese Beziehungen als Teil desselben Übergangs.
