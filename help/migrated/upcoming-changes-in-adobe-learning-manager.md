---
title: Neue Funktionen in der Adobe Learning Manager-Version April 2026
description: Erfahren Sie mehr über die neuen Funktionen, Verbesserungen und wichtigen Updates in der Adobe Learning Manager-Version vom April 2026.
exl-id: 4d2129c4-42d8-446f-8837-879b5c2f42bf
source-git-commit: 78b345adf3fb39cdfa728ff4a788be1b36fff906
workflow-type: tm+mt
source-wordcount: '20211'
ht-degree: 0%

---

# Updates in Adobe Learning Manager

>[!IMPORTANT]
>
>Die Funktionen in dieser Version sind in der Beta-Version verfügbar. Funktionalität und Verhalten können sich vor der allgemeinen Verfügbarkeit ändern. Teilen Sie Feedback über Ihre üblichen Adobe-Support-Kanäle.


In diesem Dokument werden die neuen Funktionen, Verbesserungen und Updates der Version April 2026 von Adobe Learning Manager zusammengefasst. Verwenden Sie es, um Änderungen für Ihr Unternehmen zu planen und zu verstehen, was für Teilnehmer, Administratoren und Autoren verfügbar ist.

**Für Teilnehmer:** Der Fluidic Player zeigt jetzt den nächsten Modulnamen und eine Schaltfläche zum Beenden an. Die Sprache des Players kann über LTI festgelegt werden, um ein einheitliches Erlebnis auf allen Plattformen zu gewährleisten. Captivate-Inhalte umfassen ein einheitliches Inhaltsverzeichnis, Vervollständigungsticks auf Folienebene und den Export zuverlässiger Notizen. Unterstützung mehrerer Sprachen für Arbeitshilfen, Checklistenfragen und Videotextspuren (VTT). Der AI-Assistent hilft Teilnehmern dabei, Antworten innerhalb des Lernerlebnisses zu erhalten.

**Für Administratoren und Autoren:** Der Zoom-Connector unterstützt mehrere gleichzeitige VILT-Sitzungen. Freigegebene Kurse in Peer-Konten zeigen den tatsächlichen Autor anstelle von &quot;Externer Autor&quot; an. Administratoren können einschränken, wann Module gestartet werden können. Ablaufdaten für Lernobjekte werden in Teilnehmer-APIs angezeigt. Checklistenmodule unterstützen eine gewichtete Punktzahl, mehrsprachigen Fragentext und optionale Reviewerkommentare. Benutzerdefinierte Zertifikate bieten einen Drag-and-Drop-Editor mit dynamischen Feldern und KI-generierten Hintergründen. Mit dem nicht angemeldeten Experience Builder können Sie öffentliche Lernseiten erstellen, ohne sich anmelden zu müssen.

**Für Kursleiter:** Generieren Sie QR-Codes für Instanzenregistrierung und Sitzungsteilnahme. Fügen Sie während der Checklistenauswertung Kommentare oder Feedback hinzu.

**Berichterstellung und Analyse:** SCORM-Inhalte können jetzt mehrere Quizversuche in L2-Berichten melden. Die Berechnung des Zeitaufwands für das Lernen wurde in Teilnehmertranskripten verbessert. Teilnehmertranskriptberichte für Administratoren werden aktualisiert. Es sind erweiterte Suchverbesserungen verfügbar.

## Fluidic Player-Navigation: Zeigt den Namen des nächsten Moduls an.

### Übersicht

Diese Verbesserung war bereits in der Version November 2025 von Adobe Learning Manager enthalten.

Die Aktion &quot;Weiter&quot; im Player zeigt an, was passiert, wenn auf den Button geklickt wird, indem der Name des nächsten Moduls oder Kurses angezeigt und explizit signalisiert wird, wann der Teilnehmer den Player beenden wird.

### Neue Funktionen

**Bezeichnung &quot;Nächstes Modul: {ModuleName}&quot; im Player**

Das Symbol Weiter im Fluidic Player zeigt jetzt den Namen des nächsten Moduls im Kurs an. Beispiel: Nächstes Modul: Lektion 2 - Erste Schritte.

Dies gilt, wenn der Teilnehmer innerhalb desselben Kurses von einem Modul zum nächsten wechselt.

**Aktion zum Beenden des letzten Moduls löschen**

Wenn sich der Teilnehmer im letzten Modul eines Kurses befindet, wird eine neue Schaltfläche &quot;Aktion beenden&quot; angezeigt, die angibt, dass der Player durch Klicken geschlossen und wieder in den Kurskontext eingefügt wird.

**Responsives Verhalten für Inhalte für Mobilgeräte und PDF**

Bei kleineren Viewports (z. B. ~320 px Breite) wird die Beschriftung &quot;Weiter&quot; möglicherweise verkürzt oder ausgeblendet, sodass nur das Symbol angezeigt wird, um Überschneidungen mit den PDF-Steuerelementen zu vermeiden.

Bei PDF-Modulen passt der Player die Steuerelemente an eine separate Zeile an, sodass Navigationsbeschriftungen und PDF-Steuerelemente sich nicht gegenseitig stören.

**Admin > Branding > Player-Vorschau aktualisiert**

Die Player-Vorschau in Admin > Branding zeigt jetzt die neue Beschriftung an, z. B. &quot;Nächstes Modul: Lektion 2&quot;. Dadurch können Administratoren das aktualisierte Navigationsverhalten anzeigen.

### Wichtigste Vorteile

**klarere Navigation für Teilnehmer**

Die Teilnehmer müssen nicht mehr raten, was passiert, wenn sie &quot;Weiter&quot; auswählen. Auf dem Etikett ist klar angegeben, was als Nächstes kommt, ob es sich um ein Modul oder einen Kurs handelt. Diese Verringerung der Mehrdeutigkeit hilft, Zögern und Verwirrung zu lindern, insbesondere bei großen Zielgruppen im Kundenschulungsbereich, bei denen viele Teilnehmer nicht mit LMS-Schnittstellen vertraut sind.

**Höhere Kursabschlussraten**

Das klare Angeben des nächsten Schritts (nächstes Modul: {ModuleName}) und das Hinzufügen einer deutlichen Exit-Aktion für das letzte Modul verringert die Wahrscheinlichkeit, dass Teilnehmer den Kurs beenden oder den letzten Abschlussschritt übersehen.

**Berechenbarere Benutzererfahrung auf allen Geräten**

Die aktualisierten Beschriftungen entsprechen dem Verhalten &quot;Nächste&quot; oder &quot;Vorherige&quot; und den Symbolen auf Desktop, Tablet und Smartphone. Layouteinschränkungen werden auf allen Geräten und PDF-Flows beachtet, sodass Steuerelemente weiterhin verwendbar und zugänglich sind.

Dies ist besonders wichtig für Headless-Implementierungen, bei denen der Fluidic Player in ein benutzerdefiniertes Lernerlebnis eingebettet ist.

### Anwendungsszenarien

**Schulungsportale für Kunden und Partner (Headless oder AEM integriert)**

Konten, die Adobe Learning Manager in einem Headless-Setup nutzen und die Teilnehmer von externen Marketing-Kanälen leiten Diese Teilnehmer:

* Häufig werden Videoinhalte in langen Sequenzen konsumiert.

* Sie sollten ein Erlebnis wie im Lehrplan erwarten, bei dem das System die nächste Episode/das nächste Modul deutlich anzeigt.

In diesen Umgebungen wird die Bezeichnung &quot;**Nächstes Modul:{ModuleName}**&quot; wie folgt angezeigt:

* Bekräftigt die Führung der Reise.

* Minimiert das Ablegen zwischen Modulen.

**Compliance- und Zertifizierungskurse mit bestellten Modulen**

In regulierten oder Compliance-intensiven Szenarien:

* Teilnehmer müssen eine strikte Abfolge von Modulen abschließen.

* Autoren deaktivieren oft das Inhaltsverzeichnis, um ein Überspringen zu vermeiden.

Hier wird **Nächstes Modul:{ModuleName}** angezeigt:

* Bestätigt den Teilnehmern, dass sie die richtige Reihenfolge befolgen.

* Vermindert die Wahrscheinlichkeit, dass sie die nächste Aktion falsch interpretieren und den Dienst vorzeitig beenden.

**Lernpfade, in denen Kurse aufeinander folgen**

Wo Lernpfade oder Äquivalente mehrere Kurse verknüpfen. Dies ist nützlich, wenn Sie Sequenzen im Curriculum-Stil für ein großes Publikum erstellen.

**Erste Verwendung für Mobilgeräte**

Für Teilnehmer, die hauptsächlich Smartphones oder Tablets verwenden:

* Aktualisierte Beschriftungen und ein reaktionsfähiges Verhalten stellen sicher, dass die Navigation verständlich bleibt, ohne auf winzige Schließen-Symbole oder ausgeblendete Steuerelemente angewiesen zu sein.

* Dies ist wichtig für Kundenschulungen, Gig Worker oder Teilnehmer an vorderster Front, die in kurzen Sitzungen auf mobilen Geräten auf Inhalte zugreifen können.

## Zoom-Connector - Erstellen mehrerer gleichzeitiger Zoom-Sitzungen

### Übersicht

Das Upgrade des Zoom-Connectors verbessert die Verwaltung von Virtual Instructor-Led Training (VILT) durch Adobe Learning Manager. Früher konnten Benutzer jeweils nur eine Zoom-Sitzung erstellen. Mit dem neuen Update können Administratoren und Autoren über die Standardintegration mehrere Zoom-Sitzungen gleichzeitig planen.

### Neue Funktionen

#### Unterstützung für mehrere gleichzeitige Zoom-Sitzungen über den Connector

* Mit dem Zoom-Connector können jetzt mehr als eine VILT-Sitzung zum gleichen Datum/zur gleichen Zeit aus ALM erstellt werden.

* Die Planungslogik erzwingt nicht mehr die Einschränkung &quot;ein Zoom-Meeting nach dem anderen&quot; auf Konto-/Connector-Ebene.

* Administratoren und Autoren können überlappende VILT-Sitzungen (z. B. regionale Klassenzimmer, parallele Tracks oder wiederholte Sitzungen für verschiedene Partnergruppen) ohne Umgehungslösungen konfigurieren.

#### Meetings werden mit der Zoom-Identität des Kursleiters erstellt (nicht mit dem Zoom-Superadministrator)

Um gleichzeitige Meetings sicher zu unterstützen, wurde der Connector aktualisiert, sodass:

* Zoom-Meetings werden jetzt mit der E-Mail-Adresse des Kursleiters anstelle der E-Mail &quot;Zoom Super Admin&quot; erstellt.

* Das Zoom-Konto jedes Kursleiters kann parallel zu anderen Kursleitern eigene Meetings veranstalten, vorbehaltlich der Einschränkungen des bestehenden Zoom-Plans.

**Hinweis**:

* Es wird nur noch ein Kursleiter pro Meeting unterstützt.

* Wenn die E-Mail-Adresse eines Kursleiters später in Adobe Learning Manager aktualisiert wird, bleiben bestehende Meetings mit der ursprünglichen E-Mail-Adresse verknüpft, die bei der Erstellung verwendet wurde.

#### Das manuelle Einfügen der Zoom-URL für gleichzeitige Sitzungen ist nicht mehr erforderlich

Früher, als eine zweite oder dritte Zoom-Sitzung gleichzeitig ausgeführt werden musste:

* Autoren mussten Zoom-Meetings außerhalb von ALM manuell erstellen und dann die Zoom-Join-URL in die Kursinstanzkonfiguration einfügen.

* Dies war fehleranfällig und hat nicht von Connector-Funktionen wie der Anwesenheitsverfolgung profitiert.

Mit dem aktualisierten Connector:

* Alle Sessions können mithilfe des Zoom-Connectors direkt über die ALM-Benutzeroberfläche erstellt werden, auch wenn sie sich zeitlich überlappen.

* Der Sitzungslebenszyklus (Erstellung/Abbruch) wird weiterhin zentral über die Integration verwaltet.

### Wichtigste Vorteile

#### Bessere VILT-Planung im benötigten Umfang.

Organisationen haben jetzt folgende Möglichkeiten:

* Führen Sie mehrere Zoom-basierte virtuelle Klassenzimmer gleichzeitig aus (z. B. parallele Kurse an einem virtuellen Gipfel, regionale Kohorten oder separate Partnerschulungen).

* Vermeiden Sie Engpässe, die Administratoren zuvor zwangen, Sitzungen zu serialisieren, oder nutzen Sie die manuelle Zoom-Verwaltung.

#### Verringerter Administrator- und Autorenaufwand

Durch die Verbesserung entfällt Folgendes:

* Manuelle Erstellung von Zoom-Meetings außerhalb von Adobe Learning Manager.

* Kopieren Sie Zoom-URLs und fügen Sie sie für überlappende Sitzungen in jede Kursinstanz ein.

* Risiko falsch konfigurierter Links, falscher Meetings oder fehlender Anwesenheitsverfolgung.

Administratoren und Autoren können alle Zoom-Sitzungen über Adobe Learning Manager mithilfe vertrauter Workflows verwalten.

#### Bessere Ausrichtung an Zoom-Bereitstellung und Kursleiterrollen

Durch Verbinden von Meetings mit einzelnen Kursleiter-Zoom-Konten:

* Jeder Kursleiter kann innerhalb seiner eigenen Zoom-Lizenzbeschränkungen arbeiten.

* Unternehmen können ihr bestehendes Zoom-Bereitstellungsmodell verwenden (ein Konto pro Trainer, pro Geschäftseinheit usw.). und dennoch vollständig mit Adobe Learning Manager integrieren.

* Dadurch wird der Single-Point-Engpass vermieden, den die Verwendung eines gemeinsamen Super-Admin-Zoom-Benutzers für alle Sitzungen verursacht.

### Anwendungsszenarien

#### Multitrack-Veranstaltungen und -Gipfeltreffen

Kundenschulungsteams, die große Veranstaltungen durchführen (z. B. Produkt-Bootcamps, Partnergipfel oder Zertifizierungswochen), können:

* Konfigurieren Sie mehrere Zoom-basierte Sitzungen im selben Zeitfenster (für verschiedene Spuren oder Themen).

* Verwalten Sie sie alle als VILT-Module in den Kursen und Lernpfaden von Adobe Learning Manager.

* Bieten Sie Teilnehmern ein einheitliches Erlebnis, während der Connector die gesamte Erstellung von Zoom-Meetings übernimmt.

#### Globale Partner- und Kundenschulungen

Organisationen, die Kunden und Partner in verschiedenen Regionen schulen, können Folgendes:

* Führen Sie separate Zoom-Sitzungen für EMEA, APAC und Nord- und Südamerika zu überlappenden Zeiten durch, um die lokalen Arbeitszeiten abzugleichen.

* Vermeiden Sie es, einen einzelnen globalen Zeitschlitz oder manuellen Zoom-Setup für zusätzliche Kohorten zu erzwingen.

#### Interne Aktivierung

Interne Enablement-Teams (Vertrieb, Support usw.) können:

* Planen Sie parallele Onboarding-Sitzungen oder rollenbasierte Breakout-Sessions (z. B. separate Zoom-Räume für Entwickler, Administratoren und geschäftliche Stakeholder) in ALM.

* Bewahren Sie alle Sitzungen im VILT-Modell von ALM zu Reporting- und Compliance-Zwecken auf, anstatt teilweise zu nicht verwalteten Zoom-Meetings zu wechseln.

## Ursprünglichen Autor für freigegebene Kurse in Peer-Konten anzeigen

### Übersicht

Wenn ein Kurs über den Katalog für ein Peer-Konto freigegeben wird, kennzeichnet Adobe Learning Manager den Autor derzeit in der Teilnehmer-, Administrator- und Autorenansicht des empfangenden Kontos als &quot;Externer Autor&quot;. Dies kann zu Herausforderungen für Teilnehmer und Administratoren führen, insbesondere in großen Unternehmen, da es schwierig wird, den entsprechenden Inhaltseigentümer zu identifizieren und zu kontaktieren, wenn Probleme oder Fragen auftreten.

Durch die Verbesserung wird sichergestellt, dass Autoreninformationen beibehalten und für freigegebene Kurse in Peer-Konten angezeigt werden, anstatt durch einen generischen Platzhalter ersetzt zu werden.

### Neue Funktionen

Anzeigen des tatsächlichen Autorennamens für freigegebene Kurse in Peer-Konten

Bei Kursen, die über externe oder Peer-Kataloge freigegeben wurden, wird der ursprüngliche Autorenname aus dem Quellkonto jetzt im empfangenden Konto anstelle von &quot;Externer Autor&quot; angezeigt.

Dies gilt für:

* Teilnehmer-App (Kurskarte oder Kursdetails).

* Administrator- und Autorenansichten bei der Vorschau als Teilnehmer.

### Wichtigste Vorteile

#### Direkte Eigentümersichtbarkeit für freigegebene Inhalte

Teilnehmer und Administratoren in Peer-Konten können jetzt:

* Sehen Sie, wer den Kurs erstellt hat, auch wenn er über einen freigegebenen Katalog erworben wurde.

* Vermeiden Sie die generische und wenig hilfreiche Beschriftung &quot;Externer Autor&quot;.

#### Konsistentere Erlebnisse für mehrere Mandanten und Peer-Accounts

Für Kunden, die mehrmandantenfähige oder erweiterte Unternehmensszenarien ausführen:

* Derselbe Kurs wird mit konsistentem Branding für Autoren auf allen Konten angezeigt.

* Das Teilnehmererlebnis wird den Erwartungen des primären Kontos angepasst (wenn beispielsweise der Name des Autors des Quellkontos anstelle von &quot;Externer Autor&quot; angezeigt wird).

### Anwendungsszenarien

#### Großunternehmen mit Peer-Konten

Das Unternehmen verwendet ALM mit:

* ein Hauptkonto, dem die kanonischen Kurse gehören, und

* Peer-Konten, die Inhalte über freigegebene Kataloge erwerben.

Teilnehmer in Peer-Konten müssen wissen, welches Unternehmensteam einen Kurs erstellt hat, um Fragen oder Verbesserungsvorschläge korrekt weiterzuleiten.

Mit dieser Verbesserung:

* Freigegebene Kurse zeigen jetzt den richtigen Unternehmensautorennamen in Peer-Konten an.

* Die interne Supportlast des Unternehmens wird verringert, da Teilnehmer und lokale Administratoren wissen, an wen sie sich wenden müssen.

#### Interne Multi-BU-Freigabe

Wo eine Geschäftseinheit das Lernen für andere kuratiert:

* Die Eigentümer-BU kann im Autorenfeld für alle konsumierenden Konten identifiziert werden.

* Lokale L&amp;D-Administratoren können schnell erkennen, ob ein Kurs lokal oder von einer anderen Geschäftseinheit verwaltet wird, und entsprechend zusammenarbeiten.

## Verfügbarmachen des Ablaufdatums des Lernobjekts (automatische Einstellung) in Teilnehmer-APIs

### Übersicht

Durch diese Verbesserung wird das Datum der automatischen Einstellung eines Lernobjekts (LO) direkt über die APIs für Teilnehmer in Adobe Learning Manager verfügbar gemacht. Wenn ein Kurs, ein Lernpfad oder eine Zertifizierung mit einem Ablaufdatum oder einem Datum für die automatische Einstellung konfiguriert ist, sind diese Informationen jetzt Teil der LO-Daten, die von wichtigen Teilnehmerendpunkten zurückgegeben werden.

### Neue Funktionen

#### Neues Feld für das Ablaufen/automatische Einstellen in Teilnehmer-LO-APIs

* Die Teilnehmer-LO-APIs (z. B. die Endpunkte, die Lernobjekte an die Teilnehmererfahrung und an externe Plattformen zurückgeben) enthalten jetzt das LO-Ablaufdatum (das für dieses Lernobjekt konfigurierte Datum für die automatische Einstellung).

* Dieses Feld wird als Teil der LO-Entität in Antworten wie den folgenden zurückgegeben:

   * Lernobjekt abrufen (LO-Details).

   * LO-Daten, die zum Füllen der Startseite, des Katalogs und der Suchergebnisse der Teilnehmer verwendet werden.

* Das Feld ergänzt die vorhandene Frist für Fertigstellung, die bereits auf Instanzebene vorhanden ist. Das neue Feld ist speziell das Datum der automatischen Einstellung auf LO-Ebene.

#### Verfügbarkeit von durchsuchten Teilnehmererlebnissen

Da das Ablaufdatum als Teil der suchbasierten LO-Darstellung angezeigt wird, ist es jetzt überall verfügbar, wo ALM oder eine externe Plattform verwendet:

* Such-APIs oder

* suchgesteuerte Kataloge und Vorschläge zum Erstellen von Teilnehmeransichten.

**Umfang und Ausschlüsse**

Die Verbesserung gilt nur für Teilnehmer-APIs.

### Wichtigste Vorteile

#### Expiry-bewusste Teilnehmererfahrung in benutzerdefinierten LXPs

Für große und mittlere Unternehmen kann das benutzerdefinierte LXP jetzt LO-Ablaufinformationen direkt von ALM abrufen, sodass sie:

* Auf Kurskarten und Detailseiten die Beschriftungen &quot;Ablaufdatum am {date}&quot; oder &quot;Bald ablaufen&quot; anzeigen.

* Kommunizieren Sie mit der Dringlichkeit klarer, sodass die Teilnehmer Schulungen, die demnächst eingestellt werden, priorisieren.

Dies ist besonders wichtig für Compliance- oder zeitgebundene Produktschulungen, bei denen Lernobjekte regelmäßig aktualisiert werden und ältere Versionen eingestellt werden.

#### Bessere Anleitung für Teilnehmer, an denen jetzt Schulungen absolviert werden sollen

Indem das LO-Ablaufdatum angezeigt wird, kann die Teilnehmererfahrung Folgendes tun:

* Markieren Sie die Kurse, die noch gültig sind, im Vergleich zu denen, die demnächst eingestellt werden.

* Helfen Sie Teilnehmern dabei, sich nicht für Schulungen zu registrieren, die in naher Zukunft nicht mehr verfügbar oder gültig sind.

#### Übereinstimmung mit den Daten zum Abschlusstermin

Bisher haben Teilnehmer-APIs bereits das Abschlussdatum auf Instanzebene, aber nicht das Datum der automatischen Einstellung auf LO-Ebene angezeigt. Mit dieser Änderung:

Folgende Aspekte einer Schulung stehen zur Verfügung:

* &quot;Bis wann muss ich diese Instanz beenden?&quot; (Ausfülltermin).

* &quot;Bis wann wird diese Schulung angeboten?&quot; (automatische Einstellung/Ablaufdatum).

### Anwendungsszenarien

#### Ein globales Unternehmen mit striktem Management des Kurslebenszyklus

Unternehmen, die regelmäßig Kurse einstellen und ersetzen (z. B. durch Aktualisierungen von Vorschriften, Produkten oder Methoden), haben folgende Möglichkeiten:

* Vermeiden Sie Verwirrung bei den Teilnehmern darüber, ob eine Schulung schrittweise eingestellt wird.

* Motivieren Sie Teilnehmer zu aktuellen, langfristigen Angeboten.

Benutzerdefinierte Portale und interne Tools können das Ablaufdatum jetzt direkt aus ALM über die Teilnehmer-APIs lesen.

#### Externe Kunden- oder Partnerakademien

Bei Schulungen für Kunden und Partner stehen für Marketing-Seiten und -Portale oft aktuelle Schulungen im Vordergrund.

Ablaufdaten in der LO-API ermöglichen es Experience Buildern:

* Blenden Sie Inhalte aus, die kurz vor dem Eintritt in den Ruhestand stehen, oder heben Sie deren Hervorhebung auf.

* Kampagnen für den letzten Schliff entwickeln.

## Unterstützung mehrerer Sprachen für Arbeitshilfen

### Übersicht

Durch die Erweiterung wird das Lokalisierungsmodell von Adobe Learning Manager auf Arbeitshilfen erweitert, sodass Autoren verschiedene Inhaltsdateien pro Sprache an eine einzelne Arbeitshilfe anhängen können. Anstatt separate Arbeitshilfen für jede Sprache zu erstellen, können Autoren jetzt alle lokalisierten Versionen als eine logische Arbeitshilfe verwalten.

### Neue Funktionen

#### Sprachspezifischer Inhalt für Arbeitshilfen hochladen

Autoren können verschiedene Dateien pro unterstützte Sprache an eine einzelne Arbeitshilfe anhängen, z. B. an Kurse und andere LOs.

Die Funktion zum Erstellen/Bearbeiten von Arbeitshilfen unterstützt jetzt Folgendes:

* Auswählen einer Sprache.

* Hochladen der sprachspezifischen Datei für diese Sprache in derselben Arbeitshilfeentität.

#### Konsistente Sprachverarbeitung in der Benutzeroberfläche für Player und Teilnehmer

Der Fluidic Player wurde aktualisiert, sodass beim Öffnen einer Arbeitshilfe durch einen Teilnehmer die der Sprache des Teilnehmers entsprechende Inhaltsvariante angezeigt wird (sofern verfügbar).

