---
title: Entsprechungen und Stellvertreter in Adobe Learning Manager
description: Bieten Sie ein reibungsloses Lernerlebnis und eliminieren Sie redundante Schulungen mit Entsprechungen und Alternativen in ALM. Mit dieser neuen Funktion können Administratoren unidirektionale (alternierende) oder bidirektionale (äquivalente) Regeln konfigurieren, bei denen durch das Absolvieren einer Schulung automatisch ein alternativer Abschluss für eine andere erteilt wird
jcr-language: en-us
exl-id: 6bdd6ba7-e5a6-462a-8385-66b955ef25fc
source-git-commit: 4a4c42968caf6c0c8265014d99a2211da4c1cbb9
workflow-type: tm+mt
source-wordcount: '3457'
ht-degree: 0%

---

# Alternativen und Äquivalente

## Einführung

In vielen Organisationen stoßen die Teilnehmer auf Schulungssituationen, in denen verschiedene Kurse die gleiche Anforderung rechtmäßig erfüllen können. Wann sollte beispielsweise ein neuer Kurs einen älteren ersetzen? Wann sollte ein umfassenderer Kurs für einen kürzeren Kurs oder wann sollte ein spezieller Ersatzkurs angeboten werden?

Mit der Funktion &quot;Alternativer Kurs oder Lernpfad&quot; hat ALM eine formelle Möglichkeit, Folgendes zu sagen:

&quot;Wenn der Teilnehmer diese Schulung abgeschlossen hat, behandeln Sie ihn so, als hätte er die entsprechende Schulungsanforderung erfüllt.&quot;

Die Funktion funktioniert über Kurse und Lernpfade hinweg, stellt sicher, dass nachgelagerte Anforderungen wie Voraussetzungen und Compliance-Regeln eingehalten werden, und tut dies, ohne die Teilnehmer zu zwingen, sich durch redundante Inhalte zu bewegen. Darüber hinaus wird die Genauigkeit der Berichte beibehalten, indem aufgezeichnet wird, was direkt abgeschlossen wurde und was über eine Alternative erfüllt wurde.

Im Kern führt die Funktion das Konzept eines alternativen Abschlusses ein: ein spezieller Abschlussstatus, der automatisch erstellt wird, wenn ein Teilnehmer eine konfigurierte Quellschulung abschließt, die auf eine andere Zielschulung angerechnet wird.

## Alternative Beziehungen

Einige Trainingsbeziehungen sind bidirektional, d. h. jeder Kurs kann die Anforderungen des anderen erfüllen. Dies ist im Grunde ein Szenario, bei dem zwei Schulungen als gegenseitig austauschbar behandelt werden. Im Gegensatz dazu erlauben unidirektionale Beziehungen es einem Training, die Anforderungen an ein anderes zu erfüllen, aber nicht umgekehrt. ALM modelliert beide Szenarien mit demselben zugrunde liegenden alternativen Abschlussmechanismus.

* **Bidirektionale Beziehung (Entsprechungen):** Das Abschließen einer der Schulungen erfüllt die Anforderungen für die andere.
* **Unidirektionale Beziehung:** Das Abschließen von Schulung A erfüllt Schulung B, aber das Abschließen von B erfüllt A nicht. Dies ist häufig der Fall, wenn eine neuere oder umfassendere Version auf eine ältere Anforderung angerechnet werden sollte, aber nicht umgekehrt.

Zum Beispiel, wenn ein umfassenderer Superset-Kurs alles in einem einfacheren Unterset-Kurs abdeckt. Das Ausfüllen der Obermenge sollte die Anforderungen für die Untermenge erfüllen, aber nicht unbedingt umgekehrt.

Ein neuer, erweiterter Kurs, der auf eine ältere Anforderung angerechnet werden sollte.

Ein Kurs, der für eine bestimmte Zielgruppe entwickelt wurde (z. B. eine regionale oder barrierefreiheitsangepasste Variante), der immer noch die gleiche Anforderung erfüllt wie der Hauptkurs.

Eine verbesserte neue Version eines Kurses, die das Unternehmen für eine ältere Anforderung berücksichtigen möchte, aber die ältere Version sollte nicht für die neue Anforderung berücksichtigt werden.

Bei Alternativen ist die Beziehung normalerweise eine Möglichkeit. Wenn Kurs A ein Alternativkurs zu Kurs B ist, kann Abschluss A die Anforderung von B erfüllen, aber Abschluss B erfüllt nicht unbedingt A.

Wenn eine konfigurierte Quellschulung abgeschlossen ist, erstellt ALM automatisch eine alternative Abschlussfunktion für eine oder mehrere Zielschulungen.

## Welche Probleme werden dadurch gelöst?

Ohne Alternativen stehen Administratoren und Teilnehmer vor mehreren wiederkehrenden Problemen:

