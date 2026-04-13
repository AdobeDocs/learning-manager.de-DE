---
description: API-Änderungen in ALM
jcr-language: en_us
title: API-Änderungen in der April-Version
source-git-commit: 3b35c16d74c83329cee24ee9ad007a53ccbd8cf3
workflow-type: tm+mt
source-wordcount: '4093'
ht-degree: 0%

---


# API-Änderungen in der Version April 2026

Die Adobe Learning Manager-Version vom April 2026 enthält Verbesserungen der öffentlichen API für Alternativen und Entsprechungen, Zugriff im Zeitfenster auf Inhalte, inhaltsbasierte Quizversuche, nicht angemeldete Erlebnisse und die Verarbeitung von Arbeitshilfen. Die Änderungen sind weitgehend abwärtskompatibel ausgelegt und ermöglichen gleichzeitig präzisere Integrationen.

## Adaptives Lernen für Lernpfade

Diese Version bietet vollständige Unterstützung für adaptive Lernpfade durch die öffentliche API. Lernpfade (LPs) können jetzt adaptive Regeln definieren, die steuern, welche Abschnitte und Sub-Lernobjekte (Sub-LOs) für verschiedene Teilnehmergruppen sichtbar sind. Die öffentliche API spiegelt dieses Verhalten wider.

Die folgenden Endpunkte sind betroffen:

- GET /primeapi/v2/learningObjects?filter.loTypes=learningPath
- GET /primeapi/v2/learningObjects/{loId}

Das neue boolesche Attribut &quot;attributes.isAdaptive&quot; gibt an, dass ein Lernprogramm adaptive Regeln verwendet. Wenn dieses Flag true ist, wird das section-Attribut adaptiv interpretiert.

Bei Teilnehmeranrufen werden nur Abschnitte zurückgegeben, die für den aktuellen Teilnehmer sichtbar sind. Jeder Abschnitt enthält die Liste der Lernobjekt-IDs (loIds), ein obligatorisches Flag und ein mandatoryLOCount, die basierend auf der adaptiven Konfiguration für diesen Teilnehmer berechnet werden, sowie die sectionId. Die Relation relations.subLOs wird jetzt ebenfalls gefiltert, sodass sie nur die Sub-Lernobjekte enthält, die für diesen Teilnehmer sichtbar sind.

Bei Admin-Aufrufen können Abschnitte zusätzlich ein adaptiveConfig-Array verfügbar machen. Hier werden die adaptiven Regeln pro Benutzergruppe beschrieben, einschließlich userGroupId, userGroupName und ob der Abschnitt für diese Gruppe obligatorisch ist. Admin-orientierte Tools können dies nutzen, um adaptive Regeln zu visualisieren und zu verwalten.

Abschluss für Lernprogramme zurücksetzen

Mit der Version wird eine API für die __Aktualisierung (Zurücksetzen) des Abschlusses__ für Lernobjekte, einschließlich adaptiver Lernprogramme, eingeführt. Dies unterstützt Szenarien wie Umschulungen, regelmäßige Compliance-Aktualisierungen oder Programmneustarts.

Ein neuer Endpunkt ist verfügbar:

```
POST /primeapi/v2/learningObjects/{loId}/instances/{loInstanceId}/refreshCompletion
```

Dieser Vorgang erfordert entsprechende Schreibberechtigungen und setzt den Abschlussstatus für die angegebene Lernobjektinstanz im angegebenen Benutzerkontext zurück. Es ist für die Verwendung durch Admin-seitige Automatisierungen oder sorgfältig ausgewählte Teilnehmer-Tools vorgesehen.

Eine Massenversion dieser Funktion wird über eine Jobs-API geplant. Die Anforderungsform wurde entwickelt, um Benutzer per E-Mail, Benutzer-ID oder Benutzergruppen-ID anzusprechen, z. B.:

```
{  
  "emails": ["[user1@example.com](mailto:user1@example.com)", "[user2@example.com](mailto:user2@example.com)"],  
  "userIds": ["12345", "67890"],  
  "userGroupIds": ["ug1", "ug2"]  
}  
```

Integrationen sollten diese API verwenden, wenn sie die Teilnehmer in jedem Programm oder Kurs neu starten müssen. Clients müssen Fehlerantworten ordnungsgemäß verarbeiten: Die API kann Aktualisierungsanforderungen ablehnen, wenn eine Zurücksetzung nicht anwendbar ist (z. B. wenn kein Abschluss vorhanden ist oder nicht unterstützte Lernobjekttypen).

## Äquivalente und alternative Abschlüsse

Um Implementierungen zu unterstützen, bei denen mehrere Lernobjekte dieselbe Anforderung erfüllen können, enthält die Version Entsprechungen und Alternativen als öffentliche APIs.

Die Lernobjektendpunkte enthalten jetzt diese Informationen:

```
- GET /primeapi/v2/learningObjects
- GET /primeapi/v2/learningObjects/{loId}
```

Ein neues boolesches Attributattribut .isAlternateComplete gibt an, ob der Abschluss des Teilnehmers für ein bestimmtes Lernobjekt das Ergebnis eines alternativen oder gleichwertigen Lernobjekts ist und nicht das Objekt selbst. Wenn dies wahr ist, listet die Beziehung relations.alternativeCompletions die Lernobjekte auf, die als Alternativen fungierten. Dadurch können nachgelagerte Berichte und Dashboards zwischen direkten und alternativen Abschlüssen unterscheiden und zeigen, welche Alternative die Anforderung erfüllt hat.

Darüber hinaus ermöglicht eine Ansicht verwandter Lernobjekte die Erkennung potenzieller Alternativen, die ein Lernobjekt erfüllen können. Dies wird angezeigt über:

```
GET /primeapi/v2/learningObjects/{loId}/relatedLOs?type=sourceAlternateLOs&limit={n}
```

