---
description: Erläutert, wie Experience Builder öffentlich zugängliche Lernseiten und Kataloge für anonyme Besucher veröffentlichen kann, einschließlich wichtiger Funktionen, unterstützter Widgets, Voraussetzungen (Training Data Access Connector), Einschränkungen und Anleitungen zur Konfiguration, Skalierbarkeit und Migration von der älteren, nicht angemeldeten Startseite.
jcr-language: en_us
title: Konfiguration und Verwaltung nicht angemeldeter Seiten in Experience Builder
exl-id: e4685cab-08ca-4b6b-93f4-a9eecf382dc4
source-git-commit: 2f9e931523da6e3e1ed2cf60f1ad05f5caf3cc1b
workflow-type: tm+mt
source-wordcount: '6058'
ht-degree: 1%

---


# Nicht angemeldetes Erlebnis in Experience Builder

## Einführung

Das nicht angemeldete Erlebnis in Experience Builder ermöglicht es Unternehmen, ihre Lerninhalte und Portalseiten für alle Besucher anzuzeigen, einschließlich derjenigen, die sich nicht angemeldet haben. Diese Funktion soll potenzielle Teilnehmer anziehen, informieren und ansprechen, indem sie eine reibungslose und markenkonforme Vorschau Ihrer Schulungsangebote bietet, bevor sie sich anmelden oder registrieren müssen.

Mit dieser Funktion können Sie öffentlich zugängliche Seiten erstellen und anpassen, indem Sie dieselbe benutzerfreundliche Drag-and-Drop-Oberfläche verwenden, die im Standard-Experience Builder enthalten ist. Sie können für jeden, der Ihr Portal besucht, Kurskataloge, Kategorien, Pfade und Rich-Static-Content (Bilder, Text, HTML und eingebettete IFrames) präsentieren. So ist es ganz einfach, Ihre Lernprogramme hervorzuheben, neue Kurse zu fördern und einem breiteren Publikum wichtige Informationen bereitzustellen.

Besucher können den Katalog durchsuchen, Details zu Kursen und Instanzen anzeigen und die globale Suche nutzen, um verfügbare Schulungsmöglichkeiten zu erkunden. Aktionen, die jedoch die Identität eines Benutzers erfordern, z. B. die Registrierung für einen Kurs, den Zugriff auf personalisierte Funktionen (z. B. Kalender, Compliance, Leaderboard oder Soziales Lernen) oder die Nutzung von Schulungen, fordern den Besucher auf, sich anzumelden. Dieser Ansatz stellt sicher, dass vertrauliche und personalisierte Informationen sicher bleiben und dennoch ein umfassendes Vorschauerlebnis ermöglichen.

Administratoren können konfigurieren, welche Seiten und Widgets für nicht angemeldete Benutzer sichtbar sind. Dadurch wird sichergestellt, dass nur die entsprechenden Inhalte angezeigt werden. Seiten können so eingestellt werden, dass sie sowohl für angemeldete als auch für nicht angemeldete Benutzer oder ausschließlich für eine dieser Gruppen zugänglich sind. Experience Builder bietet einen Vorschaumodus, mit dem Sie genau sehen können, wie Ihre Seiten den Besuchern angezeigt werden, bevor sie veröffentlicht werden.

Um diese Funktion zu aktivieren, muss Ihr ALM-Integrationsadministrator den Connector für den Zugriff auf Schulungsdaten aktivieren. Dieser Connector stellt sicher, dass die Kurs-Metadaten öffentlich zugänglich sind.

Branding und Lokalisierung werden vollständig unterstützt, sodass Sie Seitentitel, Favoriten und Spracheinstellungen anpassen können, um sie an die Identität Ihres Unternehmens und die Anforderungen Ihrer Zielgruppe anzupassen. Als Teil des Übergangs zu dieser verbesserten Erfahrung wird die alte Startseitenfunktion für nicht angemeldete Benutzer verworfen. Daher sollten alle neuen öffentlichen Inhalte mit Experience Builder erstellt werden.

## Zweck der Funktion

Das nicht angemeldete Erlebnis in Experience Builder ermöglicht es Unternehmen, ihre Lerninhalte und Portalseiten öffentlich zu präsentieren, ohne dass sich Benutzer anmelden müssen. Dies hilft, potenzielle Teilnehmer anzulocken, zu informieren und anzusprechen, indem eine Vorschau der verfügbaren Schulungen und Ressourcen bereitgestellt wird, bevor eine Anmeldung oder Authentifizierung erforderlich ist.

## Nutzungsszenarien, bei denen kein Benutzer angemeldet ist

- **Marketing und Kontaktaufnahme**: Organisationen können ihre Schulungsprogramme für externe Zielgruppen wie potenzielle Kunden, Partner oder Stellenbewerber veröffentlichen, indem sie Kurskataloge und Programmdetails öffentlich zugänglich machen.
- **Vorabregistrierung**: Teilnehmer können verfügbare Kurse durchsuchen, Übersichten anzeigen und Kategorien erkunden, bevor sie sich registrieren oder anmelden, um ihnen dabei zu helfen, fundierte Entscheidungen zur Registrierung zu treffen.
- **Schulungsportale für Unternehmen**: Unternehmen können ein öffentlich zugängliches Portal für Konformitäts- oder Onboarding-Informationen bereitstellen, sodass neue Mitarbeiter oder Auftragnehmer sehen können, welche Schulung verfügbar ist, bevor sie Anmeldeinformationen erhalten.
- **Zielseiten für Veranstaltungen oder Kampagnen**: Organisationen, die Lernkampagnen oder Veranstaltungen durchführen, können spezielle öffentliche Seiten erstellen, um Kurse, Zeitpläne oder Ressourcen hervorzuheben und so die Sichtbarkeit und Interaktion zu erhöhen.
- **SEO und Auffindbarkeit**: Durch die Veröffentlichung ausgewählter Seiten und Kataloge verbessern Organisationen ihre Sichtbarkeit in Suchmaschinen und erleichtern es den Personen, ihre Lernangebote online zu entdecken.

## Wichtige Konzepte für nicht angemeldete Benutzer

Das nicht angemeldete Erlebnis von Experience Builder ermöglicht es Ihnen, Lerninhalte und Portalseiten öffentlich zu präsentieren, sodass Besucher ohne Anmeldung durchsuchen können.

