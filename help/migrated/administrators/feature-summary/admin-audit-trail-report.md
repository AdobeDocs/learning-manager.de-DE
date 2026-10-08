---
description: Erfahren Sie, wie der Administrator-Audit-Bericht Konfigurationsänderungen verfolgt und anzeigt, wer sie wann vorgenommen hat und welche Werte davor und danach festgelegt wurden.
jcr-language: en_us
title: Administratorprüfprotokollbericht
exl-id: 71b2ee42-ef1c-47fb-95ad-c339562e227d
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '1085'
ht-degree: 0%
---

# Administratorprüfprotokollbericht {#adminaudittrailreport}

Erstellen Sie einen Bericht mit Konfigurationsänderungen, die an den Einstellungen für &quot;Grundlagen&quot;, &quot;Erweitert&quot; und &quot;Integration&quot; Ihres Kontos vorgenommen wurden. Dieser Bericht enthält auch Informationen dazu, wer jede Änderung wann und wann vorgenommen hat und welchen Wert Sie davor und danach festgelegt haben.

## Was der Bericht erfasst

Der Administrator Audit Trail-Bericht enthält einen historischen Datensatz mit Konfigurationsänderungen, sodass Sie Folgendes feststellen können:

- Wer hat die Änderung vorgenommen?
- Wann wurde die Änderung vorgenommen?
- Wie war die Einstellung vor der Änderung?
- Die Einstellung nach der Änderung

Der Bericht behandelt Änderungen an:

- **Grundlegendes** Einstellungen
- **Erweiterte** Einstellungen
- **Integrationen** Einstellungen

Der Bericht enthält nur ergänzende Angaben: Neue Änderungsdatensätze werden im Laufe der Zeit hinzugefügt und zuvor aufgezeichnete Einträge werden nie entfernt. Auf diese Weise können Sie den gesamten Verlauf einer Einstellung über mehrere Änderungen hinweg überprüfen, nicht nur den aktuellen Wert.

Der Bericht steht jedem Benutzer mit Berichtsberechtigungen und vollständigem Zugriff auf Benutzergruppen zur Verfügung. Dies schließt vollständige Administratoren und benutzerdefinierte Administratoren ein, denen Berichtszugriff gewährt wurde.

>[!NOTE]
>
>Datensätze sind ab Update 12, September 2026 verfügbar. Änderungen, die vor dieser Aktualisierung vorgenommen wurden, sind nicht im Bericht enthalten. Siehe [Versionshinweise](/help/migrated/release-note/release-notes.md) Update 112.

## Warum dieser Bericht für die Compliance wichtig ist

Unternehmen, die in regulierten Branchen tätig sind, müssen häufig nachweisen, dass Konfigurationsänderungen an Systemen, die elektronische Datensätze verarbeiten, nachverfolgt, zurechenbar und gespeichert werden. Der Administrator-Audit-Bericht unterstützt diese Anforderungen, indem er die Person, die Einstellung, die Zeit und die Vorher- und Nachher-Werte für jede Änderung identifiziert.

>[!NOTE]
>
>Dieser Bericht unterstützt die Compliance-Aktivitäten Ihrer Organisation. Sie bescheinigt allein nicht die Einhaltung spezifischer Vorschriften oder Normen.

## Erstellen eines Administratorprüfprotokollberichts

1. Melden Sie sich bei Adobe Learning Manager als Administrator an.
2. Wählen Sie in der linken Navigation **Verwalten** > **Berichte** > **Benutzerdefinierte Berichte**.

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report1.png)

3. Scrollen Sie nach unten und wählen Sie **Administratorprüfpfad**.

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report2.png)