Die Antwort gibt Lernobjekte zurück, die als Alternativen fungieren können, und enthält ein meta.count-Feld, das die Gesamtzahl dieser Alternativen unabhängig vom aktuellen Grenzwert angibt. Integrationen können dies verwenden, um empfohlene Entsprechungen anzuzeigen oder administrative Ansichten alternativer Zuordnungen zu erstellen.

## Nutzungsszenarien für Reporting und Analysen

Benutzer, die Berichte oder Analysen generieren, sollten ihre Logik aktualisieren, um isAlternateComplete und alternativeCompletions in ihre Berichterstellungs-Workflows einzufügen.

Berichtsintegrationen, die Abschlussdaten nutzen (z. B. LT-Export, benutzerdefinierte Data Warehouse-Feeds oder BI-Dashboards), sollten ihre Logik auf das Lesen und Beibehalten beider Attribute erweitern.isAlternateComplete und relations.alternativeCompletions von den LO-APIs:

- When isAlternateComplete == false:\
  Behandeln Sie den Datensatz wie heute als __direkte Fertigstellung__ des LO.
- When isAlternateComplete == true:
   - Markieren Sie den Datensatz als __alternativen Abschluss__ in Ihrem Bericht (z. B. eine Spalte &quot;Abschlussmethode&quot; mit den Werten &quot;DIRECT&quot; vs. &quot;ALTERNATE&quot;).
   - Verwenden Sie relations.alternateCompletions.data[*].id, um __zu erfassen, welche Quell-LO(s)__ diesen Abschluss gewährt haben (z. B. &quot;Kurs B wurde über alternativen Kurs A abgeschlossen&quot;).

Typische Anwendungsfälle:

- _Kompatibilitätsberichte_ - zeigen an, dass ein Kompatibilitätskurs über ein genehmigtes Äquivalent abgeschlossen wurde, und listen den Quellkurs auf, der die Anforderung erfüllt hat.
- _Dashboards für den Programmfortschritt_ - Unterscheiden Sie Teilnehmer, die einen Pfad _direkt_ abgeschlossen haben, von denen, die ihn über Alternativen befriedigt haben, für präzisere Fortschritts- und Behebungsansichten.
- _Audit-Protokolle_ - Bei jedem LO, das isAlternateComplete=true markiert ist, können Prüfer genau sehen, welche alternativen Schulungen verwendet wurden, um diesen Abschluss zu gewähren.

Ohne die Einbeziehung dieser beiden Felder behandeln nachgelagerte Berichte alternative Abschlüsse als regelmäßige Abschlüsse und _können_ *warum* nicht erklären, wenn ein Teilnehmer eine Schulung als abgeschlossen anzeigt, die er nie direkt absolviert hat.

## Verhalten der Teilnehmer im Vergleich zur Admin-LO-API

Die Struktur der mehrsprachigen Arbeitshilfe ist sowohl in Teilnehmer- als auch in Administrator-LO-APIs identisch. Im Teilnehmerbereich werden nur die Arbeitshilfen zurückgegeben, die für den Teilnehmer sichtbar sind. Für jede sichtbare Arbeitshilfe werden jedoch alle konfigurierten Gebietsschemas über mehrere Ressourcenentitäten (eine pro Gebietsschema) und mehrere Gebietsschemas mit lokalisierten Metadaten verfügbar gemacht. Der Bereich &quot;Administrator&quot; gibt alle Arbeitshilfen zurück, die der Administrator verwalten kann, mit demselben LO-Modell und den gleichen gebietsschemaspezifischen Ressourcen-IDs. Kunden mit Teilnehmerbereich sollten die Ressource auswählen, deren attribute.locale am besten der Inhaltssprache des Teilnehmers entspricht, während Admin-Tools alle Gebietsschemas für die Berichterstellung und Verwaltung auflisten können.

## Checkliste mit Kommentarfunktion

Um Arbeitsabläufe zu unterstützen, in denen Reviewer strukturiertes Feedback zu Aktivitäten auf der Grundlage von Checklisten freigeben können, werden in dieser Version *Checklistenkommentare* und Steuerelemente zur Reviewersichtbarkeit über die Lernobjektressourcen-API angezeigt.

Checklistenbezogene Metadaten werden für learningObjectResource-Entitäten (JApiLOResource, &quot;type&quot;: &quot;learningObjectResource&quot;) verfügbar gemacht, die Checklistenressourcen innerhalb eines Kurses oder eines anderen Lernobjekts darstellen.

Die Informationen sind abrufbar unter:

```
GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources
```

Wenn die Lernobjektinstanz Ressourcen vom Typ Checkliste enthält, werden die entsprechenden learningObjectResource-Einträge im enthaltenen Array unter Attributen die Attribute comment und reviewer-visibility und unter Beziehungen die Identität des Reviewers verfügbar machen.

### Neue Kommentarattribute für Checkliste

Bei Ressourcen für Checklisten können die folgenden Attribute auf learningObjectResource vorhanden sein:

- attributes.checklistComment\
  Ein vom Reviewer für den Teilnehmer hinterlassener Freitextkommentar, z. B.:\
  &quot;checklistComment&quot;: &quot;Hervorragende Leistung! Alle Sicherheitsprotokolle wurden ordnungsgemäß befolgt.&quot;\
  Dieses Attribut ist nur mit _ausgefüllt, wenn_:
   - showChecklistComment ist true und
   - In der Checklistenkonfiguration ist enable_reviewer_comments aktiviert.