* Teilnehmer werden häufig aufgefordert, Kurse zu wiederholen, in denen Inhalte behandelt werden, die sie bereits in einer anderen Version oder einem anderen Format abgeschlossen haben.
* Die Aktualisierung von Compliance-Programmen ist einfacher, da Administratoren Schulungen ersetzen oder umstrukturieren können, ohne Teilnehmer, die ältere Versionen abgeschlossen haben, zwingen zu müssen, alternative oder ersetzte Inhalte erneut aufzunehmen.
* Die erforderliche Logik ist starr. Wenn ein Weg einen bestimmten Kurs als Voraussetzung erfordert, gibt es keine klare Möglichkeit zu erkennen, dass eine andere Schulung gut genug ist.
* Berichterstattung und Prüfungen sind schwieriger. Es gibt kein förmliches Signal dafür, dass eine Anforderung durch einen alternativen Abschluss erfüllt wurde, und es gibt keine einfache Möglichkeit, die Quelle des Kredits zu ermitteln.

Die Funktion &quot;Alternative&quot; behebt diese Probleme wie folgt:

* Vermeidung doppelter Anstrengungen für Teilnehmer, wenn Alternativen gültig sind.
* Administratoren können Schulungsstrukturen ändern (z. B. einen Kurs innerhalb eines Pfads austauschen), ohne die Abschlüsse von Teilnehmern zu brechen, die die frühere Version verwendet haben.
* Zulassen von Voraussetzungen und Konformitätsprüfungen, um sowohl direkte als auch alternative oder gleichwertige Abschlüsse zu berücksichtigen.
* Klarere Aufzeichnung in Transkripten und Berichten, ob eine Schulung direkt abgeschlossen oder über eine alternative Beziehung abgeschlossen wurde, zusammen mit der Schulung als Quelle.

## Konzeptionelle Funktionsweise der Funktion

Die Funktion basiert auf drei Hauptideen: **Beziehungen**, **Alternativer Abschluss** und **Downstream-Verhalten**.

### Beziehungen zwischen Schulungen

Administratoren definieren die Beziehungen zwischen Kursen und Lernpfaden. Für jede Beziehung wählen sie eine Quelle und ein oder mehrere Ziele. Ein einzelner Kurs kann bis zu 30 Ziele haben, je nachdem, wie viele frühere oder zugehörige Schulungen er erfüllen sollte.

Bei Entsprechungen können Administratoren die Beziehung bidirektional machen, wenn sie möchten, dass beide Schulungen einander entsprechen. Bei Stellvertretern behalten Administratoren die Richtung in der Regel einseitig, um zu reflektieren, dass nur einige Ersetzungen zulässig sind.

Diese Beziehungen werden auf der Schulungsebene gespeichert, nicht auf der Teilnehmerebene. Nach der Konfiguration und Aktivierung können diese   für alle aktuellen und zukünftigen Abschlüsse der Quellschulung, abhängig von Einstellungen auf Konto*Ebene, z. B. ob die retroaktive Vervollständigung aktiviert ist.

### Alternativer Abschluss

Wenn ein Teilnehmer eine Quellschulung abschließt, überprüft ALM alle konfigurierten alternativen Beziehungen und erstellt für jede relevante Zielschulung einen alternativen Abschlussdatensatz. Dieser Datensatz unterscheidet sich von einem normalen Abschluss:

* Es markiert die Zielschulung für den Teilnehmer, verfolgt aber, dass die Schulung über Alternativen und nicht direkt abgeschlossen wurde.
* Er zeichnet auf, welche Quellschulung verwendet wurde, um das Ziel zu erreichen.
* Es wird in einer speziellen Struktur gespeichert, sodass Berichte zwischen direkten und alternativen Abschlüssen unterscheiden können.

Teilnehmer sehen einen alternativen Abschluss, auch wenn sie nicht registriert sind. Der Bericht &quot;Teilnehmertranskript (LT)&quot; enthält nur Datensätze von Schulungen, für die sich der Teilnehmer registriert hat.

#### Teilnehmer-App-Erlebnis für alternative und gleichwertige Abschlüsse

Alternative Abschlüsse werden in der Teilnehmer-App deutlich angezeigt, sodass die Teilnehmer klar verstehen können, wie eine Schulungsanforderung erfüllt wurde, und gleichzeitig die Konsistenz mit Transkripten und Berichten gewahrt bleibt.

#### LO-Kartenverhalten

##### Alternativer Abschlussstatus

Wenn ein Teilnehmer eine Schulung über eine alternative Beziehung abschließt, zeigt die Lernobjektkarte (LO) einen eindeutigen Status an, der **Abgeschlossen über Alternative** lautet. Diese visuelle Unterscheidung hilft Teilnehmern dabei, zwischen direkten Abschlüssen und Abschlüssen zu unterscheiden, die durch konfigurierte Beziehungen gewährt werden.

