---
description: Weitere Informationen zu Teilnehmertranskripten
jcr-language: en_us
title: Änderungen an Teilnehmertranskripten
exl-id: 295c4e1f-c3c7-4f97-83c3-1234f3d47546
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%
---
# Änderungen an Teilnehmertranskripten in der April-Version

## Spalte &quot;Abschlussmethode&quot;

Die Spalte **Abschlussmethode** zeigt an, wie jeder Datensatz im Teilnehmertranskript des Administrators abgeschlossen wurde.

**Werte:**

1. **Direkt** (für direkte Abschlüsse)
2. **Alternate** (für Abschlüsse, die über alternative Beziehungen erzielt werden)
3. **Alternativer Widerruf** (wenn alle alternativen Abschlüsse aufgrund rückwirkender Unvollständigkeit und Beziehungsentfernung widerrufen werden)

>[!NOTE]
>
>Diese Spalte ist im LT des Teilnehmers nicht sichtbar. es ist nur in der Admin LT für Berichts- und Verfolgungszwecke verfügbar.

**Auswirkung**: Ermöglicht klare Audit-Verläufe, Compliance-Verfolgung und Transparenz für Administratoren in Bezug auf den Abschluss eines Kurses.

## Verfolgung des alternativen Abschlusses in Teilnehmertranskripten

Mit alternativen Abschlüssen können Teilnehmer einen Abschlusskredit für einen Zielkurs oder Lernpfad erhalten, wenn sie einen gleichwertigen Quellkurs oder -pfad basierend auf eingerichteten Beziehungen abgeschlossen haben.

Im Teilnehmertranskript (LT) wirken sich alternative Abschlüsse auf drei vorhandene Spalten aus: **Status**, **Abschlussdatum** und **Abschlussquelle**.

- **Status**: Der Status kann **Abgeschlossen** sein, auch wenn der Teilnehmer den Zielkurs oder -pfad aufgrund eines alternativen Abschlusses nicht direkt abgeschlossen hat. Andere Status (**Nicht gestartet**, **In Bearbeitung**, **Nicht registriert**) sind nicht betroffen.
- **Abschlussdatum**: Für den alternativen Abschluss wird das Datum vom Quellkurs oder -pfad geerbt. Wenn der Teilnehmer das Ziel später direkt abschließt, wird das Datum aktualisiert, um den direkten Abschluss widerzuspiegeln.
- **Vervollständigungsquelle**: Erfasst die Schulungs-ID(s) des/der Quellkurse oder -pfade, der/die den alternativen Abschluss bereitgestellt hat/haben. Mehrere aktive Quellen werden als durch Kommas getrennte IDs aufgelistet. Wenn Quellen widerrufen werden, verbleiben nur noch aktive. Wenn mehrere Quellen vorhanden sind, wird das früheste Abschlussdatum verwendet.

**Auswirkung**: Alternative Abschlüsse reduzieren die manuelle Abstimmung, automatisieren die Fortschrittsverfolgung bei Lernpfaden und Zertifizierungen und unterstützen Compliance-Anforderungen.

>[!NOTE]
>
>Teilnehmertranskripte zeigen die Spalte **Abschlussmethode** nicht an. Diese Spalte ist nur im Admin-Teilnehmertranskript verfügbar.

## Abschlussdatumslogik für Stellvertreter

Die Spalte **Abschlussdatum** im Teilnehmertranskript wird sowohl für den direkten als auch für den alternativen Abschluss verwendet.

- Bei alternativen Abschlüssen spiegelt das Datum wider, wann der Teilnehmer den Quellkurs oder -pfad abgeschlossen hat.
- Wenn der Teilnehmer das Ziel später direkt abschließt, wird das Abschlussdatum auf das direkte Abschlussdatum aktualisiert.
- Es wird keine neue Spalte für alternative Abschlussdaten eingefügt.
- Wenn mehrere Quellen einen alternativen Abschluss bereitstellen, wird das früheste aktive Abschlussdatum verwendet.
- Wenn eine Quelle widerrufen wird (bei aktivierter retroaktiver Unvollständigkeit), wird das Datum auf die nächstliegende aktive Quelle aktualisiert oder gelöscht, wenn keine aktiven Quellen mehr vorhanden sind.