- attributes.showChecklistComment\
  Ein boolesches Flag, das angibt, ob Reviewerbemerkungen dem Teilnehmer angezeigt werden sollen:\
  &quot;showChecklistComment&quot;: true\
  Dieses Attribut ist nur vorhanden _, wenn_ enable_reviewer_comments in der Checklistenkonfiguration aktiviert ist.\
  Kunden sollten dieses Flag verwenden, um zu entscheiden, ob sie ChecklisteComment in den Teilnehmererlebnissen rendern.
- attributes.showReviewerNameToLearner\
  Ein boolesches Flag, das steuert, ob der Teilnehmer die Identität des Überprüfers sehen soll:\
  &quot;showReviewerNameToLearner&quot;: true\
  Wenn dieser Wert auf &quot;true&quot; gesetzt ist, können Clients mithilfe der Beziehung checklistReviewby (siehe unten) den Namen des Reviewers auflösen und anzeigen (z. B. über eine API für die Benutzersuche).

Andere checklistenspezifische Kontexte wie checklistEvaluationStatus, isChecklistMandatory, resourceSubType: &quot;CHECKLIST&quot; und submissionDate sind ebenfalls für dieselbe learningObjectResource verfügbar, um umfangreichere Checklisten-UIs und Berichte zu unterstützen.

### Identitätsbeziehung des Überprüfers

Wenn Reviewernamen sichtbar sein sollen, enthält learningObjectResource eine Beziehung, die auf den Reviewerbenutzer verweist:

```
"relationships": {
  "checklistReviewedBy": {
    "data": {
      "id": "user_id",
      "type": "user"
    }
  }
}
```

Diese Beziehung ist nur mit _aufgefüllt, wenn_:

- showReviewerNameToLearner ist true und
- checklistReviewby ist nicht NULL (d. h. die Checkliste wurde überprüft).

Client-Anwendungen sollten:

1. Überprüfen Sie &quot;attributes.showReviewerNameToLearner&quot;.
2. Wenn true und relations.checklistReviewby.data vorhanden ist, rufen Sie die entsprechende Benutzer-API auf, um &quot;id&quot;: &quot;user_id&quot; in einen Anzeigenamen aufzulösen.
3. Geben Sie den Namen des Überprüfers neben dem Kommentar oder dem Status der Checkliste ein.

### Zugriff auf Ressourcen und Kommentare für Checkliste

Um Checklistenressourcen und ihre Kommentare für ein bestimmtes Lernobjekt abzurufen, sollten Clients:

- Anruf

```
GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources
```

- Antwort:
   - Verwenden Sie relations.instances aus dem Haupt-learningObject, um die relevanten learningObjectInstance-Einträge im Include-Code zu suchen.
   - Folgen Sie in jeder learningObjectInstance der Datei relations.loResources , um learningObjectResource-Einträge zu finden.
   - Filtern von learningObjectResource-Einträgen, wobei:
      - attributes.resourceSubType == &quot;CHECKLIST&quot; (für Checklistenressourcen) und
      - optional attributes.showChecklistComment == true, um Checklisten mit für Teilnehmer sichtbaren Kommentaren zu finden.

- Verwenden Sie für jede Checkliste learningObjectResource:
   - attributes.checklistComment (wenn vorhanden und showChecklistComment ist true)
   - attributes.checklistEvaluationStatus (z. B. &quot;PASSED&quot;)
   - attributes.showReviewerNameToLearner
   - relations.checklistReviewtBy (sofern vorhanden) zum Identifizieren des Reviewers.

Dieses Muster ermöglicht es Headless- oder benutzerdefinierten Clients, eine umfassende Checkliste zu rendern, einschließlich Status, obligatorischen/optionalen Flags und Prüfer-Feedback direkt von den Prime-APIs.

### Reporting und UX.

- _Berichterstellung und Analyse_
Integrationen, die die Leistung der Teilnehmer auf Checklisten verfolgen, können Folgendes umfassen:
   - checklistEvaluationStatus für Bestanden/Nicht bestanden oder andere Statusanzeigen.
   - isChecklistObligatorisch, um erforderliche und optionale Checklistenaktivitäten zu unterscheiden.
   - Vorhandensein oder Fehlen von checklistComment und showChecklistComment für Audits des Feedback-Coverage.
- _Teilnehmererlebnisse_
UI-Implementierungen sollten:
   - Respektieren Sie showChecklistComment, bevor Sie Anmerkungen anzeigen.
   - Verwenden Sie showReviewerNameToLearner und checklistReviewby, um zu entscheiden, ob der Name des Reviewers angezeigt oder die Überprüfung anonym gehalten werden soll.
   - Lehnen Sie sich zurück, wenn Kommentare deaktiviert sind oder nicht vorhanden sind, und zeigen Sie weiterhin den Bewertungsstatus und Informationen zur Einreichung an.

## Mehrsprachige Unterstützung für Arbeitshilfen

Um Implementierungen zu unterstützen, bei denen Arbeitshilfen in mehreren Sprachen sowohl für Teilnehmer als auch für Administratoren bereitgestellt werden müssen, erweitert diese Version die Arbeitshilfebehandlung auf *eine Ressource pro Gebietsschema* anstelle einer einzelnen hartcodierten en-US-Ressource.

Mehrsprachige Arbeitshilfen verwenden weiterhin die vorhandene Hierarchie:

_Lernobjekt_ (lo) → _learningObjectResource_ (loResource) → _Ressource_

Es sind keine Änderungen am API-Vertrag erforderlich. Jede lokalisierte Arbeitshilfe passt auf natürliche Weise in diese Struktur, mit separaten Ressourcenentitäten pro Gebietsschema und freigegebenen lokalisierten Metadaten auf den Ebenen learningObject/learningObjectResource.

Daten zur Arbeitshilfe werden angezeigt über:

```
GET /primeapi/v2/learningObjects/jobAid:{jobAidId}?include=instances.loResources.resources
```