#### Abschlussmethodenindikator

Die LO-Karte enthält eine Abschlussmethodenanzeige (z. B. eine Beschriftung oder ein Symbol), um anzuzeigen, dass der Abschluss über eine Alternative erreicht wurde. Wenn ein alternativer Abschluss später widerrufen wird, weil Änderungen wie der rückwirkende Abschluss oder das Löschen der Quellschulung vorgenommen wurden, macht ALM alle Änderungen an der Benutzeroberfläche rückgängig, die es für den alternativen Abschluss vorgenommen hat. Der Teilnehmer kann weiterhin kein LO gemäß dem aktuellen Katalogzugriffsverhalten als Ziel angeben.

#### Transparenz und Audit-Details

Teilnehmer können die LO-Karte öffnen, um zusätzliche Details anzuzeigen, darunter:

* Der Quellkurs oder Lernpfad, der den alternativen Abschluss gewährte

Dies gewährleistet Transparenz.

#### Filtern und Ansichten

##### Vervollständigungsmethodenfilter

Die Teilnehmer-App bietet einen Filter, mit dem Teilnehmer zwischen folgenden Optionen unterscheiden können:

* Abgeschlossen
* Über alternative Abschlüsse abgeschlossen (filtert LOs, die nur alternative Abschlüsse aufweisen). Wenn ein LO sowohl einen alternativen als auch einen direkten Abschluss hat, wird es nicht einbezogen.)
* Wenn Sie **Abgeschlossen** und **Abgeschlossen über Alternative** auswählen, können Sie alle Abschlüsse anzeigen.

Dadurch können die Teilnehmer schnell nachvollziehen, wie ihre Lernanforderungen erfüllt wurden.

##### Transkript- und Fortschrittsansichten

Der Filter für die Abschlussmethode ist in den Ansichten mit den Teilnehmern verfügbar. Beispiel:

* Verfolgungsabschnitte für Fortschritt und Abschluss

Aus diesen Ansichten geht eindeutig hervor, welche Schulungen direkt abgeschlossen wurden und welche über Stellvertreter absolviert wurden.

<!--
## Configure equivalent courses (complete each other)

Use this workflow to define courses that are **equal in value**, where completing either course should automatically complete the other.

1. Launch ALM and navigate to courses.
2. Select a course to configure.
3. Navigate to the **Alternates** section.
4. Search for and select one or more related courses.
5. For each selected course, enable **Completes each other**.
6. Save the configuration.

**Result**

- ALMm records a **bi-directional equivalence relationship**.
- Either course can act as a completion source for the other.

## Configure alternate courses (superset → subset)

Use this workflow when one course is a **superset** of another and should satisfy completion for the simpler or subset course.

1. Launch ALM and navigate to courses.
2. Select the **superset (primary)** course.
3. Go to the **Alternates** section.
4. Select one or more **alternate (subset)** courses.
5. Leave the relationship as **alternate** (do not enable completes each other).
6. Save the configuration.

**Result**

- Completion flows **one-way** from the source course to the alternate.
- Reverse completion is not applied.

## Apply completion logic after source course completion

Automatically evaluate and apply alternate or equivalent completion once a learner completes a configured source course. ALM:

1. Detects completion of a **source course**.
2. Evaluates configured relationships:
   - Equivalent relationships
   - Alternate relationships
3. For each related course:
   - Marks the course as completed if conditions are met
4. Creates a completion record with method **Alternate**.

**Key system rules**

- Alternate completion:
  - Satisfies prerequisites
  - Allows progress in learning paths and certifications
- Alternate completion does **not** award:
  - Skills
  - Badges
  - Gamification credits

## Record completion in Learning Transcript

Ensure alternate and equivalent completions are clearly distinguishable from direct completions for audit and reporting. ALM:

1. Updates the **Learner Transcript (LT)**.
2. Sets:
   - Completion status = Completed
   - Completion method = **Alternate**
3. Sets completion date equal to the **source course completion date**.

## Enable retroactive completion (optional)

Apply alternate or equivalent completion benefits to learners who completed source courses **before** the relationships were configured.

1. Open **Account-level settings** from Administrator home > Settings > General.
2. Enable **Retroactive completion**.
3. Save the configuration.

ALM:

1. Scans historical learner completions.
2. Applies alternate or equivalent completion where applicable.
3. Updates learner transcripts automatically.

## Enable retroactive incompletion (irreversible)

Revoke previously applied alternate or equivalent completions when relationships are removed or corrected.

1. Open **Account-level settings**.
2. Enable **Retroactive incompletion**.
3. Modify or remove alternate/equivalent relationships.