Administratoren und Autoren können Arbeitshilfen als einzelne Objekte mit Sprachvarianten anzeigen, anstatt separate Elemente pro Sprache.

### Wichtigste Vorteile

#### Einzelarbeitshilfe für alle Sprachen

Autoren können die Erstellung separater Arbeitshilfen pro Sprache vermeiden.

Alle Sprachvarianten derselben Arbeitshilfe (z. B. eine Prozedur, SOP, Checklisten-PDF oder ein Referenzhandbuch) können an einem Ort verwaltet werden.

#### Bessere Erlebnisse für globale Teilnehmer

Die Teilnehmer sehen die Arbeitshilfe automatisch in ihrer bevorzugten Sprache, d. h. es gibt Folgendes:

* Weniger Verwirrung darüber, welche Version geöffnet werden soll.

* Geringeres Risiko beim Zugriff auf veraltete oder überholte Kopien.

Dies ist besonders in mehrsprachigen Organisationen nützlich, in denen dieselbe Prozess- oder Produktdokumentation in mehreren Sprachen verfügbar sein muss.

### Anwendungsszenarien

#### Globale Bereitstellung von Referenzinhalten

Ein Unternehmen muss Teilnehmern weltweit Arbeitshilfen in mehreren Sprachen zur Verfügung stellen, z. B.:

* Produktreferenzen.

* Prozesschecklisten.

* Unterstützung von Playbooks

Anstatt separate Arbeitshilfen wie &quot;Product Quick Start - EN&quot;, &quot;Product Quick Start - DE&quot;, &quot;Product Quick Start - JP&quot; usw. zu erstellen, können sie eine Arbeitshilfe erstellen, lokalisierte Dateien für jede Sprache anhängen und es zulassen, dass ALM jedem Teilnehmer die richtige Version basierend auf den Spracheinstellungen bereitstellt.

#### Kunden- oder Partner-orientierte Dokumentation für mehrere Märkte

Für Kunden- und Partnerakademien können Arbeitshilfen Folgendes umfassen:

* Produktübersicht

* Integrationsleitfäden

* Support-Arbeitsabläufe

Mit mehrsprachigen Arbeitshilfen:

* Jeder Partner sieht die lokalisierte Version, ohne zwischen sprachspezifischen Einträgen wählen zu müssen.

* Marketing- und Enablement-Teams können eine Arbeitshilfe pro Thema in allen Sprachen verwalten.

## Einschränkung für Startzeit des Moduls festlegen

### Übersicht

Mithilfe der Erweiterung können Autoren und Administratoren in Adobe Learning Manager ein Zeitfenster definieren, in dem Teilnehmer ein Modul starten dürfen. Außerhalb des konfigurierten Start-/Endfensters bleibt das Modul in der Kursstruktur sichtbar, aber die Teilnehmer können es nicht initiieren.

Diese Funktion ist von entscheidender Bedeutung für Benutzer, die eine strengere Kontrolle darüber benötigen, wann bestimmte Inhalte verfügbar werden, oder die ihre Initiierung beenden sollten, z. B. in zeitgesteuerten Programmen, kohortenbasierten Schulungen oder zeitabhängigen Übungen.

### Neue Funktionen

Autoren können jetzt auf Modulebene innerhalb eines Kurses ein Startdatum/-uhrzeit sowie ein Enddatum/-uhrzeit konfigurieren, das bestimmt, wann Teilnehmer dieses Modul starten dürfen. Innerhalb dieses Fensters verhält sich das Modul wie gewohnt. Vor der Startzeit oder nach der Endzeit sieht der Teilnehmer das Modul in der Kursübersicht, kann es aber nicht starten.

Die Konfiguration wird in der Benutzeroberfläche für die Kurserstellung als zusätzliche Planungssteuerung für bestimmte Modultypen angezeigt, z. B. zum Selbststudium vorgesehene Inhalte, Tests oder Aktivitäten. Administratoren können diese Steuerelemente verwenden, um Module zu erstellen, die in Phasen geöffnet werden, oder um späte Starts in Programmen zu verhindern, in denen Inhalte innerhalb eines definierten Zeitraums belegt werden müssen.

#### Wichtigste Vorteile

Der Hauptvorteil besteht in der Möglichkeit, zu steuern, wann auf Module zugegriffen werden kann. Schulungsteams können die Modulverfügbarkeit mit Ereignissen aus der Praxis synchronisieren, z. B. neuen Produkteinführungen, gesetzlichen Fristen und internen Programmen. Dadurch wird sichergestellt, dass Teilnehmer erforderliche Inhalte abschließen, bevor sie auf spätere Module zugreifen können.

Beispiel: Die Kohorte 1 kann nur in Woche 2 auf Modul 2 zugreifen, während Modul 3 bis Woche 3 gesperrt bleibt. Dadurch müssen Inhalte nicht mehr manuell ein- und ausgeblendet werden und es müssen keine separaten Kursversionen erstellt werden.

Dies verbessert die Lernerfahrung der Teilnehmer: Anstatt auf Module zu schauen, auf die technisch zugegriffen werden kann, die aber zu diesem Zeitpunkt nicht sein sollten (oder bereits abgeschlossen sein sollten), sehen die Teilnehmer eine Kursstruktur, in der die Module, die sie beginnen dürfen, eindeutig mit dem beabsichtigten Zeitplan ausgerichtet sind.

#### Anwendungsszenarien

* **Kohortenbasiertes Aktivierungsprogramm**: In diesem Programm wird jede Woche ein neues Modul geöffnet. Der Inhalt für Woche 1 ist sofort verfügbar, während Woche 2 sichtbar ist, kann aber erst zu einem bestimmten Datum gestartet werden. Woche 3 folgt dem gleichen Absperrverfahren. Die Teilnehmer können den gesamten Lernpfad sehen, aber das System steuert, wann sie tatsächlich jeden Schritt beginnen können.

* **Zeitgebundene Produkt- oder Kampagnentraining**: Marketing- oder Produktteams können ein Schulungsmodul erstellen, auf das nur zugegriffen werden darf, wenn eine Kampagne aktiv ist oder eine bestimmte Version eines Produkts noch verfügbar ist. Dieses festgelegte Startfenster stellt sicher, dass Teilnehmer kein Modul zu einer eingestellten Produktversion nach der angegebenen Endzeit beginnen.

* **Bewertungs- oder Prüfungsumgebungen**: Organisationen können ein Modul (z. B. einen Test) für ein kurzes, gut definiertes Fenster öffnen (z. B. &quot;Sie können die Prüfung jederzeit zwischen 9:00 und 12:00 an einem bestimmten Datum beginnen&quot;). Die Teilnehmer können die Prüfung nicht außerhalb dieses Fensters beginnen, was eine faire Planung über Zeitzonen und Kohorten hinweg unterstützt.

## Player-Sprache über benutzerdefinierten LTI-Parameter steuern

### Übersicht

Dank der Erweiterung können externe Plattformen, die LTI (Learning Tools Interoperability) verwenden, die Sprache für Adobe Learning Manager-Inhalte zum Zeitpunkt des Starts angeben. Anstatt davon abhängig zu sein, dass der Teilnehmer die Sprache im Fluidic Player ändert, kann der LTI-Benutzer einen Sprachcode über einen benutzerdefinierten LTI-Parameter senden. Adobe Learning Manager verwendet diesen Code dann, um die entsprechende Sprachvariante auszuwählen.

### Neue Funktionen

Externe Plattformen, die als LTI-Verbraucher fungieren, können jetzt beim Starten von ALM-Inhalten einen benutzerdefinierten Sprachparameter (und die zugehörigen Player-Einstellungen) übergeben. ALM liest diesen Parameter und:

* Legt die Sprache des Players entsprechend fest.

* Startet die entsprechende Sprachvariante des Moduls, wenn mehrsprachiger Inhalt konfiguriert ist.

Das bedeutet, dass ein erstmaliger Teilnehmer, der Französisch auf der externen Plattform auswählt, den ALM-Player und das Modul direkt auf Französisch starten sieht, ohne etwas in ALM anpassen zu müssen.

Die Erweiterung ermöglicht auch Szenarien, in denen die externe Plattform ALM als Headless Content Player behandelt. So können z. B. Navigationselemente und das Inhaltsverzeichnis ausgeblendet werden, indem benutzerdefinierte Parameter zum Anpassen bestimmter Einstellungen der Benutzeroberfläche gesendet werden. Diese Einstellungen arbeiten mit dem Sprachparameter zusammen, sodass die externe Plattform ein reibungsloses Markenerlebnis bieten und gleichzeitig ALM für die Wiedergabe und das Tracking verwenden kann.

### Wichtigste Vorteile

* **Einheitliche Spracherfahrung zwischen Systemen**: Wenn ein Teilnehmer eine Sprache im externen Portal auswählt, wird diese Auswahl sofort in ALM widergespiegelt. Dadurch wird sichergestellt, dass die Teilnehmer keine Diskrepanz zwischen der Sprache des Portals und dem Kurs haben. Daher müssen sie nicht nach einem Sprachschalter im Player suchen.

* **Sprachspezifische Berichterstellung**: Die Sprachauswahl auf der Plattform ist konsistent mit ALM, wodurch die Genauigkeit der Analyse und der Teilnehmerverfolgung verbessert wird. Diese Ausrichtung unterstützt auch Konfigurationen, bei denen die ALM-eigenen Sprachsteuerelemente für bestimmte Kurse absichtlich deaktiviert oder im Fluidic Player ausgeblendet werden. In diesen Fällen dient die externe Plattform als alleinige Quelle der Wahrheit für die Sprache.

### Anwendungsszenarien

* Ein wichtiger Anwendungsfall sind große Unternehmen, die LTI-basierte Integrationen nutzen. Die Teilnehmer registrieren sich zuerst und wählen eine Sprache auf der Plattform aus. Anschließend starten sie ALM-Schulungen über LTI. Wenn ein Teilnehmer Spanisch auswählt, wird mit dieser Verbesserung das ALM-Modul automatisch auf Spanisch geöffnet. Das bedeutet, dass die Teilnehmer die Spracheinstellungen in ALM nicht anpassen müssen. Darüber hinaus bleibt das sprachbasierte Reporting konsistent mit dem, was die Teilnehmer in ALM sehen und erleben.

* Eine weitere Anwendung ist die Bereitstellung von Headless-Kurserlebnissen innerhalb eines Kunden- oder Partnerportals. In diesem Setup kann das Portal ALM-Inhalte mithilfe eines iframe einbetten, während alle Navigations- und Sprachbenutzerfunktionen (UX) außerhalb von ALM verwaltet werden. Durch die Verwendung benutzerdefinierter LTI-Parameter kann das Portal sicherstellen, dass der ALM-Player in der richtigen Sprache angezeigt wird und dass alle unnötigen Elemente der Benutzeroberfläche (z. B. das Inhaltsverzeichnis und die Navigationsschaltflächen) ausgeblendet werden. Dadurch können die Teilnehmer eine einzelne, zusammenhängende Anwendung anstelle einer unzusammenhängenden Sammlung von Tools wahrnehmen.

* Dies ist von Vorteil für Unternehmen, die umfangreiche Schulungen in mehreren Sprachen mit einem anderen LMS oder einer anderen Lernplattform durchführen. Sie können die Nutzung dieser Plattform standardisieren, um Teilnehmerprofile zu verwalten, Gebietsschemas auszuwählen und Kataloge zu präsentieren. In der Zwischenzeit dient ALM als zuverlässige Content- und Tracking-Engine, die die Sprachpräferenzen und Benutzerinteraktionen berücksichtigt, die vom externen System während jedes LTI-Starts festgelegt werden.

## Checklistenfragengewichtung für Kursleiterbewertungen

### Übersicht

Die Verbesserung führt gewichtete Checklisten ein, sodass Kursleiter und Manager die Teilnehmer mithilfe von abgestuften Skalierungen und Gesamtergebnissen bewerten können, anstatt jede Checklistenfrage als gleich zu behandeln. Ziel ist es, die Erstellung von Checklisten zu erleichtern, indem gewichtete Evaluierungen von Fragen durchgeführt werden, die es ermöglichen, die relative Bedeutung verschiedener Aktionen oder Fähigkeiten innerhalb einer einzigen Checkliste widerzuspiegeln.

### Neue Funktionen

Checklisten unterstützen die folgenden Typen:

1. Ja/Nein
Das Verhalten bleibt unverändert: Jede Frage lautet Ja/Nein und die Kriterien für das Bestehen basieren auf der Anzahl der Ja-Antworten.

2. Gleichgewichtige Fragen

   * Fragen werden auf einer numerischen Skala (standardmäßig 0-10) bewertet, wobei Folgendes gilt:

      * Die max/min-Werte auf der Skala können auf Checklistenebene angepasst werden.

      * Die Skala kann jetzt bei 0 beginnen (die vorherige Mindestpunktzahl war 1).

   * Alle Fragen haben dieselbe Höchstpunktzahl, sodass sich die Checkliste für jede Frage wie eine einheitliche Bewertungsskala verhält.

3. Different-weight questions

   * Jede Frage hat ihre eigene Höchstpunktzahl (Gewicht).

   * Die Kriterien für das Bestehen hängen vom Prozentsatz der gesamten möglichen Punktzahl ab, die der Teilnehmer über die Checkliste hinweg erreicht (z. B. &quot;Bestanden&quot;, wenn der Teilnehmer ≥ 70 % der gesamten verfügbaren Punktzahl erreicht&quot;).

Für alle Checklistentypen:

* Der **Reviewer** (Kursleiter oder Manager) wertet den Teilnehmer entsprechend dem konfigurierten Checklistentyp aus:

   * Auswählen von Ja/Nein.

   * Wählen Sie Punktzahlen auf der definierten Skala aus.

* Der **Checkliste**-Bericht wird aktualisiert, um bei Fragen mit unterschiedlicher Gewichtung Folgendes einzuschließen:

   * Die maximale Punktzahl für jede Frage.

   * Die von jedem Teilnehmer für diese Frage erreichte Punktzahl.

Dies ermöglicht eine Analyse der Gesamtleistung und der fragenspezifischen Leistung auf der Grundlage der vorgesehenen Gewichte.

### Wichtigste Vorteile

* **Richtigere, realistischere Bewertungen**: Kursleiter können die Prioritäten der realen Welt widerspiegeln, indem sie mehr Punkte für kritische Verhaltensweisen und weniger bis zu geringfügigen geben, während sie gleichzeitig einen Checklisten-Workflow verwenden, der für beobachtete oder praktische Aufgaben geeignet ist.

* **Bestanden/Nicht bestanden mit der Gesamtpunktzahl**: Bewertungen können auf der Gesamtpunktzahl in Prozent basieren, nicht nur darauf, wie viele Fragen einen Schwellenwert überschreiten, sondern auch stärker an typischen Kompetenz- oder Bewertungsschemata ausgerichtet werden.

* **Bessere Berichterstellung**: Aktualisierte Checklistenberichte zeigen die maximale Punktzahl und die erreichte Punktzahl pro Frage an, sodass Programmbesitzer und Qualitätsteams bestimmte Schwachstellen identifizieren und Schulungs- oder Evaluierungsleitfäden verfeinern können.

### Anwendungsszenarien

* **Bewertungen der Fähigkeiten von Unternehmen**: Ingenieure werden anhand praktischer, szenarienbasierter Checklisten bewertet, bei denen bestimmte Diagnose- oder Kommunikationsschritte mehr Gewicht haben müssen als kosmetische oder risikoarme Schritte. Gewichtete Fragen und Kriterien für das Bestehen der Gesamtpunktzahl machen diese Bewertungen glaubwürdiger und berechenbarer für die Leistung der realen Welt.

* **Sicherheits- und Compliance-Beobachtungen**: Im Gesundheitswesen, in der Fertigung oder im Außendienst können kritische Sicherheitsschritte mit höheren Höchstwerten versehen werden, wodurch sichergestellt wird, dass das Fehlen einer sicherheitskritischen Aktion einen größeren Einfluss auf die Gesamtpunktzahl hat als das Fehlen eines geringfügigen Verfahrensschritts.

* **Coaching und Kalibrierung**: Mit der maximalen und erreichten Punktzahl pro Frage im Bericht können Manager genau sehen, wo die Teilnehmer unterdurchschnittlich abschneiden, und die Kursleiter auf die konsistente Punktzahl kalibrieren.

## Unterstützung mehrerer Sprachen für Checklistenfragen

### Übersicht

Die Verbesserung führt mehrsprachige Unterstützung für Checklistenfragen ein, sodass Prüfer Checklisten in ihrer bevorzugten Sprache bewerten und bewerten können. Diese Funktion ist besonders in mehrsprachigen Regionen und bei globalen Bereitstellungen nützlich, da sie Autoren die Möglichkeit bietet, lokalisierte Checklistenfragen für jede unterstützte Inhaltssprache zu erstellen und gleichzeitig ein einzelnes Checklistenmodul und einen konsistenten Evaluierungsprozess beizubehalten.

In Adobe Learning Manager:

* Alle Module für Teilnehmer (SCORM, PDF, HTML usw.) kann in mehreren Inhaltssprachen bereitgestellt werden, sodass die Teilnehmer die Sprache auswählen können, die sie bevorzugen.

* In einem Checklistenmodul bewerten Prüfer (Kursleiter/Manager) Teilnehmer anhand der in dieser Checkliste definierten Fragen.

### Neue Funktionen

**Authoring**

* Autoren können jetzt Checklistenfragen in allen auf Kursebene ausgewählten Sprachen hinzufügen.

* Für jede Checkliste:

   * Es wird erwartet, dass der Autor in jeder Inhaltssprache, in der der Kurs vorhanden ist, den gleichen Fragentext bereitstellt.

   * Der Verfasser ist dafür verantwortlich, dass die Bedeutung jeder Frage in allen Sprachen konsistent ist.

**Überprüfungserlebnis**

* Reviewer sehen Checklistenfragen und die Benutzeroberfläche für die Bewertung in ihrer ausgewählten Inhaltssprache.

* Wenn eine Frage in einer Sprache ausgewertet wird:

   * Die Bewertung (Punktzahl, Ja/Nein, Status) ist in allen Sprachen logisch identisch. Es handelt sich um eine einzelne Checkliste mit mehreren Sprachansichten, nicht um separate Checklisten pro Sprache.

**Berichte**

Der Checklistenbericht zeigt den Fragentext in der Inhaltssprache des Benutzers an:

* Ein Administrator oder Reviewer, der den Bericht in jeder Sprache ausführt, sieht die lokalisierten Fragenamen für diese Sprache.

* Die zugrunde liegenden Antworten und Punktzahlen bleiben unverändert; nur Fragenbezeichnungen werden übersetzt.

### Wichtigste Vorteile

* **Bessere Prüfererfahrung**: Prüfer können vollständig in ihrer eigenen Sprache arbeiten, Fragen lesen und Bewertungen ohne Sprachbarrieren aufzeichnen.

* **Angleichung von Vorschriften und Richtlinien**: In Regionen mit Anforderungen an die Sprachgleichheit (z. B. Niederländisch/Französisch in Belgien) können Checklisten jetzt die gleichen Standards erfüllen wie andere Lernmaterialien, wodurch das Compliance-Risiko verringert wird.

* **Konsistente Auswertungslogik**: Während der Text lokalisiert ist, werden Auswertung und Bewertung in allen Sprachen gemeinsam genutzt, um sicherzustellen, dass die Ergebnisse vergleichbar und zentral verwaltet sind.

### Anwendungsszenarien

* Franchise-Unternehmen mit mehreren Ländern, die in mehreren Sprachen operieren, können einen Kurs und eine Checkliste bereitstellen und gleichzeitig lokalisierte Prüferlebnisse in jedem Gebiet bereitstellen.

* Jedes globale Unternehmen mit lokalen Kursleitern (z. B. EMEA, LATAM, APAC) kann Überprüfer in ihrer lokalen Sprache arbeiten lassen, während sie das gleiche Design und die gleiche Berichterstattung für globale Checklisten verwenden.

## Checkliste mit Kommentarfunktion für Reviewer

### Übersicht

Die Verbesserung führt eine Kommentarfunktion für Checklistenbewertungen ein, mit der Prüfer wie Kursleiter und Manager neben den numerischen Punktzahlen qualitatives Feedback abgeben können. Dieses Feedback kann den Teilnehmern bei Bedarf angezeigt werden.

Ziel ist es, auf Checklisten basierende Evaluierungen zu unterstützen, bei denen das Mentor-Feedback ebenso entscheidend ist wie das numerische Ergebnis. Dazu gehört das Hervorheben spezifischer Stärken, verbesserungswürdiger Bereiche oder das Bereitstellen von Kontext für die jeweilige Punktzahl.

Heute haben Überprüfer folgende Möglichkeiten:

* Checkliste für jeden Teilnehmer auswerten, Frage für Frage.

* Zeigen Sie Ergebnisse an und bewerten Sie Teilnehmer, die einen Fehler gemacht haben, erneut.

In realen Szenarien, wie der Luftfahrt, bewerten Außendienstmitarbeiter Werkstattagenten und Flughafenmitarbeiter. Ebenso verwenden Ausbilder und Mentoren in kleinen und mittleren Unternehmen (KMU) häufig Checklisten, um die Arbeitsleistung zu bewerten. Diese Checklisten enthalten jedoch in der Regel keinen strukturierten Abschnitt zum Erfassen von erzählerischem Feedback, das sich auf die Bewertung bezieht.

### Neue Funktionen

#### Authoring-Optionen

Autoren können jede Checkliste für Folgendes konfigurieren:

* Aktivieren oder deaktivieren Sie die Kommentarfunktion für Reviewer.

* Legen Sie fest, ob den Teilnehmern der Name des Überprüfers zusammen mit den Kommentaren angezeigt werden soll.

Auf diese Weise können Organisationen die Sichtbarkeit von Kommentaren an ihre Kultur- und Datenschutzanforderungen anpassen.

#### Ablauf beim Überprüfer

Wenn das Kommentieren aktiviert ist:

* Reviewer (Kursleiter/Manager) können während der Auswertung einer Checkliste optionale Kommentare hinzufügen.

* Sie können basierend auf den Einstellungen der Checkliste auswählen, ob Kommentare für Teilnehmer sichtbar sind.

Wenn sie einen Teilnehmer neu bewerten, können sie die Kommentare aktualisieren oder ändern, um die neueste Bewertung abzustimmen.

#### Berichterstattung und Benachrichtigungen

* Der Checklistenbericht erhält eine neue Spalte für die Anmerkungen des Überprüfers, in der der während der Bewertung abgegebene Kommentar erfasst wird.

* Teilnehmer erhalten Benachrichtigungen (in Plattform und E-Mail), wenn eine Checklistenbewertung erfolgt. Diese Benachrichtigungen umfassen Folgendes:

   * Der Kommentar und

   * Name des Reviewers, falls diese so konfiguriert wurden, dass sie sichtbar sind.

Dadurch wird sichergestellt, dass Feedback nicht nur gespeichert, sondern auch den Teilnehmern aktiv angezeigt wird.

### Wichtigste Vorteile

* **Richtigeres, coachähnliches Feedback**: Numerische Punktzahlen werden durch kontextbezogene Anmerkungen ergänzt, sodass Checklisten ein effektiveres Werkzeug für Coaching sind, nicht nur für die Einhaltung von Vorschriften.

* **Rückverfolgbarkeit und Überprüfbarkeit**: Unternehmen erhalten eine dauerhafte Aufzeichnung darüber, wer wen, wann und was sie gesagt haben, was in regulierten Umgebungen und bei Rollen mit hohem Einsatz wichtig ist.

* **Bessere Interaktion der Teilnehmer**: Die Teilnehmer erhalten klare Anleitungen in Verbindung mit bestimmten Bewertungen, wodurch sie ihre Erwartungen und nachfolgenden Schritte besser verstehen.

### Anwendungsszenarien

* Organisationen mit regulierten Umgebungen können Kommentare verwenden, um klinische Urteile oder Verfahrensfeedback für Mitarbeiter zu dokumentieren, die vor Ort beobachtet werden.

* Luftfahrt- und Bodenabfertigungsorganisationen können detaillierte Notizen zur Betriebsleistung, zu Sicherheitspraktiken und zum Kundenverhalten anhängen und so eine Checkliste in ein strukturiertes Tool für die Beratung verwandeln.

* In Mentoring und KMU-Bewertung können Kursleiter nuancierte Beobachtungen erfassen, die nicht nur in eine Punktzahl passen, z. B. &quot;Eskalation gut gehandhabt, aber Zeit-Management verbessern müssen&quot; oder &quot;hervorragender Fluss der Fehlerbehebung; einen Dokumentationsschritt verpasst.&quot;

## Mehrere Versuche auf Inhaltsebene und Quizberichte

### Übersicht

>[!IMPORTANT]
>
>Beachten Sie, dass die Funktion erst verfügbar ist, nachdem sie im Konto aktiviert wurde. Wenden Sie sich an den ALM-Support.


