---
description: Erfahren Sie mehr über die neuen Funktionen und Verbesserungen in der Version Oktober 2025 von Adobe Learning Manager
jcr-language: en_us
title: Neue Funktionen in der Adobe Learning Manager-Version Oktober 2025
source-git-commit: 5d50bd56b6663b26fc6db0ff33d19ad809e9bf6a
workflow-type: tm+mt
source-wordcount: '5638'
ht-degree: 0%

---


# Neue Funktionen in der Adobe Learning Manager-Version Oktober 2025

Die Adobe Learning Manager-Version vom Oktober 2025 enthält wesentliche Verbesserungen zur Verbesserung der Berichtsgenauigkeit, zur Erweiterung der Integrationsfunktionen und zur Verbesserung des Lernerlebnisses für Administratoren, Autoren und Teilnehmer.

* Experience Builder: Designt rollenbasierte, vollständig auf die Anforderungen eures Unternehmens zugeschnittene Lernportale. Erstellen Sie rollenbasierte Lernportale mit Widgets, Menüs und Seiten.
* Soziales Tagging in Lerntafeln: Teilnehmer können jetzt Peers mithilfe von @username in Beiträgen und Kommentaren taggen und so eine zielgerichtete Zusammenarbeit und Benachrichtigungen in Social-Learning-Communitys ermöglichen.
* Berechtigungen für Ankündigungen mit Umfang: Benutzerdefinierte Administratoren können Ankündigungen erstellen, die auf ihre zugewiesenen Benutzergruppen oder Kataloge beschränkt sind, um eine zielgerichtete Kommunikation zu gewährleisten und die Informationsüberlastung zu reduzieren.
* Sprachbasierte Fortschrittsverfolgung: Der Teilnehmerfortschritt wird jetzt für jedes Gebietsschema unabhängig gespeichert, sodass Sie nahtlos zwischen den Sprachen wechseln können, ohne den Fortschritt zu verlieren.
* Inkrementelle Verwaltung benutzerdefinierter Rollen: Administratoren können benutzerdefinierte Rollen jetzt effizienter verwalten, indem sie inkrementelle und multiinkrementelle Importe in Adobe Learning Manager unterstützen.
* Verbesserte APIs für Analyse und Migration: Neue und verbesserte APIs bieten eine bessere Verfolgung der Quizleistung, Überwachung des Migrationsstatus und Unterstützung für Benutzer-Tagging beim sozialen Lernen.

## Experience Builder

>[!IMPORTANT]
>
>Wir freuen uns, bekannt geben zu können, dass Experience Builder, das innovative Tool zur Erstellung anpassbarer Lernportale, nach der Version Oktober 2025 von Adobe Learning Manager verfügbar sein wird.
>
>Du hast jederzeit Zugriff auf weitere Updates, sobald die Version demnächst verfügbar ist. Wir freuen uns darauf zu sehen, wie ihr Experience Builder einsetzt, um eure Lernportale zu transformieren.
>
>Bei Fragen oder zusätzlichen Informationen wenden Sie sich an Ihren Customer Success Manager.

Experience Builder ist ein Programm ohne oder mit wenig Code in Adobe Learning Manager, mit dem Sie benutzerdefinierte Lernportale erstellen können. Sie ermöglicht es Ihnen, markenfreundliche, benutzerfreundliche Lernportale zu entwerfen, ohne technische Fähigkeiten oder umfassendes Programmierwissen zu benötigen.
Mit Experience Builder können Administratoren ganz einfach Seiten, Menüs und Widgets erstellen, um personalisierte Lernerlebnisse bereitzustellen, die auf ihre Zielgruppe zugeschnitten sind.

Vor Experience Builder standen Unternehmen vor mehreren Herausforderungen:

1. **Eingeschränkte Anpassung**: In Portalen gab es feste Designs mit wenigen Optionen, die Ihr Branding widerspiegeln. Administratoren konnten nur grundlegende Änderungen vornehmen, z. B. das Ändern von Kopf- und Fußzeilen oder Farben, wodurch die Möglichkeit zum Erstellen einzigartiger Erlebnisse eingeschränkt wurde.
2. **Kosten**: Die Erstellung benutzerdefinierter Portale erforderte teure Entwickler und lange Zeitpläne, deren Fertigstellung oft 6 bis 9 Monate in Anspruch nimmt. Dieser Ansatz hat die Gesamtbetriebskosten erhöht und die Bereitstellung verzögert.
3. **Allgemeine Erfahrungen**: Jeder hat den gleichen Inhalt gesehen, auch wenn er für seine Rolle oder Bedürfnisse nicht relevant war. Dieser Mangel an Personalisierung verringerte die Interaktion und Zufriedenheit der Teilnehmer.
4. **Technische Barrieren**: Nicht-technische Administratoren hatten Schwierigkeiten, Portale zu erstellen oder zu aktualisieren, weil sie Programmierkenntnisse oder externen Support benötigten.

Experience Builder löst diese Probleme mit einer einfachen Lösung ohne oder mit geringem Code für die Erstellung personalisierter Portale für Marken.

Dadurch können Administratoren Portale entwerfen, die den Anforderungen ihres Unternehmens entsprechen, ohne auf technisches Fachwissen oder externe Entwickler angewiesen zu sein.

**Anwendungsfälle**

* **Portale mit Branding**: Erstellen Sie ein Portal, das der Website Ihres Unternehmens mit Logos, Farben und Layouts entspricht. Ein Unternehmen im Gesundheitswesen kann beispielsweise ein Portal entwerfen, das sein Branding widerspiegelt und gleichzeitig Lerninhalte bereitstellt.
* **Rollenbasiertes Lernen**: Auf bestimmte Rollen zugeschnittene Seiten erstellen. Vertriebsteams können Produktschulungen anzeigen, während Ingenieure auf technische Kurse zugreifen.
* **Produktschulung**: Richten Sie spezielle Seiten für verschiedene Produkte wie Photoshop oder Illustrator ein, auf denen Widgets mit Kursen, Zertifizierungen und zugehörigen Ressourcen angezeigt werden.

In [Experience Builder](/help/migrated/administrators/feature-summary/experience-builder/overview.md) finden Sie weitere Informationen zum Erstellen benutzerdefinierter Seiten mithilfe von Widgets.

## Sprachbasierter Teilnehmerfortschritt

Derzeit verfolgt Adobe Learning Manager den Fortschritt der Teilnehmer nur für die ausgewählte Sprache, was zu erheblichen Fortschrittsverlusten beim Wechseln zwischen Sprachen/Gebietsschemas im Player führt. Diese Einschränkung kann zu einer schlechten Benutzererfahrung führen, da Teilnehmer ihren Fortschritt beim Zugriff auf Inhalte in verschiedenen Sprachen verlieren können. Der Fortschritt für jedes Modul im Player wird sowohl auf Benutzer- als auch auf Modulebene verfolgt. Dies führt zu einer Situation, in der der Fortschritt eines Benutzers überschrieben wird, wenn er zu einem zuvor verwendeten Gebietsschema für dasselbe Modul zurückkehrt.

Wenn ein Teilnehmer beispielsweise 75 % Fortschritt in Gebietsschema A (Englisch) erzielt und dann nach der Rückkehr zu Gebietsschema A zu Gebietsschema B (Spanisch) wechselt, wird sein Fortschritt auf 0 % zurückgesetzt, anstatt von 75 % fortgesetzt zu werden.

Um diese Einschränkungen zu beheben, wurde die Funktion verbessert und unterstützt jetzt die gebietsschemaspezifische Fortschrittsverfolgung:

* **Gebietsschemaspezifischer Speicher**: Wenn ein Teilnehmer im Player das Gebietsschema wechselt (z. B. von Gebietsschema A zu Gebietsschema B), speichert Adobe Learning Manager den Fortschrittsstatus jetzt separat für jedes Gebietsschema des Inhalts.
* **Fortsetzen des Fortschritts**: Wenn der Benutzer wieder zu einem zuvor verwendeten Gebietsschema wechselt (von Gebietsschema B zurück zu Gebietsschema A), wird der Inhalt an der Stelle fortgesetzt, an der er an diesem bestimmten Gebietsschema aufgehört hat.
* **Unabhängige Fortschrittsverfolgung**: Jedes Gebietsschema behält seinen eigenen Fortschrittsstatus bei, sodass Teilnehmer Inhalte in mehreren Sprachen erkunden können, ohne ihren individuellen Fortschritt in jeder Sprache zu verlieren.