ALM:

1. Identifies impacted alternate completions.
2. Revokes previously applied alternate or equivalent completions.
3. Updates transcript entries to **Alternate (Revoked)**.
-->

### Durchgehender Textfluss

**Für Teilnehmer**

1. Navigieren Sie in der Teilnehmer-App zu **Eigenes Lernen** oder **Abgeschlossene Kurse**.
2. Überprüfen Sie LO-Karten, um Schulungen zu identifizieren, die als **Abgeschlossen über Alternate** markiert sind.
3. Öffnen Sie eine LO-Karte, um (auf der Seite &quot;Übersicht&quot;) Details zur Quellschulung anzuzeigen.
4. Verwenden Sie den Filter, um **Direct**, **Alternate** oder **All** auszuwählen.
5. Überprüfen Sie die aktualisierte Liste basierend auf der ausgewählten Abschlussmethode.

**Für Administratoren und Autoren**

* Konfigurieren Sie alternative Beziehungen zwischen Kursen oder Lernpfaden in der Administratoroberfläche.

## Verhalten für rückwirkende Vervollständigung und Unvollständigkeit

ALM unterstützt den retroaktiven Abschluss und die retroaktive Unvollständigkeit, um sicherzustellen, dass alternative Beziehungen im Laufe der Zeit genau bleiben, auch wenn Beziehungen geändert oder entfernt werden, nachdem die Teilnehmer die Schulung bereits abgeschlossen haben.

### Rückwirkende Fertigstellung

#### Definition

Wenn der retroaktive Abschluss aktiviert ist, erhalten Teilnehmer, die einen Quellkurs in der Vergangenheit abgeschlossen haben, automatisch einen alternativen Abschluss für den Zielkurs, wenn später eine alternative Beziehung erstellt wird. Dadurch wird sichergestellt, dass das historische Lernen berücksichtigt wird, ohne dass die Teilnehmer eine Schulung erneut absolvieren müssen.

#### Funktionsweise

1. Ein Administrator aktiviert die retroaktive Vervollständigung auf Kontoebene.
2. Der Administrator definiert eine alternative Beziehung zwischen einer Quell- und einer Zielschulung.
3. Das System scannt die historischen Abschlussdatensätze für die Quellschulung.
4. Berechtigte Teilnehmer erhalten einen alternativen Abschluss für die Zielschulung.
5. Diese Datensätze werden in Teilnehmertranskripten und Berichten als **Abgeschlossen über Alternate** angezeigt.

>[!NOTE]
>
>Wenn die retroaktive Vervollständigung aktiviert ist, gilt sie nur für Beziehungen, die danach erstellt werden. Sie gilt nicht für Beziehungen, die bereits vor der Aktivierung der retroaktiven Einstellung bestanden.

### Rückwirkende Unvollständigkeit

#### Definition

Wenn die retroaktive Unvollständigkeit aktiviert ist, werden alternative Abschlüsse widerrufen, wenn die zugrunde liegende alternative Beziehung entfernt wird oder wenn die Quellschulung gelöscht wird.
Dadurch wird sichergestellt, dass das System die aktuellen und gültigen Schulungsverhältnisse widerspiegelt.

#### Funktionsweise

1. Ein Administrator aktiviert die rückwirkende Unvollständigkeit auf Kontoebene.
2. Der Administrator entfernt eine alternative Beziehung oder löscht die Quellschulung.
3. Das System identifiziert Teilnehmer, die über die betroffene Beziehung einen alternativen Abschluss erhalten haben.
4. Die entsprechenden alternativen Abschlussdatensätze werden widerrufen.
5. Widerrufene Datensätze werden in Transkripten und Berichten zur Audit-Sichtbarkeit als **Alternate (Widerrufen)** markiert.

#### Auswirkungen auf Voraussetzungen

Alternative Abschlüsse - auch rückwirkend gewährte - werden bei der Bewertung von Voraussetzungen als gültige Abschlüsse behandelt. Wenn ein Teilnehmer **Abgeschlossen über Alternate** hat, kann er mit Kursen fortfahren, die die Zielschulung erfordern.

Wenn ein alternativer Abschluss später durch eine rückwirkende Unvollständigkeit widerrufen wird, verliert der Teilnehmer möglicherweise die Berechtigung für Kurse, die von dieser Voraussetzung abhängen. Wenn der Teilnehmer das abhängige/nachfolgende LO nicht gestartet hat, wird die vom Quell-LO verwaltete Berechtigung zurückgesetzt. Wenn der Teilnehmer bereits ein abhängiges/nachfolgendes LO gestartet oder abgeschlossen hat, hat dies keine Auswirkungen.

#### Auswirkungen auf Lernpfade und Zertifizierungen