Wenn eine Arbeitshilfe mehrere Sprachvarianten enthält, enthält das enthaltene Array mehrere &quot;type&quot;: &quot;resource&quot;-Einträge - einen für jedes Gebietsschema (z. B. en-US, fr-FR, es-ES), die alle von einem einzigen learningObjectResource verknüpft sind.

### Mehrsprachige Struktur der Arbeitshilfe

Mehrsprachige Arbeitshilfen verwenden:

- _learningObject (Typ: learningObject)_
   - Enthält lokalisierte Metadaten mit mehreren Einträgen (z. B. en-US, fr-FR), damit Clients den Titel/die Beschreibung der Arbeitshilfe in der entsprechenden Sprache anzeigen können.
- _learningObjectInstance (Typ: learningObjectInstance)_
   - Verweist auf einen oder mehrere learningObjectResource-Einträge über relations.loResources.
- _learningObjectResource (Typ: learningObjectResource)_
   - Enthält eine allgemeine Konfiguration (Inhaltstyp, Version usw.) und localizedMetadata mit mehreren Gebietsschemas.
   - Verknüpfungen zu einer oder mehreren Ressourcenentitäten über relations.resources.
- _Ressource (Typ: Ressource)_
   - *Eine pro Gebietsschema*, jede mit eigener ID, Gebietsschema, Name und URL (location/downloadUrl).

Bei einer mehrsprachigen Arbeitshilfe ist ein typisches Muster:

- learningObjectResource mit localizedMetadata für en-US und fr-FR
- relations.resources.data verweist auf:
   - Ressource mit Gebietsschema: &quot;en-US&quot;
   - Ressource mit Gebietsschema: &quot;fr-FR&quot;

Clients können die entsprechende Ressource auswählen, indem sie das Gebietsschema des Teilnehmers mit dem Feld resource.attributes.locale abgleichen.

### Neues Ressourcen-ID-Format für Arbeitshilfen

Um mehrere lokalisierte Varianten einer Arbeitshilferessource richtig zu unterscheiden, hat sich das _Ressourcen-ID-Format geändert_.

_Altes (veraltetes) Ressourcen-ID-Format_

Früher verwendeten Arbeitshilferessourcen ein undurchsichtiges ID-Format wie:

jobAid:131032_-1_-1_2_resource

Dieses Format codierte das Gebietsschema nicht, und APIs würden tatsächlich nur eine einzelne Ressource (normalerweise en-US) verfügbar machen.

_Neues Ressourcen-ID-Format (Unterstützung für mehrere Sprachen)_

Das neue Format lautet:

```
jobAid:<jobAidId>_<version>_<localeCode>
```

Beispiele:

- jobAid:131032_2_en-US
- jobAid:131032_2_fr_FR
- jobAid:131032_2_es_ES

Visuelle Aufschlüsselung:

```
jobAid:131032_2_fr_FR

        │      │ │ │

        │      │ │ └──► Locale Code (fr_FR, en_US, es_ES, etc.)

        │      │ └────► Version (2)

        │      └──────► JobAid ID (131032)

        └─────────────► Resource Type Prefix ("jobAid:")
```

Diese Struktur ermöglicht Clients Folgendes:

- Identifizieren Sie schnell, zu welcher Arbeitshilfe und Version eine Ressource gehört.
- Ziehen Sie das Gebietsschema bei Bedarf direkt aus der Ressourcen-ID.

### Abwärtskompatibilität: 

```/resources/{resourceId}```

Der Endpunkt der alten Ressource bleibt verfügbar:

```GET /primeapi/v2/resources/{resourceId}

```

Es ist jetzt _abwärtskompatibel_ mit dem alten und dem neuen ID-Format:

- _Altes ID-Format_ (z. B. jobAid:131032_-1_-1_2_resource)
   - Arbeitet weiter.
   - Gibt die _zuerst erstellte Ressource_ zurück, die mit dieser Legacy-ID verknüpft ist (in der Regel die ursprüngliche Ressource en-US).
- _Neues ID-Format_ (z. B. jobAid:131032_2_fr_FR)
   - Gibt die _exakte gebietsschemaspezifische Ressource_ zurück, die dieser ID entspricht.
   - Dies ermöglicht ein präzises Abrufen und Bearbeiten lokalisierter Varianten der Arbeitshilfe.

Integrationen, die derzeit die alten Ressourcen-IDs speichern oder auf sie verweisen, können weiterhin ohne Änderungen funktionieren, während neuere Implementierungen empfohlen werden, das neue ID-Format für gebietsschemaspezifische Operationen zu übernehmen.

### Integration und UX

- _Benutzeroberfläche für Teilnehmer/Administrator_
   - Verwenden Sie learningObject.localizedMetadata und learningObjectResource.localizedMetadata, um Titel und Beschreibungen in der entsprechenden Sprache anzuzeigen.
   - Verwenden Sie resource.attributes.locale , um die richtige URL (location/downloadUrl) für das Gebietsschema des Teilnehmers auszuwählen.
   - Implementieren Sie das Fallback-Verhalten (z. B. Fallback auf en-US), wenn das genaue Gebietsschema eines Teilnehmers nicht verfügbar ist.
- _APIs und Speicher_
   - Speichern Sie bei neuen Integrationen die _Ressourcenkennung im neuen Format_ (```jobAid:<jobAidId>_<version>_<localeCode>```), um einen eindeutigen gebietsschemaspezifischen Abruf zu ermöglichen.
   - Ältere IDs können weiterhin mit /resources/{resourceId} verwendet werden, sie unterscheiden jedoch nicht zwischen Gebietsschemas.

## Zeitschlitzbeschränkungen für das Starten von Modulen

