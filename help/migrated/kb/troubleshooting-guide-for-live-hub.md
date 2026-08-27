---
title: Leitfaden zur Fehlerbehebung für Live Hub (Beta)
description: Häufige Fehlermeldungen und Benachrichtigungen, die während einer Live Hub-Sitzung auftreten können, sowie deren Ursachen und Schritte zu ihrer Behebung.
source-git-commit: a454fbcdfc37a139245d925dd01bb931d6f83432
workflow-type: tm+mt
source-wordcount: '1072'
ht-degree: 2%

---


# Leitfaden zur Fehlerbehebung für Live Hub (Beta)

Während einer Live-Hub-Sitzung erhalten Kursleiter möglicherweise Fehlermeldungen oder Benachrichtigungen, die verhindern, dass bestimmte Aktionen wie erwartet abgeschlossen werden. In diesem Artikel werden häufige Fehler beschrieben, die auf Kursleiter zutreffen, sowie deren mögliche Ursachen und die Schritte, die Sie unternehmen können, um diese Fehler zu beheben.

## Verbindungsprobleme

| Fehlermeldung | Szenario | Vorschläge zur Fehlerbehebung |
|---|---|---|
| Es ist ein Fehler aufgetreten. Versuchen Sie es noch einmal. | Ein allgemeiner Konnektivitäts- oder sitzungsbedingter Fehler tritt beispielsweise auf, wenn Sie einer Sitzung beitreten oder mit dieser interagieren und die Anforderung aufgrund von Netzwerkinstabilität, einer abgelaufenen ALM-Sitzung oder eines in Konflikt stehenden Browserstatus, z. B. wenn mehrere Registerkarten für dasselbe Meeting geöffnet sind, fehlschlägt. | <ul><li>Prüfen Sie Ihre Netzwerkverbindung und sorgen Sie für eine stabile Bandbreite ohne VPN-/Proxy-Interferenzen.</li><li>Vergewissern Sie sich, dass Sie mit einer gültigen Sitzung bei ALM angemeldet sind - melden Sie sich ab und wieder an, wenn Ihre Sitzung abgelaufen ist.</li><li>Vermeiden Sie es, sich gleichzeitig von mehreren Registerkarten aus an einem Meeting zu beteiligen.</li><li>Versuchen Sie es mit einem inkognito/privaten Fenster oder leeren Sie den Browsercache, wenn das Problem weiterhin besteht.</li><li>Seite aktualisieren: Die meisten vorübergehenden Fehler werden nach einem Neustart behoben. Wenden Sie sich an den Support, wenn es erneut auftritt.</li></ul> |

## Probleme mit Quiz-Registerkarten

Die folgenden Meldungen können angezeigt werden, wenn ein Kursleiter ein Quiz erstellt oder startet und das Quiz nicht die zum Starten erforderlichen Anforderungen erfüllt.

| Fehlermeldung | Szenario | Vorschläge zur Fehlerbehebung |
|---|---|---|
| Geben Sie eine Frage ein, um fortzufahren. | Ein Kursleiter versucht, ein Quiz zu starten, ohne den Fragentext einzugeben. | Geben Sie die Frage ein, geben Sie die Antwortoptionen an, wählen Sie die richtige Antwort aus und starten Sie dann das Quiz für die Teilnehmer. |
| Antwortoptionen können nicht leer gelassen werden. | Ein Kursleiter gibt den Fragentext ein, aber nicht die Antwortoptionen oder lässt eine oder mehrere Antwortoptionen leer. | Geben Sie die Frage ein, geben Sie die Antwortoptionen an, wählen Sie die richtige Antwort aus und starten Sie dann das Quiz für die Teilnehmer. |
| Markieren Sie die richtige Antwort. | Ein Kursleiter gibt die Frage- und Antwortoptionen ein, wählt aber keine richtige Antwortoption aus. | Geben Sie die Frage ein, geben Sie die Antwortoptionen an, wählen Sie die richtige Antwort aus und starten Sie dann das Quiz für die Teilnehmer. |