Alternative Abschlüsse tragen zum Abschluss von Lernpfaden und unbefristeten Zertifizierungen bei. Teilnehmer können diese Programme erweitern oder abschließen, wenn die erforderlichen Schulungen über alternative Beziehungen absolviert werden.

Wenn ein alternativer Abschluss widerrufen wird, verlieren die betroffenen Lernpfade oder Zertifizierungen möglicherweise den Fortschritt, bis die Anforderung durch einen gültigen Abschluss erfüllt wird.

### Durchgängiger Arbeitsablauf

#### Aktivieren der retroaktiven Vervollständigung oder Unvollständigkeit

1. Administratoren navigieren zu den Kontoeinstellungen und aktivieren die rückwirkende Fertigstellung und/oder die rückwirkende Nicht-Fertigstellung.
2. Administratoren erstellen, ändern oder entfernen alternative Beziehungen zwischen Schulungen.

#### Systemaktionen

* **Für den rückwirkenden Abschluss**:
Das System gewährt alternative Abschlüsse auf der Grundlage historischer Quellenabschlüsse.
* **Für rückwirkende Unvollständigkeit**:
Das System widerruft alternative Abschlüsse, wenn Beziehungen entfernt oder Quelltrainings gelöscht werden.

#### Teilnehmererlebnis

Teilnehmer sehen aktualisierte Abschlussstatus auf LO-Karten und in Transkripten, z. B.:

* **Abgeschlossen über Alternative**

Wenn ein alternativer Abschluss widerrufen wird, wird auf der Teilnehmer-Benutzeroberfläche keine Beschriftung angezeigt. In Berichten und Transkripten werden Abschlussmethoden wie folgt angezeigt:

* Alternative
* Alternative (Widerrufen)
* Direkt

Voraussetzungsprüfungen, der Fortschritt des Lernpfads und der Zertifizierungsstatus werden basierend auf dem aktuellen Abschlussstatus dynamisch aktualisiert.

Bestellte LOs werden basierend auf der alternativen Fertigstellung dynamisch entsperrt.

Kenntnisse, Abzeichen, Gamification-Punkte oder Feedback werden den Teilnehmern nach dem alternativen Abschluss der Ziele nicht zugewiesen.

#### Berichterstattung und Prüfung

Alle rückwirkenden Änderungen werden im Bericht &quot;Teilnehmertranskript (LT)&quot; widergespiegelt. Nachdem die Quelle gelöscht wurde, kann im Teilnehmertranskript weiterhin eine Quelltrainings-ID neben **Alternativer widerrufen** angezeigt werden. In den Berichten wird eindeutig unterschieden zwischen direkten und alternativen Abschlüssen und widerrufenen alternativen Abschlüssen, um die Einhaltung der Vorschriften zu unterstützen, Untersuchungen zu unterstützen und Audits durchzuführen.

Der Registrierungsbericht lässt das Feld &quot;Abschlussquelle&quot; leer, wenn der Vorgang direkt abgeschlossen wird, während im Teilnehmertranskript die E-Mail-Adresse und der Typ dafür angezeigt werden.

Wenn ein Ziel aus der Quelle entfernt wird (oder die Quelle selbst gelöscht wird), zeigt der Registrierungsbericht möglicherweise nicht den gleichen Status **Alternate oder Alternate (Revoked)** an, wie im Teilnehmertranskript gezeigt.

Auch wenn   **Alternates** sind deaktiviert. Verlaufseinträge in den Zeilen **Inhaltsüberwachung** oder **Registrierung** zeigen möglicherweise weiterhin Aktivitäten im Zusammenhang mit Alternates an.

Das Abschlussdatum kann dem Registrierungsdatum vorausgehen, wenn ein LO über einen alternativen Pfad **abgeschlossen wird, bevor der Teilnehmer sich tatsächlich registriert**. Da alternative Abschlüsse unabhängig vom Teilnehmerstatus auftreten können (**Registriert**, **Nicht registriert** oder **In Bearbeitung**), können Teilnehmer das LO zuerst abschließen und sich erst später für den Zielkurs registrieren.

## Auswirkungen des Ausscheidens und Löschens von Quellschulungen in Alternativen

Der Lebenszyklusstatus einer Quellschulung (eingestellt oder gelöscht) wirkt sich direkt darauf aus, wie alternative Abschlüsse für Teilnehmer beibehalten werden. ALM behandelt diese Szenarien unterschiedlich, um die historische Genauigkeit zu erhalten und gleichzeitig sicherzustellen, dass die aktuellen Beziehungen gültig bleiben.

### Schulung &quot;Quelle einstellen&quot;

#### Definition

Durch das Einstellen eines Kurses ist dieser für neue Registrierungen nicht mehr verfügbar, während er im System zur historischen Referenz, zur Berichterstellung und zu Prüfzwecken gespeichert wird.