**Auswirkung**: Stellt eine genaue historische Verfolgung und konsistentes Reporting sicher, selbst wenn sich im Laufe der Zeit alternative Beziehungen ändern.

## Widerrufene alternative Abschlüsse

Widerrufene alternative Abschlüsse treten auf, wenn alle Quellbeziehungen für einen Zielkurs oder Lernpfad entfernt werden, sofern die retroaktive Unvollständigkeit aktiviert ist.

### Auslösebedingungen

- Die retroaktive Unvollständigkeit muss auf Kontoebene aktiviert werden.
- Der Widerruf tritt nur auf, wenn **alle** aktiven Quellbeziehungen entfernt werden.
- Wenn mindestens eine Quelle verbleibt, bleibt die alternative Vervollständigung bestehen und die Spalte der Vervollständigungsquelle wird entsprechend aktualisiert.

### Auswirkungen auf das Teilnehmertranskript

- **Status**: Wenn alle alternativen Abschlüsse widerrufen werden und kein direkter Abschluss vorhanden ist, wird der Status aktualisiert (z. B. von **Abgeschlossen** auf **Nicht gestartet** oder **In Bearbeitung**).
- **Abschlussdatum**: Wird gelöscht, wenn keine aktiven Quellen vorhanden sind und kein direkter Abschluss erfolgt.
- **Vervollständigungsquelle**: Aktualisiert, um widerrufene Quellen zu entfernen wird gelöscht, wenn alle Quellen widerrufen werden.

Wenn der Teilnehmer einen direkten Abschluss hat, wirkt sich das Widerrufen alternativer Quellen nicht auf den Abschlussstatus oder das Abschlussdatum aus.

>[!NOTE]
>
>Wenn mehrere Quellen einen alternativen Abschluss bereitstellen und nur einige widerrufen werden, spiegelt das Transkript die verbleibenden aktiven Quellen und ihr frühestes Abschlussdatum wider. Wenn alle Quellen widerrufen werden und kein direkter Abschluss vorhanden ist, verliert der Teilnehmer den Abschlussstatus für das Ziel.

## Verbesserte Berichterstellung für Anmerkungen von Checklisten-Reviewern

Reviewerkommentare aus Checklistenmodulen sind jetzt im Teilnehmertranskriptbericht unter einer umbenannten Spalte mit dem Namen **Reviewerbemerkungen.** enthalten.

| Bereich | Alter Spaltenname | Neuer Spaltenname | Anmerkungen |
|------|-----------------|-----------------|-------|
| Teilnehmertranskripte (Administrator) | Einreichungskommentar | Anmerkungen des Reviewers | Gilt für alle Admin LT-Quellen: Benutzeroberfläche, Job-API, Verbindungen. |

Diese Änderung gilt einheitlich für alle Admin LT-Quellen (UI-Exporte, Job API-Berichte und Verbindungen, sofern zutreffend). Bei einer von der Verbindung exportierten LT werden die Anmerkungen des Reviewers am Ende als separate Spalte angezeigt (bei Verbindungen, die den Übermittlungskommentar nicht gelegt haben). So wird sichergestellt, dass bei der Integration in den Downstream das Feedback des Reviewers von anderen Kommentaren unterschieden werden kann.

**Auswirkung:** Teilnehmer und Administratoren können konsolidiertes Feedback anzeigen, wodurch die Transparenz verbessert und die Leistungsbewertung unterstützt wird.

>[!NOTE]
>
>Für die Teilnehmertranskripte für Teilnehmer wird die Spalte, die zuvor mit **Übermittlungskommentar** beschriftet war, jetzt in **Anmerkungen des Reviewers** umbenannt und mit dem Kommentar des Checklisten-Reviewers ausgefüllt, wenn dieser aktiviert ist.

## Verbesserte Berechnung der Lernzeit

Der Teilnehmertranskriptbericht verwendet jetzt eine verfeinerte Logik, um zwischen aktiver und inaktiver Lernzeit basierend auf Benutzeraktivität und Fokus auf Browserregisterkarten zu unterscheiden.

**Auswirkung**: Bietet präzisere Messungen der Interaktion mit Teilnehmern und unterstützt Compliance-Berichte und -Analysen.