Einige Lernerlebnisse dürfen nur innerhalb eines festgelegten Zeitfensters verfügbar sein. In der Version werden Zeitfensterinformationen zu Lernobjektressourcen angezeigt und ein Validierungsendpunkt wird eingeführt, der überprüft, ob ein Teilnehmer eine Ressource zur aktuellen Zeit starten kann.

Zeitfenster-Metadaten sind über den Endpunkt verfügbar:

```GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources```

Auf der Lernobjektressourcenebene kann jetzt ein timeSlot-Objekt in den Attributen vorhanden sein, wobei die Werte startTime und endTime in UTC angegeben werden. Hier wird das Fenster angegeben, in dem die Ressource gestartet werden kann.

Vor dem Starten eines Moduls können Integrationen einen neuen Validierungsendpunkt aufrufen:

```GET /primeapi/v2/learningObjects/{loId}/instances/{loInstanceId}/loResources/{loResourceId}/canStart```

Dieser Endpunkt, der für Szenarien mit Lesevorgängen durch Teilnehmer vorgesehen ist, gibt unter Berücksichtigung des konfigurierten Zeitfensters, des Bereitstellungstyps und anderer Back-End-Regeln zurück, ob der Teilnehmer die Ressource derzeit starten darf.

Benutzerdefinierte Player und Clientanwendungen sollten canStart verwenden, um einen zeitbasierten Zugriff zu erzwingen, und die timeSlot-Metadaten verwenden, um klare Nachrichten darüber anzuzeigen, wann Inhalt verfügbar wird oder abläuft. Negative Antworten von canStart sollten explizit behandelt werden, um die Teilnehmer darüber zu informieren, warum der Inhalt noch nicht oder nicht mehr gestartet werden kann.

## Inhaltsbasierte Tests mit mehreren Versuchen

Manche Inhaltspakete nutzen nicht nur Adobe Learning Manager, sondern implementieren auch eigene Funktionen zur Verfolgung von Versuchen. Die Version enthält ein Flag, das angibt, wenn Versuche vom Inhalt selbst gesteuert werden.

Über:

```GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources```

Lernobjektressourcen können jetzt ein boolesches Attribut hasContentDrivenAttemptTracking verfügbar machen. Wenn dies der Fall ist, verwaltet das Quiz oder Modul Versuche intern (z. B. über SCORM oder xAPI-Logik), und die Standardversuchszähler der Plattform geben möglicherweise die Erfahrung des Teilnehmers nicht vollständig wieder.

Integrationen, die die Anzahl der Versuche anzeigen oder das Wiederholungsverhalten steuern, sollten dieses Flag aktivieren. Wenn es aktiviert ist, sollten sie keine Versuchsbeschränkungen ausschließlich aus Plattform-Metadaten ableiten und sich auf Content-Side-Reporting (z. B. über xAPI-Anweisungen) oder unternehmensspezifische Regeln verlassen.

## Verhaltensänderung im Format der Arbeitshilferessourcen-ID

Diese Version enthält eine wichtige __Verhaltensänderung__ im Format der Arbeitshilferessourcen-IDs. Auch wenn kein neuer Endpunkt betroffen ist, hat dies direkte Auswirkungen auf Systeme, die diese IDs speichern oder analysieren.

Früher verwendeten Arbeitshilferessourcen-IDs ein Format wie:

```jobAid:<jobAidId>_-1_-1_2_resource```

In der Version vom April 2026 wird dies durch ein vereinfachtes und expliziteres Format ersetzt:

```jobAid:<jobAidId>_<version>_<localeCode>```

Beispiel:

jobAid:131032_2_fr_FR

Die Komponenten sind:

- ```<jobAidId>```: die numerische Arbeitshilfen-ID (z. B. 131032),
- ```<version>```: Versionsnummer der Arbeitshilfe (z. B. 2),
- ```<localeCode>```: der Gebietsschemacode (z. B. en_US, fr_FR, es_ES).

Jede Integration, die Ressourcen indiziert oder in Arbeitshilferessourcen-IDs verbleibt, muss ihre Analyse- und Speicherlogik aktualisieren, um das neue Format zu erkennen. Da sich die Bezeichner selbst ändern, wird dringend empfohlen, alle lokalen Indizes, die von Arbeitshilferessourcen-IDs nach dem Upgrade auf die Version vom April 2026 neu zu erstellen.

## Kursbannerbilder über Migration festlegen

Sie können jetzt Kursbannerbilder in Adobe Learning Manager als Teil Ihres Standardmigrations-Workflows festlegen oder aktualisieren. Auf diese Weise können Sie große Kataloge starten und bereinigen und gleichzeitig die Konsistenz Ihrer Kursseiten beibehalten, ohne sie manuell bearbeiten zu müssen

### Definition von Bannerbildern

Bannerbilder werden in der _course.csv_-Migrationsdatei konfiguriert, die Sie bereits verwenden, um Kursmetadaten bereitzustellen, z. B.:

- id
- courseName
- courseCreationDate
- state
- Autorin
- thumbnailUrl

Mit dieser Verbesserung enthält die &quot;course.csv&quot;-Spezifikation eine zusätzliche _optionale Spalte_ für das Kursbannerbild. Der genaue Kopfzeilenname ist in der CSV-Spezifikation definiert, die Sie von Ihrem Learning Manager-Konto herunterladen (sie kann z. B. als bannerUrl oder bannerImageUrl angezeigt werden).

Die Bannerspalte:

- Zeigt auf die Bilddatei, die Sie als _Kursbanner_ verwenden möchten.
- Funktioniert auf die gleiche Weise wie thumbnailUrl und verwendet Bilder, die in Ihrem konfigurierten Inhalts-Repository (Box/FTP) verfügbar sind.

### Vorbereiten von Bannerbildern für die Migration