## Probleme auf der Registerkarte &quot;Umfrage&quot;

Die folgenden Meldungen können angezeigt werden, wenn ein Kursleiter eine Umfrage dupliziert, löscht oder zurücksetzt.

| Fehlermeldung | Szenario | Vorschläge zur Fehlerbehebung |
|---|---|---|
| Die Umfrage konnte nicht dupliziert werden. Versuchen Sie es noch einmal. | Ein Kursleiter dupliziert eine vorhandene Abstimmung und das Duplikat wird nicht erstellt. | Schließen Sie das Bedienfeld &quot;Umfragen und Tests&quot; und wiederholen Sie das Duplizieren der Umfrage. |
| Es konnten nicht alle Umfragen gelöscht werden. Versuchen Sie es noch einmal. | Ein Kursleiter löscht alle Umfragen auf einmal mit Alle löschen , und der Massenlöschvorgang schlägt fehl oder wird nur teilweise abgeschlossen. | Schließen Sie das Bedienfeld &quot;Umfragen und Tests&quot; und versuchen Sie erneut, die Umfragen mit &quot;Alle Umfragen löschen&quot; zu löschen. |
| Die Abstimmung konnte nicht gelöscht werden. Versuchen Sie es noch einmal. | Ein Kursleiter löscht eine einzelne Umfrage und der Löschvorgang wird nicht abgeschlossen. | Schließen Sie das Bedienfeld &quot;Umfragen und Tests&quot; und versuchen Sie erneut, die Umfrage zu löschen. |
| Umfrage konnte nicht zurückgesetzt werden. Versuchen Sie es noch einmal. | Ein Kursleiter setzt eine zuvor ausgeführte Abstimmung zurück, sodass sie wiederverwendet werden kann, und das Zurücksetzen wird nicht abgeschlossen. | Schließen Sie das Bedienfeld &quot;Umfragen und Tests&quot; und versuchen Sie erneut, die Umfrage zurückzusetzen. |

## Probleme beim Hochladen von Inhalten

Die folgende Meldung kann angezeigt werden, wenn ein Kursleiter eine Referenzdatei hochlädt, die der AI-Assistent zum Beantworten von Fragen verwendet.

| Fehlermeldung | Szenario | Vorschläge zur Fehlerbehebung |
|---|---|---|
| Die Datei konnte nicht verarbeitet werden. Versuchen Sie es noch einmal. | Ein Kursleiter lädt eine beschädigte, leere oder kennwortgeschützte Datei hoch, die nicht verarbeitet werden kann. | Konvertieren Sie die Datei in ein unterstütztes Format (PDF oder PPT) und laden Sie sie erneut hoch. |

## Probleme beim Hochladen von Inhalten

Die folgenden Meldungen werden als Popup-Benachrichtigungen angezeigt, wenn ein Kursleiter eine Referenzdatei hochlädt, die der AI-Assistent verwendet, und die Datei eine bestimmte Validierungsprüfung nicht besteht.

| Fehlermeldung | Szenario | Vorschläge zur Fehlerbehebung |
|---|---|---|
| Die Datei konnte nicht verarbeitet werden. Überprüfen Sie die Datei und versuchen Sie es erneut. | Ein Kursleiter lädt eine Datei hoch, die beschädigt ist. | Überprüfen Sie das Dateiformat, konvertieren Sie es in ein unterstütztes Format (PDF oder PPT) und laden Sie es erneut hoch. |
| Die Datei ist kennwortgeschützt. Bitte entfernen Sie das Kennwort und laden Sie es erneut hoch. | Ein Kursleiter lädt eine Datei hoch, die kennwortgeschützt ist. | Entfernen Sie den Kennwortschutz aus der Datei und laden Sie sie erneut hoch. |
| Die Datei enthält keinen zu verarbeitenden Inhalt. Bitte laden Sie eine Datei mit Text hoch. | Ein Kursleiter lädt eine Datei hoch, die keinen Inhalt hat, den der AI-Assistent verarbeiten kann. | Lade eine Datei hoch, die Text enthält. |
| &quot;FileName.pdf&quot; überschreitet das Limit von 1 MB. | Ein Kursleiter lädt eine PDF-Datei hoch, die die 1-MB-Dateigrößenbeschränkung überschreitet. | Komprimieren oder reduzieren Sie die PDF-Dateigröße auf unter 1 MB und laden Sie sie dann erneut hoch. |
| &quot;FileName.pptx&quot; überschreitet das Limit von 3 MB. | Ein Kursleiter lädt eine PPT-Datei hoch, die die Dateigrößenbeschränkung von 3 MB überschreitet. | Komprimieren oder reduzieren Sie die PPT-Dateigröße auf unter 3 MB und laden Sie sie dann erneut hoch. |