Derzeit unterstützt ALM mehrere Versuche auf LMS-Ebene über die Funktion &quot;Mehrere Quizversuche (MQA)&quot;:

* Autoren können Versuche auf Kursebene (angewendet auf alle Quiz tragenden Module im Kurs) oder auf Modulebene (pro Quizmodul) konfigurieren.

* Folgende Versuche sind möglich:

   * Eine bestimmte Zahl (z. B. 3 Versuche) oder

   * Unendliche Versuche, gesteuert auf LMS-Ebene.

* Wenn ein Teilnehmer ein Modul über den Fluidic Player absolviert und dann den Player schließt oder das Modul abschließt, wird diese Sitzung als einzelner LMS-Versuch behandelt.

* Jeder LMS-Versuch wird im L2-Quizbericht als neue Zeile erfasst.

Wenn die Inhaltsdatei selbst (z. B. ein Articulate SCORM-Quiz) jedoch eine eigene Logik für mehrere Versuche implementiert, unterscheidet oder verfolgt der L2-Quizbericht von ALM diese internen Versuche derzeit nicht ordnungsgemäß.

Diese Verbesserung führt eine Verfolgung mehrerer Versuche auf Inhaltsebene für Tests ein, sodass Adobe Learning Manager jeden Versuch innerhalb des Inhalts selbst im L2-Quizbericht genau erfassen kann. Es wurde für Situationen entwickelt, in denen das Content-Authoring-Tool (z. B. Articulate SCORM) Quizversuche unabhängig verwaltet. Mit dieser Funktion werden Versuche in der ALM-Berichterstellung korrekt widergespiegelt, ohne von den MQA-Einstellungen (Multiple Quiz Attempt) auf LMS-Ebene abhängig zu sein.

### Neue Funktionen

#### Autorenflag für Versuche auf Inhaltsebene

* Beim Hochladen von Inhalten in die Inhaltsbibliothek können Autoren jetzt angeben, dass in eine bestimmte Inhaltsdatei mehrere Versuche eingebettet sind.

* Dies ist eine Pro-Content-Einstellung, die ALM anweist, Versuche, die innerhalb des Inhalts definiert wurden, als Quelle der Wahrheit zu behandeln.

#### Kurs-/Modulverhalten

Wenn solche Inhalte in einem Kurs verwendet werden:

* Das Modul leitet seine Versuche vom Inhalt ab, nicht von LMS MQA.

* Teilnehmer sehen nur einen Versuch auf LMS-Ebene:

   * In der Kursübersicht und Modulansicht wird keine LMS-Schaltfläche &quot;Erneut versuchen&quot; für dieses Modul angezeigt.

   * Die Handhabung von Versuchen (z. B. Wiederholungsversuche innerhalb des Quiz) wird durch den Inhalt selbst gesteuert.

#### Berichte

Der L2-Quizbericht behandelt jeden Versuch auf Inhaltsebene als separate Versuchszeile:

* Jeder im Inhalt konfigurierte interne Quizversuch wird im L2-Quizbericht als eigene Zeile angezeigt, z. B. wie Versuche auf LMS-Ebene heute dargestellt werden.

* Das Format jeder Zeile bleibt mit den vorhandenen Mehrfachzeilen in L2-Berichten identisch (gleiche Spalten, Struktur und Semantik).

* So erhalten Sie ein konsistentes Reporting-Erlebnis:

   * Unabhängig davon, ob Versuche von LMS MQA oder vom Inhalt gesteuert werden, zeigt der L2-Quizbericht eine Zeile pro Versuch an.

#### Wichtigste Vorteile

* Präziser Versuchsverlauf für SCORM-Quiz, bei denen Versuche intern von Tools wie Articulate gesteuert werden, ohne dass die MQA-Konfiguration auf LMS-Ebene obenauf erzwungen wird.

* Übersichtlicheres Erlebnis für Teilnehmer: Bei inhaltsgesteuerten Versuchen sehen die Teilnehmer einen einzelnen Steckplatz auf LMS-Ebene und müssen nicht mit den LMS-Steuerelementen für erneute Versuche interagieren. Alle erneuten Versuche werden innerhalb der Quiz-Benutzeroberfläche durchgeführt, die sie bereits kennen.

* Flexible Architektur: Benutzer können auswählen, ob ALM MQA oder Versuche auf Content-Ebene das Verhalten pro Modul steuern sollen, je nachdem, wie ihr Content erstellt wurde und wie sie es vorziehen, Versuche zu verwalten.

* Konsistentes Berichtsmodell: Nachgeschaltete Benutzer des L2-Quizberichts können jede Zeile als &quot;einen Versuch&quot; behandeln, unabhängig davon, wo die Versuchslogik ihren Ursprung hat.

#### Anwendungsszenarien

* Unternehmen, die Articulate SCORM verwenden, können eine eigenständige Quizlogik innerhalb des SCORM-Pakets beibehalten und gleichzeitig ein präzises Reporting auf Versuchsebene in ALM ohne zusätzliche LMS-Konfiguration erreichen.

* Unternehmen, die von Anbietern bereitgestellte SCORM-Inhalte verwenden, müssen keine zusätzlichen Versuche und Wiederholungen mehr mit MQA auf LMS-Ebene durchführen oder diese ändern.

## QR-Codes von Kursleitern für die Instanzenregistrierung und die Sitzungsteilnahme

### Übersicht

Diese Verbesserung bietet Kursleitern die Möglichkeit, selbst QR-Codes für folgende Zwecke zu generieren:

* Registrierung für Kursinstanzen,

* Sitzungsteilnahme oder

* Anmeldung + gemeinsame Teilnahme

auf Sitzungsebene. Es wurde für Situationen entwickelt, in denen Teilnehmer einen physischen oder hybriden Klassenzimmer betreten und eine schnelle Self-Service-Option benötigen, um sich mit einem QR-Code zu registrieren und ihre Teilnahme aufzuzeichnen.

### Neue Funktionen

#### Von einem Kursleiter generierte QR-Codes

* Kursleiter können QR-Codes auf Sitzungsebene für Folgendes generieren:

   * In Instanz registrieren: Teilnehmer können sich für die Instanz registrieren, die die aktuelle Sitzung enthält.

   * Sitzungsteilnahme vermerken: Die Teilnehmer scannen während/nach der Sitzung, um die Teilnahme an dieser bestimmten Sitzung aufzuzeichnen.

   * Instanz registrieren + Sitzungsteilnahme markieren : Ein kombinierter QR für Teilnehmer, die noch nicht registriert sind und ihre Teilnahme in einem Schritt markieren müssen.

* Kursleiter können die benötigten QR-Codes basierend auf dem Szenario (Registrierung, Teilnahme oder beides) exportieren.

#### Verpacken von QR-Codes

Die exportierte QR-Code-PDF umfasst:

* Kursname

* Instanzname

* Sitzungsname

Diese erleichtern es Kursleitern und Koordinatoren, den richtigen QR-Code für jede Sitzung zu identifizieren und zu drucken.

### Wichtigste Vorteile

* **Eigenständigkeit des Kursleiters**: Kursleiter müssen nicht mehr warten, bis Administratoren QR-Codes erstellen. Sie können sie direkt für jede Sitzung generieren und so die Agilität verbessern und den Koordinations-Overhead reduzieren.

* **Bessere Klassenzimmerlogistik**: Für begehbare oder Vor-Ort-Zielgruppen (z. B. Außendienstmitarbeiter, Verkaufsraummitarbeiter oder externe Teilnehmer) können Kursleiter die Anmeldung und die Anwesenheit vor Ort mithilfe von QR-Codes verwalten.

* **Geringere Administrator-Arbeitslast**: Admin-Teams können sich auf die Konfiguration und Governance konzentrieren, anstatt routinemäßige QR-Code-Generierungsanforderungen für jede Sitzung zu behandeln.

### Anwendungsszenarien

* Unternehmen, die große Mengen an Vor-Ort-Sitzungen durchführen (z. B. Produktschulungen für Fachleute), können es den Kursleitern ermöglichen, sitzungsspezifische QR-Codes zu drucken, die die Teilnahme mit einem Scan registrieren und markieren.

* Bei Schulungen für Einzelhandel, Fertigung und Gesundheitswesen, bei denen Teilnehmer oft direkt vom Boden aus oder ohne vorherige Anmeldung an Sitzungen teilnehmen, kann ein QR-Code &quot;Anmeldung + Teilnahme&quot; an der Tür platziert werden. Dies ermöglicht es Teilnehmern, ihre Anmeldung und Anwesenheit über ihre Telefone selbst zu bearbeiten.

* Schulungen für Partner oder Kunden ermöglichen es dem Trainer vor Ort, sich einfach an Änderungen im Raum, zusätzliche Sitzungen oder zusätzliche Teilnehmer anzupassen, ohne den Administrator um neue QR-Codes bitten zu müssen.

## Verbesserungen am Captivate- und ALM-Player

### Übersicht

Diese Erweiterung verbessert die Wiedergabe von Adobe Captivate-Inhalten im Adobe Learning Manager-Player (ALM), insbesondere nach den jüngsten Änderungen an der Captivate-Architektur. Ziel ist es, Teilnehmern die native Interaktion mit Captivate-Modulen in ALM zu ermöglichen und gleichzeitig sicherzustellen, dass Navigation, Abschlussverfolgung und Notizen klar, konsistent und zuverlässig sind.

### Neue Funktionen

#### Einheitliches Inhaltsverzeichniserlebnis

* Nur das ALM-Inhaltsverzeichnis wird auf der linken Seite des Players angezeigt.

* Das Inhaltsverzeichnis des Captivate wird ausgeblendet, wenn das Modul in ALM abgespielt wird.

* Dadurch werden doppelte Darstellungen entfernt, eine einzige Quelle für die Navigation sichergestellt und Platz auf dem Bildschirm frei.

#### Feedback zum visuellen Abschluss

* Das ALM-Inhaltsverzeichnis zeigt grüne Häkchen (oder entsprechende visuelle Hinweise) an, die auf den Abschluss der Folie hinweisen.

* Wenn die Teilnehmer durch die Captivate-Folien blättern, gibt das ALM-Inhaltsverzeichnis an, welche Folien abgeschlossen wurden, und stimmt mit den Erwartungen der Teilnehmer an moderne Kursspieler überein.

#### Kontextbezogene Fortschrittssteuerungen

* Die Steuerelemente des Players werden je nach Folientyp angepasst:

   * Für Videofolien:

      * Zeigt eine Zeitverlaufsleiste an, die die Videowiedergabe widerspiegelt.

* Für Nicht-Video-Folien:

   * Steuerelemente für die Foliennavigation anzeigen (nächste/vorherige Folie usw.) anstelle einer nicht funktionierenden Zeitleiste.

      * Dadurch wird vermieden, dass bei bestimmten Folientypen irrelevante oder nicht funktionierende Steuerelemente angezeigt werden.

#### Optimierte Navigation

* Die separate Modulnavigationsleiste (ALM) und die Kursnavigationsleiste werden zu einer einzigen, intuitiven Leiste zusammengeführt.

* Diese einheitliche Navigation:

   * Es unterscheidet deutlich zwischen dem Wechsel durch das Captivate-Modul und dem Wechsel zurück zur Kurs-/Modulebene.

   * Reduziert Verwechslungen, die durch mehrere Balken mit sich überschneidenden Zwecken entstehen.

#### Verlässliche Notizverknüpfungen

* Notizen sind mit Foliennummern und nicht mit Zeitstempeln verknüpft.

* Diese Änderung:

   * Behebt Exportfehler, die durch fehlende oder falsche Zeitstempel verursacht wurden.

   * Stellt sicher, dass Notizen konsistent als PDF exportiert werden können, mit einer zuverlässigen Zuordnung zwischen Notizen und dem Folienkontext, zu dem sie gehören.

### Wichtigste Vorteile

* Übersichtlicheres Einzelspielererlebnis: Die Teilnehmer interagieren mit einem Inhaltsverzeichnis und einem Navigationsmodell und reduzieren so Verwirrung und kognitive Belastung.

* Genaue Angaben zum Abschluss und Fortschritt: Ticks auf Folienebene und Kontextsteuerelemente helfen Teilnehmern zu verstehen, wo sie sich befinden und was noch übrig ist.

* Zuverlässigere Notizen und Exporte: Durch die Verknüpfung von Notizen mit Folien anstelle fragiler Zeitstempel erhalten Benutzer einen zuverlässigen Workflow für Notizen zum PDF, selbst bei folienbasierten Captivate-Inhalten.

* Beibehaltener Autorenworkflow: Autoren behalten die Einfachheit der direkten Veröffentlichung auf ALM durch Captivate bei, während Teilnehmer ein modernes, integriertes Wiedergabeerlebnis ohne zusätzlichen Authoring-Aufwand erhalten.

### Anwendungsszenarien

* Aktivierungsprogramme, die für interaktive Simulationen auf Captivate setzen, können Inhalte in ALM bereitstellen, um sicherzustellen, dass Navigation, Abschlussverfolgung und Anmerkungen für die Teilnehmer konsistent funktionieren.

* Unternehmen, die Captivate als ihr wichtigstes Werkzeug zum Erstellen von Inhalten verwenden, können die Veröffentlichung mit einem Klick verwalten und Verwechslungen mit doppelten Inhaltsverzeichnissen und nicht funktionalen Steuerelementen für Teilnehmer vermeiden.

* Organisationen, die Notizen verwenden, die aus Captivate-Inhalten in ALM exportiert wurden (für Coaching, Compliance oder Datensätze), können auf Folgendes zugreifen:

   * Notizen werden korrekt mit Folien verknüpft.

   * PDF werden wie erwartet generiert.

## Verbesserte Berechnung des Zeitaufwands für das Lernen in Teilnehmertranskripten

### Übersicht

Adobe Learning Manager hat mit der Version vom April 2026 überarbeitet, wie die Lernzeit in Teilnehmertranskripten berechnet wird. Früher konnte die Berichtslogik zu ungenauen Zeiten führen, wenn Teilnehmer den Player offen ließen, ohne mit dem Inhalt zu interagieren, was zu Diskrepanzen führte. Die neue Methode verfolgt jetzt die aktive Zeit basierend auf Benutzerinteraktionen, insbesondere wenn die Registerkarte aktiv ist und Benutzeraktivitäten vorhanden sind. Diese Änderung führt zu genaueren Daten.

Dieses Update verbessert Berichte und Dashboards, sodass Administratoren die Compliance besser gewährleisten und den Fortschritt der Teilnehmer verfolgen können. Überprüfen Sie nach der Veröffentlichung Ihre Teilnehmertranskripte, um diese Verbesserungen anzuzeigen.

Die aktualisierte Berechnungsmethode konzentriert sich auf die tatsächliche Interaktion, z. B. den aktiven Tabulatorfokus und die jüngsten Benutzerinteraktionen, wodurch die Genauigkeit der Zeitberichte in den folgenden Bereichen verbessert wird:

* Teilnehmertranskripte (UI)
* Metriken zum Admin Dashboard
* Kursregistrierungsberichte
* APIs und Connectors

### Änderungen

Die Spalte **Zeitaufwand zum Lernen** in den Teilnehmertranskripten verwendet jetzt eine verbesserte Logik, um die Zeit genauer zu berechnen. Anstatt einfach die Öffnungs-/Schließzeiten des Players zu verfolgen, unterscheidet das System jetzt basierend auf der Interaktion des Benutzers zwischen aktiven und Leerlaufzeiten.

* **Aktive Zeit**: Zeitpunkt, zu dem der Teilnehmer aktiv aktiv beteiligt ist (z. B. auf der richtigen Registerkarte, Ausführen von Aktionen wie Bildlauf oder Anzeigen von Videos).
* **Leerlaufzeit**: Zeit, zu der der Teilnehmer nicht aktiviert ist (z. B. Tabulatorwechsel, keine Aktivität für mehr als 10 Minuten), was von der Gesamtzahl ausgeschlossen ist.

Dies gilt für die meisten Modultypen, mit Ausnahme der SCORM-, Captivate- und XAPI-Module, bei denen die Originallogik beibehalten wird.

### Funktionsweise

Die neue Berechnung variiert je nach Modultyp:

* **Video- und Audiomodule**: Aktiv, wenn der Inhalt abgespielt wird, selbst wenn der Teilnehmer zu einer anderen Registerkarte wechselt. Der Tabulatorfokus ist für die Verfolgung der Wiedergabezeit nicht erforderlich.
* **Statische Module (PDF, PPT, Excel usw.)**: Aktiv, wenn auf der Registerkarte und Ausführen von Aktivitäten (Mausbewegung, Scrollen, Klicken, Tastatureingabe) innerhalb der letzten 10 Minuten. Wenn 10 Minuten lang keine Aktivität erfolgt, wechselt sie in den Leerlauf.
* **SCORM und Captivate** behalten die ursprüngliche Öffnungs-/Schließlogik bei.
* **xAPI** verwendet jetzt die tabulatorbasierte aktive Zeiterkennung, wobei die Zeit nur gezählt wird, wenn die Registerkarte aktiv ist. Beachten Sie, dass AICC-Inhalt **nicht** unterstützt wird.
* **HTML, LTI und andere Inhalte**: Kann abweichen; überprüfen Sie die Teilnehmertranskripte auf Richtigkeit.

Die Leerlaufzeit wird abgezogen, um sicherzustellen, dass nur die tatsächliche Interaktionszeit gemeldet wird.

>[!NOTE]
>
>Wenn Ihr Laptop in den Ruhemodus wechselt, wird die Lernzeit möglicherweise nicht korrekt verfolgt. Dies liegt daran, dass die Aktivitätsverfolgung angehalten wird, während das System in den Ruhemodus wechselt, und erst dann fortgesetzt wird, wenn das Notebook wieder aktiviert wird.


### Zusammenfassungstabelle

| **Modultyp** | **Aktive Zeit (gezählt)** | **Leerlaufzeit (ausgeschlossen)** |
| --- | --- | --- |
| **Video/Audio** | Wiedergabezeit | Nicht gestartet; beendet; **\>10 Min. angehalten** |
| **Statisch (PDF/PPT/DOC)** | Registerkarte aktiv **und** Aktivität in den letzten **10 Min.** | Keine Aktivität **\>10 Min.**; Registerkarte inaktiv |
| **SCORM** | Von der Content-Laufzeit gemeldete Zeit | Leerlauf kann nicht erkannt werden |
| **Captivate** | Slide-basiertes Timing | Leerlauf kann nicht erkannt werden |
| **xAPI** | Tabulator aktiv | Tabulator inaktiv |
| **HTML** | Player-Öffnungszeit mit aktiver Registerkarte | Tabulator inaktiv |
| **LTI-Hersteller/Verbraucher** | Wenn LTI-Inhalte im ALM-Player abgespielt werden (d. h., ALM verwendet LTI-Inhalte, die auf einem anderen LMS gehostet werden, das als Produzent fungiert), gilt diese zeitaufwendige Logik.<br><br>Wenn der Inhalt jedoch außerhalb des LMS abgespielt wird (d. h., der Inhalt wird in ALM gehostet, dann ist ALM der Produzent, aber die Wiedergabe erfolgt in einem externen Player), gilt dieser Teil der Zeitberechnungslogik nicht.  <br>**Hinweis**: LTI-Verbraucher wird in Adobe Learning Manager nicht unterstützt. | Tabulator inaktiv |

**Hinweis**:

* **Erneute Besuche und parallele Sitzungen**: Zählen Sie als aktiv, wenn die oben genannten Bedingungen erfüllt sind.
* **Alle Geräte, Browser, Sprachen**: Inbegriffen; mobile Offlinenutzung wird nach der Synchronisierung hinzugefügt.

### Vorteile der neuen Berechnung

* **Genaue Berichterstellung**: Eliminiert überhöhte Zeiten durch unbeaufsichtigte Spieler und bietet realistische Lerndauern.
* **Bessere Compliance**: Unterstützt eine genaue Nachverfolgung für obligatorische Schulungen (z. B. die monatliche Anforderung eines Unternehmens von 5 Stunden).
* **Verbesserte Dashboards**: Diagramme für Benutzeraktivitäten und Berichte zu Zeitaufwand geben jetzt die tatsächliche Interaktion wieder.
* **Einblicke zu Teilnehmern**: Hilft Administratoren dabei, echte Fortschritte zu identifizieren und unengagierte Teilnehmer anzusprechen.

### Auswirkungen von Reporting und Analysen

* **Teilnehmertranskripte:** &quot;Aufgewandte Lernzeit&quot; spiegelt jetzt **die tatsächliche Interaktion wider**.
* **Admin-Dashboard:** Metriken, die die Zeit enthalten (z. B. Kacheln für &quot;aufgewendete Zeit&quot;, Trends), zeigen **niedrigere, aber realistischere** Werte in Szenarien, in denen die Leerlaufzeit zuvor zu überhöhten Ergebnissen geführt hat.
* **Kursregistrierungsberichte:** Zeitbezogene Felder übernehmen die **neue Berechnung** nach dem Start.
* **Vergleichbarkeitshinweis:** Da historische Daten nicht neu berechnet werden, kann bei Zeitreihenanalysen, die sich über das Veröffentlichungsdatum erstrecken, eine **Schrittänderung** angezeigt werden. Berücksichtigen Sie in den Analyse-Tools Anmerkungen oder Segmentierung nach Datum.

### API und Connectors

* **Es wurden keine Schemaänderungen** an vorhandenen Endpunkten/Feldern vorgenommen, die Zeitaufwand melden.
* **Feldsemantik** wird aktualisiert, um _Berechnung der aktiven Zeit_ für Sitzungen **nach dem** Funktionsstart widerzuspiegeln.
* **Connectors und Exporte**, die zeitaufwendige Felder verbrauchen, erhalten die aktualisierten Werte automatisch in der Zukunft.

### Abwärtskompatibilität und Datenmigration

* **Verlaufssitzungen:** Nicht neu berechnet.
* **Neue Sitzungen:** Verwenden Sie die **Neue**-Berechnung zur aktiven Zeit.
* **Gemischte Zeiträume:** Segmentieren Sie bei Audits oder Längsschnittberichten nach **vor/nach dem Start**, um Fehlinterpretationen zu vermeiden.

### Bekannte Einschränkungen

* **Interaktiver Inhalt** (SCORM/Captivate) ist weiterhin auf Timing angewiesen, das vom Inhalt bereitgestellt wird. Eine Leerlauferkennung im Inhalt ist nicht verfügbar.
* **Iframe-basierter Inhalt** (HTML/xAPI) schränkt die Erkennung feinkörniger Interaktionen ein. Stattdessen wird der Registerkartenfokus verwendet.

### Häufige Fragen

**Ändert dieses Update historische Datensätze?**

Anzahl Die Änderung gilt nur für Sitzungen nach dem Start der Funktion.

**Wie überprüfe ich die Änderungen?**

Überprüfen Sie die Teilnehmertranskripte für die letzten Module, und vergleichen Sie die Zeiten mit den erwarteten Dauern.

**Betrifft dies alle Konten?**

Ja, es handelt sich um ein globales Update für alle Adobe Learning Manager-Konten.

**Müssen Teilnehmer aktiv werden?**

Anzahl Die Änderung erfolgt automatisch und ist für die Teilnehmer transparent.

**Was passiert, wenn Teilnehmer Inhalte offen lassen?**

Die Leerlaufzeit ist nun ausgeschlossen, sodass Übermeldungen vermieden werden.

**Werden Video-/Audiositzungen automatisch angehalten, wenn die Registerkarte inaktiv ist?**

Anzahl Das Wiedergabeverhalten bleibt unverändert. Die Zeit ist ausgeschlossen, wenn sie länger als 10 Minuten angehalten wurde oder wenn sie nicht aktiv gespielt wird.

**Wird die Offline-Aktivität für mobile Endgeräte widergespiegelt?**

Ja. Die Offline-Nutzung ist bei der Synchronisierung des Geräts enthalten.

**Was soll ich tun, wenn meine Dashboards jetzt niedrigere Durchschnittswerte anzeigen?**

Dies wird erwartet, wenn die Leerlaufzeit zuvor die Ergebnisse überhöht hatte. Versieh Anmerkungen in Dashboards, und passe die Ziele nach Bedarf an.

**Sind Voraussetzungen vorhanden?**

Keine, die Änderung erfolgt automatisch.

## Aktualisierung der Teilnehmertranskriptberichte für Administratoren

Wir aktualisieren die Lernaktranskriptberichte (LT) für Administratoren, um Checklistenbasierte Bewertungen und Feedback von Prüfern besser zu unterstützen.

## Was ändert sich?

### &#x200B;1. Spaltenumbenennung im Admin-Teilnehmertranskript

Die vorhandene Spalte **Übermittlungskommentar** im Admin Learning
Das Transkript lautet:

1. **Umbenannt in:** `Reviewer's remarks`

### In dieser Spalte angezeigte Daten:

* **Für Übermittlungsmodule:**
In der Spalte wird weiterhin der Übermittlungskommentar angezeigt (keine Verhaltensänderung).