#### Auswirkungen

* Vorhandene alternative Abschlüsse, die über den eingestellten Quellkurs gewährt wurden, bleiben gültig.
* Teilnehmer, die den Quellkurs zuvor abgeschlossen haben, haben weiterhin einen alternativen Abschluss für den Zielkurs.
* Es werden keine neuen alternativen Abschlüsse aus dem eingestellten Kurs generiert, da er von neuen Teilnehmern nicht abgeschlossen werden kann.
* Teilnehmertranskripte und Berichte zeigen weiterhin **Abgeschlossen über alternative** für betroffene Teilnehmer an.

### Quellschulung löschen

#### Definition

Wenn Sie einen Kurs löschen, wird er vollständig aus dem System entfernt, einschließlich der Abschlussdatensätze und der konfigurierten Beziehungen.

#### Auswirkungen

* Wenn eine Quellschulung gelöscht wird, ändert sich der Status möglicherweise in **Alternate (Revoked)**. Das Einstellen eines LO löst diesen Status nicht aus.
* Wenn die retroaktive Unvollständigkeit aktiviert ist, werden alle alternativen Abschlüsse, die über den gelöschten Quellkurs gewährt wurden, widerrufen.
* Teilnehmertranskripte und Berichte werden aktualisiert, um **Alternate (Revoked)** für Audit- und Compliance-Sichtbarkeit anzuzeigen.
* Der Abschluss von Lernpfaden und die Verfügbarkeit von Zertifikaten sind davon nicht betroffen.
* Es können keine weiteren alternativen Abschlüsse aus dem gelöschten Kurs gewährt werden.

#### Arbeitsablauf

1. Ein Administrator beendet den Quellkurs oder löscht ihn über die Administratoroberfläche.
2. Das System wertet alle alternativen Abschlüsse aus, die vom Quellkurs abgeleitet wurden.
3. Der Abschlussstatus wird basierend auf dem Kursstatus aktualisiert:
   * **Eingestellt:** Bestehende alternative Abschlüsse bleiben unverändert.
   * **Gelöscht:** Alternative Abschlüsse werden widerrufen, wenn rückwirkende Unvollständigkeit aktiviert ist.
4. Teilnehmertranskripte und -berichte spiegeln den aktualisierten Status wider, um Compliance- und Audit-Anforderungen zu unterstützen.

## Keine Verkettung von Beziehungen

ALM unterstützt keine Verkettung alternativer Beziehungen. Alternative Abschlüsse werden nur für direkt konfigurierte Beziehungen gewährt und werden nicht auf mehrere Kursebenen übertragen.

### Konzept: keine Verkettung von Beziehungen

#### Definition

Verkettung bezieht sich darauf, dass alternative Beziehungen über mehrere Kurse verteilt werden können. Wenn beispielsweise Kurs A ein Alternativkurs zu Kurs B und Kurs B ein Alternativkurs zu Kurs C ist, würde die Verkettung bedeuten, dass durch Abschluss von Kurs A der Abschluss für Kurs C gewährt wird.

#### Richtlinie

Verkettung wird nicht unterstützt. Alternative und äquivalente Beziehungen werden nur auf einer einzigen Ebene ausgewertet. Wenn Sie einen Quell-Kurs abschließen, wird der alternative Abschluss nur für den oder die unmittelbaren Ziel-Kurse gewährt, nicht für nachgelagerte Ziele.

### Arbeitsablauf

#### Einrichtung der Beziehung

Ein Administrator definiert alternative Beziehungen zwischen Kursen, z. B.:

* Kurs A → Kurs B
* Kurs B → Kurs C

#### Abschlussereignis

Ein Teilnehmer schließt Kurs A direkt ab.

#### Systemaktion

* Das System gewährt den alternativen Abschluss für Kurs B, wenn die Beziehung A → B definiert ist.
* Das System gewährt keinen alternativen Abschluss für Kurs C, selbst wenn eine Beziehung zwischen B → C besteht.

#### Direkte Abschlussanforderung

Um einen alternativen Abschluss für Kurs C zu erhalten, muss der Teilnehmer:

* Kurs B direkt abschließen oder
* Schließen Sie einen Kurs ab, der explizit als direkte Alternative oder gleichwertige Option für Kurs C konfiguriert ist.

## Auswirkungen

### Keine indirekten Vorteile

Teilnehmer können für Kurse, die weiter unten in einer Beziehungskette liegen, keine Abschlussgutschrift erhalten, es sei denn, jeder Kurs (oder seine direkte Alternative) ist abgeschlossen. Dadurch wird sichergestellt, dass die Lernanforderungen explizit und vorhersehbar erfüllt werden.

### Vereinfachte Prüfung und Berichterstattung