1. Bannerbilder hochladen: Platzieren Sie Ihre Bannerbilddateien im selben Box- oder FTP-Speicherort, den Sie auch für andere Migrationsassets verwenden, und folgen Sie dabei Ihrer bestehenden Verzeichnisstruktur.
2. Dateiformat überprüfen:
Verwenden Sie eines der unterstützten Bildformate (z. B. png, jpg, jpeg, gif), wie in den Systemanforderungen beschrieben:
   1. [*Systemanforderungen*](/help/migrated/system-requirements.md)
3. Aktualisieren Sie &quot;course.csv&quot;: Verweisen Sie in der neuen Bannerspalte auf den relativen Pfad oder Bezeichner des Bannerbilds. Ein konzeptuelles Beispiel:

```
id,courseName,courseCreationDate,state,author,thumbnailUrl,bannerUrl  
12345,DEMO1,2018-05-05T08:56:21.000Z,Published,Sudheer,pic1.png,banners/banner1.png  
45678,DEMO2,2018-05-05T08:56:21.000Z,Published,Sudheer,pic2.png,banners/banner2.png  
```

### Banner während eines Migrationslaufs anwenden

Sobald Ihre &quot;course.csv&quot; aktualisiert wurde, ist der Ablauf wie bei jeder anderen Migration:

1. _CSV hochladen_
Laden Sie die aktualisierte Datei &quot;course.csv&quot; (und alle anderen relevanten Dateien) in den für die Migration konfigurierten Box-/FTP-Ordner hoch. Dateinamen müssen genau mit den in der Datei &quot;csv_specifications.zip&quot; angegebenen Namen übereinstimmen (Groß- und Kleinschreibung wird unterschieden).
2. _Sprint-Ausführung starten_
Starten Sie in Adobe Learning Manager als Integrations-Admin eine _Sprint-Ausführung_ der Migration, die &quot;course.csv&quot; enthält.\
   Die Migrations-Engine liest die Bannerspalte und wendet das Bannerbild auf jeden Kurs an.
3. _Überprüfungsergebnisse und Fehlerprotokolle_
Nach dem Sprint:
   1. Überprüfen Sie die Banner in den Apps _Autor_ und _Teilnehmer_.
   2. Wenn einige Zeilen fehlschlagen (z. B. aufgrund eines ungültigen Dateipfads oder eines nicht unterstützten Formats), laden Sie die Fehler-CSV aus dem Migrationslauf herunter und korrigieren Sie die Daten.

### Neue Kurse und vorhandene Kurse

Das Bannerfeld funktioniert in beiden Fällen:

- _Neue Kurse, die über die Migration erstellt wurden_
Wenn ein Kurs zum ersten Mal aus &quot;course.csv&quot; erstellt und die Bannerspalte ausgefüllt wird, wird dieses Banner sofort festgelegt.
- _Vorhandene Kurse (Nachrüstung/Korrekturen)_
Wenn Sie die Migration mit derselben Kurs-ID und einem neuen Bannerwert erneut ausführen:
   - Learning Manager sucht den vorhandenen Kurs.
   - Das Bannerbild ist _aktualisiert_ auf das neue Bild, das in der CSV-Datei angegeben ist.

Die tatsächlichen Spaltennamen und Pfade müssen mit der _heruntergeladenen CSV-Spezifikation_ und dem Layout Ihres Inhalts-Repositorys übereinstimmen.

## Entfernen der Bestellspalte in LearningProgramCourse

Adobe Learning Manager unterstützt jetzt ein vereinfachtes Modell für die _Kursbestellung innerhalb von Lernpfaden (Lernprogramme)_ während der Migration. Als Teil dieser Änderung wird die _Order-Spalte_ aus der Migrationsdatei learning_program_course.csv entfernt.

Zuvor enthielt die Datei learning_program_course.csv eine Spalte (häufig als &quot;order&quot; oder ähnlich bezeichnet), in der die folgenden Aktionen ausgeführt wurden:

- Legen Sie die _Position_ jedes Kurses innerhalb eines Lernprogramms explizit fest, basierend auf dem numerischen Wert in dieser Spalte.
- Administratoren oder Skripte müssen diese numerische Sequenz manuell verwalten, insbesondere beim Einfügen oder Neuanordnen von Kursen.

Adobe Learning Manager verwendet jetzt nicht mehr die Bestellspalte in learning_program_course.csv, um die Kursreihenfolge zu bestimmen. Stattdessen konzentriert sich die Migrations-CSV auf _, welche Kurse zu welchem Lernprogramm gehören_, und nicht darauf, wie sie numerisch sortiert werden.

## Auswirkungen auf CSVs der Migration

### learning_program_course.csv

Sie sollten die alte Spalte mit der Reihenfolge als entfernt oder ignoriert behandeln:

- Verlassen Sie sich nicht darauf, die Abfolge von Kursen in einem Lernprogramm während der Migration zu steuern.
- Wenn Sie noch eine Bestellspalte aus älteren Vorlagen haben:
   - Der Learning Manager ignoriert es für die Bestellung.
   - Sie können sie im Laufe der Zeit sicher aus der CSV-Datei entfernen, um Ihre Migrationsdateien zu vereinfachen.
- Die erforderliche Kernzuordnung bleibt erhalten:
   - Lernprogramm-ID ↔ Kurs-ID (sowie alle anderen noch dokumentierten Spalten, z. B. id, learningProgramId, courseId und dates).