* **Für Checklistenmodule:**
In der Spalte wird nun der Bewertungskommentar (die Anmerkungen des Prüfers der Checkliste) angezeigt.

Diese Änderung gilt für alle Admin LT-Quellen:

* LT, von der Admin-Benutzeroberfläche heruntergeladen
* Einb. Einb. über die Job-API
* Einb. generiert über Connectors

Nach dieser Änderung enthält dieselbe Spalte: - Einreichungskommentare für Einreichungsmodule

* Bewertungskommentare für Checklistenmodule

Unter dem neuen Headernamen **Anmerkungen des Reviewers**.

### &#x200B;2. Neue Spalte in Connector-basierten Lernaktranskript-Exporten

Für vom Connector exportierte Lerntranskripte:

* Am Ende des Berichts wird eine neue Spalte mit dem Namen **Anmerkungen des Reviewers** hinzugefügt.
* Diese Spalte enthält die Kommentare des Überprüfers, die an dem oben beschriebenen Verhalten ausgerichtet sind:
   * Übermittlungskommentare für Übermittlungsmodule
   * Bewertungskommentare für Checklistenmodule

## Auswirkungen auf vorhandene Integrationen und Automatisierungen

Wenn Sie Teilnehmertranskriptberichte in benutzerdefinierten Integrationen, Automatisierungen oder externen Reporting-Tools verwenden, überprüfen Sie die folgenden Szenarien:

| Szenario | Auswirkungen | Wichtig |
|----------|--------|----------------|
| Sie identifizieren Felder in Admin LT anhand des Spaltennamens (z. B. &quot;Einreichungskommentar&quot;) | Die Spaltenüberschrift ändert sich zu den Anmerkungen des Überprüfers. | Ja. Aktualisieren Sie alle Zuordnungen oder Logik, die auf den Einreichungskommentar verweisen, um die Anmerkungen des Überprüfers zu verwenden. |
| Sie identifizieren Felder in Admin LT nur durch die Spaltenposition (indexbasiert). | Die Position dieser Spalte bleibt in Admin LT gleich. | In der Regel keine Aktion. Wenn Ihre Logik nicht vom Kopfzeilentext abhängt, ist keine Änderung für Admin LT erforderlich. Ändern Sie einfach den Spaltennamen, wenn derzeit die Spalte &quot;Übermittlungskommentare&quot; verwendet wird. |
| Sie verwenden ein vom Connector exportiertes LT und verlassen sich auf eine feste Spaltenanzahl oder eine bestimmte Position in der letzten Spalte | Eine neue Spalte wird am Ende des Berichts angehängt. | Ja. Passen Sie die Analyse- oder Validierungslogik an, um eine zusätzliche Spalte am Ende der Datei zu berücksichtigen. |
| Sie verwenden vom Connector exportiertes LT und Map nach Spaltennamen | Eine neue Spalte mit Anmerkungen des Reviewers ist verfügbar. | Optional. Eine Änderung ist nur erforderlich, wenn Sie die neuen Kommentardaten des Reviewers/der Checkliste nutzen möchten. |

**Was Sie tun sollten**

* Überprüfen Sie alle Skripte, ETL-Jobs, Dashboards oder Integrationen, die Admin Learning Transkript-Berichte nutzen.
* Wenn Sie auf den alten Spaltennamen _Übermittlungskommentar_ verweisen, aktualisieren Sie Ihre Konfiguration oder Ihren Code, um die Anmerkungen des Überprüfers für den neuen Spaltennamen zu verwenden.
* Wenn Sie konnektorbasierte LT-Exporte verwenden und eine feste Anzahl von Spalten oder eine feste letzte Spalte annehmen, aktualisieren Sie Ihre Logik, um eine zusätzliche Spalte am Ende des Exports zu behandeln.

Wenn Ihre aktuelle Implementierung ausschließlich auf Spaltenpositionen in Admin LT basiert und nicht validiert wird oder vom Spaltenkopftext abhängt, ist keine Änderung für Admin LT selbst erforderlich. Nur bei Connector-Exporten ist Aufmerksamkeit erforderlich, wenn Sie von einem festen Layout abhängig sind.


## Nicht angemeldetes Erlebnis in Experience Builder

Das nicht angemeldete Erlebnis in Experience Builder ermöglicht es Unternehmen, ihre Lerninhalte und Portalseiten für alle Besucher anzuzeigen, einschließlich derjenigen, die sich nicht angemeldet haben. Diese Funktion soll potenzielle Teilnehmer anziehen, informieren und ansprechen, indem sie eine reibungslose und markenkonforme Vorschau Ihrer Schulungsangebote bietet, bevor sie sich anmelden oder registrieren müssen.

Mit dieser Funktion können Sie öffentlich zugängliche Seiten erstellen und anpassen, indem Sie dieselbe benutzerfreundliche Drag-and-Drop-Oberfläche verwenden, die im Standard-Experience Builder enthalten ist. Sie können für jeden, der Ihr Portal besucht, Kurskataloge, Kategorien, Pfade und Rich-Static-Content (Bilder, Text, HTML und eingebettete IFrames) präsentieren. Dadurch ist es ganz einfach, Ihre Lernprogramme hervorzuheben, neue Kurse zu fördern und einem breiteren Publikum wichtige Informationen bereitzustellen.

Besucher können den Katalog durchsuchen, Details zu Kursen und Instanzen anzeigen und die globale Suche nutzen, um verfügbare Schulungsmöglichkeiten zu erkunden. Aktionen, die jedoch die Identität eines Benutzers erfordern, z. B. die Registrierung für einen Kurs, den Zugriff auf personalisierte Funktionen (z. B. Kalender, Compliance, Leaderboard oder Soziales Lernen) oder die Nutzung von Schulungen, fordern den Besucher auf, sich anzumelden. Dieser Ansatz stellt sicher, dass vertrauliche und personalisierte Informationen sicher bleiben und dennoch ein umfassendes Vorschauerlebnis ermöglichen.

Administratoren können konfigurieren, welche Seiten und Widgets für nicht angemeldete Benutzer sichtbar sind. Dadurch wird sichergestellt, dass nur die entsprechenden Inhalte angezeigt werden. Seiten können so eingestellt werden, dass sie sowohl für angemeldete als auch für nicht angemeldete Benutzer oder ausschließlich für eine dieser Gruppen zugänglich sind. Experience Builder bietet einen Vorschaumodus, mit dem Sie genau sehen können, wie Ihre Seiten den Besuchern angezeigt werden, bevor sie veröffentlicht werden.

Um diese Funktion zu aktivieren, muss Ihr ALM-Integrationsadministrator den Connector für den Zugriff auf Schulungsdaten aktivieren. Dieser Connector stellt sicher, dass die Kurs-Metadaten öffentlich zugänglich sind.

Branding und Lokalisierung werden vollständig unterstützt, sodass Sie Seitentitel, Favoriten und Spracheinstellungen anpassen können, um sie an die Identität Ihres Unternehmens und die Anforderungen Ihrer Zielgruppe anzupassen. Als Teil des Übergangs zu dieser verbesserten Erfahrung wird die alte Startseitenfunktion für nicht angemeldete Benutzer verworfen. Daher sollten alle neuen öffentlichen Inhalte mit Experience Builder erstellt werden.

### Zweck der Funktion

Das nicht angemeldete Erlebnis in Experience Builder ermöglicht es Unternehmen, ihre Lerninhalte und Portalseiten öffentlich zu präsentieren, ohne dass sich Benutzer anmelden müssen. Dies hilft, potenzielle Teilnehmer anzulocken, zu informieren und anzusprechen, indem eine Vorschau der verfügbaren Schulungen und Ressourcen bereitgestellt wird, bevor eine Anmeldung oder Authentifizierung erforderlich ist.

### Nutzungsszenarien in der Praxis bei nicht angemeldeten Benutzern

* **Marketing und Kontaktaufnahme**: Organisationen können ihre Schulungsprogramme für externe Zielgruppen wie potenzielle Kunden, Partner oder Stellenbewerber veröffentlichen, indem sie Kurskataloge und Programmdetails öffentlich zugänglich machen.
* **Vorabregistrierung**: Teilnehmer können verfügbare Kurse durchsuchen, Übersichten anzeigen und Kategorien erkunden, bevor sie sich registrieren oder anmelden, um ihnen dabei zu helfen, fundierte Entscheidungen zur Registrierung zu treffen.
* **Schulungsportale für Unternehmen**: Unternehmen können ein öffentlich zugängliches Portal für Konformitäts- oder Onboarding-Informationen bereitstellen, sodass neue Mitarbeiter oder Auftragnehmer sehen können, welche Schulung verfügbar ist, bevor sie Anmeldeinformationen erhalten.
* **Zielseiten für Veranstaltungen oder Kampagnen**: Organisationen, die Lernkampagnen oder Veranstaltungen durchführen, können spezielle öffentliche Seiten erstellen, um Kurse, Zeitpläne oder Ressourcen hervorzuheben und so die Sichtbarkeit und Interaktion zu erhöhen.
* **SEO und Auffindbarkeit**: Durch die Veröffentlichung ausgewählter Seiten und Kataloge verbessern Organisationen ihre Sichtbarkeit in Suchmaschinen und helfen den Personen, ihre Lernangebote online zu entdecken.

### Wichtige Konzepte für nicht angemeldete Benutzer

Das nicht angemeldete Erlebnis von Experience Builder ermöglicht es Ihnen, Lerninhalte und Portalseiten öffentlich zu präsentieren, sodass Besucher ohne Anmeldung durchsuchen können.

* **Öffentliche Seiten und Menüs erstellen**: Sie richten Seiten und ein einzelnes Menü ein, auf das jeder unabhängig vom Anmeldestatus zugreifen kann.
* **Nur unterstützte Widgets hinzufügen**: Sie fügen Widgets hinzu, die keinen Benutzerkontext benötigen (Kategorien, Kurse und Lernpfade, Inhaltsfeld, HTML, iframe), während das System benutzerspezifische Widgets ausblendet.
* **Adaptives Seitenverhalten konfigurieren**: Sie entscheiden, ob eine Seite sowohl für angemeldete als auch für nicht angemeldete Benutzer angezeigt wird, und das System passt sichtbare Widgets und Inhalte basierend auf dem Anmeldestatus an.
* **Beide Erlebnisse in der Vorschau anzeigen**: Sie verwenden Vorschauoptionen, um zu sehen, wie Seiten nach angemeldeten und nicht angemeldeten Benutzern suchen, wobei Unterschiede in der Sichtbarkeit und dem Inhalt der Widgets bestehen.
* **Globale Suche aktivieren**: Besucher suchen nach Kursen und Inhalten, erhalten jedoch nur einfache Suchfunktionen ohne erweiterte AI-Integration.
* **Besucher können den Katalog und die Kursübersichten durchsuchen**: Besucher können Katalogseiten, Kursdetails und Instanzen durchsuchen, müssen sich jedoch anmelden, um sich zu registrieren oder auf personalisierte Funktionen zuzugreifen.
* **Branding und Lokalisierung anpassen**: Sie legen die Favicons und Spracheinstellungen so fest, dass sie mit dem Branding und der Barrierefreiheit Ihrer Organisation übereinstimmen.
* **Connector für den Zugriff auf Schulungsdaten aktivieren**: Sie aktivieren diesen Connector, um Kursmetadaten zur öffentlichen Anzeige zu exportieren und nicht angemeldete Seiten auf dem neuesten Stand zu halten.
* **Umgang mit hohem Traffic mit gemeinsam genutzter Infrastruktur**: Das System verwaltet große Mengen anonymer Besucher mithilfe gemeinsam genutzter Ressourcen und Ratenbegrenzung.
* **Optimieren für SEO**: Die Plattform bereitet öffentliche Seiten für die Suchmaschinenindizierung vor, sodass Ihre Lerninhalte leichter zu finden sind.

### Voraussetzungen für nicht angemeldetes Erlebnis

* Sie müssen den Connector für den Zugriff auf Schulungsdaten im Integrationsadministrator aktivieren, bevor Sie die nicht angemeldete Erfahrung verwenden können.
* Der Connector exportiert Kurs-Metadaten in ein öffentliches Repository, wodurch nicht angemeldete Seiten aktualisiert werden.

#### Initialisierung des Connectors für den Schulungsdatenzugriff

Der Connector für den Training Data Access (TDA) ist eine wichtige Voraussetzung für die Aktivierung der neuen Funktion &quot;Experience Builder&quot;, die nicht angemeldet ist, in ALM. Dieser Connector erleichtert den Export von Schulungsmetadaten, sodass Ihr Portal Kursinformationen für nicht angemeldete Benutzer anzeigen kann.

* **Connector-Aktivierung**: Sie müssen den TDA-Connector über das Integrations-Admin-Fenster aktivieren. Dieser Schritt aktiviert die nicht angemeldete Funktion von Experience Builder und macht relevante UI-Optionen auf der Administratoroberfläche sichtbar.
* **Metadatenexport**: Nach der Aktivierung exportiert der Connector wichtige Schulungsmetadaten (z. B. Kursname, Beschreibung, Übersicht, Bewertung, Dauer und Kenntnisse) aus ALM in ein öffentliches Repository. Diese Daten werden verwendet, um nicht angemeldete Seiten und Widgets aufzufüllen.
* **Planung und Synchronisierung**: Der Exportvorgang kann geplant werden (z. B. täglich), um sicherzustellen, dass Ihr Portal die neuesten Kursupdates enthält. Änderungen, die in ALM vorgenommen wurden, werden abhängig von der Zwischenspeicherung und der Exportfrequenz nach dem nächsten Exportzyklus auf den nicht angemeldeten Seiten angezeigt.
* **Verfügbarkeit von Funktionen**: Auf die nicht angemeldeten Funktionen von Experience Builder, einschließlich Menüerstellung, Widget-Unterstützung und Katalogsichtbarkeit, kann erst nach der Initialisierung des TDA-Connectors zugegriffen werden. Wenn der Connector nicht aktiviert ist, bleibt Ihr Experience Builder auf angemeldete Benutzerszenarien beschränkt.
* **Migration und Support**: Bei Konten, die von älteren, nicht angemeldeten Homepage-Funktionen wechseln, ist die Initialisierung des TDA-Connectors der erste Schritt zur Migration. So wird sichergestellt, dass ihr die Flexibilität und erweiterten Funktionen des neuen Experience Builder nutzen könnt.


### Was Besucher ohne Anmeldung tun können

Auf einer nicht angemeldeten Experience Builder-Website können Besucher den Schulungskatalog durchsuchen, indem sie die Katalogseite für öffentliche Kataloge öffnen. Sie können Filter wie Katalog, Produkt, Rolle, Typ, Kenntnisse und Tags verwenden, je nachdem, wie Sie die Site konfiguriert haben. Besucher können auch über die globale Suchleiste in der Kopfzeile nach Schulungen suchen (sofern aktiviert) und die Suchergebnisse direkt auf der Katalogseite anzeigen.

Besucher können Schulungsdetails anzeigen, indem sie Übersichtsseiten für Kurse, Lernpfade und Zertifizierungen öffnen. Auf diesen Seiten werden wichtige Metadaten angezeigt, einschließlich Titel, Beschreibung, Autor, Dauer, Format, Tags und Kenntnissen.

Darüber hinaus können Besucher statische und Werbeinhalte erkunden. Sie können Text- und Rich-Content-Blöcke lesen, Banner und Bildkacheln anzeigen und mit eingebetteten iframes wie externen Microsites, Videos oder Tools interagieren.

Wenn ein Besucher auf &quot;Registrieren&quot; klickt oder versucht, die Schulung zu starten, werden sie vom System aufgefordert, sich anzumelden oder sich anzumelden. Nach erfolgreicher Anmeldung wird der Besucher auf die entsprechende Seite umgeleitet, unabhängig davon, ob es sich um die Startseite, eine benutzerdefinierte Seite oder die ausgewählte Schulung handelt.

### Was ohne Anmeldung nicht verfügbar ist

Auf einer nicht angemeldeten Experience Builder-Website können Besucher nicht auf Funktionen oder Inhalte zugreifen, für die eine Benutzerauthentifizierung erforderlich ist. Sie können sich nicht für Schulungen registrieren, Kurse starten oder nutzen oder auf personalisierte Widgets wie &quot;Eigenes Lernen&quot;, &quot;Kalender&quot;, &quot;Konformität&quot;, &quot;Leaderboard&quot; oder &quot;Soziales Lernen&quot; zugreifen. Diese Widgets hängen von benutzerspezifischen Daten ab und sind nur nach der Anmeldung verfügbar.

Besucher können auch keine Aktionen ausführen, wie z. B. sich für einen Kurs registrieren oder auf Inhalte zugreifen, für die die Verfolgung des Fortschritts oder des Benutzerkontexts erforderlich ist. Wenn Sie versuchen, sich zu registrieren oder eine Schulung zu starten, wird der Besucher aufgefordert, sich anzumelden oder sich anzumelden, bevor Sie fortfahren.

### Unterstützte Widgets im nicht angemeldeten Modus

Im nicht angemeldeten Modus werden nur Widgets unterstützt, die keine benutzerspezifischen Daten benötigen. Dazu gehören:

* Widget &quot;Kategorien&quot;, das verfügbare Schulungskategorien anzeigt.
* Widget &quot;Kurse und Pfade&quot;, das Kurse und Lernpfade aus dem öffentlichen Katalog anzeigt.
* Feld &quot;Inhalt&quot; zum Hinzufügen von statischem Text, Bildern oder Werbeinhalten.
* HTML-Widget zum Einbetten von benutzerdefiniertem HTML-Inhalt.
* Iframe-Widget zur Anzeige externer Sites, Videos oder Werkzeuge auf der Seite.
* Widgets, für die Benutzerkontext erforderlich ist, z. B. &quot;Eigenes Lernen&quot;, &quot;Kalender&quot;, &quot;Konformität&quot;, &quot;Leaderboard&quot; und &quot;Soziales Lernen&quot;, sind im nicht angemeldeten Modus nicht verfügbar.

### Seiten und Menüs ohne angemeldeten Benutzer

* Es wird nur ein nicht angemeldetes Menü unterstützt, das für alle Besucher ohne Authentifizierung sichtbar ist.
* Seiten können sowohl angemeldeten als auch nicht angemeldeten Menüs hinzugefügt werden. Befindet sich eine Seite in beiden Menüs, werden Widgets und Inhalte entsprechend dem Anmeldestatus des Benutzers angepasst.
* Nicht angemeldete Menüs bieten kein Zielgruppen-Targeting oder keine Personalisierung. Jeder sieht den gleichen Satz von Seiten.
* Widgets, die im nicht angemeldeten Modus nicht unterstützt werden, werden automatisch ausgeblendet. Das Seitenlayout wird angepasst, um Lücken zu füllen.
* Die Menü- und Seitenverwaltung (Hinzufügen, Vorschau, Löschen) ähnelt dem angemeldeten Modus, weist jedoch Anpassungen für nicht angemeldete Einschränkungen auf.

### Suchen- und Katalogverhalten

Im nicht angemeldeten Modus können Benutzer auf die Katalogseite zugreifen und die Suche verwenden, um verfügbare Kurse und Lernpfade zu durchsuchen. Auf der Katalogseite werden alle öffentlichen Kurse zusammen mit Filtern und Suchfunktionen angezeigt. Es folgen dieselben Kontoeinstellungen wie im angemeldeten Modus. Wenn ein Benutzer sucht, werden die Ergebnisse auf der Katalogseite angezeigt und Benutzer können die Kurs- und Instanzübersichtsseiten anzeigen, ohne sich anzumelden. Für Aktionen wie die Registrierung ist jedoch eine Anmeldung erforderlich.

Wenn ein Benutzer versucht, sich zu registrieren, muss er sich zuerst anmelden. Die Suche nach nicht angemeldeten Benutzern ist einfacher als die nach angemeldeten Benutzern und umfasst keine erweiterten Funktionen wie die AI Assistant-Integration.

### Technische Umsetzung

#### Einrichtung des Schulungsdatenzugriffs-Connectors

Sie müssen den Connector für den Zugriff auf die Schulungsdaten im Admin-Bereich der Integration aktivieren, bevor Sie die Funktion &quot;Experience Builder&quot; verwenden können, bei der Sie nicht angemeldet sind. Dieser Connector exportiert Schulungsmetadaten aus ALM in ein öffentliches Repository, sodass sie über APIs für Ihre nicht angemeldeten Seiten zugänglich sind. Das Connector-Setup ist eine Voraussetzung für die Aktivierung der Funktion und stellt sicher, dass Ihr Portal aktuelle Schulungsinformationen anzeigt.

#### Metadatenexport und -synchronisierung

Der Connector exportiert wichtige Metadatenfelder wie Kursname, Übersicht, Beschreibung, Bewertung, Dauer und Kenntnisse. Sie können Exporte (z. B. täglich) planen, damit Ihr Portal mit ALM synchronisiert ist. Nicht alle Metadatenfelder können einbezogen werden. Eine vollständige Liste erhalten Sie vom Engineering. Exportierte Daten werden zum Ausfüllen nicht angemeldeter Seiten verwendet, und Änderungen in ALM werden nach dem nächsten Exportzyklus angezeigt.

#### Zwischenspeichern und Exporthäufigkeit

Das System verwendet die Exportfrequenz des Backends und das Frontend-Caching, um Datenaktualisierungen zu verwalten. Änderungen, die in ALM vorgenommen wurden, werden nach der geplanten Aktualisierung von Export und Cache auf Ihrem Portal widergespiegelt. Einige Updates werden aufgrund dieser Mechanismen möglicherweise nicht sofort angezeigt. Wenn Sie schnellere Updates benötigen, passen Sie den Exportplan an oder leeren Sie den Cache nach Bedarf.

#### Unterstützung für CSS/JS-Anpassung

Auf der Registerkarte &quot;Anpassung&quot; können Sie benutzerdefinierte CSS- und JavaScript-Einstellungen für angemeldete und nicht angemeldete Seiten vornehmen. Auf diese Weise könnt ihr ein konsistentes Branding gewährleisten, benutzerdefinierte UI-Elemente hinzufügen und die User Experience im gesamten Portal verbessern. Alle Anpassungen werden global angewendet, um ein einheitliches Erscheinungsbild zu gewährleisten.

#### URL-Unterschiede und Branding (Favoritensymbol, Seitentitel)

Nicht angemeldete und angemeldete Seiten können unterschiedliche URLs haben, um Benutzerstatus zu unterscheiden. Du kannst Favoritensymbol und Seitentitel für dein Portal anpassen, um deine Markenidentität zu stärken. Diese Funktionen sind in Experience Builder verfügbar. Wenden Sie sich an das Engineering, um den neuesten Status bezüglich des nicht angemeldeten Supports zu erfahren.

### Performance und Skalierbarkeit

#### Gemeinsam genutzter Stack im Vergleich zu Premium Stack

Der gemeinsam genutzte Stack ermöglicht es mehreren Kunden, den nicht angemeldeten Experience Builder in einer gemeinsamen Infrastruktur zu verwenden und so Standard-Traffic-Level zu unterstützen. Der Premium-Stack ist eine kostenpflichtige Option, die dedizierte Ressourcen, Echtzeitfunktionen und höhere Lizenzbeschränkungen für Kunden mit erweiterten Anforderungen bietet. Wählen Sie den Stapel basierend auf dem erwarteten Traffic und den Geschäftsanforderungen aus.

#### Verkehrsbeschränkungen und Gebührenbegrenzung

Der gemeinsam genutzte Stack erzwingt Verkehrsbeschränkungen, um eine faire Nutzung unter den Kunden zu gewährleisten. Das Engineering implementiert Ratenbegrenzungen, um zu verhindern, dass ein einzelner Kunde alle Ressourcen verbraucht. Wenn ihr Marketing-Kampagnen plant oder hohe Traffic-Zahlen erwartet, stimmt euch mit der technischen Abteilung ab, um eure Grenzen zu kennen und Unterbrechungen von Services zu vermeiden. Mithilfe der Ratenbegrenzung können Systemstabilität und -leistung für alle Benutzer gewährleistet werden.

#### Überlegungen zu Mehrmandantenfähigkeit und SEO

Die Plattform unterstützt mehrere Mandanten, sodass mehrere Kunden ihre Portale in einer gemeinsam genutzten Infrastruktur hosten können. Nicht angemeldete Seiten sind SEO-freundlich, zusammen mit sitemap.xml und robots.txt, um die Sichtbarkeit von Suchmaschinen zu optimieren. Dadurch wird sichergestellt, dass Ihr Portal von Suchmaschinen erkannt und entsprechend indiziert werden kann.

### Migration und Abschaffung

#### Übergang von einer vorhandenen nicht angemeldeten Startseite

Sie sollten Ihre Startseite mit dem neuen Experience Builder neu erstellen, um mehr Flexibilität, Widget-Unterstützung und ein verbessertes Benutzererlebnis zu erhalten. Der Übergangsplan sorgt für minimale Unterbrechungen und kontinuierlichen Support.

#### Kommunikationsplan