- **Öffentliche Seiten und Menüs erstellen**: Sie richten Seiten und ein einzelnes Menü ein, auf das jeder unabhängig vom Anmeldestatus zugreifen kann.
- **Nur unterstützte Widgets hinzufügen**: Sie fügen Widgets hinzu, die keinen Benutzerkontext benötigen (Kategorien, Kurse und Lernpfade, Inhaltsfeld, HTML, iframe), während das System benutzerspezifische Widgets ausblendet.
- **Adaptives Seitenverhalten konfigurieren**: Sie entscheiden, ob eine Seite sowohl für angemeldete als auch für nicht angemeldete Benutzer angezeigt wird, und das System passt sichtbare Widgets und Inhalte basierend auf dem Anmeldestatus an.
- **Beide Erlebnisse in der Vorschau anzeigen**: Sie verwenden Vorschauoptionen, um zu sehen, wie Seiten nach angemeldeten und nicht angemeldeten Benutzern suchen, wobei Unterschiede in der Sichtbarkeit und dem Inhalt der Widgets bestehen.
- **Globale Suche aktivieren**: Besucher suchen nach Kursen und Inhalten, erhalten jedoch nur einfache Suchfunktionen ohne erweiterte AI-Integration.
- **Besucher können den Katalog und die Kursübersichten durchsuchen**: Besucher können Katalogseiten, Kursdetails und Instanzen durchsuchen, müssen sich jedoch anmelden, um sich zu registrieren oder auf personalisierte Funktionen zuzugreifen.
- **Branding und Lokalisierung anpassen**: Sie legen die Favicons und Spracheinstellungen so fest, dass sie mit dem Branding und der Barrierefreiheit Ihrer Organisation übereinstimmen.
- **Connector für den Zugriff auf Schulungsdaten aktivieren**: Sie aktivieren diesen Connector, um Kursmetadaten zur öffentlichen Anzeige zu exportieren und nicht angemeldete Seiten auf dem neuesten Stand zu halten.
- **Umgang mit hohem Traffic mit gemeinsam genutzter Infrastruktur**: Das System verwaltet große Mengen anonymer Besucher mithilfe gemeinsam genutzter Ressourcen und Ratenbegrenzung.
- **Optimieren für SEO**: Die Plattform bereitet öffentliche Seiten für die Suchmaschinenindizierung vor, sodass Ihre Lerninhalte leichter zu finden sind.

## Voraussetzungen für nicht angemeldetes Erlebnis

- Sie müssen den Connector für den Zugriff auf Schulungsdaten im Integrationsadministrator aktivieren, bevor Sie die nicht angemeldete Erfahrung verwenden können.
- Der Connector exportiert Kurs-Metadaten in ein öffentliches Repository, wodurch nicht angemeldete Seiten aktualisiert werden.

### TDA-Connector-Initialisierung

Der Connector für den Training Data Access (TDA) ist eine wichtige Voraussetzung für die Aktivierung der neuen Funktion &quot;Experience Builder&quot;, die nicht angemeldet ist, in ALM. Dieser Connector erleichtert den Export von Schulungsmetadaten, sodass Ihr Portal Kursinformationen für nicht angemeldete Benutzer anzeigen kann.

- **Connector-Aktivierung**: Sie müssen den TDA-Connector über das Integrations-Admin-Fenster aktivieren. Durch diesen Schritt wird die nicht angemeldete Experience Builder-Funktion freigeschaltet und die relevanten UI-Optionen werden auf der Administratoroberfläche angezeigt.
- **Metadatenexport**: Nach der Aktivierung exportiert der Connector wichtige Schulungsmetadaten (z. B. Kursname, Beschreibung, Übersicht, Bewertung, Dauer und Kenntnisse) aus ALM in ein öffentliches Repository. Diese Daten werden verwendet, um nicht angemeldete Seiten und Widgets aufzufüllen.
- **Planung und Synchronisierung**: Der Exportvorgang kann (z. B. täglich) geplant werden, um sicherzustellen, dass Ihr Portal die neuesten Kursupdates enthält. Änderungen, die in ALM vorgenommen wurden, werden abhängig von der Zwischenspeicherung und der Exportfrequenz nach dem nächsten Exportzyklus auf den nicht angemeldeten Seiten angezeigt.
- **Verfügbarkeit von Funktionen**: Auf die nicht angemeldeten Funktionen von Experience Builder, einschließlich Menüerstellung, Widget-Unterstützung und Katalogsichtbarkeit, kann erst nach der Initialisierung des TDA-Connectors zugegriffen werden. Wenn der Connector nicht aktiviert ist, bleibt Ihr Experience Builder auf angemeldete Benutzerszenarien beschränkt.
- **Migration und Support**: Bei Konten, die von älteren, nicht angemeldeten Homepage-Funktionen wechseln, ist die Initialisierung des TDA-Connectors der erste Schritt zur Migration. Sie stellt sicher, dass Sie die Flexibilität und die erweiterten Funktionen des neuen Experience Builder nutzen können.

## Was Besucher ohne Anmeldung tun können

Auf einer nicht angemeldeten Experience Builder-Website können Besucher den Schulungskatalog durchsuchen, indem sie die Katalogseite für öffentliche Kataloge öffnen. Sie können Filter wie Katalog, Produkt, Rolle, Typ, Kenntnisse und Tags verwenden, je nachdem, wie Sie die Site konfiguriert haben. Besucher können auch über die globale Suchleiste in der Kopfzeile nach Schulungen suchen (sofern aktiviert) und die Suchergebnisse direkt auf der Katalogseite anzeigen.

Besucher können Schulungsdetails anzeigen, indem sie Übersichtsseiten für Kurse, Lernpfade und Zertifizierungen öffnen. Auf diesen Seiten werden wichtige Metadaten angezeigt, einschließlich Titel, Beschreibung, Autor, Dauer, Format, Tags und Kenntnissen.

Darüber hinaus können Besucher statische und Werbeinhalte erkunden. Sie können Text- und Rich-Content-Blöcke lesen, Banner und Bildkacheln anzeigen und mit eingebetteten iframes wie externen Microsites, Videos oder Tools interagieren.

Wenn ein Besucher auf &quot;Registrieren&quot; klickt oder versucht, die Schulung zu starten, werden sie vom System aufgefordert, sich anzumelden oder sich anzumelden. Nach erfolgreicher Anmeldung wird der Besucher auf die entsprechende Seite umgeleitet, unabhängig davon, ob es sich um die Startseite, eine benutzerdefinierte Seite oder die ausgewählte Schulung handelt.

## Was ohne Anmeldung nicht verfügbar ist

Auf einer nicht angemeldeten Experience Builder-Website können Besucher nicht auf Funktionen oder Inhalte zugreifen, für die eine Benutzerauthentifizierung erforderlich ist. Sie können sich nicht für Schulungen registrieren, Kurse starten oder nutzen oder auf personalisierte Widgets wie &quot;Eigenes Lernen&quot;, &quot;Kalender&quot;, &quot;Konformität&quot;, &quot;Leaderboard&quot; oder &quot;Soziales Lernen&quot; zugreifen. Diese Widgets hängen von benutzerspezifischen Daten ab und sind nur nach der Anmeldung verfügbar.

