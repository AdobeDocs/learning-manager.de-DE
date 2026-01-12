---
jcr-language: en_us
title: Fehlerbehebung für Probleme mit der Integration von Salesforce (SFDC) in Adobe Learning Manager
description: Beheben Sie häufige Salesforce(SFDC)-Integrationsprobleme mit Adobe Learning Manager (ALM), einschließlich fehlgeschlagener Exporte, Feldberechtigungsprobleme in benutzerdefinierten SFDC-Objekten und wichtige SFDC-ALM-Kompatibilitätshinweise.
contentowner: saghosh
source-git-commit: cedb4acc89e7d972a4752e10c4fb6930c4633f6a
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---


# Fehlerbehebung für Probleme mit der Integration von Salesforce (SFDC) in Adobe Learning Manager

## Fehlerbehebung bei SFDC-Exportfehlern (kein Export für 2-3+ Stunden)

Wenn der SFDC-Export seit mehr als **2-3 Stunden** nicht erfolgreich abgeschlossen wurde, verwenden Sie die folgenden Schritte, um das Problem zu identifizieren und zu verstehen.

1. Rufen Sie die Seite **Salesforce-Startseite** auf.
2. Geben Sie im Suchfeld **Schnellsuche** **`Bulk Data Load Jobs`** ein, und öffnen Sie es.
3. Auf der Seite werden Massendatenladeaufträge für die **letzten 7 Tage** angezeigt.
4. Suchen Sie nach Aufträgen, die mit **Adobe Learning Manager (ALM)-Objekten** verknüpft sind.
5. Klicken Sie auf den spezifischen Job, den Sie untersuchen möchten.
6. Scrollen Sie zum **Ende** der Einzelvorgangsseite, um die **Fehlermeldung** und zusätzliche Details anzuzeigen.

In vielen Fällen ist die Ursache **unzureichende Berechtigungen auf Feldebene in SFDC**. Der fehlerhafte Feldname könnte wie folgt aussehen:

- `cp_Module_ID`
- oder andere `cp_...` Felder, die sich auf benutzerdefinierte ALM-Objekte beziehen.

Wenn solche Felder im Fehler angezeigt werden, fahren Sie mit dem nächsten Abschnitt fort.

## Gewähren von Feldberechtigungen für benutzerdefinierte ALM-Objektfelder in SFDC

Verwenden Sie die **Funktion Eingabehilfen für Felder**, um Berechtigungsprobleme für bestimmte Felder zu beheben (z. B. `cp_Module_ID`).

### Schritte

1. Rufen Sie die Seite **Salesforce-Startseite** auf.
2. Geben Sie im Suchfeld **Schnellsuche** **`Field Accessibility`** ein, und öffnen Sie es.
3. Wählen Sie aus der Liste der Objekte den entsprechenden **Berichtstyp/das entsprechende**-Objekt aus.
   - Beispiel: `cp_LearnerTranscript_xxxx_xxxx` für den Teilnehmertranskriptbericht (LT).
4. Wählen Sie auf der nächsten Seite **&quot;Nach Feldern anzeigen&quot;**.
5. Wählen Sie in der Dropdown-Liste **Feld** das Feld aus, das im Exportfehler angezeigt wurde.
   - Beispiel: `cp_Module_ID`.
6. Klicken Sie in der Zugriffsmatrix auf den Eintrag **&quot;Hidden&quot;** für das Profil **Systemadministrator** (und andere relevante Profile, falls erforderlich).
7. Auf der nächsten Seite:
   - Aktivieren Sie **&quot;Visible&quot;**, wo immer dies angemessen ist.
   - Klicken Sie unten auf der Seite auf **Speichern**.
8. Nach dem Speichern kehren Sie zur Eingabehilfeansicht des Felds zurück. Das Feld sollte jetzt als **&quot;Bearbeitbar&quot;** für **Systemadministrator** (und alle anderen von Ihnen aktualisierten Profile) angezeigt werden.

## Wiederholen Sie diesen Vorgang für alle betroffenen Felder und wiederholen Sie den Export.

1. **Wiederholen** Sie die Schritte zur Barrierefreiheit der Felder in Abschnitt 2 für **jedes Feld**, für das in **Massendatenladeaufträgen** Berechtigungsprobleme gemeldet wurden.
2. Sobald alle problematischen Felder über die entsprechende Sichtbarkeit und Bearbeitungsberechtigungen verfügen:
   - Wechseln Sie zurück zu **Adobe Learning Manager**.
   - Versuchen Sie in der Konfiguration **SFDC-Connector** **den Export erneut**.


## Wichtige Hinweise und Einschränkungen

Berücksichtigen Sie diese SFDC-ALM-Spezifikationen beim Entwurf oder bei der Fehlerbehebung von Integrationen.

### Keine automatische Objekt-/Felderstellung in SFDC

- Der **SFDC-Connector erstellt keine neuen Objekte oder Felder in Salesforce**.
- Wenn ein **neues Feld in ALM** hinzugefügt wird und in SFDC angezeigt werden soll:
   - Erstellen Sie manuell **das entsprechende benutzerdefinierte Feld** in SFDC.
   - **Ordnen Sie das benutzerdefinierte SFDC-Feld dem** entsprechenden ALM-Feld **in der Connector-Konfiguration zu.**
   - Stellen Sie sicher, dass das neue Feld über **Berechtigungen auf Feldebene** verfügt (verwenden Sie Abschnitt 2).

### Rückruf-URL für ALM-Konten mit benutzerdefinierten Domänen

- Wenn das ALM-Konto eine **benutzerdefinierte Domäne** verwendet, muss das Engineering-Team diese benutzerdefinierte Domäne **der zulässigen** Rückruf-URL **für die OAuth-Produktions-App des SFDC-Connectors hinzufügen.**
- Dies erfolgt über eine **Jira-Anforderung** an das Engineering.
- Andernfalls kann der OAuth-Flow für den Connector fehlschlagen.

### Zeitzonenbegrenzung (nur UTC)

- Wenn die SFDC-Organisation eine andere **-Zeitzone als UTC** verwendet, können **Abschluss- und Registrierungsdaten während der Synchronisierung verpasst werden**.
- Grund: ALM **unterstützt derzeit nur die UTC-Zeitzone** für die SFDC-Integration.
- Interne Referenz: PAPI-24525 wird ausgelöst, um zusätzliche Zeitzonen zu unterstützen.

### Einschränkung des Datentyps filtern (Auswahlliste vs. Checkliste)

- ALM unterstützt das Importieren von **SFDC-Filtern, die mit Auswahllistenfeldern erstellt wurden**.
- ALM **unterstützt keine**-Filter, die auf Checklisten-/Mehrfachauswahl-Kontrollkästchenfeldern basieren.
- Grund: ALM **unterstützt nur Zeichenfolgendatentypen** für SFDC-Filter.