4. **Bereich auswählen**: Wählen Sie den Berichtszeitraum für — **Letzte Woche**, **Letzter Monat** oder **Daten auswählen**. Wenn Sie **Daten wählen**, geben Sie ein **Von**-Datum und ein **Bis**-Datum ein.
5. **Einstellungstyp auswählen**: Wählen Sie **Alle auswählen**, **Grundlagen**, **Integrationen** oder **Erweitert**.

   Um die vollständige Liste der Einstellungen anzuzeigen, die von diesem Bericht über &quot;Grundlagen&quot;, &quot;Integrationen&quot; und &quot;Erweitert&quot; verfolgt werden, wählen Sie **Einstellungsliste herunterladen**.

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report6.png)

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report3.png)

6. Wählen Sie **Generieren**.

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report4.png)

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report5.png)

Eine `.csv`-Datei mit den Änderungen wird in den Ordner Downloads Ihres Browsers heruntergeladen. Die Berichterstellung kann einen Moment dauern - Sie können Adobe Learning Manager weiterhin verwenden, während es verarbeitet wird. Wenn Sie das Browserfenster schließen, bevor der Bericht fertig ist, beginnt der Download bei der nächsten Anmeldung.

## Häufige Verwendungszwecke für diesen Bericht

- **Eine unerwartete Einstellungsänderung untersuchen** — Bestätigen Sie, was sich wann geändert hat und wer die Änderung vorgenommen hat, anstatt sich auf Annahmen zu verlassen.
- **Von mehreren Administratoren vorgenommene Änderungen überprüfen** — Erstellen Sie eine konsolidierte Ansicht aller Konfigurationsaktivitäten, die für einen bestimmten Zeitraum im Berichtsbereich liegen, anstatt jeden Administrator einzeln zu kontaktieren.
- **Genehmigte Konfigurationsänderung bestätigen** — Überprüfen Sie, ob der erwartete Administrator die Änderung innerhalb des erwarteten Zeitraums vorgenommen hat und ob der neue Wert mit dem genehmigten Wert übereinstimmt.
- **Verlauf einer Einstellung mit mehreren Änderungen vergleichen** — Verwenden Sie die Spalte **Revision**, um zu sehen, wie oft eine bestimmte Einstellung geändert wurde, und prüfen Sie jeden aufgezeichneten Wert in der Reihenfolge, einschließlich, ob eine spätere Änderung einen früheren Wert wiederhergestellt hat.
- **Unterstützung einer Kompatibilitätsprüfung** — Generieren Sie den Bericht für den zu überprüfenden Zeitraum als Teil Ihrer administrativen und Kompatibilitätsdatensätze.
- **Einstellungen nach einer Richtlinienänderung überprüfen** — Überprüfen Sie, ob die beabsichtigten Konfigurationsupdates konsistent angewendet wurden, und ermitteln Sie alle unerwarteten Änderungen.
- **Verlaufsdatensatz verwalten** — Laden Sie Berichte gemäß den Methoden zur Datensatzverwaltung Ihres Unternehmens herunter, und bewahren Sie sie auf.

## Berichtsspaltenreferenz

Die heruntergeladene `.csv`-Datei enthält die folgenden Spalten.

| Spalte | Beschreibung |
|---|---|
| **Ereignis-ID** | Eine eindeutige Identifizierung für diesen spezifischen Änderungsdatensatz. |
| **Zeitstempel (UTC)** | Datum und Uhrzeit der Änderung in der koordinierten Weltzeit. |
| **E-Mail** | Die E-Mail-Adresse des Administrators, der die Änderung vorgenommen hat. |
| **UUID** | Eine eindeutige Identifizierung für den Administrator, der die Änderung vorgenommen hat. Wird nur ausgefüllt, wenn die UUID auf Kontoebene aktiviert ist. |
| **Administratorname** | Der Anzeigename des Administrators, der die Änderung vorgenommen hat. |
| **Ereignistyp** | Die aufgezeichnete Ereigniskategorie, z. B. `Modify`, `Create` oder `Delete`. |
| **Aktionstyp** | Der Typ der für die Einstellung ausgeführten Aktion, z. B. `CREATE_SETTING`, `UPDATE_SETTING` oder `DELETE_SETTING`. |
| **Objekttyp** | Das geänderte Einstellungs- oder Konfigurationsobjekt. |
| **Objekt-ID** | Die eindeutige Identifizierung der spezifischen Einstellung oder des Konfigurationsobjekts, die bzw. das geändert wurde. |
| **Vorheriger Wert** | Der Wert der Einstellung vor der Änderung. (Bei einer gelöschten Einstellung wird hier der Wert angezeigt, der vor dem Löschen vorhanden war.) |
| **Neuer Wert** | Der Wert der Einstellung nach der Änderung. (Bei einer gelöschten Einstellung ist diese leer.) |
| **Revision** | Gibt an, wie oft diese bestimmte Objekt-ID geändert wurde, wenn das Ereignis aufgezeichnet wird. Die erste aufgezeichnete Änderung für ein Objekt beginnt bei 1. |