Besucher können auch keine Aktionen ausführen, wie z. B. sich für einen Kurs registrieren oder auf Inhalte zugreifen, für die die Verfolgung des Fortschritts oder des Benutzerkontexts erforderlich ist. Wenn Sie versuchen, sich zu registrieren oder eine Schulung zu starten, wird der Besucher aufgefordert, sich anzumelden oder sich anzumelden, bevor Sie fortfahren.

## Unterstützte Widgets im nicht angemeldeten Modus

Im nicht angemeldeten Modus werden nur Widgets unterstützt, die keine benutzerspezifischen Daten benötigen. Dazu gehören:

- Widget &quot;Kategorien&quot;, das verfügbare Schulungskategorien anzeigt.
- Widget &quot;Kurse und Pfade&quot;, das Kurse und Lernpfade aus dem öffentlichen Katalog anzeigt. 1
- Feld &quot;Inhalt&quot; zum Hinzufügen von statischem Text, Bildern oder Werbeinhalten.
- HTML-Widget zum Einbetten von benutzerdefiniertem HTML-Inhalt.
- Iframe-Widget zur Anzeige externer Sites, Videos oder Werkzeuge auf der Seite.
- Widgets, für die Benutzerkontext erforderlich ist, z. B. &quot;Eigenes Lernen&quot;, &quot;Kalender&quot;, &quot;Konformität&quot;, &quot;Leaderboard&quot; und &quot;Soziales Lernen&quot;, sind im nicht angemeldeten Modus nicht verfügbar.

Widgets, die Benutzerkontext benötigen, wie &quot;Eigenes Lernen&quot;, &quot;Kalender&quot;, &quot;Konformität&quot;, &quot;Leaderboard&quot; und &quot;Soziales Lernen&quot;, sind im nicht angemeldeten Modus nicht verfügbar

## Seiten und Menüs ohne angemeldeten Benutzer

- Es wird nur ein nicht angemeldetes Menü unterstützt, das für alle Besucher ohne Authentifizierung sichtbar ist.
- Seiten können sowohl angemeldeten als auch nicht angemeldeten Menüs hinzugefügt werden. Befindet sich eine Seite in beiden Menüs, werden Widgets und Inhalte entsprechend dem Anmeldestatus des Benutzers angepasst.
- Nicht angemeldete Menüs bieten kein Zielgruppen-Targeting oder keine Personalisierung. Jeder sieht den gleichen Satz von Seiten.
- Widgets, die im nicht angemeldeten Modus nicht unterstützt werden, werden automatisch ausgeblendet. Das Seitenlayout wird angepasst, um Lücken zu füllen.
- Die Menü- und Seitenverwaltung (Hinzufügen, Vorschau, Löschen) ähnelt dem angemeldeten Modus, weist jedoch Anpassungen für nicht angemeldete Einschränkungen auf.

## Suchen- und Katalogverhalten

Im nicht angemeldeten Modus können Benutzer auf die Katalogseite zugreifen und die Suche verwenden, um verfügbare Kurse und Lernpfade zu durchsuchen. Auf der Katalogseite werden alle öffentlichen Kurse zusammen mit Filtern und Suchfunktionen angezeigt. Es folgen dieselben Kontoeinstellungen wie im angemeldeten Modus. Wenn ein Benutzer sucht, werden die Ergebnisse auf der Katalogseite angezeigt und Benutzer können die Kurs- und Instanzübersichtsseiten anzeigen, ohne sich anzumelden. Für Aktionen wie die Registrierung ist jedoch eine Anmeldung erforderlich.

Wenn ein Benutzer versucht, sich zu registrieren, muss er sich zuerst anmelden. Die Suche nach nicht angemeldeten Benutzern ist einfacher als die nach angemeldeten Benutzern und umfasst keine erweiterten Funktionen wie die AI Assistant-Integration.

## Technische Umsetzung

### Einrichtung des Schulungsdatenzugriffs-Connectors

Sie müssen den Connector für den Zugriff auf die Schulungsdaten im Admin-Bereich der Integration aktivieren, bevor Sie die Funktion &quot;Experience Builder&quot; verwenden können, bei der Sie nicht angemeldet sind. Dieser Connector exportiert Schulungsmetadaten aus ALM in ein öffentliches Repository, sodass sie über APIs für Ihre nicht angemeldeten Seiten zugänglich sind. Das Connector-Setup ist eine Voraussetzung für die Aktivierung der Funktion und stellt sicher, dass Ihr Portal aktuelle Schulungsinformationen anzeigt.

Metadatenexport und -synchronisierung\
Der Connector exportiert wichtige Metadatenfelder wie Kursname, Übersicht, Beschreibung, Bewertung, Dauer und Kenntnisse. Sie können Exporte (z. B. täglich) planen, damit Ihr Portal mit ALM synchronisiert ist. Nicht alle Metadatenfelder können einbezogen werden. Eine vollständige Liste erhalten Sie vom Engineering. Exportierte Daten werden zum Ausfüllen nicht angemeldeter Seiten verwendet, und Änderungen in ALM werden nach dem nächsten Exportzyklus angezeigt.

Zwischenspeichern und Exporthäufigkeit\
Das System verwendet die Exportfrequenz des Backends und das Frontend-Caching, um Datenaktualisierungen zu verwalten. Änderungen, die in ALM vorgenommen wurden, werden nach der geplanten Aktualisierung von Export und Cache auf Ihrem Portal widergespiegelt. Einige Updates werden aufgrund dieser Mechanismen möglicherweise nicht sofort angezeigt. Wenn Sie schnellere Updates benötigen, passen Sie den Exportplan an oder leeren Sie den Cache nach Bedarf.

Unterstützung für CSS/JS-Anpassung\
Auf der Registerkarte &quot;Anpassung&quot; können Sie benutzerdefinierte CSS- und JavaScript-Einstellungen für angemeldete und nicht angemeldete Seiten vornehmen. Auf diese Weise könnt ihr ein konsistentes Branding gewährleisten, benutzerdefinierte UI-Elemente hinzufügen und die User Experience im gesamten Portal verbessern. Alle Anpassungen werden global angewendet, um ein einheitliches Erscheinungsbild zu gewährleisten.

URL-Unterschiede und Branding (Favoritensymbol, Seitentitel)\
Nicht angemeldete und angemeldete Seiten können unterschiedliche URLs haben, um Benutzerstatus zu unterscheiden. Du kannst Favoritensymbol und Seitentitel für dein Portal anpassen, um deine Markenidentität zu stärken. Diese Funktionen sind in Experience Builder verfügbar. Wenden Sie sich an das Engineering, um den neuesten Status bezüglich des nicht angemeldeten Supports zu erfahren.

## Performance und Skalierbarkeit

### Gemeinsam genutzter Stack im Vergleich zu Premium Stack

