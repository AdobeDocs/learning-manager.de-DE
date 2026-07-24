---
jcr-language: en_us
title: Externes Lernen in Adobe Learning Manager senden
description: Manager können externe Lernanforderungen überprüfen, die von ihren Teammitgliedern eingereicht wurden, die Details und den Abschlussnachweis überprüfen und jede Anforderung mit einem optionalen Kommentar genehmigen oder ablehnen. Genehmigte Einreichungen werden dem Teilnehmertranskript hinzugefügt.
contentowner: saghosh
source-git-commit: 2495d33fc1595bd962ba07988123e3563d4c69a0
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 1%

---


# Externe Lernanforderungen als Manager prüfen

Wenn ein Teilnehmer in Ihrem Team eine externe Lernanforderung in Adobe Learning Manager sendet, erhalten Sie eine plattforminterne Benachrichtigung. Sie können die Übermittlungsdetails überprüfen, die Anforderung genehmigen oder ablehnen und einen Kommentar für den Teilnehmer hinzufügen.

## Funktionsweise des Manager-Überprüfungsarbeitsablaufs

Wenn ein Teilnehmer eine externe Lernanforderung sendet, geschieht Folgendes:

1. Sie erhalten eine **In-App-Benachrichtigung**, in der Sie aufgefordert werden, die Übermittlung zu überprüfen. Die Übermittlung wird auf der Registerkarte **Externes Lernen** in Ihrem Manager-Dashboard angezeigt.
2. Sie öffnen eine Übermittlung, überprüfen alle Felder und alle hochgeladenen Dokumente als Nachweis und wählen **Genehmigen** oder **Ablehnen**.
3. Sie können einen **Überprüfungskommentar** hinzufügen, den der Teilnehmer sieht, wenn er seine Benachrichtigung erhält.
4. Der Teilnehmer erhält eine **plattforminterne Benachrichtigung** mit Ihrer Entscheidung.

Wenn Sie eine Übermittlung genehmigen, wird die externe Lernaktivität zum **Admin-Teilnehmertranskript** hinzugefügt und im Teilnehmertranskriptdatensatz angezeigt.

<!--You can also change a previously **Rejected** submission to **Approved** if the circumstances change.-->

## Einreichung überprüfen und genehmigen oder ablehnen

1. Melden Sie sich bei Adobe Learning Manager als Manager an.

2. Wählen Sie im linken Navigationsbereich **Externes Lernen**.

3. Wählen Sie in der Übermittlungsliste die zu überprüfende Anforderung aus. Einreichungen werden nach dem Sendedatum sortiert - die zuletzt versendete Einsendung steht hierbei ganz oben.

4. Vollständige Überprüfung der Einreichung:

   - Titel, Beschreibung, Daten, Dauer und Punktzahl

   - Alle benutzerdefinierten Felder, die von Ihrem Administrator konfiguriert wurden

   - Das beigefügte Proof-Dokument, sofern vorhanden. Wählen Sie den Anhang zum Anzeigen oder Herunterladen aus.

5. Wählen Sie **Genehmigen** oder **Ablehnen**.

6. Geben Sie im Feld **Prüfkommentar** Anmerkungen für den Teilnehmer ein. Dies ist optional, wird aber empfohlen, wenn eine Anforderung abgelehnt wird. Der Teilnehmer weiß also, was zu korrigieren ist.

7. Wählen Sie **Senden**.

Der Teilnehmer erhält eine In-App-Benachrichtigung über Ihre Entscheidung. Wenn Sie die Einreichung genehmigt haben, wird sie jetzt im Teilnehmertranskript angezeigt.

## Einreichungswarteschlange verwalten

Ihre Warteschlange für externes Lernen zeigt alle ausstehenden und früheren Einreichungen aus Ihren direkten Berichten an.

**Nach Status filtern**

Verwenden Sie den **Status**-Filter, um die Liste einzugrenzen:

- **Alle**- zeigt jede Übermittlung unabhängig vom Status an