## Probleme bei Arbeitsgruppensitzungen

Die folgenden Meldungen können angezeigt werden, wenn ein Kursleiter versucht, eine Arbeitsgruppensitzung zu starten.

| Fehlermeldung | Szenario | Vorschläge zur Fehlerbehebung |
|---|---|---|
| Die Trennung kann nicht gestartet werden - Verbindung wird unterbrochen. Versuchen Sie es erneut, wenn die Verbindung wiederhergestellt wird. | Ein Kursleiter versucht, Arbeitsräume zu starten, während seine Verbindung derzeit unterbrochen oder erneut hergestellt wird. | Warten Sie, bis sich die Verbindung stabilisiert hat (achten Sie auf eine Anzeige für eine erneute Verbindung), und starten Sie die Arbeitsräume erneut. |
| Das Aufteilen konnte nicht gestartet werden. Versuchen Sie es noch einmal. | Ein Kursleiter startet Arbeitsräume, und die Anforderung zum Starten schlägt fehl. | Starten Sie die Arbeitsräume erneut. Wenn das Problem weiterhin besteht, schließen Sie das Bedienfeld &quot;Arbeitsgruppen&quot; und versuchen Sie es erneut. |
| Die Zusammenfassung konnte nicht generiert werden. | Dieser Fehler kann an drei Stellen auftreten:  die Live-Übersicht **Raum** überprüfen, eine **raumspezifische Übersicht** im Arbeitsgruppenbericht und die **Gesamtübersicht** im Arbeitsgruppenbericht, je nach Ursache: <ul><li>Kein Teilnehmer sprach während der Diskussion im Raum.</li><li>Die Diskussion im Raum dauerte weniger als 60 Sekunden.</li><li>Nur ein Arbeitsraum hat eine Zusammenfassung generiert.</li></ul> | Korrigieren Sie die Ursache wie oben beschrieben: <ul><li>Sorgen Sie dafür, dass die Teilnehmer während der Diskussion im Raum aktiv sprechen.</li><li>Stellen Sie sicher, dass die Diskussion mindestens 60 Sekunden dauert, bevor Sie die Zusammenfassung überprüfen oder generieren.</li><li>Stellen Sie sicher, dass mindestens 2 Arbeitsräume einzelne Übersichten erstellt haben, bevor die Gesamtübersicht generiert werden kann.</li><li>Wenn das Problem weiterhin besteht, nachdem die relevante Ursache behoben wurde, warten Sie einen Moment und versuchen Sie es erneut.</li></ul> |

## Antworten auf Probleme mit der Generierung von Toasts

Die folgende Meldung kann angezeigt werden, wenn ein Kursleiter den AI-Assistenten auffordert, eine Antwort auf die Frage eines Teilnehmers im Chat zu generieren.

| Fehlermeldung | Szenario | Vorschläge zur Fehlerbehebung |
|---|---|---|
| Dies wurde in der Sitzung nicht behandelt. | Ein Teilnehmer stellt eine Frage, die in der hochgeladenen Inhaltsreferenz nicht behandelt wird. Dies ist ein erwartetes Verhalten, kein Fehler. | Beantworten Sie die Frage manuell. |