Der gemeinsam genutzte Stack ermöglicht es mehreren Kunden, den nicht angemeldeten Experience Builder in einer gemeinsamen Infrastruktur zu verwenden und so Standard-Traffic-Level zu unterstützen. Der Premium-Stack ist eine kostenpflichtige Option, die dedizierte Ressourcen, Echtzeitfunktionen und höhere Lizenzbeschränkungen für Kunden mit erweiterten Anforderungen bietet. Wählen Sie den Stapel basierend auf dem erwarteten Traffic und den Geschäftsanforderungen aus.

### Verkehrsbeschränkungen und Gebührenbegrenzung

Der gemeinsam genutzte Stack erzwingt Verkehrsbeschränkungen, um eine faire Nutzung unter den Kunden zu gewährleisten. Das Engineering implementiert Ratenbegrenzungen, um zu verhindern, dass ein einzelner Kunde alle Ressourcen verbraucht. Wenn ihr Marketing-Kampagnen plant oder hohe Traffic-Zahlen erwartet, stimmt euch mit der technischen Abteilung ab, um eure Grenzen zu kennen und Unterbrechungen von Services zu vermeiden. Mithilfe der Ratenbegrenzung können Systemstabilität und -leistung für alle Benutzer gewährleistet werden.

Überlegungen zu Mehrmandantenfähigkeit und SEO\
Die Plattform unterstützt mehrere Mandanten, sodass mehrere Kunden ihre Portale in einer gemeinsam genutzten Infrastruktur hosten können. Nicht angemeldete Seiten sind SEO-freundlich, zusammen mit sitemap.xml und robots.txt, um die Sichtbarkeit von Suchmaschinen zu optimieren. Dadurch wird sichergestellt, dass Ihr Portal von Suchmaschinen erkannt und entsprechend indiziert werden kann.

## Migration und Abschaffung

### Übergang von einer vorhandenen nicht angemeldeten Startseite

Die ältere Funktion für nicht angemeldete Startseiten wird veraltet sein. Neue Konten sehen diese Option nicht, und vorhandene Konten, die sie verwenden, werden benachrichtigt, zur Experience Builder-basierten Lösung zu migrieren. Sie sollten Ihre Startseite mit dem neuen Experience Builder neu erstellen, um mehr Flexibilität, Widget-Unterstützung und ein verbessertes Benutzererlebnis zu erhalten. Der Übergangsplan sorgt für minimale Unterbrechungen und kontinuierlichen Support.

Kommunikationsplan\
Kunden, die die ältere Startseite verwenden, erhalten eine klare Mitteilung über den Zeitplan für die Abschaffung und die Migrationsschritte. Es wird Support angeboten, der dir hilft, deine Homepage auf die neue Experience Builder-Plattform zu verschieben, sodass du von neuen Funktionen und laufenden Updates profitieren kannst.

### Unterstützung für Lokalisierung und Anmeldung

Gebietsschema-Fallback-Logik\
Das System zeigt die Seiten in dem Gebietsschema an, in dem sie erstellt wurden. Wenn das Gebietsschema eines Benutzers nicht verfügbar ist, verwendet das System eine Fallback-Logik, um das nächstbeste verfügbare Gebietsschema auszuwählen. Dadurch wird sichergestellt, dass Benutzer Inhalte immer in einer unterstützten Sprache anzeigen können, was die Zugänglichkeit und die Zufriedenheit der Benutzer verbessert.

Unterstützte Anmeldetypen\
Das nicht angemeldete Erlebnis unterstützt alle in ALM verfügbaren Anmeldetypen, einschließlich SSO und Standardanmeldung. Benutzer können Inhalte durchsuchen, ohne sich anzumelden, und werden bei Bedarf aufgefordert, sich anzumelden, z. B. um sich für einen Kurs zu registrieren oder auf personalisierte Funktionen zuzugreifen. Dies ermöglicht einen reibungslosen Übergang vom Browsen zur Interaktion.

## Nicht angemeldete APIs

### Admin-Lernobjekt-API

Nicht angemeldete Experience Builder-Seiten und Headless-Portale organisieren oder filtern Kurse oft nach Produkten und Rollen. Die Admin LO-API wurde verbessert, um sicherzustellen, dass diese Verknüpfungen für Backend- und Headless-Integrationen sowie für den TDA-Connector konsistent zugänglich sind.

**Endpunkt und Verhalten**

Sie verwenden weiterhin den vorhandenen Admin LO-Endpunkt:

GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=products,roles


Dabei gilt:

- loId ist die Lernobjekt-ID (z. B. Kurs:12345).
- enforcedFields[learningObject] weist die API an, Produkte und Rollen für dieses LO explizit einzuschließen.

Dies wird dadurch erreicht, dass sichergestellt wird, dass die Produkt- und Rollenzuordnungen des LO in der Antwort vorhanden sind, wenn sie über enforcedFields angefordert werden. Die Antwort enthält dann in Attributen die Produkt- und Rollenmetadaten, die zum Berechnen oder Verfügbarmachen der empfohlenen Produkte (rec_products) und Rollen (rec_roles) für Experience Builder und andere Benutzer erforderlich sind.

Ein typischer Anruf von einem Administrator oder einer Integration sieht wie folgt aus:

curl -X GET \
  &quot;https://{your-domain}/primeapi/v2/learningObjects/course:12345?enforcedFields[learningObject]=products,roles&quot; \
  -H &quot;Autorisierung: Träger {admin_token}&quot; \
  -H &quot;Akzeptieren: application/vnd.api+json&quot;

Die zurückgegebene LO-JSON-Datei ist dieselbe Grundstruktur wie zuvor, aber jetzt können Sie sich darauf verlassen, dass Produkt-/Rollenfelder vorhanden sind, wenn Sie sie mit enforcedFields anfordern. Integrationen, die keine erzwungenen Felder verwenden, verhalten sich weiterhin wie zuvor.

### Liste der Lernobjekte - JobAid-Unterstützung im effectModifiedDate-Filter

**Zweck**

Der TDA-Connector (Training Data Access) und Headless-Implementierungen müssen häufig eine inkrementelle Synchronisierung ausführen, basierend auf dem **Datum der effektiven Änderung** der Lernobjekte. Bis zu dieser Version wurden JobAids (LO-Typ jobAid) nicht korrekt behandelt, wenn sie mit den Filtern effectModifiedDate kombiniert wurden. Diese Version behebt dies, sodass JobAids inkrementell synchronisiert werden können, genau wie Kurse und Lernpfade.

**Endpunkt und Verhalten**

Sie verwenden den vorhandenen LO-Listingendpunkt mit Datumsfiltern und dem LO-Typ:

GET /primeapi/v2/learningObjects\
?filter.effectModifiedDate.fromDate=2025-03-15T13:14:56.000Z\
&amp;filter.effectModifiedDate.toDate=2025-03-20T13:14:56.000Z\
&amp;filter.loTypes=jobAid


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
        "authorNames": ["Sid"],  
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
              { "id": "jobAid:144891_-1", "type": "learningObjectInstance" }  
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

