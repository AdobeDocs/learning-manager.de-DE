---
description: Erfahren Sie mehr über die neuen Funktionen und Verbesserungen in der Version April 2026 von Adobe Learning Manager, einschließlich API- und Webhooks-Änderungen
jcr-language: en_us
title: Neue Funktionen in der Adobe Learning Manager-Version April 2026
source-git-commit: f4ff53bf053b2c8c756961af990505d23ab22db3
workflow-type: tm+mt
source-wordcount: '1768'
ht-degree: 0%

---


# Neue Funktionen in der Adobe Learning Manager-Version April 2026

**Für Teilnehmer:** Der Fluidic Player zeigt jetzt den nächsten Modulnamen und eine Schaltfläche zum Beenden an. Die Sprache des Players kann über LTI festgelegt werden, um ein einheitliches Erlebnis auf allen Plattformen zu gewährleisten. Der benutzerdefinierte Parametername ist &quot;locale&quot; und akzeptiert den Gebietsschemacode. Beispiel: locale=fr-FR. Captivate-Inhalte umfassen ein einheitliches Inhaltsverzeichnis, Vervollständigungsticks auf Folienebene und den Export zuverlässiger Notizen. Unterstützung mehrerer Sprachen für Arbeitshilfen, Checklistenfragen und Videotextspuren (VTT). Der AI-Assistent hilft Teilnehmern dabei, Antworten innerhalb des Lernerlebnisses zu erhalten.

**Für Administratoren und Autoren:** Der Zoom-Connector unterstützt mehrere gleichzeitige VILT-Sitzungen. Freigegebene Kurse in Peer-Konten zeigen den tatsächlichen Autor anstelle von &quot;Externer Autor&quot; an. Administratoren können einschränken, wann Module gestartet werden können. Ablaufdaten für Lernobjekte werden in Teilnehmer-APIs angezeigt. Checklistenmodule unterstützen eine gewichtete Punktzahl, mehrsprachigen Fragentext und optionale Reviewerkommentare. Benutzerdefinierte Zertifikate bieten einen Drag-and-Drop-Editor mit dynamischen Feldern und KI-generierten Hintergründen. Mit dem nicht angemeldeten Experience Builder können Sie öffentliche Lernseiten erstellen, ohne sich anmelden zu müssen.

**Für Kursleiter:** Generieren Sie QR-Codes für Instanzenregistrierung und Sitzungsteilnahme. Fügen Sie während der Checklistenauswertung Kommentare oder Feedback hinzu.

**Berichterstellung und Analyse:** SCORM-Inhalte können jetzt mehrere Quizversuche in L2-Berichten melden. Die Berechnung des Zeitaufwands für das Lernen wurde in Teilnehmertranskripten verbessert. Teilnehmertranskriptberichte für Administratoren werden aktualisiert. Es sind erweiterte Suchverbesserungen verfügbar.

**Anmeldemethode:** Erfahren Sie, wie die OpenID Connect-Anmeldung in Adobe Learning Manager für Teilnehmer, Autoren und Administratoren funktioniert. OpenID Connect (OIDC) ist eine gängige Anmeldemethode, die auf Webstandards basiert. Viele Unternehmen nutzen
Identitätsanbieter (z. B. Okta, Google Workspace oder Microsoft Entra ID) für Mitarbeiter und Partner.

Weitere Informationen finden Sie unter [Melden Sie sich mit OIDC](/help/migrated/oidc.md) an.

## Webhooks und Migration in Alternativen und Entsprechungen

### Webhooks

Wenn ein Teilnehmer einen Kurs über eine Alternative oder Beziehung abschließt, löst ALM ein Webhook-Ereignis aus, das vom standardmäßigen Webhook für den Kursabschluss getrennt ist. Dadurch wird sichergestellt, dass Integrationen bei Bedarf unterschiedlich auf alternative Abschlüsse reagieren können. Webhook-Ereignisse werden auch ausgelöst, wenn eine rückwirkende Fertigstellung oder eine rückwirkende Unvollständigkeit erfolgt, die historische Aktualisierungen sowie Beziehungsänderungen abdeckt.