Die folgenden Inhaltstypen werden für den sprachbasierten Teilnehmerfortschritt nicht unterstützt:

* Video- und Audioinhalte werden nicht unterstützt.
* Inhalte von Drittanbietern, einschließlich Go1, LinkedIn Learning, getAbstract und Harvard ManageMentor, werden nicht unterstützt.
* Für den Inhalt, der keine Daten an den Learning Record Store (LRS) sendet, wird der Fortschritt nicht verfolgt oder gespeichert.
* Benutzer von mobilen Apps können den Fortschritt dieser Funktion im Offline-Modus nicht verfolgen.

Weitere Informationen zum sprachbasierten Teilnehmerfortschritt finden Sie unter [Eigenes Lernen](/help/migrated/learners/feature-summary/courses.md#language-based-progress-management).

## Inkrementelle und multiinkrementelle Unterstützung für benutzerdefinierte Rollen

Adobe Learning Manager unterstützt jetzt inkrementelle und multiinkrementelle Importe für benutzerdefinierte Rollen und Rollenzuweisungen. Bei inkrementellen Importen können Administratoren nur neue, aktualisierte oder gelöschte Datensätze der Benutzer hochladen, anstatt die gesamte CSV-Datei erneut hochzuladen.

Multiinkrementelle Importe erweitern diese Möglichkeit, indem große Organisationen inkrementelle Dateien nach Region oder Abteilung aufteilen (z. B. USA, EU, APAC) und parallel verarbeiten können. Adobe Learning Manager unterstützt außerdem bis zu 20 inkrementelle Benutzer-CSVs und die entsprechenden CSVs für benutzerdefinierte Rollen, sodass sie für große Vorgänge skalierbar sind.

Administratoren können jetzt Rollen- und Benutzerrollendateien (role.csv und user_role.csv) inkrementell zusammen mit Benutzerdateien (user.csv) hochladen, anstatt immer vollständige Uploads vorzunehmen. Jeder Benutzerimport (user1.csv) ist mit seinen eigenen Rollen- und Rollenzuordnungsdateien (user1_role.csv, user1_user_role.csv) verknüpft, die in separaten FTP-Ordnern gespeichert sind.

Die folgenden drei zusätzlichen Spalten wurden den folgenden CSVs hinzugefügt:

* Benutzerregistrierungsstatus (user.csv): Gibt den aktuellen Registrierungsstatus des Benutzers im System an (z. B. aktiv, inaktiv oder gelöscht).
* Rollenstatus (role.csv): Gibt an, ob eine benutzerdefinierte Rolle derzeit im Konto aktiv oder inaktiv ist.
* Benutzerrollenstatus (user_role.csv): Definiert den Status der Zuordnung zwischen einem Benutzer und einer Rolle und zeigt an, ob die Zuordnung aktiv ist oder entfernt wurde.

Die Adobe Learning Manager erfasst jetzt das Hinzufügen, Aktualisieren und Löschen von Aktionen in den Benutzerprüfungs- und benutzerdefinierten Rollenberichten, sodass Administratoren Änderungen besser einsehen können.

>[!NOTE]
>
>Diese Änderungen gelten nur für Konten, die inkrementelle Benutzer verwenden.

Weitere Informationen zur inkrementellen und multiinkrementellen Unterstützung für benutzerdefinierte Rollen finden Sie unter [Inkrementelle und multiinkrementelle Unterstützung für benutzerdefinierte Rollen](/help/migrated/integration-admin/feature-summary/configure-role-csv-files.md#incremental-and-multi-incremental-support-for-custom-roles).

## Verbesserungen der Go1-Integration

Die Go1-Integration wurde verbessert, um die direkte Kuratierung von Go1-Kursen zum Erstellen von Lernprogrammen (LP) in Adobe Learning Manager zu ermöglichen. Dieses Update unterstützt die Einbindung von Go1-Kursen in wiederkehrende Zertifizierungen und führt eine neue Version des Go1-Content-Hub-Erlebnisses ein, die eine effizientere Kurskuration ermöglicht.

* Erstellen und verwalten Sie Playlist(s) direkt in Go1 mithilfe von KI-Chat-Unterstützung oder manueller Auswahl.
* Schließen Sie Go1-Kurse in wiederkehrende Zertifizierungszyklen mit automatischem Zurücksetzen des Fortschritts ein. Weitere Informationen zum Erstellen von Zertifikaten finden Sie unter [Zertifizierungen](/help/migrated/administrators/feature-summary/certifications.md).
* Aktualisierte Benutzeroberfläche für die Inhaltserkennung für eine verbesserte Suche und Kuration von Inhalten.

**Wichtige Hinweise**

* Für alle Go1-Funktionen ist eine aktive Go1-Lizenz erforderlich.
* Frühere kostenlose Go1-Inhalte werden eingestellt. Unternehmen müssen die erforderlichen Content-Pakete in der Vorschau anzeigen und erwerben.
* Administratoren und Autoren können Wiedergabelisten erstellen und verwalten. Teilnehmer behalten den schreibgeschützten Zugriff.

Zeigen Sie [Go1-Kurse für den Lernpfad kuratieren](/help/migrated/administrators/feature-summary/content-marketplace/curate-go1-playlist.md) an, um weitere Informationen zum Hinzufügen von Go1-Kursen zum Lernpfad zu erhalten.

## Unterstützung für Video-URLs im Aktivitätsmodul

Das Aktivitätsmodul unterstützt jetzt das Einbetten von Vimeo-URLs, ähnlich wie bei YouTube-Einbettungen. Dank dieser Verbesserung können Administratoren Vimeo-Videolinks direkt zum Aktivitätsmodul hinzufügen. Wenn Autoren einen Kurs erstellen und ein Aktivitätsmodul hinzufügen, sehen sie jetzt eine Option zum Einfügen einer Vimeo-URL. Ähnlich wie YouTube-Links hinzugefügt werden, können Autoren einen Vimeo-Link direkt in das Modul-Setup einfügen. Nach der Veröffentlichung können die Teilnehmer das Vimeo-Video nahtlos in der Teilnehmer-App wiedergeben, ohne außerhalb der Plattform umgeleitet zu werden.

Weitere Informationen zum Hinzufügen von Modulen zu den Kursen finden Sie unter [Module hinzufügen](/help/migrated/authors/feature-summary/courses.md#add-modules).

## Zeitzoneninformationen für CR/VC-Module

Details zur Zeitzone werden jetzt für Klassenzimmermodule (CR) und virtuelle Klassenzimmermodule (VC) auf der Seite &quot;Kursübersicht&quot;, der Instanzseite, der Seite &quot;Teilnehmervorschau&quot; und im Kalender-Widget angezeigt. Teilnehmer und Administratoren können die Zeitzone, die mit geplanten Sitzungen verknüpft ist, auf wichtigen Seiten und in Kalendereinladungen deutlich sehen. Die Teilnehmer können Sitzungen besser planen und beitreten, ohne Missverständnisse bei der Zeitzone. Diese Verbesserung ist nur in der Immersive Learner-App verfügbar.

Teilnehmer in verschiedenen Regionen können die Sitzungszeit in der richtigen Zeitzone bestätigen. Durch eine klare Anzeige der Zeitzone können verpasste Sitzungen verhindert und eine präzise Kalenderplanung sichergestellt werden.

## Automatisches Ausfüllen des Namens des Autors beim Erstellen eines Kurses

Während der Kurserstellung wird das Feld **[!UICONTROL Autor(en)]** jetzt automatisch mit dem Namen der Autoren ausgefüllt, die den Kurs erstellen. Autoren müssen ihre eigenen Namen nicht mehr manuell eingeben. Weitere Autoren können nach wie vor hinzugefügt oder aktualisiert werden.

Bei Organisationen mit strengen Inhaltseigentumsregeln stellt die automatische Auffüllung sicher, dass die Autoren immer korrekt zugeordnet werden. Wenn Sie einen vorhandenen Kurs bearbeiten, können Autoren Co-Autoren aktualisieren oder hinzufügen, ohne den automatisch ausgefüllten Eintrag zu verlieren.

Weitere Informationen zum Erstellen eines Kurses finden Sie unter [Kurs erstellen](/help/migrated/authors/feature-summary/courses.md#create-a-course---advanced-workflow).

## Externe Profile beim Ändern des Profils suchen

Zuvor scrollten Administratoren durch die gesamte Liste der externen Profile und wählten das gewünschte Profil manuell aus, wenn sie Teilnehmer neu zuweisen. Dies machte den Prozess zeitaufwendig, insbesondere für Konten mit vielen Profilen. Dank dieser Verbesserung können Administratoren und benutzerdefinierte Administratoren jetzt direkt auf der Registerkarte während des Workflows zum Ändern des Profils nach externen Profilen suchen.

**Anwendungsfälle**

* Bei Konten mit Hunderten von externen Profilen (z. B. Franchise-Standorte, Partnerunternehmen oder regionale Gruppen) können Administratoren das genaue Profil jetzt sofort mithilfe der Suche finden, wodurch Fehler reduziert und Zeit gespart werden können.
* Bei organisatorischen Änderungen wie Zusammenschlüssen oder Neuausrichtungen von Abteilungen müssen die Teilnehmer möglicherweise gesammelt auf neue externe Profile verschoben werden. Durch die suchbasierte Neuzuweisung wird diese Aufgabe reibungsloser und genauer.

Weitere Informationen zum Ändern des Profils finden Sie unter [Externes Profil ändern](/help/migrated/administrators/feature-summary/add-users-user-groups.md#change-profile).

## Einen Co-Organizer für Microsoft Teams-Sitzungen hinzufügen

Bisher konnten Autoren Microsoft Teams-Sessions nur einen einzigen Organisator zuweisen. Dank dieser Verbesserung können Administratoren jetzt Co-Organizer zu einer Sitzung hinzufügen. Ein neues Feld, **[!UICONTROL Co-Organizer]**, wurde in Microsoft Teams-Sessions eingeführt, sodass Autoren zusätzliche Organisatoren neben dem primären Organisator zuweisen können.

Autoren können für jede Microsoft Teams-Session mehrere Co-Organisatoren zuweisen. Mitorganisatoren haben den gleichen Zugriff und die gleichen Berechtigungen wie der primäre Organisator. Autoren können bis zu 10 Organisatoren pro Sitzung hinzufügen, was mehr Flexibilität bietet und die Sitzungsverwaltung verbessert.

**Anwendungsfall**

Bei umfangreichen Sessions mit vielen Teilnehmern können Co-Organisatoren dabei helfen, die Anwesenheit zu verwalten, Diskussionen zu moderieren und den Chat zu überwachen, während der primäre Organisator sich auf die Durchführung der Schulung konzentriert.

Im Artikel [Module hinzufügen](/help/migrated/authors/feature-summary/courses.md#add-modules) finden Sie weitere Informationen zum Hinzufügen von CR/VC-Sitzungen zu den Kursen.

## Bericht zu interessierten Teilnehmern herunterladen

Wenn ein Administrator alle Kursinstanzen einstellt (z. B. am Ende des Kurslebenszyklus), wird die Schaltfläche **[!UICONTROL Registrieren]** auf der Seite **[!UICONTROL Kursübersicht]** durch die Option [!UICONTROL Interesse registrieren] ersetzt. Teilnehmer können diese Option auswählen, um ihr Interesse an der Teilnahme am Kurs zu bekunden. Administratoren können jetzt eine Liste von Teilnehmern anzeigen und exportieren, die Interesse an einem Kurs registriert haben.

Administratoren können dann auf diese Liste zugreifen und sie als Bericht herunterladen. Eine **[!UICONTROL Schaltfläche für interessierte Teilnehmer]** wurde der Kursseite hinzugefügt, wenn keine aktiven Instanzen verfügbar sind. Hier werden der Name des Teilnehmers und das Datum, an dem er Interesse registriert hat, in der Administrator-Benutzeroberfläche angezeigt.

Administratoren können die **[!UICONTROL Aktionen]** auswählen und dann **[!UICONTROL Bericht exportieren]** auswählen, um den **[!UICONTROL Bericht für interessierte Teilnehmer]** zu exportieren.

![](assets/register-interest.png)
_Abschnitt &quot;Kursübersicht&quot;, in dem Teilnehmer die Option &quot;Interesse registrieren&quot; anzeigen können_

[Laden Sie den interessierten Teilnehmer herunter](/help/migrated/administrators/feature-summary/courses.md#download-the-interested-learner-report), um weitere Informationen zu erhalten.

## Empfehlungen in der Salesforce-App zurücksetzen

Früher konnten Teilnehmer, die die Adobe Learning Manager Salesforce-App verwendeten, Rollen und Empfehlungsvoreinstellungen nur einmal auswählen. Wenn sich ihre Rolle geändert hat, mussten sie zur nativen Adobe Learning Manager-App wechseln, um ihr Profil zu aktualisieren und die entsprechenden Kursempfehlungen zu erhalten. Mit der neuesten Erweiterung können Teilnehmer jetzt ihre Voreinstellungen direkt in der Salesforce-App schnell zurücksetzen, wenn sich ihre Rolle, ihr Team oder ihre Zuständigkeiten ändern.

Dieser optimierte Prozess stellt sicher, dass sie weiterhin aktuelle, relevante Kursempfehlungen erhalten, ohne Salesforce verlassen zu müssen. Administratoren profitieren von höheren Lern-Abschlussraten und einer besseren Ausrichtung zwischen Benutzerrollen und empfohlenen Inhalten, ohne zusätzliche Unterstützung oder Anleitung beim Plattformwechsel zu geben.

Adobe Learning Manager verfügt jetzt über die Schaltfläche **[!UICONTROL Interessen zurücksetzen]** in der Salesforce-App. Teilnehmer können jetzt ihre Rollen und Lernvoreinstellungen zurücksetzen, ohne Salesforce verlassen oder sich bei der nativen Adobe Learning Manager-App anmelden zu müssen.

Weitere Informationen zu den Rücksetzempfehlungen in der Salesforce-App finden Sie unter [Empfehlungen in der Salesforce-App zurücksetzen](/help/migrated/learners/feature-summary/sfdc-app.md#reset-recommendations-in-salesforce-app).

## Verbesserung des Kalender-Widgets

Teilnehmer können jetzt sowohl frühere als auch bevorstehende Sitzungen im Kalender-Widget sehen. Sie können den Kalender an einem beliebigen Datum durchlaufen und die Sitzungsdetails überprüfen. Das bedeutet, dass sie bereits durchgeführte Sitzungen überprüfen und verfolgen können, was sie versäumt oder besucht haben. Außerdem können sie alle bevorstehenden Sessions der nächsten 24 Monate (inklusive des aktuellen Monats) im Blick haben. So lassen sich Terminpläne leichter im Voraus planen und verwalten.

Weitere Informationen zum Kalender-Widget finden Sie unter [Kalender](/help/migrated/learners/feature-summary/learner-home-page.md#calendar).

## Benutzer in sozialen Boards markieren

Soziale Boards unterstützen jetzt Benutzer-Tagging-Funktionen, die zielgerichtetere Diskussionen und eine verbesserte Zusammenarbeit innerhalb von Lern-Communities ermöglichen. Teilnehmer können in Social-Learning-Beiträgen und Kommentaren über die Teilnehmer-App, APIs und die Adobe Learning Manager-Referenzseite mit Tags versehen werden.

Benutzer außerhalb des Bereichs des Boards können nicht mit Tags versehen werden, um unerwünschte Benachrichtigungen zu verhindern. Wenn ein mit Tags versehener Benutzer aus dem System gelöscht wird, wird er als &quot;anonym&quot; erwähnt. Das Markieren von Benutzergruppen oder &quot;@all&quot; ist nicht zulässig, um Benachrichtigungs-Spam zu verhindern.

* **@username Tagging**: Benutzer können andere Board-Mitglieder mithilfe des Formats &quot;@username&quot; mit Tags versehen.
* **Bereichsbeschränktes Tagging**: Nur Benutzer mit Zugriff auf das jeweilige Board können markiert werden, um Datenschutz und Relevanz zu gewährleisten.
* **Multi-Channel-Benachrichtigungen**: Benutzer mit Tags erhalten sowohl In-App- als auch E-Mail-Benachrichtigungen mit direkten Links zu relevanten Beiträgen oder Kommentaren.

**Anwendungsfälle**

* Fachkräfte im Gesundheitswesen, die Anregungen von bestimmten Kollegen zu medizinischen Fällen benötigen: Durch Tagging können Ärzte und Krankenschwestern schnell die richtigen Spezialisten benachrichtigen und so eine zeitnahe und präzise Beratung zu komplexen Patientenfällen gewährleisten.
* Fachexperten werden zu speziellen Themen konsultiert: Durch Tagging von Experten können Teams die richtigen Personen direkt einbeziehen, die Reaktionszeit verkürzen und die Entscheidungsfindung bei technischen oder Nischenanfragen verbessern.
* Teamdiskussionen, die Beiträge von bestimmten Stakeholdern erfordern: Durch das Markieren von Stakeholdern wird sichergestellt, dass die relevanten Entscheidungsträger über Aktualisierungen informiert sind und Beiträge liefern können, sodass Projekte auf Kurs bleiben und an den Geschäftszielen ausgerichtet sind.

Weitere Informationen zum Taggen von Benutzern in sozialen Boards finden Sie unter [Benutzer-Tagging in sozialen Boards](/help/migrated/learners/feature-summary/social-learning-web-user.md#tag-users-in-social-board-posts).

## Berechtigungen für Ankündigungsbereiche für benutzerdefinierte Administratoren

Benutzerdefinierte Administratoren können jetzt Ankündigungen erstellen, jedoch nur für ihre zugewiesenen Benutzergruppen oder Kataloge. Dadurch wird eine unbeabsichtigte Kommunikation über Organisationsgrenzen hinweg verhindert. Benutzerdefinierte Administratoren können Ankündigungen nur für Benutzer innerhalb ihres zugewiesenen Bereichs erstellen. Ankündigungen können auf bestimmte Benutzergruppen oder Kataloge beschränkt werden. Vollständige Administratoren behalten die Sichtbarkeit und Kontrolle über alle Ankündigungen, einschließlich der von benutzerdefinierten Administratoren mit Umfang erstellten Ankündigungen.

**Wichtigste Vorteile**

* Zielgerichtete Kommunikation, die sicherstellt, dass Ankündigungen nur die relevanten Zielgruppen erreichen.
* Verringerte Informationsüberlastung, indem verhindert wurde, dass irrelevante Benachrichtigungen unbeabsichtigte Benutzer erreichen.
* Behält Organisationsgrenzen bei und verhindert eine versehentliche Kommunikation.

**Wichtige Hinweise**

* Wenn sich der Umfang eines benutzerdefinierten Administrators ändert, wird für die betroffenen Ankündigungen ein Warnsymbol angezeigt und es müssen einzelne Bereichsvorgaben zurückgesetzt werden.
* Jede Ankündigung muss einzeln aktualisiert werden, wenn sich der Umfang ändert.
* Der Bericht [Benachrichtigungsankündigung](/help/migrated/administrators/feature-summary/announcements.md) zeigt nur Teilnehmer im zugewiesenen Bereich des benutzerdefinierten Administrators an.

**Anwendungsfälle**

* Franchiseorganisationen, bei denen regionale Manager nur mit ihren Franchisenehmern kommunizieren müssen.
* Große Organisationen mit Regional- oder Abteilungsadministratoren, die Ankündigungen an ihre Teams senden.

Weitere Informationen zum Erstellen einer Ankündigung für den zugewiesenen Bereich finden Sie unter [Ankündigung für den zugewiesenen Bereich erstellen](/help/migrated/administrators/feature-summary/announcements.md#create-announcement-for-the-assigned-scope).

## Benutzerdefinierte Rolle beim Veröffentlichen von Inhalten aus Adobe Captivate auswählen

Wenn ein Benutzer beim Veröffentlichen von Inhalten aus Adobe Captivate in Adobe Learning Manager über mehrere benutzerdefinierte Rollen verfügt, wird er aufgefordert, die spezifische benutzerdefinierte Rolle auszuwählen, unter der der Kurs veröffentlicht werden soll. Dies stellt sicher, dass die richtigen Rolleneigentümer und Berechtigungen auf den veröffentlichten Kurs angewendet werden.

Weitere Informationen zum Erstellen benutzerdefinierter Rollen für die Benutzer finden Sie unter [Benutzerdefinierte Rolle](/help/migrated/administrators/feature-summary/custom-role.md).

## Verbesserungen am Widget &quot;Von mir gespeichert&quot;

Wenn Sie zuvor den Streifen **[!UICONTROL Von mir gespeichert]** ausgewählt haben, wurden alle im Katalog verfügbaren Kurse angezeigt. Jetzt sehen die Teilnehmer nur ihre mit einem Lesezeichen versehenen Kurse im Streifen **[!UICONTROL Von mir gespeichert]** auf der Teilnehmer-Startseite. Wenn Sie diesen Streifen auswählen, gelangen die Teilnehmer zur Katalogseite, auf der nur die Kurse angezeigt werden, die sie gespeichert haben.

Innerhalb des Katalogs können Teilnehmer zusätzliche Filter anwenden, um ihre Suche einzugrenzen. Wenn ein Filter angewendet wird, werden nur Kurse angezeigt, die die ausgewählten Kriterien erfüllen. Zuvor mit Lesezeichen versehene Kurse werden nur angezeigt, wenn sie mit dem angewendeten Filter übereinstimmen.

Weitere Informationen zum Widget für gespeicherte Kurse auf AEM Sites finden Sie unter [Konfigurieren von Widgets für gespeicherte Kurse auf AEM Sites](/help/migrated/integrate-aem-learning-manager.md#configure-my-saved-courses-widgets-in-aem-sites).

## Unterstützung für die Anzeige der Autorennamen in freigegebenen Kursen

Wenn ein Kurs zuvor für ein [Peer-Konto](/help/migrated/administrators/feature-summary/peer-account.md) freigegeben wurde, erschien der Autor als externer Autor. Kurse zeigen jetzt den Namen des Autors an, unabhängig davon, ob es sich um einen internen Benutzer des Hauptkontos oder einen älteren Autor handelt (d. h. um einen Namen, der während der Kurserstellung als Zeichenfolge in das Feld &quot;Autoren&quot; eingegeben wurde). Wenn Sie einen Autor auswählen, wird die Anzahl der Kurse angezeigt, die sie für das Peer-Konto freigegeben haben. Diese Autoren sind jedoch keine tatsächlichen Benutzer im Peer-Konto.

Wenn ein Benutzer aus dem Hauptkonto gelöscht wird, werden seine Daten dort entfernt, die Autoreninformationen verbleiben jedoch in allen Peer-Konten, in denen sein Inhalt freigegeben wurde.

>[!NOTE]
>
>Dies ist eine kennzeichenbasierte Funktion. Wenden Sie sich an unser Support-Team unter [learningmanagersupport@adobe.com](mailto:learningmanagersupport@adobe.com), um diese Option zu aktivieren.

In [Peer-Konto](/help/migrated/administrators/feature-summary/peer-account.md) finden Sie weitere Informationen zum Freigeben von Inhalten für Peer-Konten.

## Suchsichtbarkeit für Lernobjekte niedrigerer Reihenfolge

Früher wurden einzelne Kurse in Suchergebnissen nicht durchgehend angezeigt, wenn sie Teil von Lernobjekten höherer Ordnung waren, z. B. Lernpfade oder Zertifizierungen. Wenn ein Teilnehmer nur für einen Lernpfad oder eine Zertifizierung registriert war, ergab die Suche nur die Struktur mit der höheren Reihenfolge und nicht den individuellen Kurs.

Dank dieser Verbesserung können Teilnehmer jetzt einzelne Kurse in Suchergebnissen sehen, auch wenn diese Kurse Teil von Lernpfaden oder Zertifizierungen sind. Eine neue Administratoreinstellung, **[!UICONTROL Alle registrierten Kurse in den Suchergebnissen anzeigen]**, wurde eingeführt. Wenn diese Einstellung aktiviert ist, wird bei der Suche nach einem bestimmten Kurs immer der Kurs selbst zusammen mit allen zugehörigen Lernpfaden oder Zertifizierungen angezeigt.

Weitere Informationen zu allgemeinen Einstellungen finden Sie unter [Einstellungen](/help/migrated/administrators/feature-summary/settings.md#general-settings).

## API-Änderungen

### Verbesserungen der Migrations-API

Adobe Learning Manager unterstützt jetzt die Migration verschiedener Datenobjekte in ein Konto über den Migrationsvorgang. Dieser Prozess kann sowohl über APIs als auch über die Benutzeroberfläche initiiert werden. Wenn eine Migration fehlschlägt, können Fehler über die Oberfläche heruntergeladen werden. Diese Fehler sind nützlich beim Debuggen von Migrationsfehlern und beim Verwalten der Migrationsläufe.

Mit dieser Version stehen die Fehlerprotokolle auch über die APIs zum Download zur Verfügung, um eine effiziente, programmgesteuerte Fehlerverfolgung und Fehlersuche zu ermöglichen.

**API-Änderungen**

Es gibt eine neue Migrations-API, &quot;`runStatus`&quot;, mit der Integrationsadministratoren den Status von Migrationsläufen überprüfen können, die über die API ausgelöst wurden. Dies ist in früheren Versionen von Adobe Learning Manager nicht möglich.

Darüber hinaus stellt die `runStatus`-API jetzt einen direkten Link zum Herunterladen von Fehlerprotokollen (CSV) für abgeschlossene Ausführungen bereit. Beachten Sie, dass der Link nur sieben Tage lang gültig ist und die Protokolle einen Monat lang aufbewahrt werden.

Die Antwort der `startRun`-API wurde aktualisiert und enthält nun die ID des Migrationsprojekts, die Sprint-ID und die Sprint-Lauf-ID, die zum Abfragen des neuen Statusendpunkts erforderlich sind.

#### runStatus-API

**Beschreibung**

Ruft den Status eines vorhandenen Migrationslaufs ab.

**Endpunkt**

```
GET /bulkimport/runStatus
```

**Parameter**

* **migrationProjectId**: (Erforderlich). Ein eindeutiger Bezeichner für ein Migrationsprojekt. Ein Migrationsprojekt wird verwendet, um Daten und Inhalte aus einem vorhandenen LMS (Learning Management System) in Adobe Learning Manager zu übertragen. Jedes Migrationsprojekt kann aus mehreren Sprints bestehen, die kleinere Einheiten von Migrationsaufgaben sind.

* **sprintId**: (Erforderlich). Ein eindeutiger Bezeichner für einen Sprint innerhalb eines Migrationsprojekts. Ein Sprint ist eine Teilmenge von Migrationsaufgaben, die bestimmte Lernobjekte (z. B. Kurse, Module, Teilnehmerdatensätze) umfasst, die von einem bestehenden LMS zu Adobe Learning Manager migriert werden sollen. Jeder Sprint kann unabhängig ausgeführt werden, was eine phasengesteuerte Migration ermöglicht.

* **sprintRunId**: (Erforderlich). Eine eindeutige Kennung, die zum Verfolgen der Ausführung eines bestimmten Sprints innerhalb eines Migrationsprojekts verwendet wird. Es ist mit dem eigentlichen Migrationsvorgang für die in einem Sprint definierten Elemente verknüpft. Die sprintRunId hilft bei der Überwachung, Fehlerbehebung und Verwaltung des Migrationsauftrags.

**Antwort**

```
{
  "sprintId": 2510080,
  "sprintRunId": 2740845,
  "migrationProjectId": 2509173,
  "startTime": 1746524711052,
  "endTime": 1746524711052,
  [
    {
      "id": 2609923,
      "lastHeartbeatTime": 1746524711052,
      "objectName": "content",
      "jobState": "COMPLETED",
      "errorCsvLink": "",
      "errorLogLink": "migration/5830/2509173/2510080/2740845/content_err.csv",
      "sequenceNumber": 1
    },
    {
      "id": 2609922,
      "lastHeartbeatTime": 1746524713577,
      "objectName": "course",
      "jobState": "WAITING_IN_QUEUE",
      "errorCsvLink": "",
      "errorLogLink": null,
      "sequenceNumber": 2
    }
  ]
}
```

#### startRun-API

Die `startRun`-API-Antwort wurde aktualisiert und enthält drei zusätzliche Felder: migrationProjectId, sprintId und sprintRunId. Mithilfe dieser Felder können Benutzer den Status bestimmter Migrationsausführungen mithilfe der neuen runStatus-API verfolgen und abfragen.

```
curl -X GET --header 'Accept: text/html' 'https://learningmanager.adobe.com/primeapi/v2/bulkimport/runStatus?migrationProjectId=001&sprintId=10001&sprintRunId=7'
```

Erstellt die folgende Antwort. Die Antwort enthält:

* `migrationId`
* `sprintId`
* `sprintRunId`

**Antwort**

```
{
  "status": "OK",
  "title": "BULKIMPORT_RUN_INITIATED_SUCCESSFULLY",
  "source": {
    "info": "Success",
    "migrationInfo": {
      "migrationProjectId": "001",
      "sprintId": "10001",
      "sprintRunId": "7"
    }
  }
}
```

Weitere Informationen zum Migrieren von Inhalten aus einem vorhandenen LMS finden Sie im [Migrationshandbuch](/help/migrated/integration-admin/feature-summary/migration-manual.md).

### Änderungen an der Social-API (Benutzer-Tag, Kommentare und Antworten)

Adobe Learning Manager unterstützt jetzt @user Tagging-Funktionen in sozialen Boards, mit denen Teilnehmer Peers in Beiträgen, Kommentaren und Antworten erwähnen und benachrichtigen können. Diese Funktion verbessert die Zusammenarbeit und die Suche nach Inhalten auf der gesamten Plattform.

Diese Version enthält neue API-Funktionen zur Unterstützung von Benutzererwägungen, einschließlich verbesserter POST- und GET-Endpunkte, sowie eine neue Suchfunktion für Benutzer mit Tags.

**Übersicht über API-Änderungen**

* Aktualisierte POST-APIs zum Erstellen von Beiträgen/Kommentaren/Antworten mit Benutzererwägungen
* Aktualisierte GET-APIs mit Benutzererwähnungsdaten in Antworten

**Format der Benutzererwägungen**

Ein Benutzer wird im folgenden Format erwähnt: @(Benutzer:userId)

#### Beitrag mit Erwähnungen erstellen

**Endpunkt**

```
POST /primeapi/v2/posts
```

**Beschreibung**

Erstellen Sie einen neuen Social-Learning-Beitrag mit Benutzererwägungen.

**Anforderungstext**

```
{
  "data": {
    "type": "post",
    "attributes": {
      "boardId": 13282,
      "accountId": 11152,
      "text": "<p>This is a new post mentioning @[user:11257229]</p>",
      "createdByUserId": 11257228,
      "postType": "discussion"
    },
    "id": null
  }
}
```

**Antwort**

Standardantwort nach der Erstellung mit Erwähnungsdaten in der Beziehung _userMentions_.

#### Kommentar mit Erwähnungen erstellen

**Endpunkt**

```
POST /primeapi/v2/comments
```

**Beschreibung**

Fügen Sie einem Beitrag einen Kommentar mit Benutzererwägungen hinzu.

**Anforderungstext**

```
{
  "data": {
    "type": "comment",
    "attributes": {
      "postId": 20746,
      "accountId": 11152,
      "text": "<p>Test Comment @[user:11257229]</p>",
      "createdByUserId": 11257228,
      "commentLevel": 0
    },
    "id": null
  }
}
```

#### Antwort mit Erwähnungen erstellen

**Endpunkt**

```
POST /primeapi/v2/replies
```

**Beschreibung**

Antworten Sie auf einen Kommentar mit Benutzererwägungen.

**Anforderungstext**

```
{
  "data": {
    "type": "reply",
    "attributes": {
      "postId": 20746,
      "accountId": 11152,
      "text": "<p>Thanks for the update @[user:11257229]</p>",
      "createdByUserId": 11257228,
      "commentLevel": 1,
      "parentCommentId": 55621
    },
    "id": null
  }
}
```

#### Beiträge mit Erwähnungen abrufen

**Endpunkt**

```
GET /primeapi/v2/posts/{id}
```

**Beschreibung**

Rufen Sie Beitragsdetails ab, einschließlich der genannten Benutzer.

**Antwort**

```
{
  "links": {
    "self": "https://learningmanager.adobe.com/primeapi/v2/posts/7522"
  },
  "data": {
    "id": "7522",
    "type": "post",
    "attributes": {
      "commentCount": 3,
      "dateCreated": "2025-06-10T11:33:29.000Z",
      "dateUpdated": "2025-06-25T14:52:04.000Z",
      "downVote": 0,
      "postingType": "DEFAULT",
      "richText": "<p>my updated fourth post @[user:14707776] second mention my first post</p>",
      "state": "ACTIVE",
      "text": "my updated fourth post @[user:14707776] second mention my first post",
      "upVote": 0,
      "viewsCount": 0
    },
    "relationships": {
      "createdBy": {
        "data": {
          "id": "14707776",
          "type": "user"
        }
      },
      "parent": {
        "data": {
          "id": "3971",
          "type": "board"
        }
      },
      "userMentions": {
        "data": [
          {
            "id": "14707776",
            "type": "user"
          }
        ]
      }
    }
  },
  "included": [
    {
      "id": "14707776",
      "type": "user",
      "attributes": {
        "avatarUrl": "https://cpcontents.adobe.com/public/images/default_user_avatar.svg",
        "binUserId": "45664b87-75a3-43ec-b0b7-5064958eac6f",
        "email": "user@example.com",
        "enrollOnClick": false,
        "fields": {
          "Location": "BLR"
        },
        "gamificationEnabled": true,
        "lastLoginDate": "2025-06-27T11:21:17.000Z",
        "name": "John Doe",
        "pointsEarned": 1690,
        "pointsRedeemed": 0,
        "preferredResolution": "AUTO",
        "profile": "admin",
        "roles": [
          "Learner",
          "Admin",
          "Author",
          "Instructor",
          "Integration Admin",
          "Manager"
        ],
        "state": "ACTIVE",
        "userType": "Internal"
      },
      "relationships": {
        "account": {
          "data": {
            "id": "9238",
            "type": "account"
          }
        }
      }
    }
  ]
}
```

### Änderungen an der Social-API (Benutzersuche)

**Endpunkt**

```
GET /primeapi/v2/users/search?q={searchTerm}&context=tagging
```

**Beschreibung**

Suche nach Benutzern, die für Tagging verfügbar sind, basierend auf den Einstellungen des sozialen Bereichs.

**Anforderungsparameter**


* q (erforderlich): Suchbegriff (mindestens 3 Zeichen).
* context: Setzen Sie die Option auf &quot;Tagging&quot;, damit Benutzer für Erwähnungen berechtigt sind.
* boardId (optional): Board-ID, um Benutzer basierend auf Zugriffsberechtigungen zu filtern.

**Antwort**

```
{
  "data": [
    {
      "id": "11257229",
      "type": "user",
      "attributes": {
        "name": "Jane Smith",
        "email": "jane.smith@example.com",
        "avatarUrl": "https://cpcontents.adobe.com/public/images/default_user_avatar.svg",
        "userType": "Internal",
        "state": "ACTIVE"
      }
    }
  ]
}
```

### Verbesserungen an der Teilnehmer-API für die Quizleistungsverfolgung

Die `GET /loResourceGrades`-API wurde verbessert, um detaillierte Quizleistungsdaten bereitzustellen, die eine ausgefeiltere Analyse und eine automatisierte Entscheidungsfindung ermöglichen.

Die API-Antwort enthält jetzt zwei zusätzliche Felder:

* **[!UICONTROL höchste Punktzahl]**: Die beste Punktzahl, die ein Teilnehmer bei allen Quizversuchen erzielt hat
* **[!UICONTROL maxScore]**: Die gesamte mögliche Punktzahl für das Quiz

**Beispiel für API-Antwort**

```
{
    "links": {
        "self": "https://learningmanagerstage1.adobe.com/primeapi/v2/loResourceGrades/course:15067_30122_41715_1_3400468"
    },
    "data": {
        "id": "course:15067_30122_41715_1_3400468",
        "type": "learningObjectResourceGrade",
        "attributes": {
            "completed": false,
            "duration": 0,
            "hasPassed": false,
            "highestScore": 0,
            "maxScore": 0,. 
            "progressPercent": 0,
            "score": 0
        },
        "relationships": {
            "loResource": {
                "data": {
                    "id": "course:15067_30122_41715_1",
                    "type": "learningObjectResource"
                }
            }
        }
    }
}
```

Als Antwort ist **Kurs:15067_30122_41715_1_3400468** die ID der Lernobjektressourcenklasse, für die die Informationen angefordert werden. Die `learningObjectResourceGrad`e-ID kann von der `GET /enrollments/{id}`-API abgerufen werden.

### API-Antworten unterstützen die Groß- und Kleinschreibung für Autorennamen

Die API-Antwort gibt jetzt die genaue Groß- und Kleinschreibung der alten Autorennamen an, die während der Kurserstellung oder -aktualisierung eingegeben wurden. Dadurch wird sichergestellt, dass Namen konsistent auf der Teilnehmer-Benutzeroberfläche und in öffentlichen APIs angezeigt werden.

* Wenn ein neuer Autorenname hinzugefügt wird, wird die Anfrage gespeichert und genau wie eingegeben zurückgegeben.
* Wenn ein vorhandener Autorenname entfernt und mit einer anderen Groß-/Kleinschreibung erneut hinzugefügt wird, wird die aktualisierte Groß-/Kleinschreibung berücksichtigt und in allen Kursen widergespiegelt, die diesen Autorennamen verwenden.
* Für zuvor gespeicherte Namen wird keine automatische Migration ausgeführt. Nur neu hinzugefügte oder aktualisierte Namen folgen diesem Verhalten.

### API-Erweiterung für Kalender

Der Kalender lädt jetzt die Sitzungen für den vom Benutzer ausgewählten Monat. Um sowohl frühere als auch bevorstehende Sitzungen über die API abzurufen, wurde ein neuer `year`-Parameter zum Teilnehmerendpunkt `GET /users/{id}/calendar` hinzugefügt. Die Parameter &quot;`month`&quot; und &quot;`year`&quot; müssen zusammen bereitgestellt werden, um Sitzungsdetails abzurufen.

**Beispiel-Curl**

```
curl -X GET --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth a4ae04eb9f06f4bf88abcde17' 'https://abc.adobe.com/primeapi/v2/users/12345678/calendar?month=7&year=2025&currentMonthOnly=false&filter.allSessions=false'
```

### Unterstützung für Markierungsvervollständigung über die Administrator-API

Früher hat die öffentliche API die instanzbasierte Abschlussmarkierung in Szenarien mit mehreren Registrierungen nicht unterstützt. Mit dieser Verbesserung können Sie jetzt die Kursinstanzkennung in den Anforderungstext von `POST /users/{userId}/userModuleGrade` aufnehmen, und der Administrator kann den Abschluss für eine bestimmte Instanz markieren.

### Benutzer-ID-Voreinstellungen für SCORM-Berichte festlegen

Einige Kunden benötigen die UUID des Teilnehmers (Universally Unique Identifier) anstelle der Standard-Benutzer-ID für die SCORM-Inhaltsvervollständigung. Die Verwendung der UUID bietet eine genauere Verfolgung über Lernprogramme hinweg und verhindert eine doppelte Lizenznutzung in MAU-Konten (monatlich aktiver Benutzer).

Um dies zu unterstützen, wurde eine neue Einstellung auf Kontoebene, `reporting_userid_preference`, hinzugefügt. Wenn diese Einstellung aktiviert ist, wird die UUID anstelle der Benutzer-ID gesendet, wenn Teilnehmer SCORM-Inhalte abschließen.

>[!NOTE]
>
> Wenden Sie sich an unser Support-Team unter [learningmanagersupport@adobe.com](mailto:learningmanagersupport@adobe.com), um diese Einstellung zu konfigurieren.

Das neue Attribut &quot;`reportingUserIdPreference`&quot; wurde in &quot;`get /account`&quot; eingeführt, um die Benutzer-ID-Einstellungen zu verfolgen.

### Authoring-Informationen in freigegebenen Kursen

In der Lernobjekt-API wurde die Art und Weise, wie Autorinformationen zurückgegeben werden, aktualisiert, um zwischen Hauptkontenkursen und Kursen zu unterscheiden, die für Peer-Konten freigegeben wurden:

* Freigegebene Kurse (Peer-Konto): Autorendetails werden jetzt unter einem neuen Attribut `authorDetails` zurückgegeben. Dieses Attribut gibt den Namen des Autors an, selbst wenn der Kurs von einem anderen Konto stammt.

* Hauptkontenkurse: Autoreninformationen werden weiterhin unter dem vorhandenen `authors`-Attribut zurückgegeben, ohne dass sich das aktuelle Verhalten ändert.

Diese Änderung stellt sicher, dass die Konsistenz bei der Bereitstellung von Autorendaten über die API sowohl für Haupt- als auch für gemeinsam genutzte Kurse gewährleistet ist, während gleichzeitig die Kompatibilität für vorhandene Integrationen beibehalten wird.

## Änderungen an webhooks

### Registrieren Sie LinkedIn Learning-Webhooks mithilfe des Connectors

Früher mussten Administratoren LinkedIn Learning-Webhooks über APIs manuell bei Adobe Learning Manager registrieren. Dank dieser Verbesserung unterstützt der LinkedIn Learning (LIL)-Connector jetzt die automatische Webhook-Registrierung während der neuen Verbindungseinrichtung in ALM. Die **OAuth-Server-URL** und die **Mandantenserver-URL** werden auf der LinkedIn Learning-Konfigurationsseite automatisch ausgefüllt.

Weitere Informationen zur Integration von LinkedIn Learning finden Sie unter [LinkedIn Learning](/help/migrated/integration-admin/feature-summary/connectors.md#linkedin-learning-connector).

### Änderungen an der MAU-Lizenznutzung in LinkedIn Learning

Wenn ein Teilnehmer zuvor bei MAU-Konten (Monatlich aktive Benutzer) einen LinkedIn-Lernkurs direkt auf der LinkedIn-Lernplattform abgeschlossen hat, hat Adobe Learning Manager die Lizenznutzung nicht gezählt. Die Lizenznutzung wurde nur für Kurse ausgelöst, die über den Adobe Learning Manager-Player absolviert wurden. Dies führte zu einer ungenauen Verfolgung der monatlichen aktiven Benutzer (MAU).

Dank dieser Verbesserung generiert Adobe Learning Manager jetzt einen externen Webhook, wenn ein Teilnehmer einen Kurs auf der LinkedIn-Lernplattform absolviert. Wenn Adobe Learning Manager diesen Webhook erhält, wird die Lizenznutzung berechnet, um eine exakte Verfolgung auf beiden Plattformen zu gewährleisten.

## Änderungen bei Berichten

### Mit Kursleitern markierte Abschlüsse in Teilnehmertranskripten

Inkrementelle Teilnehmertranskripte erfassen jetzt vom Kursleiter markierte Abschlüsse, auch wenn die Anwesenheit nach dem Sitzungsdatum aufgezeichnet wird.
Diese Verbesserung behebt eine kritische Lücke in inkrementellen Teilnehmertranskripten, bei der vom Kursleiter markierte Abschlüsse zuvor verpasst wurden, wenn die Teilnahme nach dem ursprünglichen Sitzungsdatum aufgezeichnet wurde.

Inkrementelle Teilnehmertranskripte sind geplante Berichte, die nur die Änderungen (z. B. Abschlüsse oder Fortschrittsaktualisierungen) erfassen, die innerhalb eines bestimmten Zeitraums auftreten, anstatt einen vollständigen historischen Datenabbild bereitzustellen. Sie werden häufig für die Automatisierung, für Dashboards und Integrationen verwendet, sodass Benutzer aktuelle Lernaktivitäten effizient verfolgen können, ohne jedes Mal den gesamten Transkriptverlauf verarbeiten zu müssen.

* **Spalte &quot;Abgeschlossenes Datum markieren (UTC-Zeitzone)&quot;**: Eine neue Zeitstempelspalte, die das genaue Datum und die exakte Uhrzeit erfasst, wenn ein Kursleiter eine Sitzung oder ein Modul als abgeschlossen markiert.
* **Verbesserte Vervollständigungsquellenverfolgung**: Verfolgt den spezifischen Kursleiter und das Modul (z. B. &quot;Klassenzimmer&quot;), in dem Abschlüsse aufgezeichnet wurden.

Diese Änderungen stellen sicher, dass nach dem Sitzungsdatum markierte Abschlüsse in den inkrementellen Teilnehmertranskripten genau widergespiegelt werden.

**Anwendungsfälle**

* Organisationen mit Klassenzimmersitzungen, bei denen Kursleiter die Anwesenheit Tage nach der tatsächlichen Sitzung vermerken können.
* Automatisierte Systeme oder Dashboards, die inkrementelle Teilnehmertranskripte für Compliance oder Reporting nutzen.

![Teilnehmertranskriptberichte zeigen markierte abgeschlossene Daten (gelb markiert) für die Verfolgung des Kursabschlusses im Adobe Learning](/help/migrated/assets/mark-completion-column.png)
_Der Teilnehmertranskriptbericht zeigt eine neue Spalte in Gelb an, in der die einzelnen Abschlussdaten für jeden Benutzer hervorgehoben werden._

Weitere Informationen zum Teilnehmertranskriptbericht finden Sie im [Teilnehmertranskript](/help/migrated/administrators/feature-summary/learner-transcripts.md).

### Erweiterter Benutzerbericht mit erweiterten Datenfeldern

Der Benutzerbericht enthält jetzt zusätzliche Felder zur Verbesserung der Benutzerverfolgung und Organisationszuordnung. Diese Updates vereinfachen die Identifizierung von Benutzern, unterstützen die Integration mit nachgelagerten Benutzerverwaltungs-Workflows, verbessern das Verständnis von Berichtsbeziehungen und wahren organisatorische Grenzen, um versehentliche Querverbindungen zu verhindern.

* Spalte &quot;Interne Benutzer-ID&quot;: Bietet eindeutige interne Kennungen für eine reibungslose Benutzerverfolgung über verschiedene Systeme und API-Endpunkte hinweg.
* Spalte &quot;Manager-E-Mail&quot;: Enthält direkte Manager-Kontaktinformationen für die Verfolgung der Organisationshierarchie.

![Benutzerbericht mit gelb markierten Spalten für die interne Benutzer-ID und Manager-E-Mail ](/help/migrated/assets/user-report-columns.png)
_Benutzerberichte, die interne Benutzer-IDs und Manager-E-Mail-Adressen hervorheben, um die Benutzerverwaltung zu optimieren_

[Laden Sie den Benutzerbericht herunter](/help/migrated/administrators/feature-summary/add-users-user-groups.md#download-the-user-report), um weitere Informationen zum Benutzerbericht zu erhalten.

### Benutzerbericht auf FTP, benutzerdefiniertes FTP und Box

**Übersicht**

Der Benutzerbericht ist jetzt für Box-, FTP- und benutzerdefinierte FTP-Connectors zusätzlich zu den vorhandenen Job-APIs verfügbar. Diese Berichte enthalten detaillierte Informationen zur internen Benutzer-ID, Benutzer-E-Mail-Adresse, zum Namen, zur Manager-E-Mail-Adresse, zum Benutzertyp und zu anderen Themen.

Berichte können nach Bedarf oder geplant erstellt werden, wobei die Daten im jeweiligen Connector gespeichert werden, um einen einfachen Zugriff und eine einfache Analyse zu ermöglichen. Diese Verbesserung verbessert die Überwachung und das Auditing von Benutzeraktivitäten und unterstützt eine bessere Sicherheit und Compliance-Verfolgung.

Diese Berichte sind zusammen mit vorhandenen Berichten wie Benutzerregistrierung, Anmeldezugriff, Gamification und Schulung verfügbar, sodass Administratoren von einem einzigen Ort aus auf alle wichtigen Berichte zugreifen können, um die Datenverwaltung und -analyse zu optimieren.

In [Connector](/help/migrated/integration-admin/feature-summary/connectors.md) finden Sie weitere Informationen zu FTP, benutzerdefiniertem FTP und Box-Connector.

### Ausgesetzte Benutzer in Teilnehmertranskripte einschließen

**Übersicht**

Unternehmen können jetzt suspendierte Benutzer (mit deaktivierten externen Profilen) in die Teilnehmertranskripte einbeziehen, um eine umfassende Aufbewahrung von historischen Lerndaten zu gewährleisten.

* Flag auf Kontoebene zum Konfigurieren der Sichtbarkeit unterbrochener Benutzer, sodass Benutzer, die ausgesetzt wurden, in Teilnehmertranskripten angezeigt werden können.
* Historische Datenaufbewahrung auch nach Deaktivierung unterbrochener externer Profile.

**Implementierungsanforderungen**

* Wenden Sie sich an Ihren Customer Success Manager (CSM), um das Flag auf Kontoebene zu aktivieren.

>[!NOTE]
>
>Dieses Flag ist standardmäßig für vorhandene Konten deaktiviert und muss explizit für neue Konten angefordert werden.

Weitere Informationen finden Sie im [Teilnehmertranskript](/help/migrated/administrators/feature-summary/learner-transcripts.md)-Artikel.

### Bericht zu Arbeitshilfen mit direkten Zugriffsverknüpfungen

**Übersicht**

Der Bericht zu Arbeitshilfen wurde verbessert und enthält jetzt direkte Download-Links zu Arbeitshilfen, wodurch das Content Management und Audit-Prozesse für Administratoren und Autoren optimiert werden. Diese Verbesserung ermöglicht direkte Datei-Downloads und URL-Zugriff vom Bericht aus. Keine manuelle Suche und kein Download von Arbeitshilfen für Compliance- oder Barrierefreiheitsprüfungen mehr erforderlich.

* Spalte &quot;Arbeitshilfeverknüpfung&quot;: Direkter Zugriff auf Arbeitshilfedateien und externe URLs innerhalb des Berichts.
* Rollenbasierte Zugriffskontrolle: Die Zugänglichkeit von Links hängt von Benutzerrollen und Katalogberechtigungen ab.
* Gelöschte Arbeitshilfen bleiben verfügbar, wenn sie noch mit aktiven Kursen verknüpft sind.

**Anwendungsfälle**

* Autoren oder Administratoren führen regelmäßige Überprüfungen der Barrierefreiheit bei Arbeitshilfen durch, wie sie von großen Organisationen verlangt werden.
* Szenarien, in denen ein schneller, rollenbasierter Zugriff auf Arbeitshilfedateien für die Überprüfung oder Einhaltung von Vorschriften erforderlich ist.

![](/help/migrated/assets/job-aid-report.png)
_Der Bericht zu Arbeitshilfen zeigt direkte Download-Links an, wodurch der Zugriff auf und das Herunterladen von Arbeitshilfen in Adobe Learning Manager erleichtert wird_

Weitere Informationen zum Bericht zu Arbeitshilfen finden Sie im [Bericht zu Arbeitshilfen](/help/migrated/administrators/feature-summary/reports.md#job-aids-report).

## In diesem Update behobene Fehler

* L2-Quizergebnisse werden jetzt korrekt für nicht interaktive Quizze generiert, einschließlich der Details der Benutzer, die sie abgeschlossen haben.
* Die Signatur wird jetzt korrekt an den Zielhost gesendet, wenn der Authentifizierungsmechanismus während der Verbindungskonfiguration auf Signatur gesetzt ist.
* In Adobe Connect-Sitzungen erstellte Dummy-Benutzer wurden nach Abschluss der Sitzung nicht gelöscht. Die SnapLogic-Pipeline entfernt diese Benutzer jetzt ordnungsgemäß, selbst wenn die `principals-delete`-API zuvor eine 200-Antworten zurückgegeben hat, ohne sie zu löschen.
* `null` `eventDetail` Objekte in API-Antworten verursachen keine Ausnahmen mehr. Das System überspringt jetzt Null-Einträge und verarbeitet das gesamte Array, wodurch vollständige Aufzeichnungen sichergestellt werden.
* In der Spalte &quot;Datum des Feedbacks&quot; in Feedbackberichten wird jetzt das richtige Datum angezeigt. Früher wurden Sekunden fälschlicherweise an den Date-Konstruktor übergeben, der Millisekunden erwartet, sodass Datumsangaben als Januar 1970 angezeigt wurden. Dies wurde korrigiert, um eine genaue Datumsanzeige beim Generieren von Feedbackberichten zu gewährleisten.
* Teilnehmer können jetzt die Registrierung für einen Flex-Lernpfad aktualisieren, selbst wenn eine der Kursinstanzen eingestellt ist. Zuvor verursachte die Auswahl einer neuen Instanz einen Konsolenfehler (Eigenschaften von nicht definierten Inhalten können nicht gelesen werden) und verhinderte die Aktualisierung.
* Ressourcennamen in Lernpfaden werden jetzt korrekt angezeigt, ohne das mittlere Wort zu brechen.
* LinkedIn Learning-Webhooks sind jetzt über den LIL-Connector aktiviert, wenn Verbindungen für neue Benutzer erstellt werden. Das System registriert das Konto auch über die private API und zeigt zusätzliche Konfigurationsinformationen (OAuth-URL und Mandanten-URL) auf der Konfigurationsseite von LinkedIn Learning an.
* Benutzerattributwerte, die über SAML-Workflows (`UpdateUserWorkerTask`) aktualisiert wurden, werden jetzt mit ihrer ursprünglichen Groß-/Kleinschreibung gespeichert, anstatt in Kleinbuchstaben konvertiert zu werden.
* Bei der Neuanordnung von Modulen in einem Kurs wird die Anzahl der obligatorischen Module nicht mehr auf &quot;Alle&quot; zurückgesetzt. Die Anzahl bleibt jetzt wie konfiguriert.
* Go1-Pipelines behandeln jetzt Sprachcodes konsistent, indem sie zweibuchstabige Codes vierbuchstabigen Codes zuordnen, ähnlich wie LinkedIn Learning-Pipelines.
* Bei Konten im Ruhestand+ sahen Teilnehmer zuvor &quot;Dieser Kurs ist nicht vorhanden&quot;, wenn sie einen Lernpfad-Kurs nach der Abmeldung von einer Zertifizierung starteten. Registrierungsquellen werden jetzt korrekt aktualisiert, sodass Kurse in Lernpfaden fehlerfrei gestartet werden können.
* Wenn die Datei &quot;module_version.csv&quot; contentType-Felder mit leeren oder null Werten enthält, funktioniert die Kurserstellung jetzt ohne Probleme.
* Kurse werden jetzt korrekt angezeigt, wenn Sie nach Katalog oder Katalogbeschriftung filtern. Bisher wurden durch Anwenden dieser Filter auf der Kursseite keine Kurse angezeigt, auch wenn sie mit dem Katalog verknüpft waren.
* In der Teilnehmer-App wurde das Drücken der TAB-TASTE im Fluidic Player auf der Schaltfläche &quot;Vollbild eingeben&quot; blockiert. Die Tastaturnavigation bewegt sich jetzt korrekt durch alle Bildschirmelemente.
* Wenn Sie den Mauszeiger über lange Kursnamen im Kompatibilitäts-Dashboard der Manager-App bewegen, wird jetzt der vollständige Name für registrierte oder kompatible Kurse angezeigt.
* Für die Spalte mit der Modulsichtbarkeit in module.csv werden nur freigegebene oder AUSGEBLENDETE Module akzeptiert. Jeder andere Wert löst während der Migration einen Fehler aus und verhindert Fehler im Backend.
* Wenn Sie einen neuen Administrator mit einer gemischten E-Mail-Adresse erstellen, werden keine doppelten Benutzereinträge mehr generiert, wenn UUID deaktiviert ist. Das System behandelt E-Mail-Groß- und Kleinschreibung jetzt konsistent, um Duplikate zu verhindern.
* Hinweis PDF werden jetzt für Sprachkurse in Arabisch, Griechisch, Hebräisch, Hindi, Thai und Ukrainisch korrekt angezeigt. Zuvor wurden die Charaktere auf der heruntergeladenen PDF verzerrt angezeigt, obwohl sie im Player korrekt angezeigt wurden.

## Systemanforderungen

[Systemanforderungen für Adobe Learning Manager anzeigen](/help/migrated/system-requirements.md).

## Versionshinweise

Lesen Sie die [Versionshinweise](/help/migrated/release-note/release-notes.md) für die neuesten Versionsupdates.

## Frühere Versionen von Adobe Learning Manager

* [Adobe Learning Manager Version Mai 2025](/help/migrated/whats-new-may-2025.md)
* [Adobe Learning Manager Version November 2025](/help/migrated/whats-new-nov-24.md)