>[!TIP]
>
>Um alle Einstellungen zu suchen, die während eines Zeitraums gelöscht wurden, filtern Sie die heruntergeladene Datei, wobei **Aktionstyp** `DELETE_SETTING` ist.

## Programmgesteuerter Zugriff auf diesen Bericht

Sie können den Administrator-Audit-Bericht programmgesteuert über die Jobs-API abrufen, anstatt ihn manuell über die Admin-App zu generieren. Dies ist nützlich, wenn Sie regelmäßige Exporte planen oder den Bericht in ein nachgelagertes Überwachungs- oder Warnsystem einspeisen möchten. Siehe [Bericht über den API-Administratorprüfpfad für Aufträge](/help/migrated/api-changes-sep-2026.md#job-api-for-admin-audit-trail-report).

## Einschränkungen

- **Lokalisierung**: Berichtsinhalt ist nicht lokalisiert. Der Bericht wird unabhängig von den konfigurierten Gebietsschemaeinstellungen Ihres Kontos in der Standardkontensprache generiert.
- **Grund für die Änderung**: Im Bericht wird nicht erfasst, warum eine Änderung vorgenommen wurde. Bewahren Sie alle zugehörigen Änderungsanforderungen, Genehmigungen oder geschäftlichen Begründungen separat auf.

## Best Practices

- Wählen Sie einen Datumsbereich aus, der die vermutete oder geplante Änderung abdeckt.
- Wählen Sie **Alle auswählen**, wenn der betroffene Einstellungsbereich nicht bekannt ist.
- Vergleichen Sie die Spalten **Vorheriger Wert** und **Neuer Wert** für jeden Eintrag.
- Verwenden Sie die Spalten **Administratorname** und **Zeitstempel**, um eine Änderung mit genehmigten Arbeits- oder internen Datensätzen zu korrelieren.
- Lassen Sie die entsprechende Änderungsanforderung, Genehmigung oder geschäftliche Begründung separat aufbewahren, wenn Ihr Unternehmen eine dokumentierte Erklärung für eine Änderung benötigt.

## Fehlerbehebung

**Ich sehe keine Datensätze vor einem bestimmten Datum.**
Datensätze sind nur ab Update 112 (September 2026) verfügbar. Änderungen, die vor dieser Aktualisierung vorgenommen wurden, sind nicht im Bericht enthalten. Siehe [Versionshinweise](/help/migrated/release-note/release-notes.md)

**Die UUID-Spalte ist für einige oder alle Datensätze leer.**
Die Spalte UUID wird nur ausgefüllt, wenn UUID auf Kontoebene aktiviert ist. Wenn sie nicht aktiviert ist, wird diese Spalte nicht angezeigt.

**Ich habe eine benutzerdefinierte Administratorrolle, aber ich kann diesen Bericht nicht finden**
Vergewissern Sie sich, dass Ihrer benutzerdefinierten Rolle Berichtsberechtigungen und der vollständige Zugriff auf Benutzergruppen gewährt wurden. Wenden Sie sich an Ihren Kontoinhaber oder einen vollständigen Administrator, um diesen Zugriff bei Bedarf anzufordern.