Lesen Sie immer die neuesten [_CSV-Spezifikationen_](https://experienceleague.adobe.com/de/docs/learning-manager/using/integration/migration-manual) aus Ihrem Learning Manager-Konto (über csv_specifications.zip), um den aktuellen Headersatz und die aktuellen Anforderungen zu bestätigen.

## timeZoneCode für Kursinstanzen

Ab dieser Version macht das Kursinstanzmodell (learningObjectInstance) ein neues Attribut verfügbar:

timeZoneCode - ein Zeichenfolgenfeld, das eine Kursinstanz explizit mit einer der konfigurierten Zeitzonen des Kontos verknüpft.

Dies ermöglicht Clients Folgendes:

- Beheben Sie die Zeitzone einer Kursinstanz auf konsistente, API-gesteuerte Weise.
- Interpretieren und zeigen Sie alle Daten/Zeiten auf Instanzebene für diese Instanz korrekt an, unabhängig von der eigenen Zeitzone des Benutzers.

### Wo timeZoneCode angezeigt wird

Das Feld wird den Attributen des learningObjectInstance-Modells hinzugefügt.
nur für Kursinstanzen.

Beispiel:

```
{
  "id": "course:1262748_1359228",
  "type": "learningObjectInstance",
  "attributes": {
    "dateCreated": "2019-08-06T13:50:39.000Z",
    "isAET": false,
    "isDefault": true,
    "timeZoneCode": "356",
    "isFlexible": false,
    "state": "Active",
    "localizedMetadata": [
      {
        "locale": "en-US",
        "name": "Default instance"
      }
    ]
  }
}
```

### So lösen Sie timeZoneCode auf

Der numerische timeZoneCode ist ein Suchschlüssel im Zeitzonenkatalog des Kontos, der über die Konto-API angezeigt wird:

```http
GET /primeapi/v2/account
Authorization: Bearer <access_token>
```

Innerhalb der Antwort sind Zeitzonen aufgeführt in:

```
"data": {
  "attributes": {
    "timeZones": [
      {
        "name": "Etc/GMT+12",
        "timeZoneCode": "356",
        "utcOffset": -720,
        "utcOffsetCode": "UTC-12:00(Etc/GMT+12)",
        "zoneId": "Etc/GMT+12"
      },
      "..."
    ]
  }
}
```

### Empfohlener Client-Flow:

1. Rufen Sie einmal GET /account auf, cachen Sie &quot;attributes.timeZones&quot; für den Mandanten.
2. Für jede Kursinstanz:
   - Lesen Sie attributes.timeZoneCode.
   - Suchen Sie den entsprechenden Eintrag in timeZones, wobei timeZoneCode übereinstimmt.
   - Verwenden Sie die zoneId, utcOffset und utcOffsetCode dieses Eintrags für die Anzeige- und Planungslogik.

## Asynchrone öffentliche APIs für die Mitgliedschaft in einer Benutzergruppe

### Einführung

Adobe Learning Manager stellt zwei asynchrone _Admin-APIs_ zur Verwaltung der Benutzergruppenmitgliedschaft bereit:

- POST /async/userGroups/{userGroupId}/users - Benutzer asynchron zu einer Benutzeroberflächengruppe hinzufügen
- DELETE /async/userGroups/{userGroupId}/users - Benutzer asynchron aus einer Benutzeroberflächengruppe entfernen

Anstatt die Mitgliedschaft in derselben Anforderung zu aktualisieren, akzeptieren diese APIs Ihren Stapel und geben eine _Ereignis-ID_ zurück. Das tatsächliche Ergebnis wird später über webhooks geliefert.

Verwenden Sie sie, wenn:

- Sie verwalten große Gruppen oder häufige Batch-Aktualisierungen.
- Latenz ist weniger wichtig als Zuverlässigkeit und Durchsatz.
- Statt UI-Klicks erstellen Sie Integrationen (HR, CRM, LXP).

Bei kleinen, interaktiven Administratoraktionen können Sie die synchronen `/userGroups/{id}/users`-APIs weiterhin verwenden.

### Authentifizierung und Basis-URL

Diese APIs sind Teil der standardmäßigen __v2 Admin-API__-Oberfläche.

- [Basis-URL (prod)](https://learningmanager.adobe.com/docs/primeapi/v2/)
- Auth: OAuth 2.0-Zugriffstoken mit `admin:write`-Bereich
- Erforderliche Kopfzeilen:
   - Autorisierung: Bearer &lt;Zugriffstoken>
   - Content-Type: application/json
   - Akzeptieren: application/json

Das allgemeine Verhalten der Admin-API und die Bereiche finden Sie unter:

- [Entwicklerhandbuch](/help/migrated/integration-admin/feature-summary/developer-manual.md)
- [API-Referenzhandbuch](https://learningmanager.adobe.com/docs/primeapi/v2/)

### Anforderungsformat

Sowohl __add__ als auch __remove__ verwenden exakt die gleiche Körperform.

#### Text

```
{
  "metadata": {
    "event_id": "my-optional-correlation-id",
    "sourceSystem": "HRIS",
    "batchId": "hr_2026_03_30_0001"
  },
  "data": [
    { "type": "user", "id": "11101219" },
    { "type": "user", "id": "11101220" }
  ]
}
```

#### Daten (erforderlich)

data ist die Liste der Benutzerressourcen-IDs für diesen Stapel.

- `type` muss &quot;Benutzer&quot; sein.
- `id` ist die _numerische Benutzer-ID_ in ALM (keine E-Mail-Adresse, keine UUID).

#### Einschränkungen

- `data` muss vorhanden und nicht leer sein.
- Mindestens ein Benutzer ist erforderlich.
- Die maximale Nutzlastgröße beträgt 20 Benutzer pro Anforderung.
- Alle IDs müssen numerisch sein und sich auf gültige Benutzer beziehen.

Wenn eine dieser Bedingungen fehlschlägt, gibt die API einen Fehler zurück und es befindet sich nichts in der Warteschlange.

#### Metadaten (optional)

`metadata` sind alle zusätzlichen Korrelationsdaten, die Sie im Webhook wiedergeben möchten.

Typische Verwendung:

- `event_id` - von Ihnen generierte Korrelations-ID.
- `sourceSystem` - Name des Upstream-Systems.
- `batchId` - Batch- oder Auftragsbezeichner.

Der Dienst gibt dieses Objekt unverändert in der Webhook-Antwort zurück, sodass Sie den Rückruf mit Ihrem internen Auftrag abgleichen können.

Einschränkungen:

- Optional; kann vollständig weggelassen werden.
- Die kombinierte Länge aller Tasten und Werte darf 1000 Zeichen nicht überschreiten.

### Antwortformat

Beide Endpunkte reagieren synchron mit einer Ereignis-ID:

```
{ "event_id": "cd2972c8-cb15-47a0-a23f-e4a16cb720f5" }
```

Verhalten:

- Wenn `metadata.event_id` übergeben wird, wird dieser Wert verwendet.
- Andernfalls generiert der Dienst eine UUID.

Sie sollten immer:

- Speichern Sie `event_id` als primären Bezeichner für den Stapel.
- Erwarten Sie, dass Sie den gleichen Wert im Webhook-Rückruf erhalten.

Weitere Informationen finden Sie unter [Webhooks zum Hinzufügen und Entfernen von Benutzergruppenmitgliedschaft](/help/migrated/integration-admin/feature-summary/webhooks.md#webhooks-for-adding-and-removing-user-group-membership).

## Häufige Fragen

_Wie ändert die Version vom April 2026 die learningObjects-API für adaptive Lernprogramme?_

Diese Version fügt ein isAdaptive-Flag für Lernprogramme hinzu und macht Abschnitte und Sub-LOs lernerorientiert. In adaptiven Programmen sehen Teilnehmer nur die Abschnitte und Sub-Lernobjekte, die für sie basierend auf adaptiven Regeln sichtbar sind, während Administratoren die zugrunde liegende adaptive Konfiguration für eine Benutzergruppe sehen können.

_Muss ich meine Integration aktualisieren, wenn davon ausgegangen wird, dass alle Abschnitte und untergeordneten LOs immer zurückgegeben werden?_

Ja. Bei adaptiven Lernprogrammen gibt die API jetzt nur die Abschnitte und untergeordneten LOs zurück, die für den aktuellen Teilnehmer sichtbar sind. Clientcode sollte die Antwort als autoritative, möglicherweise gefilterte Ansicht behandeln, anstatt eine vollständige Liste anzunehmen.

_Wie kann ich den Abschluss eines Teilnehmers für einen Kurs oder ein Lernprogramm programmgesteuert zurücksetzen?_

Verwenden Sie den neuen Endpunkt:

```POST /primeapi/v2/learningObjects/{loId}/instances/{loInstanceId}/refreshCompletion```
Dadurch wird die Fertigstellung für die Zielinstanz zurückgesetzt, wenn Berechtigungen und Status dies zulassen.

_Wie erkenne ich, ob ein Teilnehmer etwas über ein alternatives oder gleichwertiges Lernobjekt abgeschlossen hat?_

Überprüfen Sie das isAlternateComplete-Attribut auf dem Lernobjekt. Wenn dieser Wert wahr ist, listet die alternativeCompletions-Beziehung die Lernobjekte auf, die als Alternativen für den Abschluss dieses Teilnehmers fungierten.

_Wie finde ich alle Alternativen, die ein bestimmtes Lernobjekt erfüllen können?_

Verwenden Sie den folgenden Endpunkt:

```GET /primeapi/v2/learningObjects/{loId}/relatedLOs?type=sourceAlternateLOs&limit={n}```

und verwenden Sie das Datenarray (für die Stellvertreter) und meta.count (für die Gesamtzahl der Stellvertreter).

_Woher weiß ich, ob ein Teilnehmer derzeit ein Modul starten darf?_

Rufen Sie zunächst den timeSlot der Ressource aus:

```GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources```
und verwenden Sie dann:

```GET /primeapi/v2/learningObjects/{loId}/instances/{loInstanceId}/loResources/{loResourceId}/canStart```

_Was bedeutet &quot;hasContentDrivenAttemptTracking&quot; für eine Ressource?_

Es gibt an, dass die Verfolgung von Versuchen durch den Inhalt selbst gesteuert wird (z. B. über SCORM/xAPI-Logik) und nicht nur durch Plattformzähler. Wenn das stimmt, verlassen Sie sich nicht nur auf die Anzahl der Versuche auf der Plattform oder die Begrenzungen für Ihre Benutzererfahrung und Ihr Reporting.

_Wie erhalte ich Menüs, die für nicht angemeldete Benutzer geeignet sind (öffentliche Erfahrungen)?_

Verwendung:

```GET /primeapi/v2/templates/menus?include=pages,subMenus.pages&isNonLoggedIn=true```

Dies gibt für anonyme Benutzer gefilterte Menü- und Seitenstrukturen zurück, die für Experience Builder oder andere Headless-Sites geeignet sind.

_Was hat sich bei der Filterung von Arbeitshilfen mit effectModifiedDate geändert?_

Anforderungen, die filter.effectModifiedDate mit filter.loTypes=jobAid kombinieren, geben jetzt korrekt nur Arbeitshilfen innerhalb des angegebenen Datumsfensters zurück.

_Was hat sich im Format der Arbeitshilferessourcen-ID geändert, und wie sollte ich damit umgehen?_

Das ID-Format wurde von Werten wie:

```jobAid:<jobAidId>_-1_-1_2_resource```

an:

```jobAid:<jobAidId>_<version>_<localeCode>```

Beispiel: jobAid:131032_2_fr_FR. Jedes System, auf dem Arbeitshilferessourcen-IDs gespeichert oder analysiert werden, muss aktualisiert werden, und Sie sollten nach dem Upgrade auf die Version vom April 2026 die Neuerstellung lokaler Indizes planen, die von diesen IDs codiert werden.