Kunden, die die ältere Startseite verwenden, erhalten eine klare Mitteilung über den Zeitplan für die Abschaffung und die Migrationsschritte. Es wird Support angeboten, der dir hilft, deine Homepage auf die neue Experience Builder-Plattform zu verschieben, sodass du von neuen Funktionen und laufenden Updates profitieren kannst.

### Unterstützung für Lokalisierung und Anmeldung

#### Gebietsschema-Fallback-Logik

Das System zeigt die Seiten in dem Gebietsschema an, in dem sie erstellt wurden. Wenn das Gebietsschema eines Benutzers nicht verfügbar ist, verwendet das System eine Fallback-Logik, um das nächstbeste verfügbare Gebietsschema auszuwählen. Dadurch wird sichergestellt, dass Benutzer Inhalte immer in einer unterstützten Sprache anzeigen können, was die Zugänglichkeit und die Zufriedenheit der Benutzer verbessert.

#### Unterstützte Anmeldetypen

Das nicht angemeldete Erlebnis unterstützt alle in ALM verfügbaren Anmeldetypen, einschließlich SSO und Standardanmeldung. Benutzer können Inhalte durchsuchen, ohne sich anzumelden, und werden bei Bedarf aufgefordert, sich anzumelden, z. B. um sich für einen Kurs zu registrieren oder auf personalisierte Funktionen zuzugreifen. Dies ermöglicht einen reibungslosen Übergang vom Browsen zur Interaktion.


### Nicht angemeldete APIs

#### Admin-Lernobjekt-API

Nicht angemeldete Experience Builder-Seiten und Headless-Portale organisieren oder filtern Kurse oft nach Produkten und Rollen. Die Admin LO-API wurde verbessert, um sicherzustellen, dass diese Verknüpfungen für Backend- und Headless-Integrationen sowie für den TDA-Connector konsistent zugänglich sind.

**Endpunkt und Verhalten**

Sie verwenden weiterhin den vorhandenen Admin LO-Endpunkt:

```
GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=products,roles
```

Dabei gilt:

* loId ist die Lernobjekt-ID (z. B. Kurs:12345).
* enforcedFields[learningObject] weist die API an, Produkte und Rollen für dieses LO explizit einzuschließen.

Dies wird dadurch erreicht, dass sichergestellt wird, dass die Produkt- und Rollenzuordnungen des LO in der Antwort vorhanden sind, wenn sie über enforcedFields angefordert werden. Die Antwort enthält dann in Attributen die Produkt- und Rollenmetadaten, die zum Berechnen oder Verfügbarmachen der empfohlenen Produkte (rec\_products) und Rollen (rec\_roles) für Experience Builder und andere Benutzer erforderlich sind.

Ein typischer Anruf von einem Administrator oder einer Integration sieht wie folgt aus:

```
url -X GET \
 "https://{your-domain}/primeapi/v2/learningObjects/course:12345?enforcedFields[learningObject]=products,roles" \
 -H "Authorization: Bearer {admin\_token}" \
 -H "Accept: application/vnd.api+json
```

Die zurückgegebene LO-JSON-Datei ist dieselbe Grundstruktur wie zuvor, aber jetzt können Sie sich darauf verlassen, dass Produkt-/Rollenfelder vorhanden sind, wenn Sie sie mit enforcedFields anfordern. Integrationen, die keine erzwungenen Felder verwenden, verhalten sich weiterhin wie zuvor.

#### Liste der Lernobjekte - JobAid-Unterstützung im effectModifiedDate-Filter

**Zweck**

Der TDA-Connector (Training Data Access) und Headless-Implementierungen müssen häufig eine inkrementelle Synchronisierung ausführen, basierend auf dem **Datum der effektiven Änderung** der Lernobjekte. Bis zu dieser Version wurden JobAids (LO-Typ jobAid) nicht korrekt behandelt, wenn sie mit den Filtern effectModifiedDate kombiniert wurden. Diese Version behebt dies, sodass JobAids inkrementell wie Kurse und Lernpfade synchronisiert werden können.

**Endpunkt und Verhalten**

Sie verwenden den vorhandenen LO-Listingendpunkt mit Datumsfiltern und dem LO-Typ:

```
GET /primeapi/v2/learningObjects
 ?filter.effectiveModifiedDate.fromDate=2025-03-15T13:14:56.000Z
 &filter.effectiveModifiedDate.toDate=2025-03-20T13:14:56.000Z
 &filter.loTypes=jobAid
```

Wenn filter.loTypes=jobAid bisher mit einem effectModifiedDate-Bereich kombiniert wurde, hat der Filter JobAids effektiv ausgeschlossen und der Aufruf hat sich so verhalten, als ob JobAids nicht unterstützt wurden.

Ab dieser Aktualisierung gibt der Aufruf nur noch JobAid-Lernobjekte zurück, deren effectModifiedDate sich innerhalb des angegebenen Fensters befindet.

```
{
 "links": {
 "self": "https://acapapiserver/primeapi/v2/learningObjects?page[limit]=10&filter.effectiveModifiedDate.fromDate=2026-01-19T13:14:56.000Z&filter.effectiveModifiedDate.toDate=2026-01-21T13:14:56.000Z&filter.loTypes=jobAid"
 },
 "data": [
 {
 "id": "jobAid:144968",
 "type": "learningObject",
 "attributes": {
 "authorNames": ["Author"],
 "dateCreated": "2026-01-20T08:48:55.000Z",
 "datePublished": "2026-01-20T08:48:55.000Z",
 "dateUpdated": "2026-01-20T08:48:55.000Z",
 "effectiveModifiedDate": "2026-01-05T07:31:18.000Z",
 "loType": "jobAid",
 "loFormat": "Content",
 "loResourceType": "Content",
 "localizedMetadata": [
 {
 "description": "Link jobAid new",
 "locale": "en-US",
 "name": "Link jobAid new"
 },
 {
 "description": "Link jobAid new fre",
 "locale": "fr-FR",
 "name": "Link jobAid new fre"
 }
 ],
 "relationships": {
 "authors": {
 "data": [
 { "id": "13385176", "type": "user" }
 ]
 },
 "instances": {
 "data": [
 { "id": "jobAid:144891\_-1", "type": "learningObjectInstance" }
 ]
 }
 }
 }
 }
 ]
}
```

Dies bedeutet, dass Sie jetzt inkrementelle JobAid-Synchronisationen auf der Grundlage von effectModifiedDate sicher implementieren können, wie Sie es bereits bei anderen Typen tun.

Wenn Sie filter.loTypes=jobAid weglassen, bleibt das Verhalten für andere LO-Typen unverändert. Die Änderung wirkt sich nur auf die Kombination von JobAid mit diesem Filter aus.

#### **Menü-API: Nicht angemeldeter Menüfilter**

**Zweck**

Experience Builder und Headless-Frontends benötigen eine einfache Möglichkeit, das **nicht angemeldete Menü** abzurufen, das die Navigation für öffentliche Besucher definiert. Vor dieser Version mussten Sie alle Menüs abrufen und dann eine benutzerdefinierte Logik anwenden, um zu identifizieren, welche die nicht angemeldete Navigation darstellte. Diese Version fügt einen einfachen serverseitigen Filter hinzu.

**Endpunkt und Verhalten**

Sie verwenden den vorhandenen Menüauflistungsendpunkt mit einem neuen Abfrageparameter:

```
GET /primeapi/v2/templates/menus?include=pages,subMenus.pages&isNonLoggedIn=true
```

Die wichtigsten Punkte:

* include=pages,subMenus.pages ist optional, wird aber empfohlen, wenn Sie die Seiten- und Untermenü-Seitendetails in derselben Antwort benötigen.
* isNonLoggedIn=true ist neu in dieser Version und weist den Server an, nur Menüs zurückzugeben, die als nicht angemeldete Menüs gekennzeichnet sind.

Ohne den isNonLoggedIn-Parameter verhält sich der Endpunkt genau wie zuvor und gibt Menüs entsprechend dem vorhandenen Standardverhalten zurück. Mit isNonLoggedIn=true gibt es in der Regel das einzelne Menü zurück, das vom nicht angemeldeten Erlebnis für Ihr Konto verwendet wird (da es normalerweise ein nicht angemeldetes Menü pro Konto gibt).

In der Praxis kann ein Kunde jetzt Folgendes ausstellen:

```
curl -X GET \
 "https://{your-domain}/primeapi/v2/templates/menus?include=pages,subMenus.pages&isNonLoggedIn=true" \
 -H "Authorization: Bearer {admin\_token}" \
 -H "Accept: application/vnd.api+json"
```

und rufen Sie die nicht angemeldete Navigationsstruktur in einem Aufruf zurück, mit allen Seiten, die für anonyme Besucher sichtbar sein sollten.

Dies ist besonders nützlich, wenn Sie eine Headless-Site ohne angemeldeten Benutzer erstellen und dieselbe Navigation wie in Experience Builder spiegeln möchten oder wenn Sie debuggen, ob das nicht angemeldete Menü korrekt konfiguriert wurde.

### Liste benutzerdefinierter Domänen zulassen

Der nicht angemeldete Stapel besteht aus:

* Eine öffentliche CDN-Domäne (z. B. cpcontents.adobe.com oder yourdomain.example.com), die Layouts, Konfigurations-JSON und statische Assets bereitstellt.
* Ein Endpunkt eines öffentlichen Elasticsearchs (ES), der Katalog- und Suchdaten bereitstellt, jedoch nur, wenn die Anforderung von einer **zugelassenen Domäne** für dieses ALM-Konto stammt.

Wenn Sie eine benutzerdefinierte Domäne einführen, funktioniert diese nahtlos, ohne dass dem vorhandenen Prozess zum Hinzufügen einer benutzerdefinierten Domäne zusätzlicher Aufwand folgt.

#### Voraussetzungen

Bevor Sie eine benutzerdefinierte Domäne für nicht angemeldete Benutzer auf die Positivliste setzen:

1. Die benutzerdefinierte Domäne wird für Ihr ALM-Konto konfiguriert (z. B. verweist DNS für academy.yourcompany.com auf Adobe/Akamai und es werden Zertifikate bereitgestellt).
2. Der **TDA-Connector (Training Data Access)** ist für das Konto aktiviert.
3. Die **nicht angemeldete Experience Builder**-Funktion ist aktiviert (Adobe-seitig).

Mit diesen Schritten wird sichergestellt, dass

* Ihr Konto verfügt über eine nicht angemeldete **Konto-JSON** (häufig als accountConfig / experienceBuilderConfig bezeichnet), die Felder wie cpDomain, almDomain, almCdnBaseUrl, esBaseUrl und zugelassenen Domänen enthält.
* Der nicht angemeldete Stapel weiß, wo Daten bereitgestellt werden sollen und von welchen Domänen Anfragen angenommen werden sollen.

#### Funktionsweise der Zulassungsliste

Die Zulassungsliste wird in der Konfiguration gespeichert, die TDA exportiert, und der nicht angemeldete Stack liest. Diese Konfiguration umfasst:

* Die ALM-Domänen (cpDomain, almDomain).
* Die **CDN-Basis-URL** für nicht angemeldeten Inhalt (almCdnBaseUrl).
* Die **URL der öffentlichen Suchbasis** (esBaseUrl).
* Die Liste der Domänen, die nicht angemeldete Aufrufe für dieses Konto veröffentlichen dürfen.

Damit Experience Builder, der nicht angemeldet ist, in einer benutzerdefinierten Domäne funktioniert:

* Der Browser muss die nicht angemeldete HTML von dieser benutzerdefinierten Domäne (oder von der nicht angemeldeten ALM-CDN-Domäne, je nach Einrichtung) laden.
* Aufrufe von dieser Domäne an die öffentlichen ES- und CDN-Endpunkte müssen akzeptiert werden. Dies geschieht nur, wenn die Domäne in der Zulassungsliste vorhanden ist.

Diese Version fügt eine neue, nicht angemeldete CDN-Domäne cpcontents.adobe.com hinzu und gibt an, dass sie in die **zugelassenen Domänen** im TDA-Connector platziert werden muss. Für vorhandene nicht angemeldete native Benutzer ist hierfür ein Update erforderlich.

#### Benutzerdefinierte Domäne zulassen

**Benutzerdefinierte Domäne in ALM konfigurieren**

Arbeiten Sie mit Adobe zusammen, um Ihre Domäne wie academy.yourcompany.com als benutzerdefinierte Domäne für Ihr ALM-Konto zu registrieren. Sie aktualisieren DNS so, dass es wie angewiesen auf Adobe Akamai zeigt, und warten Sie, bis SSL und Routing abgeschlossen sind.

An diesem Punkt kann sowohl angemeldeter als auch nicht angemeldeter Datenverkehr über diese Domäne ALM erreichen, aber nicht angemeldete Such- und Katalogaufrufe können weiterhin blockiert werden, wenn die Domäne nicht auf der Zulassungsliste steht.

**TDA und nicht angemeldeten Experience Builder aktivieren**

Voraussetzungen:

* Der **Schulungsdatenzugriffsconnector** ist aktiviert.
* Die **nicht angemeldete Experience Builder**-Funktion ist für das Konto aktiviert.

Durch Aktivieren von TDA wird die JSON-Datei des nicht angemeldeten Kontos erstellt oder aktualisiert. Bei neuen Konten wird im Prozess standardmäßig auch die neue nicht angemeldete CDN-Domäne (cpcontent.adobe.com) auf die Zulassungsliste gesetzt, sodass der öffentliche ES-Endpunkt Aufrufe von dieser Domäne erwartet.

Bei Konten, die bereits den älteren nicht angemeldeten Stapel verwendet haben, müssen vorhandene Connectors gelöscht und neu erstellt werden, um die neue Domäne zu nutzen.

**Benutzerdefinierte Domäne zur Zulassungsliste hinzufügen**

Entscheidend ist, dem nicht angemeldeten ES-Stack mitzuteilen, dass academy.yourcompany.com ein genehmigter Ursprung ist. Es gibt zwei gemeinsame Pfade.

1. **TDA-Connector wieder aktivieren (einfach, Self-Service-freundlich)**

Bestehende native nicht angemeldete Benutzer müssen die TDA-Verbindung löschen und erneut aktivieren, damit die neue Domäne automatisch auf die Zulassungsliste gesetzt wird. Damit werden zwei Dinge erreicht:

1. Die JSON-Datei für das nicht angemeldete Konto wird neu generiert.
2. Die auf der Zulassungsliste aufgeführten Domänen werden aktualisiert, um die neue, nicht angemeldete CDN-Domäne und Ihre benutzerdefinierte Domäne einzubeziehen.

Dies wird empfohlen, wenn Sie eine kleine Anzahl von Konten haben und es zulassen können, dass der Connector vorübergehend deaktiviert und wieder aktiviert wird.

1. **Überprüfen Sie, ob die Domäne tatsächlich auf die Zulassungsliste gesetzt ist**

Öffnen Sie nach der Zulassungsauflistung Ihre nicht angemeldete Site in der benutzerdefinierten Domäne und überprüfen Sie die Browsernetzwerkaufrufe.

Sie möchten Folgendes sehen:

* Anforderungen an almCdnBaseUrl (z. B. <https://cpcontent.adobe.com/>...) erfolgreich mit 200/304.
* Anforderungen an esBaseUrl (API für die öffentliche Suche, z. B. <https://primeapps.adobe.com/almsearch/api/v1/>...) Erfolgreich, JSON wird mit Such-/Katalogdaten zurückgegeben.

Wenn diese Aufrufe 4xx oder explizite Fehler zurückgeben, die &quot;nicht vertrauenswürdige Domäne&quot; oder &quot;Ursprung nicht zulässig&quot; nahe legen, ist die Zulassungsliste unvollständig oder falsch konfiguriert, und der Support muss sie anpassen.

Die nicht angemeldete LLD stellt außerdem fest, dass die Kontokonfiguration einen erwarteten Domänenwert enthalten kann. Zur Laufzeit überprüft die Site, ob die Domäne in der URL mit dem in der Konfiguration festgelegten Wert übereinstimmt. Ist dies nicht der Fall, kann der Benutzer zu einer Fehlerseite umgeleitet werden. Dies schützt vor dem Zugriff auf die Konfiguration eines Kunden über die Domäne eines anderen Kunden.

### Verwendung von Empfehlungen in Experience Builder ohne Anmeldung

Mit dem nicht angemeldeten Experience Builder können Sie öffentliche Lernseiten erstellen, auf denen Besucher Ihren Katalog durchsuchen und markierte Inhalte anzeigen können, bevor sie sich anmelden. Auch wenn diese Besucher anonym sind, können Sie empfohlene Schulungen mithilfe von Metadaten und Widgets darstellen.

In der angemeldeten Teilnehmer-App können Empfehlungen personalisiert werden: Sie können vom Profil, dem Verlauf, den Kenntnissen und dem Fortschritt des Teilnehmers abhängen. Im **nicht angemeldeten**-Erlebnis ist noch keine Teilnehmeridentität vorhanden, daher kann die Plattform nicht pro Benutzer personalisiert werden.

Recommendations im nicht angemeldeten Modus sind daher:

* **Kuratiert oder regelbasiert**: basierend auf Katalog, Produkt, Rolle, Beschriftungen, Tags und anderen Metadaten.
* **Segmentorientiert**: &quot;Für Entwickler empfohlen&quot;, &quot;Für Partner empfohlen&quot;, &quot;Für Anfänger empfohlen&quot;.
* **Marketing-orientiert**: Ermöglicht es Besuchern, sich anzumelden, nachdem sie sich angemeldet haben.

### Metadaten und APIs, die Empfehlungen unterstützen

Hinter den Kulissen verwenden nicht angemeldete Seiten Folgendes:

* Der **TDA-Connector** zum Exportieren von Lernobjektmetadaten (Kurse, Pfade, Zertifizierungen, Arbeitshilfen) in einen öffentlichen Suchindex.
* Der **öffentliche Suchstapel** zum Beantworten von Abfragen aus nicht angemeldeten Widgets (Katalog, Suche, Kurse und Pfade, Kategorien).
* Die **API für Admin-Lernobjekte** zum Verfügbarmachen von Produkt- und Rollenmetadaten, die für Empfehlungsregeln verwendet werden können.

In dieser Version wurde die Admin LO-API erweitert, sodass Produkt- und Rollenzuordnungen zuverlässig verfügbar sind:

```
GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=products,roles
```

Dadurch können Widgets und Headless-Integrationen regelbasierte Empfehlungen erstellen, die Produkte, Rollen, Katalogbeschriftungen, Tags und andere Felder konsistent verwenden.

### Entwerfen von Empfehlungsabschnitten mit Experience Builder-Widgets

Sie erstellen Empfehlungsabschnitte auf nicht angemeldeten Seiten, indem Sie **Experience Builder-Widgets** mit Metadatenfiltern kombinieren.

#### **Widget für Kurse und Pfade**

Verwenden Sie das Widget **Kurse und Pfade**, wenn Sie eine Zeile oder ein Raster mit empfohlenen Elementen anzeigen möchten. In der Konfiguration können Sie wählen:

* Aus welchen Katalogen abgerufen werden soll.
* Welche Katalogbeschriftungen, Produkte, Rollen oder Tags als Filter verwendet werden sollen.
* Gibt an, ob Kurse, Pfade, Zertifizierungen, Arbeitshilfen oder ein Mix angezeigt werden sollen.
* Sortieren und maximale Anzahl von Elementen.

Beispielsweise können Sie Folgendes erstellen:

* &quot;Für Entwickler empfohlen&quot;: Filtert nach einem Produkt oder einer Rolle, die Sie für den Entwicklerinhalt verwenden.
* &quot;Hier starten&quot;: Filtern Sie nach einer Beschriftung wie &quot;Starter&quot; oder &quot;Onboarding&quot;.
* &quot;Empfohlen in diesem Quartal&quot;: Filtert nach einem zeitgebundenen Label wie featured-q3-2026.

Das Widget lernt nicht vom Verhalten, sondern zeigt an, welche Übereinstimmungen mit den von Ihnen definierten Metadatenregeln bestehen. Aus Sicht des Besuchers sieht es jedoch wie ein Empfehlungsstreifen aus.

#### **Kategorien-Widget**

Verwenden Sie das Widget **Kategorien**, um Besuchern zu helfen, in &quot;empfohlene&quot; Inhaltssätze zu navigieren, auch wenn sie Ihre Produktnamen nicht kennen.

Sie können Kacheln konfigurieren, die jeweils ein Segment darstellen, z. B.:

* &quot;Für Administratoren&quot;
* &quot;Für Vertriebsteams&quot;
* &quot;Für Partner&quot;
* &quot;Nach Produktlinie&quot;

Jede Kachel kann eine der folgenden Verknüpfungen enthalten:

* Eine gefilterte Katalogseite (z. B. der Katalog, der nach bestimmten Produkten oder Beschriftungen gefiltert wurde).
* Eine dedizierte, nicht angemeldete Seite, die für dieses Segment vorkonfigurierte Kurse und Pfade verwendet.

So erhaltet ihr ein Erlebnis nach &quot;empfohlenen Pfaden nach Segmenten&quot; ohne Personalisierung.

### Erstellen segmentbasierter Empfehlungen

Da nicht angemeldete Besucher noch kein ALM-Profil haben, ist es nützlich, Empfehlungen **nach Segment** zu entwerfen und die Auswahl der Besucher selbst zu ermöglichen.

1. Verwenden Sie eine **nicht angemeldete Startseite**, die kurz erklärt, für wen Ihre Akademie vorgesehen ist, und eine kleine Anzahl von Segmenteintrittspunkten anzeigt (z. B. &quot;Entwickler&quot;, &quot;Marketer&quot;, &quot;Partner&quot;, &quot;Neue Mitarbeiter&quot;). Dies kann mit einem Kategorien-Widget oder einem einfachen Inhaltsfeld oder einem HTML-Abschnitt mit Schaltflächen erfolgen.
2. Erstellen Sie für jedes Segment eine **dedizierte, nicht angemeldete Seite** in Experience Builder. Verwenden Sie auf dieser Seite ein oder mehrere Kurse- und Pfade-Widgets, die mit Filtern konfiguriert sind, die die Empfehlungen für diese Gruppe darstellen. Für &quot;Entwickler&quot; können Sie beispielsweise nach folgenden Elementen filtern:
   1. Katalog = &quot;Öffentliche Fortbildung&quot;
   2. Product = &quot;Adobe Experience Manager&quot;
   3. Tags = &quot;Grundlagen für Entwickler&quot;
3. Verwenden Sie diese Segmentseiten als Ziel Ihrer Marketing-Kampagnen und als Ziel der Kacheln auf der nicht angemeldeten Startseite.

Besucher nehmen an, dass sie auf ihre Situation zugeschnittene Empfehlungen sehen, obwohl die Logik zur Entwurfszeit über Metadaten definiert wird.

### Übergang von nicht angemeldeten zu personalisierten Empfehlungen

Nicht angemeldete Empfehlungen betreffen hauptsächlich **Auffindbarkeit** und **Konvertierung**. Sobald sich Besucher entscheiden, sich anzumelden oder eine Schulung zu starten, melden sie sich an und werden zu vollständigen Teilnehmern mit einem Profil und einem Verlauf.

Der übliche Ablauf ist:

1. Ein Besucher entdeckt Inhalte in Ihren nicht angemeldeten Empfehlungsabschnitten (Startseitenempfehlungen, Zielseiten-Segmentierung, hervorgehobene Zeilen).
2. Sie klicken auf eine Kurs- oder Pfadübersicht und wählen &quot;Registrieren&quot; oder &quot;Starten&quot;.
3. ALM fordert sie auf, sich anzumelden oder sich anzumelden.
4. Nach der Anmeldung wird das standardmäßige Anmeldeerlebnis für Teilnehmer übernommen, das Folgendes umfasst:
   1. &quot;Eigenes Lernen&quot;
   2. Logger Katalog mit persönlichem Fortschritt
   3. Alle internen Empfehlungssysteme, die Sie für bestehende Teilnehmer verwenden.

Mit anderen Worten, die angemeldeten Empfehlungen helfen ihnen dabei, zu entscheiden, was sie als Nächstes tun und weiter machen wollen.

### Verwendung von Arbeitshilfen im neuen, nicht angemeldeten Experience Builder

Auf der **Benutzeroberfläche** nehmen Arbeitshilfen hauptsächlich über Widgets, die Lernobjekte anzeigen können, an nicht angemeldeten Erlebnissen teil:

1. **Widget für Kurse und Pfade**
Dieses Widget kann mehrere LO-Typen anzeigen, einschließlich Arbeitshilfen. Auf nicht angemeldeten Seiten können Sie folgende Einstellungen vornehmen:
   1. Schließen Sie Arbeitshilfen explizit ein oder aus.
   2. Filtern Sie Arbeitshilfen nach Katalog, Produkt, Rolle, Beschriftungen, Tags und anderen Metadaten.
   3. Stellen Sie sie neben Kursen und Pfaden oder als separaten &quot;Ressourcen&quot;-Streifen vor.

Auf einer öffentlichen Landingpage können Sie beispielsweise einen Streifen mit dem Titel &quot;Hilfreiche Ressourcen&quot; konfigurieren, der nur Arbeitshilfen anzeigt, und einen anderen Streifen mit dem Titel &quot;Empfohlene Kurse&quot;, der Kurse und Pfade anzeigt.

1. **Katalogseite und Suche**
Die nicht angemeldeten **catalog**- und **search**-Oberflächen verwenden den öffentlichen Suchindex (gespeist vom Connector für den Zugriff auf Schulungsdaten). Dieser Index unterstützt Arbeitshilfen jetzt korrekt. Gehen Sie deshalb wie folgt vor:
   1. Nicht angemeldete Suchergebnisse können Arbeitshilfen enthalten.
   2. Nicht angemeldete Katalogfilter (nach Typ, Produkt, Tags usw.) können Arbeitshilfen beinhalten, solange Ihre Kontokonfiguration und Widgets so eingerichtet sind, dass sie angezeigt werden.
2. **LO-Übersichtsseiten**
Wenn ein Besucher auf eine Arbeitshilfe in einem Widget oder im Katalog klickt, geht er zu einer **LO-Übersichtsseite** für diese Arbeitshilfe im nicht angemeldeten Modus. Dort können sie die Beschreibung und die Metadaten lesen. Für den tatsächlichen Download oder Verbrauch ist in der Regel noch eine Anmeldung erforderlich, aber das Vorhandensein und die Auffindbarkeit der Arbeitshilfe selbst wird durch das nicht angemeldete Erlebnis gehandhabt.

### Anzeige von Arbeitshilfen über nicht angemeldete APIs

Auf der **API-Seite** werden Arbeitshilfen unterstützt von:

1. Der **Schulungsdatenzugriffsconnector und die öffentliche Suche**
TDA exportiert Arbeitshilfemetadaten zusammen mit anderen LO-Typen in den öffentlichen Suchindex, der nicht angemeldete Such- und Katalogabfragen bereitstellt. Darauf setzen Experience Builder und Headless-Frontends.
2. Die Liste der **Lernobjekte mit effektivemÄnderungsdatum**
In dieser Version wurde der LO-Listing-Endpunkt korrigiert, sodass Arbeitshilfen mit dem Filter effectModifiedDate ordnungsgemäß funktionieren. Sie können jetzt folgende Telefonnummern anrufen:

```
GET /primeapi/v2/learningObjects
 ?filter.effectiveModifiedDate.fromDate=2026-01-19T13:14:56.000Z
 &filter.effectiveModifiedDate.toDate=2026-01-21T13:14:56.000Z
 &filter.loTypes=jobAid
```

Vor dieser Änderung wurden beim Kombinieren von &quot;effectModifiedDate&quot; mit &quot;loTypes=jobAid&quot; keine Arbeitshilfen zuverlässig zurückgegeben. Das bedeutet:

1. Ihre TDA- oder ETL-Aufträge können **die Arbeitshilfen** für nicht angemeldete Erlebnisse inkrementell synchronisieren, genau wie bei Kursen und Pfaden.
2. Jede Headless-Implementierung, die ein öffentliches Verzeichnis für Arbeitshilfen erstellt, kann Änderungen basierend auf effectModifiedDate und loType=jobAid abfragen.

**Hinweis**:

Im Status &quot;nicht angemeldet&quot;:

* Arbeitshilfen sind hauptsächlich **auffindbar**: Besucher können sehen, dass sie vorhanden sind, Beschreibungen lesen und verstehen, wie sie Themen oder Kurse unterstützen.
* Die tatsächliche **Nutzung** (das Herunterladen oder Öffnen der Arbeitshilfeinhalte) erfordert in der Regel noch eine Anmeldung, insbesondere wenn Arbeitshilfen als Teil lizenzierter oder interner Inhalte betrachtet werden.

### Änderungen an der Kurzbeschreibung in der LO-Suche (nicht angemeldet)

Beim nicht angemeldeten Kurs werden die Suche nach und die Auflistung von Lernobjekten (LOs) durch den Connector für den Zugriff auf Schulungsdaten (TDA) und einen öffentlichen Elasticsearch-Index unterstützt. Früher verwendete dieser Stapel ein einzelnes Übersichts-/Beschreibungsfeld für jedes LO. Kunden, die Headless-Portale ohne angemeldete Benutzer erstellen, wollten auf LO-Kacheln dieselbe kurze Beschreibung anzeigen, die die Benutzeroberfläche des angemeldeten Teilnehmers zeigt, und nicht nur die lange Übersicht.

Mit der Änderung wird Unterstützung für die LO **Kurzbeschreibung** in APIs für die Suche und die Auflistung ohne angemeldete Benutzer eingeführt:

* Für **Kurse** lauten die vorhandenen Benutzeroberflächensemantiken:
* Eingeschriebene Karten zeigen eine Kurzbeschreibung (140 Zeichen Feld), falls vorhanden, ansonsten werden sie auf die lange Detailübersicht zurückgeführt.
* Für **Lernpfade** verwendet die angemeldete Benutzeroberfläche das Feld &quot;Vorteile&quot; als kurze Beschreibung (sofern definiert) und kehrt andernfalls zur Übersicht zurück.
* Für **Zertifizierungen** wird eine kurze Beschreibung mit einer längeren Zertifizierungsübersicht als Fallback verwendet.
* Für **Arbeitshilfen** wird das Hauptbeschreibungsfeld verwendet.

### Weitere Änderungen

#### Einschränkung, dass zwei Konten nicht dieselbe benutzerdefinierte Domäne gemeinsam nutzen können

In den nicht angemeldeten und angemeldeten Architekturen von Adobe Learning Manager wird eine **benutzerdefinierte Domäne** (z. B. academy.example.com) als global eindeutiger Schlüssel behandelt, der genau einem ALM-Konto zugeordnet werden muss. Die Plattform erzwingt daher eine strenge Einschränkung, dass **keine zwei Konten dieselbe benutzerdefinierte Domäne** gemeinsam nutzen können. Dies ist für Sicherheit, Routing und SEO erforderlich: Die Routing-Ebene und der nicht angemeldete Stapel verwenden die Domäne, um die richtige Kontokonfiguration zu nachzuschlagen (einschließlich der nicht angemeldeten Konto-JSON, der Experience Builder-Menüs, des Brandings und der TDA-/Suchendpunkte).

Wenn dieselbe benutzerdefinierte Domäne für zwei Konten zugelassen wird, ist es nicht möglich, die Rückgabe der Kontodaten zu garantieren. Außerdem kann dies zu mandantenübergreifenden Lecks führen und generierte Artefakte wie sitemap.xml und robots.txt beschädigen, die pro Konto erstellt, aber von Suchmaschinen pro Host entdeckt werden. Operativ bedeutet dies, dass Sie beim Zuweisen oder Verschieben einer benutzerdefinierten Domäne zuerst sicherstellen müssen, dass sie nicht an ein anderes Konto angehängt ist (oder dort die Registrierung aufheben), und das interne Tool von Adobe lehnt Versuche ab, dieselbe Domäne an mehrere Konten zu binden.

#### Browserzwischenspeicherung von Ressourcen bei nicht angemeldetem Benutzer

Bei nicht angemeldeten Adobe Learning Manager-Anwendern ist das Zwischenspeichern von Ressourcen im Browser ein zentraler Bestandteil der Performance- und Skalierungsstrategie, da öffentliche Seiten großen, manchmal stacheligen Marketing-Traffic mit geringer Latenz und minimaler Ursprungslast verarbeiten müssen. Statische und halbstatische Assets wie die nicht angemeldete HTML-Shell (z. B. index.html/guest.html), die JSON-Konfiguration auf Kontoebene (account.json oder config.json), das Experience Builder-Seitenlayout JSON (Menüs, Widget-Layouts, Karteneinstellungen), CSS, JS, Bilder und Favicons werden von einem Akamai CDN (cpcontents.adobe.com / cpcontent.adobe.com) mit Cache-Headern bereitgestellt, die sowohl CDN- als auch browserseitige Wiederverwendung unterstützen, sodass der Browser nach dem ersten Laden der Seite nachfolgende nicht angemeldete Seiten weitgehend rendern kann aus dem Cache löschen und nur bei Bedarf über ETag oder Last-Modified erneut validieren.

## Mehrsprachige Arbeitshilfen

### Einführung

Mithilfe mehrsprachiger Arbeitshilfen in Adobe Learning Manager (ALM) können Autoren und Administratoren unterstützende Dokumente, Hilfslinien oder Ressourcen in mehreren Sprachen in einem einzigen Arbeitshilfeeintrag zur Verfügung stellen. Teilnehmer aus verschiedenen Regionen können auf relevante Materialien in ihrer bevorzugten Sprache zugreifen, was das Verständnis, die Compliance und die Benutzerfreundlichkeit verbessert.

### Vorheriges Verhalten

Früher unterstützten Arbeitshilfen in ALM nur eine einzelne Inhaltsdatei pro Arbeitshilfe, auch wenn Name und Beschreibung lokalisiert werden konnten. Um dieselbe Ressource in mehreren Sprachen bereitzustellen, mussten Autoren für jede Sprache separate Arbeitshilfen erstellen. Dies führte zu Doppelarbeit, Verwirrung und einem erhöhten Verwaltungsaufwand. Es gab keine einheitliche Verwaltung mehrsprachiger Ressourcen, was die Konsistenz und Verfolgung der Verwendung erschwerte.

### Anwendungsszenarien

* **Aktivierung für globale Mitarbeiter**: Stellen Sie Sicherheitshandbücher, Prozessleitfäden oder Referenzdokumente in mehreren Sprachen für verschiedene Mitarbeiter bereit.
* **Einhaltung behördlicher Auflagen**: Stellen Sie sicher, dass alle Mitarbeiter die gleiche Dokumentation zur Einhaltung der Vorschriften in ihrer Muttersprache erhalten.
* **Konsistentes Onboarding**: Stellen Sie für Neueinstellungen weltweit Checklisten für das Onboarding oder FAQs in lokalen Sprachen zur Verfügung.
* **Reduzierte Duplizierung**: Verwalten Sie alle Sprachversionen einer Arbeitshilfe in einem einzigen Eintrag, wodurch Aktualisierungen und Berichterstellung vereinfacht werden.

### Wichtigste Funktionen

* **Unterstützung mehrerer Sprachen**: Fügen Sie eine eindeutige Datei oder URL für jede unterstützte Sprache in einer einzelnen Arbeitshilfe an.
* **Lokalisierter Name und Beschreibung**: Geben Sie den Namen und die Beschreibung der Arbeitshilfe in jeder Sprache ein.
* **Einheitliche Verwaltung**: Bearbeiten, aktualisieren und erstellen Sie Berichte zu allen Sprachversionen von einem zentralen Ort aus.
* **Abwärtskompatibilität**: Vorhandene Einzelsprachauftragshilfen werden automatisch in allen hinzugefügten Sprachen repliziert, bis neue Dateien hochgeladen werden.

### Erstellen einer mehrsprachigen Arbeitshilfe

1. Wechseln Sie zur Autorenrolle und wählen Sie **Arbeitshilfen** aus.
2. Wählen Sie **Arbeitshilfe erstellen**.
3. Geben Sie den Namen und die Beschreibung der Arbeitshilfe in der Standardsprache ein.
4. Fügen Sie die primäre Inhaltsdatei oder URL für die Standardsprache hinzu.
5. Speichern Sie die Arbeitshilfe.

### Zusätzliche Sprachen hinzufügen

1. Wählen Sie im Arbeitshilfeeditor die Option **Sprache hinzufügen**.
2. Wählen Sie die gewünschte(n) Sprache(n) aus der Liste aus.
3. Für jede hinzugefügte Sprache:
   * Geben Sie den lokalisierten Namen und die Beschreibung ein.
   * Laden Sie die entsprechende Inhaltsdatei hoch oder geben Sie eine sprachspezifische URL an.
4. Wiederholen Sie diesen Vorgang für alle erforderlichen Sprachen.

### Bearbeiten und Verwalten von Sprachen

1. Um eine Datei oder eine Beschreibung für eine bestimmte Sprache zu aktualisieren, wählen Sie die Registerkarte &quot;Sprache&quot; aus und nehmen Sie die erforderlichen Änderungen vor.
2. Wenn eine Sprache nach Veröffentlichung der Arbeitshilfe hinzugefügt wird, wird die Originaldatei automatisch der neuen Sprache zugewiesen, bis eine eindeutige Datei hochgeladen wird.
3. Entfernen oder ersetzen Sie Dateien für jede beliebige Sprache nach Bedarf.

### Publish und Teilnehmererlebnis

1. Nachdem alle Sprachen und Dateien hinzugefügt wurden, veröffentlichen Sie die Arbeitshilfe.
2. Die Teilnehmer sehen die Arbeitshilfe in ihrer ausgewählten Inhaltssprache mit der entsprechenden Datei oder URL.
3. Wenn die Sprache eines Teilnehmers nicht verfügbar ist, wird die Standardsprachdatei angezeigt.

### Berichte

1. Laden Sie Arbeitshilfeberichte herunter, um Details zu allen Dateien und Sprachen anzuzeigen, die mit den einzelnen Arbeitshilfen verknüpft sind.
2. Berichte enthalten Sprache, Dateinamen und Nutzungsdaten für die Nachverfolgung.

### Best Practices

* Präzise Übersetzung von Namen, Beschreibungen und Inhaltsdateien.
* Überprüfe und aktualisiere Dateien regelmäßig, um die sprachübergreifende Konsistenz sicherzustellen.
* Verwenden Sie klare Benennungskonventionen, um Dateien für verschiedene Sprachen zu unterscheiden.
* Testen Sie die Lernerfahrung der Teilnehmer, indem Sie die Inhaltssprachen wechseln, um die richtige Dateibereitstellung zu überprüfen.

### Fehlerbehebung

* **Fehlende Datei für eine Sprache**: Die Standarddatei wird angezeigt. Stellen Sie sicher, dass in allen Sprachen die richtige Datei hochgeladen wurde.
* **Ältere Arbeitshilfen**: Fügen Sie neue Sprachdateien hinzu, um automatisch replizierte Originale zu ersetzen.
* **Falsche angezeigte Sprache**: Überprüfen Sie die Spracheinstellungen des Teilnehmers für den Inhalt und die Sprachkonfiguration der Arbeitshilfe.

Mithilfe mehrsprachiger Arbeitshilfen können Sie einer globalen Zielgruppe in einem einzigen Eintrag unterstützende Ressourcen zur Verfügung stellen, Doppelarbeit reduzieren und sicherstellen, dass jeder Teilnehmer die richtigen Informationen in der gewünschten Sprache erhält. Diese Funktion verbessert die Barrierefreiheit, Compliance und Verwaltungseffizienz in Adobe Learning Manager.

## Erhalten Sie Antworten mit dem AI Assistant für Teilnehmer

AI Assistant for Learners ist ein gesprächsorientierter, KI-gestützter Assistent in Adobe Learning Manager, der Sie schneller zu den Informationen führt, die Sie benötigen. Wenn du Fragen in natürlicher Sprache stellst, kannst du kontextbezogene Erklärungen abrufen, relevante Kurse anschauen und Einblicke aus Lerninhalten gewinnen - ohne manuell in Katalogen suchen zu müssen.

### Funktionen

* **Intelligente Fragenbeantwortungen:** Behandelt sowohl Gespräche mit einer als auch mit mehreren Umdrehungen, sodass Sie Fragen ganz natürlich stellen können. Antworten werden aus Kursen, Lernpfaden, Zertifizierungen und Arbeitshilfen abgeleitet.
* **Inhaltsbasierte Antworten mit Zitaten:** Ruft Informationen direkt aus Lernmaterialien ab und enthält Zitate, die auf den ursprünglichen Kurs, das Modul oder die ursprüngliche Ressource verweisen.
* **Kompatibilität umfassender Inhalte:** Unterstützt eine Vielzahl von Formaten, einschließlich Dokumenten, Präsentationen, Videos, Audiodateien, HTML-Inhalt und SCORM-Modulen (Sharable Content Object Reference Model).
* **Nahtloses Benutzererlebnis:** Als Seitenbereich über die Teilnehmerseiten hinweg verfügbar, wobei der sitzungsbasierte Chatverlauf für Kontinuität beibehalten wird.
* **Leistungsstarke Administratorsteuerelemente:** Administratoren können den Assistenten aktivieren oder deaktivieren, den Zugriff durch Benutzergruppen einschränken und auswählen, welche internen Kataloge als Quelle für AI-generierte Antworten verwendet werden.

### Vorteile

* **Schnellerer Zugriff auf Wissen:** Sie erhalten sofortige Antworten auf Ihre Fragen, sodass Sie nicht mehr durch mehrere Kurse oder Dokumente navigieren müssen.
* **Höhere Interaktion:** Durch konversationale Interaktionen wird das Lernerlebnis natürlicher, intuitiver und zugänglicher.
* **Besseres Verständnis:** Sie können Folgefragen stellen, um Konzepte zu klären und Themen eingehender zu untersuchen.
* **Skalierbare Lernunterstützung:** Automatisierte, KI-gestützte Antworten minimieren die Abhängigkeit von Fachexperten und Support-Teams.

Weitere Informationen zum [AI Assistant für Teilnehmer](/help/migrated/learners/feature-summary/learner-ai-assistant.md).

## Unterstützung von mehrsprachigen Video-Text-Tracks (VTT)

Die Unterstützung mehrsprachiger Videotextspuren (VTT) in Adobe Learning Manager ermöglicht es Autoren, Untertitel und Untertitel für Video- und Audioinhalte in mehreren Sprachen bereitzustellen. Diese Funktion vereinfacht die Lokalisierung, macht Schulungen für ein weltweites Publikum zugänglich und stellt die Einhaltung von Standards für Barrierefreiheit sicher. Autoren können VTT-Dateien automatisch direkt auf der Plattform generieren, übersetzen, überprüfen und bearbeiten.

### Anwendungsfälle

* **Globale Schulung:** Stellen Sie Videoinhalte mit Untertiteln in mehreren Sprachen bereit, um internationale Teilnehmer zu erreichen.
* **Barrierefreiheitskonformität:** Geben Sie Untertitel für hörgeschädigte Benutzer in ihrer bevorzugten Sprache an.
* **Schnellere Lokalisierung:** Reduzieren Sie den manuellen Aufwand, und beschleunigen Sie die Bereitstellung von Inhalten, indem Sie VTT-Dateien automatisch generieren und übersetzen.
* **Konsistentes Erlebnis:** Stellen Sie sicher, dass alle Teilnehmer unabhängig von der Sprache die gleichen Informationen erhalten.

### Wichtigste Funktionen

* **Mehrsprachige Übersetzung:** Übersetzen Sie Untertitel in eine der 39 unterstützten nicht englischen Sprachen.
* **In-App-Überprüfung und -Bearbeitung:** Überprüfen, bearbeiten und laden Sie VTT-Dateien vor der Veröffentlichung herunter.
* **Benachrichtigungen:** Erhalten Sie In-App-Benachrichtigungen, wenn die VTT-Generierung und -Übersetzung abgeschlossen sind.
* **Nahtlose Veröffentlichung:** Publish hat Untertitel für Teilnehmer fertig gestellt, auf die sie in der von ihnen gewählten Sprache zugreifen können.

### Inhalte hochladen und VTT generieren

1. Wechseln Sie zur Inhaltsbibliothek und wählen Sie **Hinzufügen > Inhalt** aus.
2. Lade eine MP3- oder MP4-Datei hoch.
3. Wählen Sie im Dialogfeld &quot;Hochladen&quot; die Option &quot;**Übersetzungen generieren**&quot;.
4. Wählen Sie die ursprüngliche Inhaltssprache aus (die Standardsprache ist die Sprache der Datei).
5. Wählen Sie weitere Zielsprachen für die Übersetzung aus (bis zu 39 werden unterstützt).
6. Wählen Sie **Speichern**. Das System beginnt mit der Generierung und Übersetzung von VTT-Dateien.

### Status überwachen

1. Nach dem Speichern wird der neue Inhaltseintrag in der Inhaltsbibliothek angezeigt.
2. Eine Fortschrittsanzeige zeigt den Status der VTT-Generierung und -Übersetzung an.
3. Sie erhalten eine In-App-Benachrichtigung, wenn der Vorgang abgeschlossen ist.

### Überprüfen und Bearbeiten von VTT-Dateien

1. Öffnen Sie den Inhalt in der Inhaltsbibliothek im Modus **Bearbeiten**.
2. Wählen Sie für jede Sprache den Link **Überprüfung** neben der VTT-Datei.
3. In einem Popupfenster werden die Untertitel für diese Sprache angezeigt.
4. Bearbeiten Sie Untertitel direkt im Popup oder laden Sie die VTT-Datei für die Offline-Bearbeitung herunter.
5. Laden Sie nach dem Vornehmen von Änderungen die überarbeiteten Untertitel hoch bzw. fügen Sie sie wieder in das Popup-Fenster ein.
6. Speichern Sie Ihre Änderungen.

### Publish-Untertitel

1. Wenn Sie mit allen Sprachbeschriftungen zufrieden sind, veröffentlichen Sie den Inhalt.
2. Teilnehmer sehen Untertiteloptionen in allen veröffentlichten Sprachen, wenn sie das Video anzeigen.

### Weitere Informationen

* **Unterstützte Sprachen:** Alle 39 nicht englischsprachigen Sprachen, die von Adobe Learning Manager unterstützt werden.
* **Benachrichtigungen:** Autoren werden benachrichtigt, wenn die VTT-Generierung und -Übersetzung abgeschlossen sind.
* **Bearbeitungsflexibilität:** Beschriftungen können in der App oder offline bearbeitet und erneut hochgeladen werden.
* **Skalierbarkeit:** Konzipiert für Lokalisierungs- und Barrierefreiheitsanforderungen in Unternehmen.
* **Manueller VTT-Upload nicht erforderlich:** Das System kann VTT-Dateien mithilfe des hochgeladenen Videos/Audios von Grund auf neu generieren.

### Best Practices

* Überprüfen Sie automatisch generierte Untertitel vor der Veröffentlichung immer auf ihre Genauigkeit.
* Stellen Sie Übersetzungen für alle wichtigen Teilnehmergruppen bereit, um die Zugänglichkeit zu maximieren.
* Verwenden Sie das Benachrichtigungssystem, um über den Verarbeitungsstatus auf dem Laufenden zu bleiben.
* Aktualisieren Sie regelmäßig die Untertitel, wenn sich der Videoinhalt ändert.

### Fehlerbehebung

* Wenn die VTT-Generierung fehlschlägt, stellen Sie sicher, dass Ihre Datei in einem unterstützten Format (MP3/MP4) vorliegt.
* Überprüfen Sie bei fehlenden Sprachen, ob sie während des Uploads unterstützt und ausgewählt werden.
* Wenn Untertitel nicht synchron sind, können Sie das Timing mit dem In-App-Editor anpassen.

Die mehrsprachige VTT-Unterstützung ermöglicht es Ihnen, barrierefreie, lokalisierte Video-Lernerlebnisse effizient bereitzustellen. Durch die automatische Generierung, Übersetzung und In-App-Bearbeitung können Sie sicherstellen, dass Ihre Inhalte alle Teilnehmer unabhängig von der Sprache erreichen und unterstützen.

## Benutzerdefinierte Zertifikate entwerfen

Mit benutzerdefinierten Zertifikaten in Adobe Learning Manager (ALM) können Administratoren und Autoren personalisierte Zertifikate für Teilnehmer entwerfen, verwalten und ausstellen. Die Funktion umfasst einen Drag-and-Drop-Editor, dynamische Felder, mehrsprachigen Support und KI-generierte Hintergründe, sodass Unternehmen Branding-Zertifikate ohne technische Kenntnisse erstellen können.

### Vorheriges Verhalten

Früher war die Zertifikaterstellung in ALM durch starre Vorlagen, fehlende Anpassung und technische Barrieren (wie z. B. die Bearbeitung von HTML) eingeschränkt. Kunden forderten einfachere Möglichkeiten zum Entwerfen von Zertifikaten, zum Hinzufügen dynamischer Felder (z. B. Name des Teilnehmers oder Kursleiter) und zur Unterstützung mehrerer Sprachen, wobei die Markenkonsistenz und das optische Erscheinungsbild erhalten blieben.

### Anwendungsszenarien

* **Markenerkennung**: Stellen Sie Zertifikate mit Firmenlogos, -farben und -schriften aus, um Compliance, Schulung oder Leistung zu gewährleisten.
* **Dynamische Personalisierung**: Automatisches Ausfüllen von Teilnehmernamen, Kursleiternamen und anderen aktiven Feldern.
* **Mehrsprachige Bereitstellung**: Stellen Sie für globale Teilnehmer Zertifikate in mehreren Sprachen bereit.
* **Flexibles Design**: Erstellen Sie Quer- oder Hochformat-Zertifikate, verwenden Sie KI-generierte Hintergründe und zeigen Sie eine Vorschau vor der Veröffentlichung an.

### Auf benutzerdefinierte Zertifikate zugreifen

1. Wechseln Sie zum Abschnitt **Erfolge** auf der Startseite des Administrators (zuvor **Abzeichen** genannt).
2. Wählen Sie **Zertifikate** aus, um Zertifikatvorlagen anzuzeigen, zu erstellen oder zu verwalten.

### Zertifikat erstellen

1. Wählen Sie **Zertifikat erstellen** aus.
2. Wählen Sie die Hoch- oder Querformat-Ausrichtung.
3. Wählen Sie eine vorhandene Vorlage aus oder beginnen Sie mit einer leeren Arbeitsfläche.
4. Geben Sie einen Zertifikatsnamen und die Standardsprache ein.
5. Fügen Sie mithilfe des Drag-and-Drop-Editors Folgendes hinzu:
   * Textfelder (mit Schrift-, Farb- und Positionierungsoptionen)
   * Bilder (Logos, Symbole usw.)
   * Dynamische Felder (Name des Teilnehmers, Name des Kursleiters usw.)
   * Zertifikatshintergründe (einfarbig, hochgeladenes Bild oder AI-generiertes Bild)
6. Bei KI-generierten Hintergründen: Geben Sie eine Eingabeaufforderung ein (z. B. &quot;Schüler, Studierende und Azubis&quot;), um mithilfe von KI Hintergründe zu generieren.

### Dynamische Felder hinzufügen

Dynamische Felder in benutzerdefinierten Adobe Learning Manager-Zertifikaten sind Platzhalter, die automatisch relevante Informationen wie den Namen des Teilnehmers, den Namen des Kursleiters oder andere kontenspezifische Daten einfügen, wenn das Zertifikat generiert wird. Dies ermöglicht personalisierte und kontextabhängige Zertifikate ohne manuelle Bearbeitung.

1. Fügen Sie dynamische Variablen wie den Namen des Teilnehmers, den Namen des Kursleiters oder andere aktive Felder ein.
2. Felder werden automatisch ausgefüllt, wenn das Zertifikat ausgestellt wird.

### Mehrsprachige Unterstützung

1. Fügen Sie dem Zertifikat neue Sprachen (z. B. Französisch, Deutsch) hinzu.
2. Geben Sie den übersetzten Text für jede Sprache ein.
3. Übersetzungen verwalten und Zertifikate in jeder Sprache in der Vorschau anzeigen.

### Vorschau anzeigen und veröffentlichen

1. Verwenden Sie die Vorschaufunktion, um zu sehen, wie das Zertifikat den Teilnehmern angezeigt wird.
2. Vorschau herunterladen oder drucken.
3. Speichere deinen Entwurf für die spätere Bearbeitung, oder veröffentliche ihn, sobald er fertig ist.

### Zertifikate anwenden

1. Administratoren können Standardzertifikate für das Konto festlegen.
2. Autoren können Zertifikate an bestimmte Lernobjektinstanzen (Kurse, Pfade usw.) anhängen.
3. Wählen Sie je nach Bedarf andere Zertifikate auf Instanzebene aus.

### Zertifikate verwalten

1. Veröffentlichte Zertifikate und Entwurfszertifikate in der Bibliothek anzeigen
2. Bearbeiten, aktualisieren oder löschen Sie Vorlagen nach Bedarf.
3. Zertifikate können über mehrere Instanzen hinweg wiederverwendet werden.

Benutzerdefinierte Zertifikate in ALM bieten eine flexible Möglichkeit, personalisierte, markenspezifische und mehrsprachige Zertifikate zu entwerfen und auszustellen. Die Funktion vereinfacht die Zertifikatverwaltung, verbessert die Anerkennung von Teilnehmern und unterstützt globale Compliance- und Branding-Anforderungen.

## Mehrsprachige Arbeitshilfen

Mithilfe mehrsprachiger Arbeitshilfen in Adobe Learning Manager (ALM) können Autoren und Administratoren unterstützende Dokumente, Hilfslinien oder Ressourcen in mehreren Sprachen in einem einzigen Arbeitshilfeeintrag zur Verfügung stellen. Teilnehmer aus verschiedenen Regionen können auf relevante Materialien in ihrer bevorzugten Sprache zugreifen, was die Barrierefreiheit, Compliance und das Benutzererlebnis verbessert.

### Vorheriges Verhalten

Zuvor war in ALM nur eine Inhaltsdatei pro Arbeitshilfe zulässig, obwohl Name und Beschreibung lokalisiert werden konnten. Um dieselbe Ressource in mehreren Sprachen bereitzustellen, mussten Autoren für jede Sprache separate Arbeitshilfen erstellen. Dies führte zu Doppelarbeit, Verwirrung und einem erhöhten Verwaltungsaufwand. Es gab keine einheitliche Verwaltung mehrsprachiger Ressourcen, was die Konsistenz und Verfolgung der Verwendung erschwerte.

### Anwendungsszenarien

* **Aktivierung für globale Mitarbeiter**: Stellen Sie Sicherheitshandbücher, Prozessleitfäden oder Referenzdokumente in mehreren Sprachen für verschiedene Mitarbeiter bereit.
* **Einhaltung behördlicher Auflagen**: Stellen Sie sicher, dass alle Mitarbeiter die gleiche Dokumentation zur Einhaltung der Vorschriften in ihrer Muttersprache erhalten.
* **Konsistentes Onboarding**: Stellen Sie für Neueinstellungen weltweit Checklisten für das Onboarding oder FAQs in lokalen Sprachen zur Verfügung.
* **Reduzierte Duplizierung**: Verwalten Sie alle Sprachversionen einer Arbeitshilfe in einem einzigen Eintrag, wodurch Aktualisierungen und Berichterstellung vereinfacht werden.

### Erstellen einer mehrsprachigen Arbeitshilfe

1. Wechseln Sie zur Autorenrolle und wählen Sie **Arbeitshilfen** aus.
2. Wählen Sie **Arbeitshilfe erstellen**.
3. Geben Sie den Namen und die Beschreibung der Arbeitshilfe in der Standardsprache ein.
4. Laden Sie die Datei mit dem primären Inhalt hoch oder geben Sie eine URL für die Standardsprache an.
5. Speichern Sie die Arbeitshilfe.

### Zusätzliche Sprachen hinzufügen

1. Wählen Sie im Arbeitshilfeeditor die Option **Sprache hinzufügen**.
2. Wählen Sie die gewünschte(n) Sprache(n) aus der Liste aus.
3. Für jede hinzugefügte Sprache:
   * Geben Sie den lokalisierten Namen und die Beschreibung ein.
   * Laden Sie die entsprechende Inhaltsdatei hoch oder geben Sie eine sprachspezifische URL an.
4. Wiederholen Sie diesen Vorgang für alle erforderlichen Sprachen.

### Bearbeiten und Verwalten von Sprachen

1. Um eine Datei oder eine Beschreibung für eine bestimmte Sprache zu aktualisieren, wählen Sie die Registerkarte &quot;Sprache&quot; aus und nehmen Sie die erforderlichen Änderungen vor.
2. Wenn eine Sprache nach Veröffentlichung der Arbeitshilfe hinzugefügt wird, wird die Originaldatei automatisch der neuen Sprache zugewiesen, bis eine eindeutige Datei hochgeladen wird.
3. Entfernen oder ersetzen Sie Dateien für jede beliebige Sprache nach Bedarf.

### Publish und Teilnehmererlebnis

1. Nachdem alle Sprachen und Dateien hinzugefügt wurden, veröffentlichen Sie die Arbeitshilfe.
2. Die Teilnehmer sehen die Arbeitshilfe in ihrer ausgewählten Inhaltssprache mit der entsprechenden Datei oder URL.
3. Wenn die Sprache eines Teilnehmers nicht verfügbar ist, wird die Standardsprachdatei angezeigt.

### Berichte

1. Laden Sie Arbeitshilfeberichte herunter, um Details zu allen Dateien und Sprachen anzuzeigen, die mit den einzelnen Arbeitshilfen verknüpft sind.
2. Berichte enthalten Sprache, Dateinamen und Nutzungsdaten für die Nachverfolgung.

Mithilfe mehrsprachiger Arbeitshilfen in ALM können Sie einer globalen Zielgruppe in einem einzigen Eintrag unterstützende Ressourcen bereitstellen, Doppelarbeit reduzieren und sicherstellen, dass jeder Teilnehmer die richtigen Informationen in der gewünschten Sprache erhält. Diese Funktion verbessert die Barrierefreiheit, Compliance und Verwaltungseffizienz in Adobe Learning Manager.

## Wiedergabeverbesserungen für Captivate-generierte Kurse

Das Update verbessert das Wiedergabeerlebnis für Adobe Captivate-Inhalte in ALM erheblich, indem eine einheitliche und optimierte Benutzeroberfläche eingeführt wird.

Der ALM-Player zeigt jetzt ein einzelnes, konsolidiertes Inhaltsverzeichnis an, das das Captivate-Inhaltsverzeichnis ausblendet, und bietet klare Abschlussanzeigen auf Folienebene, einschließlich grüner Häkchen für die visuelle Fortschrittsverfolgung.

Das System vereinfacht die Navigation, indem es Modul- und Kurssteuerungen in einer intuitiven Leiste zusammenführt und so die Verwirrung der Teilnehmer verringert.

Kontextsensitive Fortschrittssteuerungen verbessern die Benutzerfreundlichkeit, indem Videofortschrittsleisten nur auf Videofolien und Steuerelemente für die Foliennavigation nur auf Nicht-Videofolien angezeigt werden.

Darüber hinaus verknüpft das System jetzt Notizen mit Foliennummern anstelle von Zeitstempeln, um einen zuverlässigen PDF-Export zu gewährleisten und vorherige Formatinkonsistenzen zu beheben.

## Verbesserungen der Checkliste

### Unterstützung mehrerer Sprachen für Checkliste

Mit dieser Funktion können Sie Checklistenmodule in mehreren Sprachen erstellen und verwalten. Jede Frage, jede Anweisung und jedes Bewertungskriterium der Checkliste kann übersetzt werden, sodass Prüfer und Teilnehmer mit der Checkliste in ihrer bevorzugten Sprache interagieren. Das System zeigt die Checkliste in der vom Benutzer ausgewählten Inhaltssprache an, was die Zugänglichkeit und Compliance für globale Teams verbessert.

1. Fügen Sie in Ihrem Kurs ein Checklistenmodul hinzu oder bearbeiten Sie es.
2. Wählen Sie alle zu unterstützenden Sprachen aus den Sprachoptionen aus.
3. Geben Sie für jede Sprache Übersetzungen für jede Checklistenfrage, jede Anweisung und jedes Bewertungskriterium ein.
4. Speichern Sie Ihre Änderungen. Die Checkliste wird in der vom Reviewer oder Teilnehmer ausgewählten Inhaltssprache angezeigt.
5. Wenn Sie später eine neue Sprache hinzufügen, geben Sie vor der Veröffentlichung Übersetzungen für alle Fragen und Kriterien an.
6. Wählen Sie beim Herunterladen von Checklistenberichten Ihre bevorzugte Sprache aus, um den Bericht in dieser Sprache anzuzeigen.

### Checklistenfragengewichtung für Kursleiterbewertungen

Mit dieser Funktion können Sie jeder Checklistenfrage unterschiedliche Höchstpunktzahlen (Gewichtung) zuweisen. Sie können die unterschiedliche Bedeutung oder Schwierigkeit jeder Frage widerspiegeln, was genauere und aussagekräftigere Bewertungen unterstützt. Das System berechnet die Gesamtpunktzahl basierend auf Ihren Eingaben und bestimmt, ob der Teilnehmer die von Ihnen festgelegten Kriterien besteht oder nicht.

1. Wählen Sie beim Hinzufügen eines Checklistenmoduls **Benutzerdefinierte Bewertung** aus.
2. Legen Sie für jede Checklistenfrage eine eindeutige Höchstpunktzahl fest, die ihre Bedeutung widerspiegelt.
3. Definieren Sie den Gesamtwert zum Bestehen der Checkliste.
4. Speichern und veröffentlichen Sie die Checkliste.
5. Bewerten Sie als Kursleiter oder Reviewer jeden Teilnehmer, indem Sie jeder Frage eine Punktzahl zuweisen (bis zu dem von Ihnen festgelegten Maximum).
6. Das System berechnet die Gesamtpunktzahl und ermittelt den Bestanden-/Nicht-Bestehen-Status.
7. Laden Sie Checklistenberichte herunter, um sowohl die erreichte als auch die maximale Punktzahl für jede Frage und die Gesamtpunktzahl anzuzeigen.

### Checkliste mit Kommentarfunktion für Reviewer

Mit dieser Funktion können Reviewer während der Checklistenauswertung Kommentare oder Feedback hinzufügen. Sie können jedem Teilnehmer ein personalisiertes, verwertbares Feedback geben. Sie können auch Ihren Namen mit Ihren Kommentaren anzeigen, um die Transparenz zu erhöhen. Alle Anmerkungen werden im Transkript des Teilnehmers gespeichert und in die Berichte der Checkliste aufgenommen.

1. Aktivieren Sie beim Einrichten der Checkliste **Anmerkungen des Reviewers**.
2. Aktivieren Sie optional **Reviewernamen für Teilnehmer anzeigen**, wenn Ihr Name mit Ihren Kommentaren angezeigt werden soll.
3. Geben Sie während der Bewertung Kommentare oder Feedback für den Teilnehmer in das Feld mit den bereitgestellten Anmerkungen ein.
4. Wählen Sie aus, ob Ihre Kommentare für den Teilnehmer sichtbar sein sollen.
5. Senden Sie Ihre Bewertung. Wenn diese Option aktiviert ist, sieht der Teilnehmer Ihre Anmerkungen und Ihren Namen neben den Ergebnissen.
6. Alle Kommentare werden im Transkript des Teilnehmers gespeichert und zur späteren Referenz in die Checklistenberichte aufgenommen.

## Erweiterte Suchverbesserungen

Die Suchergebnisse in der erweiterten Suche sind jetzt genauer und relevanter. Genaue Stichwortübereinstimmungen werden bei der inhaltsbezogenen Suche und den Metadaten höher eingestuft, was es den Teilnehmern erleichtert, genau das zu finden, wonach sie suchen.

Teilnehmer können jetzt auch registrierte Lernobjekte in den Suchergebnissen sehen, selbst wenn sie nicht Teil eines barrierefreien Katalogs sind, wodurch sichergestellt wird, dass keine relevanten Inhalte verpasst werden. Darüber hinaus wurde das Ranking der Arbeitshilfen sowohl für die erweiterte Suche als auch für die inhaltsinterne Suche verbessert, sodass die relevantesten Ressourcen schneller angezeigt werden.


## Entsprechungen und Stellvertreter

### Übersicht

In vielen Organisationen stoßen Lernende auf Schulungssituationen, in denen verschiedene Kurse die gleiche Anforderung rechtmäßig erfüllen können, z. B. wenn ein neuer Kurs einen älteren ersetzt, wenn ein umfassenderer Kurs einen kürzeren Kurs abhalten kann oder wenn ein spezieller Ersatzkurs angeboten werden muss.

Mit der Funktion &quot;Alternativer Kurs oder Lernpfad&quot; hat ALM eine formelle Möglichkeit, Folgendes zu sagen:

&quot;Wenn der Teilnehmer diese Schulung abgeschlossen hat, behandeln Sie ihn so, als hätte er die entsprechende Schulungsanforderung erfüllt.&quot;

Die Funktion funktioniert über Kurse und Lernpfade hinweg, stellt sicher, dass nachgelagerte Anforderungen wie Voraussetzungen und Compliance-Regeln eingehalten werden, und tut dies, ohne die Teilnehmer zu zwingen, sich durch redundante Inhalte zu bewegen. Darüber hinaus wird die Genauigkeit der Berichte beibehalten, indem aufgezeichnet wird, was direkt abgeschlossen wurde und was über eine Alternative erfüllt wurde.

Im Kern führt die Funktion das Konzept eines alternativen Abschlusses ein: ein spezieller Abschlussstatus, der automatisch erstellt wird, wenn ein Teilnehmer eine konfigurierte Quellschulung abschließt, die auf eine andere Zielschulung angerechnet wird.

### Äquivalenz und Alternative

Einige Trainingsbeziehungen sind bidirektional, d. h. jeder Kurs kann die Anforderungen des anderen erfüllen. Dies ist im Grunde ein Szenario, bei dem zwei Schulungen als gegenseitig austauschbar behandelt werden. Im Gegensatz dazu erlauben unidirektionale Beziehungen es einem Training, die Anforderungen an ein anderes zu erfüllen, aber nicht umgekehrt. ALM modelliert beide Szenarien mit demselben zugrunde liegenden alternativen*Vervollständigungsmechanismus.

* **Bidirektionale Beziehung:** Das Abschließen einer der Schulungen erfüllt die Anforderungen für die andere.
* **Unidirektionale Beziehung:** Das Abschließen von Schulung A erfüllt Schulung B, aber das Abschließen von B erfüllt A nicht. Dies ist häufig der Fall, wenn eine neuere oder umfassendere Version auf eine ältere Anforderung angerechnet werden sollte, aber nicht umgekehrt.

Alternativen werden am häufigsten in **unidirektionalen** Szenarien verwendet, z. B. wenn ein umfassenderer Superset-Kurs alles in einem einfacheren Unterset-Kurs abdeckt. Das Ausfüllen der Obermenge sollte die Anforderungen für die Untermenge erfüllen, aber nicht unbedingt umgekehrt.

* Ein neuer, erweiterter Kurs, der auf eine ältere Anforderung angerechnet werden sollte.
* Ein Kurs, der für eine bestimmte Zielgruppe entwickelt wurde (z. B. eine regionale oder an die Barrierefreiheit angepasste Variante), der weiterhin die gleiche Anforderung erfüllt wie der Hauptkurs.
* Eine verbesserte neue Version eines Kurses, die das Unternehmen für eine ältere Anforderung berücksichtigen möchte, aber die ältere Version sollte nicht für die neue Anforderung berücksichtigt werden.

Bei Alternativen ist die Beziehung normalerweise **einseitig*Richtung**. Wenn Kurs A ein Alternativkurs zu Kurs B ist, kann Abschluss A die Anforderung von B erfüllen, aber Abschluss B erfüllt nicht unbedingt A.

Sowohl die Äquivalenz als auch die Alternative verwenden denselben zugrunde liegenden Mechanismus in ALM: Wenn eine konfigurierte Quellschulung abgeschlossen ist, erstellt ALM automatisch eine alternative Abschlussfunktion für eine oder mehrere Zielschulungen.

### Welche Probleme werden dadurch gelöst?

Ohne Alternativen und Gleichwertigkeit stehen Administratoren und Teilnehmer vor mehreren wiederkehrenden Problemen:

* Teilnehmer werden häufig aufgefordert, Kurse zu wiederholen, in denen Inhalte behandelt werden, die sie bereits in einer anderen Version oder einem anderen Format abgeschlossen haben.
* Die Aktualisierung von Compliance-Programmen ist einfacher, da Administratoren Schulungen ersetzen oder umstrukturieren können, ohne Teilnehmer, die ältere Versionen abgeschlossen haben, zwingen zu müssen, äquivalente oder ersetzte Inhalte erneut zu übernehmen.
* Die erforderliche Logik ist starr. Wenn ein Weg einen bestimmten Kurs als Voraussetzung erfordert, gibt es keine klare Möglichkeit zu erkennen, dass eine andere Schulung gut genug ist.
* Berichterstattung und Prüfungen sind schwieriger. Es gibt kein förmliches Signal dafür, dass eine Anforderung durch einen alternativen Abschluss erfüllt wurde, und es gibt keine einfache Möglichkeit, die Quelle des Kredits zu ermitteln.

Die Funktion &quot;Alternativen und Äquivalenz&quot; behebt diese Probleme wie folgt:

* Vermeidung doppelter Anstrengungen für Teilnehmer, wenn Alternativen gültig sind.
* Administratoren können Schulungsstrukturen ändern (z. B. einen Kurs innerhalb eines Pfads austauschen), ohne die Abschlüsse von Teilnehmern zu brechen, die die frühere Version verwendet haben.
* Zulassen von Voraussetzungen und Konformitätsprüfungen, um sowohl direkte als auch alternative oder gleichwertige Abschlüsse zu berücksichtigen.
* Klarere Aufzeichnung in Transkripten und Berichten, ob eine Schulung direkt abgeschlossen oder über eine alternative Beziehung abgeschlossen wurde, zusammen mit der Schulung als Quelle.

### Konzeptionelle Funktionsweise der Funktion

Die Funktion basiert auf drei Hauptideen: **Beziehungen**, **Alternativer Abschluss** und **Downstream-Verhalten**.

#### Beziehungen zwischen Schulungen

Administratoren definieren die Beziehungen zwischen Kursen und Lernpfaden. Für jede Beziehung wählen sie eine **Quelle** und ein oder mehrere **Ziele**. Ein einzelner Kurs kann bis zu 30 Ziele haben, je nachdem, wie viele frühere oder zugehörige Schulungen er erfüllen sollte.

Bei der Entsprechung können Administratoren die Beziehung **bidirektional** erstellen, wenn sie möchten, dass beide Schulungen einander entsprechen. Bei &quot;Alternativen&quot; behalten Administratoren die Richtung in der Regel einseitig, um anzugeben, dass nur einige Ersetzungen zulässig sind.

Diese Beziehungen werden auf der Schulungsebene gespeichert, nicht auf der Teilnehmerebene. Nach der Konfiguration und Aktivierung gelten sie für alle aktuellen und zukünftigen Abschlüsse der Quellschulung, abhängig von Einstellungen auf Konto*-Ebene, z. B. ob der retroaktive Abschluss aktiviert ist.

### Alternativer Abschluss

Wenn ein Teilnehmer eine Quellschulung abschließt, überprüft ALM alle konfigurierten alternativen oder äquivalenten Beziehungen und erstellt für jede relevante Zielschulung einen **alternativen Abschlussdatensatz**. Dieser Datensatz unterscheidet sich von einem normalen Abschluss:

* Es markiert die Zielschulung für den Teilnehmer, behält aber den Überblick, dass die Schulung über eine alternative Schulung oder eine Äquivalenz abgeschlossen wurde und nicht direkt.
* Er zeichnet auf, welche Quellschulung verwendet wurde, um das Ziel zu erreichen.
* Es wird in einer speziellen Struktur gespeichert, sodass Berichte zwischen direkten und alternativen Abschlüssen unterscheiden können.

Teilnehmer sehen einen alternativen Abschluss, auch wenn sie nicht registriert sind. Der Bericht &quot;Teilnehmertranskript (LT)&quot; enthält nur Datensätze von Schulungen, für die sich der Teilnehmer registriert hat.

### Teilnehmer-App-Erlebnis für alternative und gleichwertige Abschlüsse

Alternative und gleichwertige Abschlüsse werden in der Teilnehmer-App deutlich angezeigt, sodass die Teilnehmer klar verstehen können, wie eine Schulungsanforderung erfüllt wurde, und gleichzeitig die Konsistenz mit Transkripten und Berichten gewahrt bleibt.

#### LO-Kartenverhalten

#### Alternativer Abschlussstatus

Wenn ein Teilnehmer eine Schulung über eine alternative oder gleichwertige Beziehung abschließt, zeigt die Lernobjektkarte (LO) einen eindeutigen Status an, z. B. **Abgeschlossen über Alternative**.\
Diese visuelle Unterscheidung hilft Teilnehmern dabei, zwischen direkten Abschlüssen und Abschlüssen zu unterscheiden, die durch konfigurierte Beziehungen gewährt werden.

#### Abschlussmethodenindikator

Die LO-Karte enthält einen Indikator für die Abschlussmethode (z. B. eine Beschriftung oder ein Symbol), um anzuzeigen, dass der Abschluss über ein **Alternate** erreicht wurde.\
Wenn ein alternativer Abschluss später widerrufen wird, weil Änderungen vorgenommen wurden, z. B. der Abschluss rückwirkend nicht abgeschlossen oder die Quellschulung gelöscht wurde, wird die LO-Karte aktualisiert, um **Alternate (Revoked)** anzuzeigen.

#### Transparenz und Audit-Details

Teilnehmer können die LO-Karte öffnen, um zusätzliche Details anzuzeigen, darunter:

* Der Quellkurs oder Lernpfad, der den alternativen Abschluss gewährte
* Das mit der Quellschulung verknüpfte Abschlussdatum

Dies gewährleistet Transparenz und unterstützt Audit- und Compliance-Prüfungen.

#### Filtern und Ansichten

#### Vervollständigungsmethodenfilter

Die Teilnehmer-App bietet einen Filter, mit dem Teilnehmer zwischen folgenden Optionen unterscheiden können:

* **Direkte** Abschlüsse
* **Alternative** Abschlüsse
* **Alle** Abschlüsse

Dadurch können die Teilnehmer schnell nachvollziehen, wie ihre Lernanforderungen erfüllt wurden.

#### Transkript- und Fortschrittsansichten

Der Filter für die Abschlussmethode ist in den Ansichten mit Teilnehmer*innen verfügbar, z. B.:

* Teilnehmertranskripte
* Verfolgungsabschnitte für Fortschritt und Abschluss

Aus diesen Ansichten geht eindeutig hervor, welche Schulungen direkt abgeschlossen wurden und welche durch Stellvertreter oder Äquivalenz absolviert wurden.

#### Berichtsausrichtung

Die Filterlogik in der Teilnehmer-App entspricht der Spalte **Abschlussmethode**, die in Berichten verwendet wird.\
Dies stellt sicher, dass die Konsistenz zwischen dem, was die Teilnehmer in der Benutzeroberfläche sehen, und dem, was Administratoren in Exporten und Konformitätsberichten sehen, gewährleistet ist.

#### End *to* end flow

#### Für Teilnehmer

1. Navigieren Sie in der Teilnehmer-App zu **Eigenes Lernen** oder **Abgeschlossene Kurse**.
2. Überprüfen Sie LO-Karten, um Schulungen zu identifizieren, die als **Abgeschlossen über Alternate** markiert sind.
3. Öffnen Sie eine LO-Karte, um Details zur Quellschulung und zum Abschlussdatum anzuzeigen.
4. Verwenden Sie das Filtermenü in der Transkript- oder Kurslistenansicht, um **Direct**, **Alternate** oder **All** auszuwählen.
5. Überprüfen Sie die aktualisierte Liste basierend auf der ausgewählten Abschlussmethode.

#### Für Administratoren und Autoren

1. Konfigurieren Sie äquivalente oder alternative Beziehungen zwischen Kursen oder Lernpfaden in der Administratoroberfläche.
2. Stellen Sie sicher, dass alternative Abschlüsse auf LO-Karten und in den Filtern für Teilnehmer* korrekt widergespiegelt werden.
3. Verwenden Sie Teilnehmeransichten und Berichte, um die Konsistenz zwischen der Benutzeroberfläche und den exportierten Daten zu bestätigen.
4. Wenn eine Quellschulung eingestellt oder gelöscht wird, überprüfen Sie, ob die betroffenen LO-Karten entsprechend aktualisiert wurden (z. B. wird **Alternate (Revoked)** angezeigt, falls zutreffend).

## Verhalten für rückwirkende Vervollständigung und Unvollständigkeit

ALM unterstützt die retroaktive Vervollständigung und die retroaktive Unvollständigkeit, um sicherzustellen, dass alternative und äquivalente Beziehungen im Zeitverlauf präzise bleiben, auch wenn Beziehungen erstellt, geändert oder entfernt werden, nachdem die Teilnehmer die Schulung bereits abgeschlossen haben.

### Rückwirkende Fertigstellung

#### Definition

Wenn der retroaktive Abschluss aktiviert ist, erhalten Teilnehmer, die einen Quellkurs in der Vergangenheit abgeschlossen haben, automatisch einen alternativen Abschluss für den Zielkurs, wenn später eine entsprechende oder alternative Beziehung erstellt wird.\
Dadurch wird sichergestellt, dass das historische Lernen berücksichtigt wird, ohne dass die Teilnehmer eine Schulung erneut absolvieren müssen.

#### Funktionsweise

1. Ein Administrator aktiviert die retroaktive Vervollständigung auf Kontoebene.
2. Der Administrator definiert eine äquivalente oder alternative Beziehung zwischen einer Quell- und einer Zielschulung.
3. Das System scannt die historischen Abschlussdatensätze für die Quellschulung.
4. Berechtigte Teilnehmer erhalten einen alternativen Abschluss für die Zielschulung.
5. Diese Datensätze werden in Teilnehmertranskripten und Berichten als **Abgeschlossen über Alternate** angezeigt.

### Rückwirkende Unvollständigkeit

#### Definition

Wenn die retroaktive Unvollständigkeit aktiviert ist, werden alternative Abschlüsse widerrufen, wenn die zugrunde liegende Äquivalent- oder alternative Beziehung entfernt wird oder wenn die Quellschulung gelöscht wird.\
Dadurch wird sichergestellt, dass das System die aktuellen und gültigen Schulungsverhältnisse widerspiegelt.

#### Funktionsweise

1. Ein Administrator aktiviert die rückwirkende Unvollständigkeit auf Kontoebene.
2. Der Administrator entfernt eine alternative oder gleichwertige Beziehung oder löscht die Quellschulung.
3. Das System identifiziert Teilnehmer, die über die betroffene Beziehung einen alternativen Abschluss erhalten haben.
4. Die entsprechenden alternativen Abschlussdatensätze werden widerrufen.
5. Widerrufene Datensätze werden in Transkripten und Berichten zur Audit-Sichtbarkeit als **Alternate (Widerrufen)** markiert.

### Auswirkungen auf Voraussetzungen

Alternative Abschlüsse - auch rückwirkend gewährte - werden bei der Bewertung von Voraussetzungen als gültige Abschlüsse behandelt.\
Wenn ein Teilnehmer **Abgeschlossen über Alternate** hat, kann er mit Kursen fortfahren, die die Zielschulung erfordern.

Wenn ein alternativer Abschluss später durch eine retroaktive Unvollständigkeit widerrufen wird, verliert der Teilnehmer möglicherweise die Berechtigung für Kurse, die von dieser Voraussetzung abhängen.

### Auswirkungen auf Lernpfade und Zertifizierungen

Alternative Abschlüsse tragen zum Fortschritt und zum Abschluss von Lernpfaden und Zertifizierungen bei.\
Die Teilnehmer können diese Programme erweitern oder abschließen, wenn die erforderlichen Schulungen über alternative oder gleichwertige Beziehungen absolviert werden.

Wenn ein alternativer Abschluss widerrufen wird, verlieren die betroffenen Lernpfade oder Zertifizierungen möglicherweise den Fortschritt oder den Abschlussstatus, bis die Anforderung durch einen gültigen Abschluss erfüllt wird.

### End *to* End-Workflow

#### Aktivieren der retroaktiven Vervollständigung oder Unvollständigkeit

1. Administratoren navigieren zu den Kontoeinstellungen und aktivieren die rückwirkende Fertigstellung und/oder die rückwirkende Nicht-Fertigstellung.
2. Administratoren erstellen, ändern oder entfernen äquivalente oder alternative Beziehungen zwischen Schulungen.

#### Systemaktionen

* **Für den rückwirkenden Abschluss:**\
  Das System gewährt alternative Abschlüsse auf der Grundlage historischer Quellenabschlüsse.
* **Für rückwirkende Unvollständigkeit:**\
  Das System widerruft alternative Abschlüsse, wenn Beziehungen entfernt oder Quelltrainings gelöscht werden.

#### Teilnehmererlebnis

Teilnehmer sehen aktualisierte Abschlussstatus auf LO-Karten und in Transkripten, z. B.:

* **Abgeschlossen über Alternative**
* **Alternate (widerrufen)**

Voraussetzungsprüfungen, der Fortschritt des Lernpfads und der Zertifizierungsstatus werden basierend auf dem aktuellen Abschlussstatus dynamisch aktualisiert.

#### Berichterstattung und Prüfung

Alle rückwirkenden Änderungen werden im Bericht &quot;Teilnehmertranskript (LT)&quot; widergespiegelt.\
In den Berichten wird eindeutig unterschieden zwischen direkten und alternativen Abschlüssen und widerrufenen alternativen Abschlüssen, um die Einhaltung der Vorschriften zu unterstützen, Untersuchungen zu unterstützen und Audits durchzuführen.

### Verhalten für rückwirkende Vervollständigung und Unvollständigkeit

ALM unterstützt die retroaktive Vervollständigung und die retroaktive Unvollständigkeit, um sicherzustellen, dass alternative und äquivalente Beziehungen im Zeitverlauf präzise bleiben, auch wenn Beziehungen erstellt, geändert oder entfernt werden, nachdem die Teilnehmer die Schulung bereits abgeschlossen haben.

#### Rückwirkende Fertigstellung

#### Definition

Wenn der retroaktive Abschluss aktiviert ist, erhalten Teilnehmer, die einen Quellkurs in der Vergangenheit abgeschlossen haben, automatisch einen alternativen Abschluss für den Zielkurs, wenn später eine entsprechende oder alternative Beziehung erstellt wird.\
Dadurch wird sichergestellt, dass das historische Lernen berücksichtigt wird, ohne dass die Teilnehmer eine Schulung erneut absolvieren müssen.

#### Funktionsweise

1. Ein Administrator aktiviert die retroaktive Vervollständigung auf Kontoebene.
2. Der Administrator definiert eine äquivalente oder alternative Beziehung zwischen einer Quell- und einer Zielschulung.
3. Das System scannt die historischen Abschlussdatensätze für die Quellschulung.
4. Berechtigte Teilnehmer erhalten einen alternativen Abschluss für die Zielschulung.
5. Diese Datensätze werden in Teilnehmertranskripten und Berichten als **Abgeschlossen über Alternate** angezeigt.

#### Rückwirkende Unvollständigkeit

#### Definition

Wenn die retroaktive Unvollständigkeit aktiviert ist, werden alternative Abschlüsse widerrufen, wenn die zugrunde liegende Äquivalent- oder alternative Beziehung entfernt wird oder wenn die Quellschulung gelöscht wird.\
Dadurch wird sichergestellt, dass das System die aktuellen und gültigen Schulungsverhältnisse widerspiegelt.

#### Funktionsweise

1. Ein Administrator aktiviert die rückwirkende Unvollständigkeit auf Kontoebene.
2. Der Administrator entfernt eine alternative oder gleichwertige Beziehung oder löscht die Quellschulung.
3. Das System identifiziert Teilnehmer, die über die betroffene Beziehung einen alternativen Abschluss erhalten haben.
4. Die entsprechenden alternativen Abschlussdatensätze werden widerrufen.
5. Widerrufene Datensätze werden in Transkripten und Berichten zur Audit-Sichtbarkeit als **Alternate (Widerrufen)** markiert.

#### Auswirkungen auf Voraussetzungen

Alternative Abschlüsse - auch rückwirkend gewährte - werden bei der Bewertung von Voraussetzungen als gültige Abschlüsse behandelt.\
Wenn ein Teilnehmer **Abgeschlossen über Alternate** hat, kann er mit Kursen fortfahren, die die Zielschulung erfordern.

Wenn ein alternativer Abschluss später durch eine retroaktive Unvollständigkeit widerrufen wird, verliert der Teilnehmer möglicherweise die Berechtigung für Kurse, die von dieser Voraussetzung abhängen.

#### Auswirkungen auf Lernpfade und Zertifizierungen

Alternative Abschlüsse tragen zum Fortschritt und zum Abschluss von Lernpfaden und Zertifizierungen bei.\
Die Teilnehmer können diese Programme erweitern oder abschließen, wenn die erforderlichen Schulungen über alternative oder gleichwertige Beziehungen absolviert werden.

Wenn ein alternativer Abschluss widerrufen wird, verlieren die betroffenen Lernpfade oder Zertifizierungen möglicherweise den Fortschritt oder den Abschlussstatus, bis die Anforderung durch einen gültigen Abschluss erfüllt wird.

#### End *to* End-Workflow

#### Aktivieren der retroaktiven Vervollständigung oder Unvollständigkeit

1. Administratoren navigieren zu den Kontoeinstellungen und aktivieren die rückwirkende Fertigstellung und/oder die rückwirkende Nicht-Fertigstellung.
2. Administratoren erstellen, ändern oder entfernen äquivalente oder alternative Beziehungen zwischen Schulungen.

#### Systemaktionen

* **Für den rückwirkenden Abschluss:**\
  Das System gewährt alternative Abschlüsse auf der Grundlage historischer Quellenabschlüsse.
* **Für rückwirkende Unvollständigkeit:**\
  Das System widerruft alternative Abschlüsse, wenn Beziehungen entfernt oder Quelltrainings gelöscht werden.

#### Teilnehmererlebnis

Teilnehmer sehen aktualisierte Abschlussstatus auf LO-Karten und in Transkripten, z. B.:

* **Abgeschlossen über Alternative**
* **Alternate (widerrufen)**

Voraussetzungsprüfungen, der Fortschritt des Lernpfads und der Zertifizierungsstatus werden basierend auf dem aktuellen Abschlussstatus dynamisch aktualisiert.

#### Berichterstattung und Prüfung

Alle rückwirkenden Änderungen werden im Bericht &quot;Teilnehmertranskript (LT)&quot; widergespiegelt.\
In den Berichten wird eindeutig unterschieden zwischen direkten und alternativen Abschlüssen und widerrufenen alternativen Abschlüssen, um die Einhaltung der Vorschriften zu unterstützen, Untersuchungen zu unterstützen und Audits durchzuführen.

### Webhooks für Äquivalente und Stellvertreter

ALM stellt dedizierte Webhook-Ereignisse für gleichwertige und alternative Abschlüsse bereit, um Automatisierung, Integrationen und Synchronisierung mit externen Systemen zu unterstützen.

Diese Ereignisse ermöglichen es externen Verbrauchern, zuverlässig zwischen direkten Abschlüssen und Abschlüssen zu unterscheiden, die durch alternative oder gleichwertige Beziehungen gewährt werden.

#### Übersicht

Wenn ein Teilnehmer einen Kurs über eine alternative oder gleichwertige Beziehung abschließt, löst ALM ein Webhook-Ereignis aus, das vom standardmäßigen Webhook für den Kursabschluss getrennt ist.\
Dadurch wird sichergestellt, dass Integrationen bei Bedarf unterschiedlich auf alternative Abschlüsse reagieren können.

Webhook-Ereignisse werden auch ausgelöst, wenn eine rückwirkende Fertigstellung oder eine rückwirkende Unvollständigkeit erfolgt, die historische Aktualisierungen sowie Beziehungsänderungen abdeckt.

#### Webhook-Ereignisverhalten

* Ein eindeutiges Webhook-Ereignis wird ausgelöst, wenn ein Teilnehmer für einen Zielkurs den Status **Abgeschlossen über Alternative** erhält.
* Das Ereignis wird generiert, wenn der Teilnehmer einen konfigurierten Quellkurs abschließt, der dem Ziel durch eine entsprechende oder alternative Beziehung entspricht.
* Dieser Webhook wird nicht für direkte Kursabschlüsse ausgelöst.
* Wenn der retroaktive Abschluss oder die retroaktive Unvollständigkeit aktiviert ist, werden Webhook-Ereignisse für jeden betroffenen Teilnehmer und jeden Zielkurs ausgegeben.

#### Webhook-Nutzlastdetails

Die Webhook-Nutzlast mit alternativem Abschluss umfasst die folgenden Schlüsselattribute:

* **Teilnehmer-ID**\
  Identifiziert den Teilnehmer, der den alternativen Abschluss erhalten hat.

* **Quellkurs**\
  Der Kurs oder Lernpfad, den der Teilnehmer direkt abgeschlossen hat.

* **Zielkurs**\
  Der Kurs, der über die alternative oder gleichwertige Beziehung als abgeschlossen markiert ist.

* **Abschlussmethode**\
  Gibt an, dass die Abschlussmethode **alternativ** ist.

* **Abschlussdatum**\
  Abgeleitet vom Abschlussdatum des Quellkurses.

* **Beziehungstyp**\
  Gibt an, ob die Beziehung **äquivalent** oder **alternativ** ist.

Bei Szenarien mit rückwirkender Nicht-Fertigstellung zeigen Webhook-Ereignisse an, dass eine vorhandene alternative Fertigstellung widerrufen wurde.

#### Überlegungen zur Integration

Externe Systeme können die folgenden Webhook-Ereignisse verwenden, um:

* Teilnehmerdatensätze aktualisieren
* Abschlussstatus synchronisieren
* Auslösen von Benachrichtigungen oder nachgeschalteten Workflows
* Audit-Verläufe für Compliance-Zwecke verwalten

Webhook-Verbraucher sollten explizit zwischen **direkten** und **alternativen** Abschlüssen unterscheiden.\
Alternative Abschlüsse gewähren keine Qualifikationen, Abzeichen oder Gamification-Prämien und sollten in nachgelagerten Systemen entsprechend gehandhabt werden.

### Auswirkungen des Ausscheidens und Löschens von Schulungen in Äquivalenten und Alternativprogrammen

Der Lebenszyklusstatus einer Quellschulung (eingestellt oder gelöscht) wirkt sich direkt darauf aus, wie alternative und gleichwertige Abschlüsse für Teilnehmer beibehalten werden. ALM behandelt diese Szenarien unterschiedlich, um die historische Genauigkeit zu erhalten und gleichzeitig sicherzustellen, dass die aktuellen Beziehungen gültig bleiben.

#### Ausscheiden aus dem Berufsleben

##### Definition

Durch das Einstellen eines Kurses ist dieser für neue Registrierungen nicht mehr verfügbar, während er im System zur historischen Referenz, zur Berichterstellung und zu Prüfzwecken gespeichert wird.

##### Auswirkungen

* Vorhandene alternative Abschlüsse, die über den eingestellten Quellkurs gewährt wurden, bleiben gültig.
* Teilnehmer, die den Quellkurs zuvor abgeschlossen haben, haben weiterhin einen alternativen Abschluss für den Zielkurs.
* Es werden keine neuen alternativen Abschlüsse aus dem eingestellten Kurs generiert, da er von neuen Teilnehmern nicht abgeschlossen werden kann.
* Teilnehmertranskripte und Berichte zeigen weiterhin **Abgeschlossen über Alternate** für betroffene Teilnehmer an.

#### Löschen der Quellschulung

#### Definition

Wenn Sie einen Kurs löschen, wird er vollständig aus dem System entfernt, einschließlich der Abschlussdatensätze und der konfigurierten Beziehungen.

#### Auswirkungen

* Wenn die retroaktive Unvollständigkeit aktiviert ist, werden alle alternativen Abschlüsse, die über den gelöschten Quellkurs gewährt wurden, widerrufen.
* Teilnehmertranskripte und Berichte werden aktualisiert, um **Alternate (Revoked)** für Audit- und Compliance-Sichtbarkeit anzuzeigen.
* Teilnehmer verlieren möglicherweise den Fortschritt oder den Abschlussstatus in Lernpfaden, Zertifizierungen oder Voraussetzungen, die von der widerrufenen alternativen Fertigstellung abhängen.
* Es können keine weiteren alternativen Abschlüsse aus dem gelöschten Kurs gewährt werden.

#### Workflow

1. Ein Administrator beendet den Quellkurs oder löscht ihn über die Administratoroberfläche.
2. Das System bewertet alle alternativen und äquivalenten Abschlüsse, die vom Quellkurs abgeleitet werden.
3. Der Abschlussstatus wird basierend auf dem Kursstatus aktualisiert:
   * **Eingestellt:** Bestehende alternative Abschlüsse bleiben unverändert.
   * **Gelöscht:** Alternative Abschlüsse werden widerrufen, wenn rückwirkende Unvollständigkeit aktiviert ist.
4. Teilnehmertranskripte und -berichte spiegeln den aktualisierten Status wider, um Compliance- und Audit-Anforderungen zu unterstützen.

### Keine Verkettung von Beziehungen

ALM unterstützt keine Verkettung alternativer oder gleichwertiger Beziehungen. Alternative Abschlüsse werden nur für direkt konfigurierte Beziehungen gewährt und werden nicht auf mehrere Kursebenen übertragen.

#### Konzept: keine Verkettung von Beziehungen

#### Definition

Verkettung bezieht sich darauf, dass alternative oder gleichwertige Beziehungen über mehrere Kurse verteilt werden können.\
Wenn beispielsweise Kurs A ein Alternativkurs zu Kurs B und Kurs B ein Alternativkurs zu Kurs C ist, würde die Verkettung bedeuten, dass durch Abschluss von Kurs A der Abschluss für Kurs C gewährt wird.

#### Richtlinie

Verkettung wird nicht unterstützt.\
Alternative und äquivalente Beziehungen werden nur auf einer einzigen Ebene ausgewertet. Wenn Sie einen Quell-Kurs abschließen, wird der alternative Abschluss nur für den oder die unmittelbaren Ziel-Kurse gewährt, nicht für nachgelagerte Ziele.

#### Workflow

#### Einrichtung der Beziehung

Ein Administrator definiert alternative oder gleichwertige Beziehungen zwischen Kursen, z. B.:

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

### Auswirkungen

#### Keine indirekten Vorteile

Teilnehmer können für Kurse, die weiter unten in einer Beziehungskette liegen, keine Abschlussgutschrift erhalten, es sei denn, jeder Kurs (oder seine direkte Alternative) ist abgeschlossen.\
Dadurch wird sichergestellt, dass die Lernanforderungen explizit und vorhersehbar erfüllt werden.

#### Vereinfachte Prüfung und Berichterstattung

Berichte und Teilnehmertranskripte zeigen alternative Abschlüsse nur für direkte Beziehungen an.\
Dadurch werden komplexe, mehrstufige Prüfprotokolle vermieden, und es wird Klarheit bei der Prüfung der Art und Weise gewährleistet, wie ein Abschluss gewährt wurde.

### Katalogfreigabe mit Peer-Konten: Beziehungen nicht freigegeben

Mit der Katalogfreigabe können Lernobjekte (LOs) über Peer-Konten hinweg freigegeben werden. Alternative und gleichwertige Beziehungen werden jedoch innerhalb der einzelnen Konten unabhängig verwaltet und nicht freigegeben.

#### Konzept: Katalogfreigabe und Beziehungen

#### Katalogfreigabe

Konten können Kataloge mit Peer-Konten teilen, um den Zugriff auf Kurse, Lernpfade und andere Lernobjekte kontenübergreifend zu ermöglichen.

#### Nicht freigegebene Beziehungen

Im Quellkonto konfigurierte alternative, äquivalente und alternative Vervollständigungsbeziehungen werden nicht freigegeben oder repliziert, wenn ein Katalog freigegeben wird.\
Jedes Konto unterhält und bewertet seine eigenen Beziehungen unabhängig.

### Workflow

#### Katalogfreigabe

Ein Administrator in **Konto A** gibt einen Katalog mit Lernobjekten für **Konto B** frei.

#### Beziehungskonfiguration

Bei Konto A können zwischen den Lernobjekten im freigegebenen Katalog alternative oder gleichwertige Beziehungen definiert sein.

#### Zugriff auf Peer-Konten

Konto B erhält Zugriff auf die freigegebenen Lernobjekte, übernimmt jedoch keine alternativen oder gleichwertigen Beziehungen, die in Konto A konfiguriert sind.

#### Unabhängiges Management

Wenn Konto B ein ähnliches alternatives oder gleichwertiges Verhalten erfordert, muss ein Administrator in Konto B die Beziehungen innerhalb dieses Kontos manuell konfigurieren.

#### Auswirkungen

#### Keine automatische Weiterleitung von Beziehungen

Alternative und gleichwertige Beziehungen sind in Peer-Konten nicht automatisch über die Katalogfreigabe verfügbar.

#### Manuelle Einrichtung erforderlich

Jedes Peer-Konto ist für die Definition und Verwaltung eigener Beziehungen für gemeinsam genutzte Lernobjekte verantwortlich.

#### Überlegungen zur Konsistenz

Das Abschlussverhalten, die Zufriedenheit mit Vorbedingungen und die Berichterstellung können je nach Konto unterschiedlich sein, es sei denn, die Beziehungen werden absichtlich durch manuelle Konfiguration abgeglichen.


### Downstream-Verhalten

Sobald ein alternativer Abschluss für eine Zielschulung vorhanden ist, verwendet ALM diese für nachgelagerte Prüfungen:

* Wenn die Zielschulung eine **Voraussetzung** für andere Schulungen ist, hat der Teilnehmer Anspruch auf diese Schulungen, als ob er das Ziel abgeschlossen hätte.
* Wenn das Ziel ein **obligatorischer Kurs in einem Lernpfad ist**, kann die Abschlusslogik des Pfads den Teilnehmer so behandeln, als habe er diesen Teil abgeschlossen, und den Pfad als abgeschlossen markieren, wenn andere Bedingungen erfüllt sind.
* Compliance- und andere Dashboards wie das Gruppen-Erfolgs-Dashboard, die davon abhängen, ob eine Schulungsanforderung erfüllt ist, können Teilnehmer einschließen, die nur alternative Abschlüsse haben.

Das System unterscheidet zwischen tatsächlicher und alternativer Fertigstellung, sodass

* Wenn der Teilnehmer später die Zielschulung direkt absolviert und sie abschließt, kann dieser direkte Abschluss die Notwendigkeit des alternativen Abschlusses überschreiben.
* Wenn die Beziehung zwischen Quelle und Ziel entfernt oder geändert wird, kann ALM die alternativen Abschlüsse entfernen oder anpassen, ohne echte Abschlüsse zu berühren, sofern rückwirkende nicht abgeschlossene Abschlüsse für das Konto aktiviert sind.

Alternative Abschlüsse sollen die tatsächliche Teilnehmeraktivität in der Zielschulung nicht beeinträchtigen. Sie fungieren als Overlay, das überarbeitet werden kann, wenn sich die Beziehungen ändern.