Berichte und Teilnehmertranskripte zeigen alternative Abschlüsse nur für direkte Beziehungen an. Dadurch werden komplexe, mehrstufige Prüfprotokolle vermieden, und es wird Klarheit bei der Prüfung der Art und Weise gewährleistet, wie ein Abschluss gewährt wurde.

## Katalogfreigabe mit Peer-Konten: Beziehungen nicht freigegeben

Die Katalogfreigabe ermöglicht die Freigabe von LOs über Peer-Konten hinweg, aber alternative und äquivalente Beziehungen werden innerhalb jedes Kontos unabhängig verwaltet und nicht freigegeben.

### Konzept: Katalogfreigabe und Beziehungen

#### Katalogfreigabe

Konten können Kataloge mit Peer-Konten teilen, um den Zugriff auf Kurse, Lernpfade und andere LOs kontenübergreifend zu ermöglichen.

#### Nicht freigegebene Beziehungen

Im Quellkonto konfigurierte alternative, äquivalente und alternative Vervollständigungsbeziehungen werden nicht freigegeben oder repliziert, wenn ein Katalog freigegeben wird. Jedes Konto unterhält und bewertet seine eigenen Beziehungen unabhängig.

### Arbeitsablauf

#### Katalogfreigabe

Ein Administrator in **Konto A** gibt einen Katalog mit LOs für **Konto B** frei.

#### Beziehungskonfiguration

Konto A kann über alternative Beziehungen verfügen, die zwischen den LOs im freigegebenen Katalog definiert sind.

#### Zugriff auf Peer-Konten

Konto B erhält Zugriff auf die freigegebenen Lernobjekte, übernimmt jedoch keine alternativen Beziehungen, die in Konto A konfiguriert sind.

#### Unabhängiges Management

Wenn Konto B ein ähnliches alternatives Verhalten erfordert, muss ein Administrator in Konto B die Beziehungen innerhalb dieses Kontos manuell konfigurieren.

#### Auswirkungen

##### Keine automatische Weiterleitung von Beziehungen

Alternative Beziehungen sind in Peer-Konten nicht automatisch über die Katalogfreigabe verfügbar.

##### Manuelle Einrichtung erforderlich

Jedes Peer-Konto ist für die Definition und Verwaltung seiner eigenen Beziehungen für gemeinsam genutzte LOs verantwortlich.

##### Überlegungen zur Konsistenz

Das Abschlussverhalten, die Zufriedenheit mit Vorbedingungen und die Berichterstellung können je nach Konto unterschiedlich sein, es sei denn, die Beziehungen werden absichtlich durch manuelle Konfiguration abgeglichen.

## Downstream-Verhalten

Sobald ein alternativer Abschluss für eine Zielschulung vorhanden ist, verwendet ALM diese für nachgelagerte Prüfungen:

* Wenn die Zielschulung eine **Voraussetzung** für andere Schulungen ist, hat der Teilnehmer Anspruch auf diese Schulungen, als ob er das Ziel abgeschlossen hätte.
* Wenn das Ziel ein **obligatorischer Kurs in einem Lernpfad ist**, kann die Abschlusslogik des Pfads den Teilnehmer so behandeln, als habe er diesen Teil abgeschlossen, und den Pfad als abgeschlossen markieren, wenn andere Bedingungen erfüllt sind.
* Compliance- und andere Dashboards wie das Gruppen-Erfolgs-Dashboard, die davon abhängen, ob eine Schulungsanforderung erfüllt ist, können Teilnehmer einschließen, die nur alternative Abschlüsse haben.

Das System unterscheidet zwischen tatsächlicher und alternativer Fertigstellung, sodass

* Wenn der Teilnehmer später die Zielschulung direkt absolviert und sie abschließt, kann dieser direkte Abschluss die Notwendigkeit des alternativen Abschlusses überschreiben.
* Wenn die Beziehung zwischen Quelle und Ziel entfernt oder geändert wird, kann ALM die alternativen Abschlüsse entfernen, ohne echte Abschlüsse zu berühren, sofern rückwirkende Unvollständigkeiten für das Konto aktiviert sind.

Alternative Abschlüsse sollen die tatsächliche Teilnehmeraktivität in der Zielschulung nicht beeinträchtigen. Sie fungieren als Overlay, das überarbeitet werden kann, wenn sich die Beziehungen ändern.

## E-Mails und Benachrichtigungen

Sobald ein Teilnehmer einen Kurs abgeschlossen hat, erhält der Teilnehmer eine In-App-Benachrichtigung und eine E-Mail, die den Status des Kurses und dessen Abschluss anzeigt - unabhängig davon, ob der Kurs über einen alternativen Kurs abgeschlossen wurde.

