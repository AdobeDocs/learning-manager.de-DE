---
jcr-language: en_us
title: Probleme bei der Anmeldung in Learning Manager
description: Probleme beim Anmelden im Adobe Learning Manager
contentowner: nluke
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 87%

---



# Probleme bei der Anmeldung in Learning Manager

## Problem

Die Anmeldung bei Adobe Learning Manager ist nicht möglich.

## Fehler

Bei der Anmeldung bei Adobe Learning Manager wird die folgende Fehlermeldung angezeigt:

![](assets/cp-error.png)

*Fehlermeldung für eine abgelaufene Sitzung*

## Ursache

Wenn sich ein Benutzer über SSO anmeldet, wird ein Sitzungs-Cookie erstellt, das im Browser gespeichert wird. Außerdem kann sich der Benutzer damit bei anderen Anwendungen anmelden. Die meisten SSOs sind so konfiguriert, dass nach 24 Stunden eine Abmeldung erfolgt. Der Benutzer muss sich für eine neue Sitzung erneut authentifizieren.

In bestimmten Fällen kann ein Benutzer aufgrund veralteter SSO-Cookies nicht auf das System zugreifen. Diese Cookies werden zur Authentifizierung an Adobe Learning Manager weitergeleitet. Die Sitzung wird nicht beendet, wenn ein Benutzer den Browser lange nicht schließt oder sich nicht abgemeldet hat.

Adobe Learning Manager lehnt diese veralteten Cookies ab, was zu einem Fehler führt.

## Auflösung

Wenn ein veraltetes Cookie von Adobe Learning Manager abgelehnt wird, probieren Sie die folgenden Optionen aus:

1. Löschen Sie die Browser-Cookies und den Cache. Weitere Informationen finden Sie in diesem [Dokument](unable-log-in-learning-manager.md).

   Alternativ kann der IDP-Administrator eine erzwungene Abmeldung nach einer bestimmten festgelegten Zeit definieren. Dieser Schritt authentifiziert den Benutzer erneut, um eine neue Sitzung zu starten.

Es gibt andere Gründe, warum dieser Fehler auftritt, aber der oben genannte ist ein häufiges Szenario.

## Referenzlinks:

[Microsoft: Sitzung mit bedingtem Zugriff in einem Leben](https://docs.microsoft.com/de-de/azure/active-directory/conditional-access/howto-conditional-access-session-lifetime)