Weitere Informationen finden Sie unter [Webhooks](/help/migrated/integration-admin/feature-summary/webhooks.md#webhooks-for-alternates).

### Migration

Das CSV-basierte Datenmodell und Migrationsverhalten zur Einführung der Lernobjektäquivalenz (LO) im System wird in [Webhooks](/help/migrated/integration-admin/feature-summary/migration-manual.md#migration-for-alternates-and-equivalents) beschrieben.

## Automatische Bereinigung gelöschter Benutzer

Die automatische Bereinigung gelöschter Benutzer ist eine Funktion, mit der Daten für Benutzer bereinigt werden, die bereits in ALM gelöscht wurden. Die Bereinigung erfolgt nach einer konfigurierbaren Aufbewahrungsfrist, wobei der Schwerpunkt auf Massenvorgängen liegt, sodass große Kundenkonten effizient bearbeitet werden können, ohne dass die Performance beeinträchtigt wird.

Weitere Informationen finden Sie unter [Automatische Bereinigung gelöschter Benutzer](/help/migrated/administrators/feature-summary/purge-users.md#auto-purge-of-deleted-users).

## Einstellen der Zugriffszeit des Moduls

Mithilfe der Erweiterung können Autoren und Administratoren in Adobe Learning Manager ein Zeitfenster definieren, in dem Teilnehmer ein Modul starten dürfen. Außerhalb des konfigurierten Start-/Endfensters bleibt das Modul in der Kursstruktur sichtbar, aber die Teilnehmer können es nicht initiieren.

Weitere Informationen finden Sie unter [Modulzugriffszeitsteuerung einstellen](/help/migrated/administrators/feature-summary/module-access-time-control.md).

## Änderungen an Teilnehmertranskripten

Diese Version verbessert den Teilnehmertranskriptbericht (LT) durch eine bessere Überprüfbarkeit und Compliance-Unterstützung.

* Eine neue Spalte &quot;Abschlussmethode&quot; in der Admin LT zeigt an, ob Abschlüsse direkt, alternativ oder widerrufen wurden, während alternative Abschlüsse jetzt den Status, das Abschlussdatum und die Abschlussquelle beeinflussen, indem sie geerbte Daten aus Quelltrainings verwenden und aktualisieren, wenn Quellen widerrufen werden oder direkte Abschlüsse auftreten.
* Widerrufene Alternativen passen Status, Abschlussdatum und Abschlussquelle automatisch an, wenn alle qualifizierenden Beziehungen entfernt werden und die rückwirkende Unvollständigkeit aktiviert ist.
* Das Reviewer-Feedback aus Checklistenmodulen ist in der Spalte &quot;Anmerkungen des Reviewers&quot; unter &quot;Administrator- und Teilnehmer-LTs&quot; und in allen Exportkanälen standardisiert.
* Und schließlich kann bei der Berechnung der Lernzeit zwischen aktiver und inaktiver Zeit besser unterschieden werden, wodurch die Genauigkeit der Interaktions- und Compliance-Berichte verbessert wird.

Weitere Informationen finden Sie unter [Änderungen im Teilnehmertranskriptbericht](/help/migrated/administrators/feature-summary/reports/changes-in-learner-transcript.md).

## Checkliste mit Kommentarfunktion für Reviewer

Mit dieser Funktion können Reviewer während der Checklistenauswertung Kommentare oder Feedback hinzufügen. Sie können jedem Teilnehmer ein personalisiertes, verwertbares Feedback geben. Sie können auch Ihren Namen mit Ihren Kommentaren anzeigen, um die Transparenz zu erhöhen. Alle Anmerkungen werden im Transkript des Teilnehmers gespeichert und in die Berichte der Checkliste aufgenommen.

Weitere Informationen finden Sie unter [Checkliste mit Kommentaren konfigurieren](/help/migrated/authors/feature-summary/courses.md#checklist-with-commenting).

## Unterstützung mehrerer Sprachen für Checkliste

Mit dieser Funktion können Sie Checklistenmodule in mehreren Sprachen erstellen und verwalten. Jede Frage, jede Anweisung und jedes Bewertungskriterium der Checkliste kann übersetzt werden, sodass Prüfer und Teilnehmer mit der Checkliste in ihrer bevorzugten Sprache interagieren. Das System zeigt die Checkliste in der vom Benutzer ausgewählten Inhaltssprache an, was die Zugänglichkeit und Compliance für globale Teams verbessert.

[Mehrsprachige Checkliste in Modulen erstellen](/help/migrated/authors/feature-summary/courses.md#create-a-multi-language-checklist) anzeigen

## Checklistenfragengewichtung für Kursleiterbewertungen

Mit dieser Funktion können Sie jeder Checklistenfrage unterschiedliche Höchstpunktzahlen (Gewichtung) zuweisen. Sie können die unterschiedliche Bedeutung oder Schwierigkeit jeder Frage widerspiegeln, was genauere und aussagekräftigere Bewertungen unterstützt. Das System berechnet die Gesamtpunktzahl basierend auf Ihren Eingaben und bestimmt, ob der Teilnehmer die von Ihnen festgelegten Kriterien besteht oder nicht.

[Gewichtete Checklistenfragen erstellen](/help/migrated/authors/feature-summary/courses.md#how-to-create-a-weighted-checklist) anzeigen

## Benutzerdefinierte Zertifikate

Mit benutzerdefinierten Zertifikaten in Adobe Learning Manager (ALM) können Administratoren und Autoren personalisierte Zertifikate für Teilnehmer entwerfen, verwalten und ausstellen.

Die Funktion umfasst einen Drag-and-Drop-Editor, dynamische Felder, mehrsprachigen Support und KI-generierte Hintergründe, mit denen Organisationen ohne technische Kenntnisse Markenzertifikate erstellen können.

[Benutzerdefinierte Zertifikate entwerfen](/help/migrated/administrators/feature-summary/create-customize-certificate.md) anzeigen

## Nicht angemeldete Benutzererfahrung in Experience Builder

Das nicht angemeldete Erlebnis in Experience Builder ermöglicht es Unternehmen, ihre Lerninhalte und Portalseiten für alle Besucher anzuzeigen, einschließlich derjenigen, die sich nicht angemeldet haben. Diese Funktion soll potenzielle Teilnehmer anziehen, informieren und ansprechen, indem sie eine reibungslose und markenkonforme Vorschau Ihrer Schulungsangebote bietet, bevor sie sich anmelden oder registrieren müssen.

[Nicht angemeldetes Erlebnis in Experience Builder anzeigen](/help/migrated/administrators/feature-summary/experience-builder/non-logged-in-experience.md)

## Erweiterte Suchverbesserungen

Die Suchergebnisse in der erweiterten Suche sind jetzt genauer und relevanter. Genaue Stichwortübereinstimmungen werden bei der inhaltsbezogenen Suche und den Metadaten höher eingestuft, was es den Teilnehmern erleichtert, genau das zu finden, wonach sie suchen.

Teilnehmer können jetzt auch registrierte Lernobjekte in Suchergebnissen sehen, selbst wenn sie nicht Teil eines barrierefreien Katalogs sind. So wird sichergestellt, dass keine relevanten Inhalte verpasst werden. Darüber hinaus wurde das Ranking der Arbeitshilfen sowohl für die erweiterte Suche als auch für die inhaltsinterne Suche verbessert, sodass die relevantesten Ressourcen schneller angezeigt werden.

## Mehrsprachige Arbeitshilfen

Mithilfe mehrsprachiger Arbeitshilfen in Adobe Learning Manager (ALM) können Autoren und Administratoren unterstützende Dokumente, Hilfslinien oder Ressourcen in mehreren Sprachen in einem einzigen Arbeitshilfeeintrag zur Verfügung stellen. Teilnehmer aus verschiedenen Regionen können auf relevante Materialien in ihrer bevorzugten Sprache zugreifen, was das Verständnis, die Compliance und die Benutzerfreundlichkeit verbessert.

Weitere Informationen finden Sie unter [Mehrsprachige Arbeitshilfen hinzufügen](/help/migrated/authors/feature-summary/job-aids.md#create-a-multilingual-job-aid).

## Unterstützung von mehrsprachigen Video-Text-Tracks (VTT) (für Autoren)

Die Unterstützung mehrsprachiger Videotextspuren (VTT) in Adobe Learning Manager ermöglicht es Autoren, Untertitel und Untertitel für Video- und Audioinhalte in mehreren Sprachen bereitzustellen. Diese Funktion vereinfacht die Lokalisierung, macht Schulungen für ein weltweites Publikum zugänglich und stellt die Einhaltung von Standards für Barrierefreiheit sicher. Autoren können VTT-Dateien automatisch direkt auf der Plattform generieren, übersetzen, überprüfen und bearbeiten.

Weitere Informationen finden Sie unter [Unterstützung mehrsprachiger VTT-Anwendungen](/help/migrated/authors/feature-summary/content-library.md#multi-lingual-vtt-support).

## Ursprünglichen Autor für freigegebene Kurse in Peer-Konten anzeigen

Wenn ein Kurs über den Katalog für ein Peer-Konto freigegeben wird, kennzeichnet Adobe Learning Manager den Autor derzeit in der Teilnehmer-, Administrator- und Autorenansicht des empfangenden Kontos als &quot;Externer Autor&quot;. Dies kann zu Herausforderungen für Teilnehmer und Administratoren führen, insbesondere in großen Unternehmen, da es schwierig wird, den entsprechenden Inhaltseigentümer zu identifizieren und zu kontaktieren, wenn Probleme oder Fragen auftreten.

Durch die Verbesserung wird sichergestellt, dass Autoreninformationen beibehalten und für freigegebene Kurse in Peer-Konten angezeigt werden, anstatt durch einen generischen Platzhalter ersetzt zu werden.

### Neue Funktionen

Anzeigen des tatsächlichen Autorennamens für freigegebene Kurse in Peer-Konten

Bei Kursen, die über externe oder Peer-Kataloge freigegeben wurden, wird der ursprüngliche Autorenname aus dem Quellkonto jetzt im empfangenden Konto anstelle von &quot;Externer Autor&quot; angezeigt.

Dies gilt für:

* Teilnehmer-App (Kurskarte oder Kursdetails).
* Administrator- und Autorenansichten bei der Vorschau als Teilnehmer.

Weitere Informationen finden Sie unter [Anzeige des Autorennamens für freigegebene Kurse](/help/migrated/administrators/feature-summary/peer-account.md#author-name-display-for-shared-courses-including-previously-acquired-courses).

## Entsprechungen und Stellvertreter

Bieten Sie ein reibungsloses Lernerlebnis und eliminieren Sie redundante Schulungen mit Entsprechungen und Alternativen in ALM. Mit dieser neuen Funktion können Administratoren unidirektionale (alternierende) oder bidirektionale (äquivalente) Regeln konfigurieren, bei denen durch das Absolvieren einer Schulung automatisch ein alternativer Abschluss für eine andere erteilt wird. Diese Funktion wurde entwickelt, um große Lern-Ökosysteme zu optimieren, und stellt sicher, dass Teilnehmer Inhalte umgehen, die sie bereits gemeistert haben, und Organisationen reduzieren die Support-Tickets für Administratoren drastisch, eliminieren manuelle Überschreibungen und pflegen eine sauberere, genauere Lernbilanz.

Weitere Informationen finden Sie unter [Entsprechungen und Alternativen](/help/migrated/administrators/feature-summary/alternates-equivalence.md).

## QR-Codes von Kursleitern für die Instanzenregistrierung und die Sitzungsteilnahme

Kursleiter können QR-Codes selbst generieren für:

* Registrierung für Kursinstanzen,
* Sitzungsteilnahme oder
* Anmeldung + gemeinsame Teilnahme

auf Sitzungsebene. Es wurde für Situationen entwickelt, in denen Teilnehmer einen physischen oder hybriden Klassenzimmer betreten und eine schnelle Self-Service-Option benötigen, um sich mit einem QR-Code zu registrieren und ihre Teilnahme aufzuzeichnen.

Weitere Informationen finden Sie unter [QR-Codes für Teilnehmerregistrierung und Anwesenheit herunterladen](/help/migrated/instructors/feature-summary/learners.md#download-qr-codes-for-learner-enrollment-and-attendance).

## Kalendereinladungen (ICS) mit Sitzungslinks

Adobe Learning Manager enthält den Link **Sitzung beitreten direkt in Kalendereinladungen (ICS-Dateien)**, die an Teilnehmer und Kursleiter gesendet wurden. So können Teilnehmer direkt aus ihrem Kalender heraus an Sitzungen teilnehmen, ohne nach der Sitzungs-E-Mail suchen zu müssen.

Diese Verbesserung verbessert die Benutzerfreundlichkeit für Kalenderclients wie **Gmail** und **Outlook**.

Weitere Informationen finden Sie unter [Kalendereinladungen mit Sitzungslinks](/help/migrated/instructors/feature-summary/learners.md#joining-a-session-from-gmail).

## KI-Assistent für Teilnehmende

Mit dem AI Assistant (Beta) für Teilnehmer können sie schnell Antworten auf die zugewiesenen Lerninhalte finden, ohne sich durch ganze Kurse bewegen zu müssen. Sie können Fragen in verständlicher Sprache stellen und erhalten präzise, zielgerichtete Antworten mit Quell-Links zu den relevanten Kursinhalten.

Funktionen, unterstützte Szenarien und Einschränkungen können sich mit der Weiterentwicklung der Funktion ändern. Der AI Assistant ist ein generativer KI-gestützter Chat-Begleiter in Adobe Learning Manager, der schnelle, präzise Antworten mithilfe Ihrer vertrauenswürdigen Lerninhalte bereitstellt. Sie enthält Zitate, damit Sie immer wissen, aus welcher Quelle die Informationen stammen.

[AI-Assistent für Teilnehmer anzeigen](/help/migrated/learners/feature-summary/learner-ai-assistant.md)


## API-Änderungen in der Version

Die Adobe Learning Manager-Version vom April 2026 enthält Verbesserungen der öffentlichen API für Alternativen und Entsprechungen, Zugriff im Zeitfenster auf Inhalte, inhaltsbasierte Quizversuche, nicht angemeldete Erlebnisse und die Verarbeitung von Arbeitshilfen. Die Änderungen sind weitgehend abwärtskompatibel ausgelegt und ermöglichen gleichzeitig präzisere Integrationen.

[API-Änderungen in der April-Version anzeigen](/help/migrated/api-changes-alm.md)

## Systemanforderungen

[Systemanforderungen für Adobe Learning Manager anzeigen](/help/migrated/system-requirements.md).

## Versionshinweise

Lesen Sie die [Versionshinweise](/help/migrated/release-note/release-notes.md) für die neuesten Versionsupdates.

## Frühere Versionen von Adobe Learning Manager

* [Adobe Learning Manager Version Oktober 2025](/help/migrated/whats-new-october-2025.md)
* [Adobe Learning Manager Version Mai 2025](/help/migrated/whats-new-may-2025.md)