>[!NOTE]
>
>Der alternative Abschluss kann weiterhin Benachrichtigungen für Ziel-LOs in Katalogen auslösen, in denen der Teilnehmer nicht sehen kann. Alternative Benachrichtigungen zu Abschlüssen/Unvollständigkeiten werden in der immersiven App für Mobilgeräte möglicherweise nicht auf die gleiche Weise wie anderswo angezeigt.

## Einen alternativen Kurs hinzufügen

Als Administrator können Sie alternative Kurse und Pfade hinzufügen, damit die Teilnehmer mehrere Möglichkeiten haben, ihre Kurse und Pfade abzuschließen.

1. Navigieren Sie zum Abschnitt **Lernen** > **Kurse**. Eine Liste der verfügbaren Kurse wird angezeigt.
   ![](assets/ALM-courses-main.png)
   *Kursliste*
2. Navigieren Sie zu dem Kurs, für den Sie einen alternativen Kurs hinzufügen möchten.
   ![](assets/ALM-course-single.png)
   *Hinzufügen eines alternativen Kurses zu einem Kurs*
3. Navigieren Sie zum Abschnitt **Verwalten** > **Alternative Kurse/Pfade**.
   ![](assets/ALM-alt-train-paths.png)
   *Alternative Schulungen/Pfade*
4. Wählen Sie **Kurse/Pfade hinzufügen**. Eine Liste der verfügbaren Kurse wird angezeigt.
   ![](assets/ALM-alt-courses-list.png)
   *Liste der verfügbaren Kurse*
5. Wählen Sie die Kurse aus, die als **Alternate** markiert werden sollen, indem Sie das Kontrollkästchen für jeden Kurs links oben auf der Kachel aktivieren.
   ![](assets/ALM-alt-courses-added.png)
   *Alternativer Kurs hinzufügen*
6. Wählen Sie **Hinzufügen** aus.

   >[!NOTE]
   >
   >An dieser Stelle können Sie die alternativen Kurse entfernen, wenn Sie dies wünschen. Um die alternativen Kurse zu entfernen, wählen Sie **Alternative entfernen** neben jedem Kurs auf der rechten Seite.

7. Wählen Sie **Speichern**. Die alternativen Kurse werden jetzt gespeichert.

Der Fortschritt wird durch den alternativen Abschluss nicht beeinflusst. Wenn ein Kurs oder Lernpfad über einen alternativen Abschluss abgeschlossen wird, kann der Teilnehmer weiterhin direkt darauf zugreifen und sie nutzen, um das Lernen zu vertiefen und nachgelagerte Vorteile zu nutzen (z. B. Gamification-Punkte). In solchen Fällen spiegelt der Fortschrittsstatus den tatsächlichen Fortschritt des Teilnehmers bei der direkten Nutzung wider, unabhängig vom Status des alternativen Abschlusses. Sie erhalten auch eine In-App-Benachrichtigung und eine E-Mail-Benachrichtigung über den Abschluss über eine Alternative.

Diese Fertigstellung hat mehrere Vorteile, die im Folgenden aufgeführt sind:

* Dies gilt als Abschluss als Teil des Lernpfads, in dem dieser vorhanden ist.
* Dadurch werden auch alle anderen verknüpften Kurse/Pfade geöffnet.

## Einstellungen für Hauptbenutzer

Die folgenden Einstellungen ermöglichen es Benutzern, rückwirkende Abschlüsse und Unvollständigkeiten zu verwenden.

1. Navigieren Sie zum Abschnitt **Konfigurieren** > **Einstellungen** > **Grundlagen** Abschnitt > **Allgemein** > **Abschnitt &quot;Alternativer Kurs/Pfade&quot;**.
2. Wählen Sie **Rückwirkende Abschlüsse aktivieren** und **Rückwirkende Abschlüsse aktivieren** oder je nach Anforderung nur eine der beiden Optionen.
   ![](assets/ALM-alt-train-paths-settings-powerusers.png)
   *Rückwirkende Beendigung oder Unvollständigkeit aktivieren*

## Teilnehmertranskriptberichte

Die Art und Weise, wie ein Teilnehmer einen Kurs/Pfad abschließt, wird im Teilnehmertranskriptbericht erfasst. Die folgenden Szenarien werden erfasst:

1. Wenn ein Teilnehmer einen Kurs direkt abschließt, ohne sich für einen alternativen Kurs zu entscheiden, wird dies im Teilnehmertranskriptbericht widergespiegelt
2. Wenn ein Teilnehmer einen alternativen Kurs abschließt, wird dies im Teilnehmertranskriptbericht widergespiegelt
3. Wenn alle alternativen Abschlüsse aufgrund rückwirkender Unvollständigkeit und des Entfernens von Beziehungen widerrufen werden, wird dies im Teilnehmertranskriptbericht widergespiegelt.
