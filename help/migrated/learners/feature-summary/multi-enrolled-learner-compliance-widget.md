---
description: Erfahren Sie, wie das Widget "Teilnehmer-Compliance" jede registrierte Instanz eines Kurses mit mehreren Registrierungen auflistet, für den eine Frist gilt, und wie die API dies unterstützt
jcr-language: en_us
title: Mehrfach registrierte Kurse, die im Widget "Teilnehmerkonformität" angezeigt werden
exl-id: 6484c815-ecae-4a75-ba10-ef42e4ff50a6
source-git-commit: d762bc8f199b703169878acbb52d0d7e3e0d6973
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 1%
---

# Mehrere registrierte Kurse im Widget &quot;Teilnehmerkonformität&quot;

In Adobe Learning Manager kann ein Teilnehmer für mehrere Instanzen desselben Kurses registriert werden. Das Widget &quot;Teilnehmer-Konformität&quot; listet jetzt jede registrierte Instanz auf, für die eine Frist gilt. Teilnehmer sehen daher jedes Fälligkeitsdatum, nicht nur die primäre Instanz.

## Was ändert sich für Kurse mit mehreren Registrierungen?

Vor dieser Änderung zeigte das Kompatibilitäts-Widget nur die primäre Instanz eines Kurses an, für den mehrere Teilnehmer registriert waren. Ein Teilnehmer, der in mehreren Instanzen registriert war, konnte die Fristen für die anderen im Widget nicht sehen.

Jetzt werden im Widget &quot;Konformität&quot; alle Instanzen angezeigt, die diese Bedingungen erfüllen:

* Der Teilnehmer wird für die Instanz registriert.
* Für die Instanz gilt eine Frist.
* Der Teilnehmer hat die Instanz nicht abgeschlossen.

In jedem Eintrag wird der Instanzname angezeigt, sodass die Teilnehmer Instanzen desselben Kurses unterscheiden können. Wenn ein Teilnehmer einen Eintrag auswählt, öffnet Adobe Learning Manager diese Instanz direkt.

Ein Teilnehmer absolviert beispielsweise einen ersten Schulungskurs. Ein Administrator registriert den Teilnehmer später bei der September-, Oktober- und November-Ausgabe desselben Kurses, wobei für jede Version ein Abgabetermin gilt. Das Kompatibilitäts-Widget listet alle drei Versionen auf.

Das Widget zählt jede Instanz separat in jeder Kompatibilitätskategorie: **Überfällig**, **Baldiger Termin innerhalb der nächsten 30 Tage** und **On-track**.

## Instanzen, die im Kompatibilitäts-Widget angezeigt werden

In der folgenden Tabelle wird beschrieben, wie das Widget jede Registrierungssituation behandelt.

| Registrierungssituation | Wird im Widget angezeigt | Hinweise |
|--------------------------------------------------|-----------------------------------|---------------------------------------|
| Registriert, Instanz hat Frist, nicht abgeschlossen | Ja | Mit dem Instanznamen angezeigt |
| Registriert, Instanz hat keine Frist | Nein | Es werden nur Instanzen mit einer Deadline angezeigt |
| Instanz abgeschlossen | Nein | Eine abgeschlossene Instanz wird nicht aufgeführt. |
| Abgeschlossen in allen registrierten Instanzen | Nein | Der Kurs wird nicht mehr angezeigt |
| Eine Instanz mit einer Frist und eine ohne | Nur die Instanz mit einer Frist |                                       |
| Nur eine registrierte Instanz | Ja | Das Widget zeigt diese Instanz an |

API-Informationen finden Sie unter [API-Unterstützung für Instanzen, für die mehrere Teilnehmer registriert sind, in der Teilnehmer-App ](/help/migrated/api-changes-dec-2026.md#multi-enrolled-compliance-widget).