### **Menü-API: Nicht angemeldeter Menüfilter**

**Zweck**

Experience Builder und Headless-Frontends benötigen eine einfache Möglichkeit, das **nicht angemeldete Menü** abzurufen, das die Navigation für öffentliche Besucher definiert. Vor dieser Version mussten Sie alle Menüs abrufen und dann eine benutzerdefinierte Logik anwenden, um zu identifizieren, welche die nicht angemeldete Navigation darstellte. Diese Version fügt einen einfachen serverseitigen Filter hinzu.

**Endpunkt und Verhalten**

Sie verwenden den vorhandenen Menüauflistungsendpunkt mit einem neuen Abfrageparameter:

GET /primeapi/v2/templates/menus?include=pages,subMenus.pages&amp;isNonLoggedIn=true


Die wichtigsten Punkte:

- include=pages,subMenus.pages ist optional, wird aber empfohlen, wenn Sie die Seiten- und Untermenü-Seitendetails in derselben Antwort benötigen.
- isNonLoggedIn=true ist neu in dieser Version und weist den Server an, nur Menüs zurückzugeben, die als nicht angemeldete Menüs gekennzeichnet sind.

Ohne den isNonLoggedIn-Parameter verhält sich der Endpunkt genau wie zuvor und gibt Menüs entsprechend dem vorhandenen Standardverhalten zurück. Mit isNonLoggedIn=true gibt es in der Regel das einzelne Menü zurück, das vom nicht angemeldeten Erlebnis für Ihr Konto verwendet wird (da es normalerweise nur ein nicht angemeldetes Menü pro Konto gibt).

In der Praxis kann ein Kunde jetzt Folgendes ausstellen:

curl -X GET \
  &quot;https://{your-domain}/primeapi/v2/templates/menus?include=pages,subMenus.pages&amp;isNonLoggedIn=true&quot; \
  -H &quot;Autorisierung: Träger {admin_token}&quot; \
  -H &quot;Akzeptieren: application/vnd.api+json&quot;


und rufen Sie die nicht angemeldete Navigationsstruktur in einem Aufruf zurück, mit allen Seiten, die für anonyme Besucher sichtbar sein sollten.

Dies ist besonders nützlich, wenn Sie eine Headless-Site ohne angemeldeten Benutzer erstellen und dieselbe Navigation wie in Experience Builder spiegeln möchten oder wenn Sie debuggen, ob das nicht angemeldete Menü korrekt konfiguriert wurde.

## Liste benutzerdefinierter Domänen zulassen

Der nicht angemeldete Stapel besteht aus:

- Eine öffentliche CDN-Domäne (z. B. cpcontents.adobe.com oder yourdomain.example.com), die Layouts, Konfigurations-JSON und statische Assets bereitstellt.
- Ein Endpunkt eines öffentlichen Elasticsearchs (ES), der Katalog- und Suchdaten bereitstellt, jedoch nur, wenn die Anforderung von einer **zugelassenen Domäne** für dieses ALM-Konto stammt.

Wenn Sie eine benutzerdefinierte Domäne einführen, funktioniert diese nahtlos, ohne dass dem vorhandenen Prozess zum Hinzufügen einer benutzerdefinierten Domäne zusätzlicher Aufwand folgt.

### Voraussetzungen

Bevor Sie eine benutzerdefinierte Domäne für nicht angemeldete Benutzer auf die Positivliste setzen:

1. Die benutzerdefinierte Domäne wird für Ihr ALM-Konto konfiguriert (z. B. verweist DNS für academy.yourcompany.com auf Adobe/Akamai und es werden Zertifikate bereitgestellt).
2. Der **TDA-Connector (Training Data Access)** ist für das Konto aktiviert.
3. Die **nicht angemeldete Experience Builder**-Funktion ist aktiviert (Adobe-seitig).

Mit diesen Schritten wird sichergestellt, dass

- Ihr Konto verfügt über eine nicht angemeldete **Konto-JSON** (häufig als accountConfig / experienceBuilderConfig bezeichnet), die Felder wie cpDomain, almDomain, almCdnBaseUrl, esBaseUrl und zugelassenen Domänen enthält.
- Der nicht angemeldete Stapel weiß, wo Daten bereitgestellt werden sollen und von welchen Domänen Anfragen angenommen werden sollen.

### Funktionsweise der Zulassungsliste

Die Zulassungsliste wird in der Konfiguration gespeichert, die TDA exportiert, und der nicht angemeldete Stack liest. Diese Konfiguration umfasst:

- Die ALM-Domänen (cpDomain, almDomain).
- Die **CDN-Basis-URL** für nicht angemeldeten Inhalt (almCdnBaseUrl).
- Die **URL der öffentlichen Suchbasis** (esBaseUrl).
- Die Liste der Domänen, die nicht angemeldete Aufrufe für dieses Konto veröffentlichen dürfen.

Damit Experience Builder, der nicht angemeldet ist, in einer benutzerdefinierten Domäne funktioniert:

- Der Browser muss die nicht angemeldete HTML von dieser benutzerdefinierten Domäne (oder von der nicht angemeldeten ALM-CDN-Domäne, je nach Einrichtung) laden.
- Aufrufe von dieser Domäne an die öffentlichen ES- und CDN-Endpunkte müssen akzeptiert werden. Dies geschieht nur, wenn die Domäne in der Zulassungsliste vorhanden ist.

Diese Version fügt eine neue, nicht angemeldete CDN-Domäne cpcontents.adobe.com hinzu und gibt an, dass sie in die **zugelassenen Domänen** im TDA-Connector platziert werden muss. Für vorhandene nicht angemeldete native Benutzer ist hierfür ein Update erforderlich.

### Benutzerdefinierte Domäne zulassen

**Benutzerdefinierte Domäne in ALM konfigurieren**

Arbeiten Sie mit Adobe zusammen, um Ihre Domäne wie academy.yourcompany.com als benutzerdefinierte Domäne für Ihr ALM-Konto zu registrieren. Sie aktualisieren DNS so, dass es wie angewiesen auf Adobe Akamai zeigt, und warten Sie, bis SSL und Routing abgeschlossen sind.

An diesem Punkt kann sowohl angemeldeter als auch nicht angemeldeter Datenverkehr über diese Domäne ALM erreichen, aber nicht angemeldete Such- und Katalogaufrufe können weiterhin blockiert werden, wenn die Domäne nicht auf der Zulassungsliste steht.

**TDA und nicht angemeldeten Experience Builder aktivieren**

Voraussetzungen:

- Der **Schulungsdatenzugriffsconnector** ist aktiviert.
- Die **nicht angemeldete Experience Builder**-Funktion ist für das Konto aktiviert.