- **Überprüfung wird erwartet-** zeigt nur Übermittlungen an, die Ihre Überprüfung ausstehen.

- **Genehmigt-** zeigt bereits genehmigte Einreichungen an

- **Abgelehnt-** zeigt Einreichungen an, die Sie abgelehnt haben

**Suchen und Sortieren**

- Verwenden Sie das Feld **Suchen**, um Einreichungen nach Teilnehmernamen zu suchen.

- Einreichungen werden standardmäßig nach dem Sendedatum sortiert, wobei die zuletzt versendete Einsendung ganz oben steht.

### Genehmigungsroutingregeln

Standardmäßig werden externe Lernobjektübermittlungen an den direkten Manager eines Teilnehmers geleitet. Die folgenden Regeln gelten, wenn einem Teilnehmer kein direkter Manager zugewiesen ist:

| **Teilnehmer hat einen Manager** | **Teilnehmer ist selbst ein Manager** | **Übermittlung an** weitergeleitet |
|---------------------------|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Ja | Nein | Direkter Manager (Standardfall) |
| Ja | Ja | Direkter Manager (Standardfall) |
| Nein | Nein | Stammkontobenutzer, wenn der Stammkontobenutzer über eine Managerrolle verfügt; Andernfalls wird die Übermittlung automatisch genehmigt. |
| Nein | Ja | Stammkontobenutzer, wenn der Stammkontobenutzer über eine Managerrolle verfügt; Andernfalls wird die Einreichung an den Teilnehmer weitergeleitet. |

Wenn Sie Fragen zur Managerzuweisung für einen bestimmten Teilnehmer haben, wenden Sie sich an Ihren Kontoadministrator.

## Berichte zu externen Lernprogrammen und Änderungen an Transkripten

Wenn die externe Lernübermittlung eines Teilnehmers in Adobe Learning Manager genehmigt wird, wird die Aktivität dem Berichtssystem hinzugefügt und sowohl im Admin-Teilnehmertranskript als auch im Teilnehmertranskript angezeigt.

### Wie externes Lernen in Teilnehmertranskripten angezeigt wird

**Hinweis:** Durch Aktivieren des externen Lernens werden dem Teilnehmertranskript des Administrators die folgenden neuen Spalten hinzugefügt: **Name für externes Lernen**, **Abschlusskommentar** und eine dynamische Spalte für jedes benutzerdefinierte Feld. Benutzerdefinierte Feldspalten werden immer am Ende des Exports angezeigt. Wenn Daten aus dem Teilnehmertranskript in automatisierte Reporting- oder BI-Tools eingespeist werden, stellen Sie sicher, dass diese Pipelines aktualisiert werden, um die zusätzlichen Spalten zu verarbeiten.

Nur **genehmigte** externe Lernobjekte werden in Transkripten angezeigt. Einreichungen im Status &quot;**Genehmigung erwartet**&quot; oder &quot;**Abgelehnt**&quot; sind nicht in den Transkriptexporten enthalten.

Das Admin-Teilnehmertranskript und das Teilnehmertranskript behandeln den externen Lerntitel unterschiedlich:

- Im **Admin-Teilnehmertranskript** wird der externe Lerntitel in der vorhandenen **LP/Certification/Course**-Spalte platziert, wobei die Spaltenstruktur mit anderen Lernaktivitätstypen konsistent bleibt.

- Im **Teilnehmertranskript** (vom Teilnehmer generiert) wird unmittelbar nach der Spalte **Modul** eine neue Spalte mit dem Namen **Externer Lernname** hinzugefügt.

Von Ihrem Administrator konfigurierte benutzerdefinierte Felder werden nach Genehmigung einer Einreichung als dynamische Spalten am Ende beider Transkript-Exporte angezeigt.

Die datumsbasierte Filterung im Admin-Teilnehmertranskript für externe Lernzeilen basiert auf dem **Abschlussdatum**, das dem Genehmigungsdatum entspricht.