Durch Aktivieren von TDA wird die JSON-Datei des nicht angemeldeten Kontos erstellt oder aktualisiert. Bei neuen Konten wird im Prozess standardmäßig auch die neue nicht angemeldete CDN-Domäne (cpcontent.adobe.com) auf die Zulassungsliste gesetzt, sodass der öffentliche ES-Endpunkt Aufrufe von dieser Domäne erwartet.

Bei Konten, die bereits den älteren nicht angemeldeten Stapel verwendet haben, wird in der M45-Spezifikation darauf hingewiesen, dass vorhandene Connectors gelöscht und neu erstellt werden müssen, um die neue Domäne zu übernehmen.

**Benutzerdefinierte Domäne zur Zulassungsliste hinzufügen**

Entscheidend ist, dem nicht angemeldeten ES-Stack mitzuteilen, dass academy.yourcompany.com ein genehmigter Ursprung ist. Es gibt zwei gemeinsame Pfade.

1. **TDA-Connector wieder aktivieren (einfach, Self-Service-freundlich)**

Das Experience Builder M45-Wiki erklärt, dass bestehende native nicht angemeldete Benutzer die TDA-Verbindung löschen und wieder aktivieren müssen, damit die neue Domäne automatisch auf die Zulassungsliste gesetzt wird. Damit werden zwei Dinge erreicht:
1. Die JSON-Datei für das nicht angemeldete Konto wird neu generiert.
2. Die zugelassenen Domänen werden aktualisiert, um die neue, nicht angemeldete CDN-Domäne und Ihre benutzerdefinierte Domäne aufzunehmen.

Dies wird empfohlen, wenn Sie eine kleine Anzahl von Konten haben und es zulassen können, dass der Connector vorübergehend deaktiviert und wieder aktiviert wird.

1. **Überprüfen Sie, ob die Domäne tatsächlich auf die Zulassungsliste gesetzt ist**

Öffnen Sie nach der Zulassungsauflistung Ihre nicht angemeldete Site in der benutzerdefinierten Domäne und überprüfen Sie die Browsernetzwerkaufrufe.

Sie möchten Folgendes sehen:

- Anforderungen an almCdnBaseUrl (z. B. [https://cpcontent.adobe.com/](https://cpcontent.adobe.com/)...) erfolgreich mit 200/304.
- Anforderungen an esBaseUrl (API für die öffentliche Suche, z. B. [https://primeapps.adobe.com/almsearch/api/v1/](https://primeapps.adobe.com/almsearch/api/v1/)...) Erfolgreich, JSON wird mit Such-/Katalogdaten zurückgegeben.

Wenn diese Aufrufe 4xx oder explizite Fehler zurückgeben, die &quot;nicht vertrauenswürdige Domäne&quot; oder &quot;Ursprung nicht zulässig&quot; nahe legen, ist die Zulassungsliste unvollständig oder falsch konfiguriert, und der Support muss sie anpassen.

Die nicht angemeldete LLD stellt außerdem fest, dass die Kontokonfiguration einen erwarteten Domänenwert enthalten kann. Zur Laufzeit überprüft die Site, ob die Domäne in der URL mit dem in der Konfiguration festgelegten Wert übereinstimmt. Ist dies nicht der Fall, kann der Benutzer zu einer Fehlerseite umgeleitet werden. Dies schützt vor dem Zugriff auf die Konfiguration eines Kunden über die Domäne eines anderen Kunden.

## Verwendung von Empfehlungen in Experience Builder ohne Anmeldung

Mit dem nicht angemeldeten Experience Builder können Sie öffentliche Lernseiten erstellen, auf denen Besucher Ihren Katalog durchsuchen und markierte Inhalte anzeigen können, bevor sie sich anmelden. Auch wenn diese Besucher anonym sind, können Sie empfohlene Schulungen mithilfe von Metadaten und Widgets darstellen.

In der angemeldeten Teilnehmer-App können Empfehlungen personalisiert werden: Sie können vom Profil, dem Verlauf, den Kenntnissen und dem Fortschritt des Teilnehmers abhängen. Im **nicht angemeldeten**-Erlebnis ist noch keine Teilnehmeridentität vorhanden, daher kann die Plattform nicht pro Benutzer personalisiert werden.

Recommendations im nicht angemeldeten Modus sind daher:

- **Kuratiert oder regelbasiert**: basierend auf Katalog, Produkt, Rolle, Beschriftungen, Tags und anderen Metadaten.
- **Segmentorientiert**: &quot;Für Entwickler empfohlen&quot;, &quot;Für Partner empfohlen&quot;, &quot;Für Anfänger empfohlen&quot;.
- **Marketing-orientiert**: Ermöglicht es Besuchern, sich anzumelden, nachdem sie sich angemeldet haben.

### Metadaten und APIs, die Empfehlungen unterstützen

Hinter den Kulissen verwenden nicht angemeldete Seiten Folgendes:

- Der **TDA-Connector** zum Exportieren von Lernobjektmetadaten (Kurse, Pfade, Zertifizierungen, Arbeitshilfen) in einen öffentlichen Suchindex.
- Der **öffentliche Suchstapel** zum Beantworten von Abfragen aus nicht angemeldeten Widgets (Katalog, Suche, Kurse und Pfade, Kategorien).
- Die **API für Admin-Lernobjekte** zum Verfügbarmachen von Produkt- und Rollenmetadaten, die für Empfehlungsregeln verwendet werden können.

In dieser Version wurde die Admin LO-API erweitert, sodass Produkt- und Rollenzuordnungen zuverlässig verfügbar sind:

GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=products,roles

Dadurch können Widgets und Headless-Integrationen regelbasierte Empfehlungen erstellen, die Produkte, Rollen, Katalogbeschriftungen, Tags und andere Felder konsistent verwenden.

### Entwerfen von Empfehlungsabschnitten mit Experience Builder-Widgets

Sie erstellen Empfehlungsabschnitte auf nicht angemeldeten Seiten, indem Sie **Experience Builder-Widgets** mit Metadatenfiltern kombinieren.

#### **Widget für Kurse und Pfade**

Verwenden Sie das Widget **Kurse und Pfade**, wenn Sie eine Zeile oder ein Raster mit empfohlenen Elementen anzeigen möchten. In der Konfiguration können Sie wählen:

- Aus welchen Katalogen abgerufen werden soll.
- Welche Katalogbeschriftungen, Produkte, Rollen oder Tags als Filter verwendet werden sollen.
- Gibt an, ob Kurse, Pfade, Zertifizierungen, Arbeitshilfen oder ein Mix angezeigt werden sollen.
- Sortieren und maximale Anzahl von Elementen.

Beispielsweise können Sie Folgendes erstellen:

- &quot;Für Entwickler empfohlen&quot;: Filtert nach einem Produkt oder einer Rolle, die Sie für den Entwicklerinhalt verwenden.
- &quot;Hier starten&quot;: Filtern Sie nach einer Beschriftung wie &quot;Starter&quot; oder &quot;Onboarding&quot;.
- &quot;Empfohlen in diesem Quartal&quot;: Filtert nach einem zeitgebundenen Label wie featured-q3-2026.

Das Widget lernt nicht vom Verhalten, sondern zeigt an, welche Übereinstimmungen mit den von Ihnen definierten Metadatenregeln bestehen. Aus Sicht des Besuchers sieht es jedoch wie ein Empfehlungsstreifen aus.

#### **Kategorien-Widget**

Verwenden Sie das Widget **Kategorien**, um Besuchern zu helfen, in &quot;empfohlene&quot; Inhaltssätze zu navigieren, auch wenn sie Ihre Produktnamen nicht kennen.

Sie können Kacheln konfigurieren, die jeweils ein Segment darstellen, z. B.:

- &quot;Für Administratoren&quot;
- &quot;Für Vertriebsteams&quot;
- &quot;Für Partner&quot;
- &quot;Nach Produktlinie&quot;

Jede Kachel kann eine der folgenden Verknüpfungen enthalten:

- Eine gefilterte Katalogseite (z. B. der Katalog, der nach bestimmten Produkten oder Beschriftungen gefiltert wurde).
- Eine dedizierte, nicht angemeldete Seite, die für dieses Segment vorkonfigurierte Kurse und Pfade verwendet.

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

## Verwendung von Arbeitshilfen im neuen, nicht angemeldeten Experience Builder

Auf der **Benutzeroberfläche** nehmen Arbeitshilfen hauptsächlich über Widgets, die Lernobjekte anzeigen können, an nicht angemeldeten Erlebnissen teil:

1. **Widget für Kurse und Pfade**\
   Dieses Widget kann mehrere LO-Typen anzeigen, einschließlich Arbeitshilfen. Auf nicht angemeldeten Seiten können Sie folgende Einstellungen vornehmen:
   1. Schließen Sie Arbeitshilfen explizit ein oder aus.
   2. Filtern Sie Arbeitshilfen nach Katalog, Produkt, Rolle, Beschriftungen, Tags und anderen Metadaten.
   3. Stellen Sie sie neben Kursen und Pfaden oder als separaten &quot;Ressourcen&quot;-Streifen vor.

Auf einer öffentlichen Landingpage können Sie beispielsweise einen Streifen mit dem Titel &quot;Hilfreiche Ressourcen&quot; konfigurieren, der nur Arbeitshilfen anzeigt, und einen anderen Streifen mit dem Titel &quot;Empfohlene Kurse&quot;, der Kurse und Pfade anzeigt.

1. **Katalogseite und Suche**\
   Die nicht angemeldeten Oberflächen **catalog** und **search** verwenden den öffentlichen Suchindex (gespeist vom Connector für den Zugriff auf Schulungsdaten). Dieser Index unterstützt Arbeitshilfen jetzt korrekt. Gehen Sie deshalb wie folgt vor:
   1. Nicht angemeldete Suchergebnisse können Arbeitshilfen enthalten.
   2. Nicht angemeldete Katalogfilter (nach Typ, Produkt, Tags usw.) können Arbeitshilfen beinhalten, solange Ihre Kontokonfiguration und Widgets so eingerichtet sind, dass sie angezeigt werden.
2. **LO-Übersichtsseiten**\
   Wenn ein Besucher auf eine Arbeitshilfe aus einem beliebigen Widget oder aus dem Katalog klickt, wird eine **LO-Übersichtsseite** für diese Arbeitshilfe im nicht angemeldeten Modus aufgerufen. Dort können sie die Beschreibung und die Metadaten lesen. Für den tatsächlichen Download oder Verbrauch ist in der Regel noch eine Anmeldung erforderlich, aber das Vorhandensein und die Auffindbarkeit der Arbeitshilfe selbst wird durch das nicht angemeldete Erlebnis gehandhabt.

### Anzeige von Arbeitshilfen über nicht angemeldete APIs

Auf der **API-Seite** werden Arbeitshilfen unterstützt von:

1. Der **Schulungsdatenzugriffsconnector und die öffentliche Suche**\
   TDA exportiert Arbeitshilfemetadaten zusammen mit anderen LO-Typen in den öffentlichen Suchindex, der nicht angemeldete Such- und Katalogabfragen bereitstellt. Darauf verlassen sich Experience Builder und Headless-Frontends.
2. Die Liste der **Lernobjekte mit effektivemÄnderungsdatum**\
   In dieser Version wurde der LO-Listing-Endpunkt korrigiert, sodass Arbeitshilfen mit dem Filter effectModifiedDate ordnungsgemäß funktionieren. Sie können jetzt folgende Telefonnummern anrufen:

GET /primeapi/v2/learningObjects\
?filter.effectModifiedDate.fromDate=2026-01-19T13:14:56.000Z\
&amp;filter.effectModifiedDate.toDate=2026-01-21T13:14:56.000Z\
&amp;filter.loTypes=jobAid


Vor dieser Änderung wurden beim Kombinieren von &quot;effectModifiedDate&quot; mit &quot;loTypes=jobAid&quot; keine Arbeitshilfen zuverlässig zurückgegeben. Jetzt tut sie dies, wie im Wiki *M45 Public API Changes* dokumentiert. Das bedeutet:

1. Ihre TDA- oder ETL-Aufträge können **die Arbeitshilfen** für nicht angemeldete Erlebnisse inkrementell synchronisieren, genau wie bei Kursen und Pfaden.
2. Jede Headless-Implementierung, die ein öffentliches Verzeichnis für Arbeitshilfen erstellt, kann Änderungen basierend auf effectModifiedDate und loType=jobAid abfragen.

Die Beispielantwort im M45-Dokument zeigt ein learningObject mit loType: &quot;jobAid&quot; und loFormat: &quot;Content&quot;, das zurückgegeben wird, wenn dieses Muster verwendet wird.

1. Die **Admin LO-API**\
   M45 ist zwar nicht spezifisch für nicht angemeldete Benutzer, aktualisiert aber auch die Admin LO-API, um Produkt- und Rollen-Metadaten für alle LO-Typen über Folgendes konsistent anzuzeigen:

GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=products,roles


Bei Arbeitshilfen bedeutet dies, dass Sie ihre Produkte, Rollen, Labels und Tags zentral verwalten und sich auf diese Metadaten in öffentlichen, nicht angemeldeten Erlebnissen verlassen können, z. B. in den Abschnitten &quot;Ressourcen für Marketer&quot; oder auf produktspezifischen Landingpages.

**Hinweis**:

Im Status &quot;nicht angemeldet&quot;:

- Arbeitshilfen sind hauptsächlich **auffindbar**: Besucher können sehen, dass sie vorhanden sind, Beschreibungen lesen und verstehen, wie sie Themen oder Kurse unterstützen.
- Die tatsächliche **Nutzung** (das Herunterladen oder Öffnen der Arbeitshilfeinhalte) erfordert in der Regel noch eine Anmeldung, insbesondere wenn Arbeitshilfen als Teil lizenzierter oder interner Inhalte betrachtet werden.

## Änderungen an &quot;Kurzbeschreibung&quot; in der LO-Suche (nicht angemeldet)

Beim nicht angemeldeten Kurs werden die Suche nach und die Auflistung von Lernobjekten (LOs) durch den Connector für den Zugriff auf Schulungsdaten (TDA) und einen öffentlichen Elasticsearch-Index unterstützt. Früher verwendete dieser Stapel ein einzelnes Übersichts-/Beschreibungsfeld für jedes LO. Kunden, die Headless-Portale ohne angemeldete Benutzer erstellen, wollten auf LO-Kacheln dieselbe kurze Beschreibung anzeigen, die die Benutzeroberfläche des angemeldeten Teilnehmers zeigt, und nicht nur die lange Übersicht.

Mit der Änderung wird Unterstützung für die LO **Kurzbeschreibung** in APIs für die Suche und die Auflistung ohne angemeldete Benutzer eingeführt:

- Für **Kurse** lauten die vorhandenen Benutzeroberflächensemantiken:
   - Logged-in-Karten zeigen &quot;Kurzbeschreibung&quot; (140 Zeichen Feld), falls vorhanden, sonst fallen sie auf die lange &quot;Detaillierte Übersicht&quot; zurück.
- Für **Lernpfade** verwendet die angemeldete Benutzeroberfläche das Feld &quot;Vorteile&quot; als kurze Beschreibung (sofern definiert) und kehrt andernfalls zur Übersicht zurück.
- Für **Zertifizierungen** wird eine kurze &quot;Beschreibung&quot; mit einer längeren &quot;Zertifizierungsübersicht&quot; als Fallback verwendet.
- Für **Arbeitshilfen** wird das Hauptbeschreibungsfeld verwendet.

## Weitere Änderungen

### Einschränkung, dass zwei Konten nicht dieselbe benutzerdefinierte Domäne gemeinsam nutzen können

In den nicht angemeldeten und angemeldeten Architekturen von Adobe Learning Manager wird eine **benutzerdefinierte Domäne** (z. B. academy.example.com) als global eindeutiger Schlüssel behandelt, der genau einem ALM-Konto zugeordnet werden muss. Die Plattform erzwingt daher eine strenge Einschränkung, dass **keine zwei Konten dieselbe benutzerdefinierte Domäne** gemeinsam nutzen können. Dies ist für Sicherheit, Routing und SEO erforderlich: Die Routing-Ebene und der nicht angemeldete Stapel verwenden die Domäne, um die richtige Kontokonfiguration zu nachzuschlagen (einschließlich der nicht angemeldeten Konto-JSON, der Experience Builder-Menüs, des Brandings und der TDA-/Suchendpunkte).

Wenn dieselbe benutzerdefinierte Domäne für zwei Konten zugelassen wird, ist es nicht möglich, die Rückgabe der Kontodaten zu garantieren. Außerdem kann dies zu mandantenübergreifenden Lecks führen und generierte Artefakte wie sitemap.xml und robots.txt beschädigen, die pro Konto erstellt, aber von Suchmaschinen pro Host entdeckt werden. Operativ bedeutet dies, dass Sie beim Zuweisen oder Verschieben einer benutzerdefinierten Domäne zuerst sicherstellen müssen, dass sie nicht an ein anderes Konto angehängt ist (oder dort die Registrierung aufheben), und das interne Tool von Adobe lehnt Versuche ab, dieselbe Domäne an mehrere Konten zu binden.

### Browserzwischenspeicherung von Ressourcen bei nicht angemeldetem Benutzer

Bei nicht angemeldeten Adobe Learning Manager-Anwendern ist das Zwischenspeichern von Ressourcen im Browser ein zentraler Bestandteil der Performance- und Skalierungsstrategie, da öffentliche Seiten großen, manchmal stacheligen Marketing-Traffic mit geringer Latenz und minimaler Ursprungslast verarbeiten müssen. Statische und halbstatische Assets wie die nicht angemeldete HTML-Shell (z. B. index.html/guest.html), die JSON-Konfiguration auf Kontoebene (account.json oder config.json), das Experience Builder-Seitenlayout JSON (Menüs, Widget-Layouts, Karteneinstellungen), CSS, JS, Bilder und Favicons werden von einem Akamai CDN (cpcontents.adobe.com / cpcontent.adobe.com) mit Cache-Headern bereitgestellt, die sowohl CDN- als auch browserseitige Wiederverwendung unterstützen, sodass der Browser nach dem ersten Laden der Seite nachfolgende nicht angemeldete Seiten weitgehend rendern kann aus dem Cache löschen und nur bei Bedarf über ETag oder Last-Modified erneut validieren.

## Starten der Optionen für die Startseite

Wählen Sie auf der Adobe Learning Manager-Homepage **Branding** aus. Wählen Sie dann im linken Bereich Nicht angemeldete Startseite aus.

![Homepage-Optionen](/help/migrated/administrators/feature-summary/assets/non-logged-in-homepage.png)

*Wählen Sie die Option &quot;Nicht angemeldete Homepage&quot; aus*

## Hinzufügen eines Banners

Fügen Sie ein Banner hinzu, um Marketing-Ankündigungen anzuzeigen oder das Trendthema des Tages vorzustellen. Wählen Sie **Banner hinzufügen**.

![Banner](/help/migrated/administrators/feature-summary/assets/add-banner-image.png)

*Banner hinzufügen*

Navigieren Sie zum Speicherort des Bildes, das als Banner verwendet werden soll. Geben Sie dann einen Link als Aktionsschaltfläche auf dem Bannerbild an.

## Kategorien hinzufügen

Diese Komponente kann verwendet werden, um den Katalog nach Tags, Kenntnissen und Katalog zu filtern. Dieser Abschnitt enthält einen Titel und eine Beschreibung für jede Kategorie. Durch Klicken wird der Benutzer zu der Katalogseite mit den angewendeten Filtern weitergeleitet.

Wählen Sie **[!UICONTROL Kategorie hinzufügen]**. Geben Sie dann die Details für die Kategorie ein.

![Kategorie hinzufügen](/help/migrated/administrators/feature-summary/assets//add-category.png)

*Kategorien hinzufügen*

Speichern Sie die Kategorie. Die Kategorie wird dem Abschnitt hinzugefügt.

## Hinzufügen eines Katalogs

Fügen Sie einen Katalog für nicht angemeldete Benutzer hinzu, damit sie die gesamte Schulung auf der Plattform durchsuchen können.

![Katalog hinzufügen](/help/migrated/administrators/feature-summary/assets//add-catalog.png)

*Katalog hinzufügen*

Alle exportierten Schulungen werden aufgeführt.
