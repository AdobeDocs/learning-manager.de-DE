---
description: Erfahren Sie, wie Sie den LinkedIn Learning-Connector mit Adobe Learning Manager integrieren
jcr-language: en_us
title: LinkedIn Learning-Connector
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 1%

---


# LinkedIn Learning-Connector in Adobe Learning Manager

## Einführung

Mit dem LinkedIn Learning-Connector können Sie LinkedIn-Lerninhalte nahtlos in Adobe Learning Manager integrieren. Mit diesem Connector können Unternehmen LinkedIn Learning-Kurse automatisch in Adobe Learning Manager integrieren, sodass Teilnehmer LinkedIn-Kurse direkt auf der Plattform suchen, sich dafür registrieren und abschließen können.

Bei der Einrichtung wird der Fortschritt der Teilnehmer an LinkedIn-Lerninhalten in Adobe Learning Manager verfolgt, sodass Administratoren Abschlüsse und verbrachte Zeit überwachen können. Sie können die automatische Synchronisierung von Inhalten planen, On-Demand-Importe ausführen und filtern, welche Kurse in Ihr System nach Sprache, Bibliothek oder benutzerdefinierten Tags importiert werden.

>[!NOTE]
>
>Wenn Sie Kurse aus LinkedIn Learning importieren, generiert Adobe Learning Manager für jeden Kurs eindeutige LO (Learning Object, Lernobjekt)-IDs. Die für LinkedIn-Lerninhalte aufgewendete Lernzeit wird von der LinkedIn-Plattform an Adobe Learning Manager gemeldet. Wenn die LinkedIn-Plattform diese Daten nicht sendet, kann Adobe Learning Manager sie nicht aufzeichnen, und die aufgewendete Zeit wird als Null angezeigt.

## Konfigurieren der Einstellungen für das LinkedIn-Lernportal

So konfigurieren Sie LinkedIn-Lernportaleinstellungen:

1. Melden Sie sich bei **LinkedIn Learning LMS** als Administrator an.
2. Wählen Sie im oberen Navigationsbereich **Admin** aus.
3. Klicken Sie auf die Registerkarte **Einstellungen**.
4. Wählen Sie in der linken Navigationsleiste **Play-back Integration** und anschließend die Registerkarte **Integration** aus.
5. Erweitern Sie **LMS-Einstellungen zum Starten von Inhalten**.
6. Fügen Sie die folgenden Hostnamen hinzu:

   - learningmanager.adobe.com
   - learningmanagerlrs.adobe.com
   - cpcontents.adobe.com
7. Wählen Sie **AICC-Integration aktivieren**.

   ![](assets/linkedin-connector1.png)
   _Wählen Sie AICC-Integration aktivieren aus, um den LinkedIn Learning-Connector zu konfigurieren_

## Connect LinkedIn Learning in Adobe Learning Manager

So konfigurieren Sie den LinkedIn Learning-Connector:

1. Melden Sie sich bei Adobe Learning Manager als Integrationsadministrator an.
2. Bewegen Sie den Mauszeiger über die Kachel **LinkedIn Learning** und wählen Sie **Connect** aus.

   ![](assets/linkedin-connector2.png)
   _Wählen Sie &quot;Verbinden&quot; aus, um den LinkedIn Learning Connector zu konfigurieren_

3. Auf der Seite Verbindungseinrichtung :
   - Geben Sie einen **Verbindungsnamen** ein.
   - Geben Sie den **Anwendungsschlüssel** und den **geheimen Schlüssel** ein.

   ![](assets/linkedin-connector3.png)
   _Geben Sie den Verbindungsnamen, den Anwendungsschlüssel und den geheimen Schlüssel ein, um den LinkedIn Learning-Connector zu konfigurieren_

   >[!NOTE]
   >
   >Der Unternehmensadministrator kann diese Schlüssel generieren, indem er eine Anwendung im LinkedIn Learning-Admin-Portal erstellt.

4. Wählen Sie **Speichern** aus, um die Verbindung hinzuzufügen.

Um eine bestehende Verbindung zu bearbeiten, wählen Sie **Verbindungen verwalten** auf der Kachel **LinkedIn Learning** aus.

>[!IMPORTANT]
>
>Die **Migration**-Funktion muss für Ihr Konto aktiviert sein, bevor Sie diesen Connector konfigurieren können.


## Verbindung und Synchronisation verwalten

So verwalten Sie den LinkedIn Learning-Connector:

1. Wählen Sie **Verbindungen verwalten** und anschließend die Verbindung aus.
2. Wählen Sie im linken Teilfenster **Konfigurieren**.
3. Wählen Sie **Verbindung aktivieren**.

   ![](assets/linkedin-connector4.png)
   _Wählen Sie auf der Seite &quot;LinkedIn Learning-Connector konfigurieren&quot; die Option &quot;Verbindung aktivieren&quot; aus._

4. Wählen Sie **Bearbeiten** aus, um die Anmeldeinformationen zu aktualisieren. Verwenden Sie **Zurücksetzen**, um Änderungen rückgängig zu machen.
5. Um die Synchronisierung zu automatisieren, wählen Sie **Zeitplan aktivieren**.
6. Legen Sie das Startdatum, die Startzeit und die Häufigkeit fest (z. B. alle 3 Tage).
7. Wählen Sie **Speichern**.

### On-Demand-Synchronisierung

So führen Sie die On-Demand-Synchronisierung aus:

1. Wählen Sie im linken Fensterbereich **On Demand Execution**.
2. Geben Sie ein **Startdatum** ein.
3. Wählen Sie eine der folgenden Optionen aus: **Aktivieren** oder **Deaktivieren des Zugriffs** auf Adobe Learning Manager während der Ausführung:
   - **Zugriff auf Adobe Learning Manager während der Ausführung aktivieren**: Keine Ausfallzeit für Benutzer.
   - **Zugriff auf Adobe Learning Manager während der Ausführung deaktivieren**: Die Anwendung ist während der Synchronisierung nicht verfügbar.

   ![](assets/linkedin-connector5.png)
   _Wählen Sie &quot;On Demand Execution&quot; aus, um den Import auszuführen_

4. Wählen Sie **Ausführen** aus, um Benutzer-Feeds und Daten aus LinkedIn Learning ab diesem Datum zu importieren.

So überwachen Sie alle Synchronisationsläufe:

Wählen Sie im linken Fensterbereich **Ausführungsstatus** aus, um den Verlauf aller Synchronisierungen, ihre Dauer, den Typ (geplant oder auf Anforderung) und den aktuellen Status (in Bearbeitung, abgeschlossen) anzuzeigen.

>[!NOTE]
>
>Wenn Sie eine Verbindung löschen und neu erstellen, werden frühere Ausführungen beibehalten und in **Ausführungsstatus** angezeigt. Sie können nur die letzte Synchronisierung erneut ausführen.

## Filtern von LinkedIn-Lerninhalten

Wenn Sie Ihren Connector einrichten, können Sie filtern, welche LinkedIn-Lernkurse importiert werden sollen.

So richten Sie Ihren Filter ein:

1. Wählen Sie im linken Fensterbereich **Filter** aus.
2. Wählen Sie die erforderliche Option unter **Schulungen filtern mit** aus.
   - **Kein Filter** - Alle Kurse importieren.
   - **Sprache** - Kurse nach bestimmten Sprachen filtern.
   - **Bibliothek** - Kurse nach LinkedIn-Lernbibliotheken filtern.
3. Wählen Sie beim Filtern nach **Sprache** die gewünschten Sprachen aus. Beispiel: **Englisch** und **Spanisch**.
4. Wählen Sie in **Schulungen importieren in** aus, wo die Kurse importiert werden sollen.
5. Wählen Sie aus, wie die importierten Kurse organisiert werden sollen.
6. Wählen Sie eine der folgenden Optionen für die Option **Schulungen auf der Grundlage von** trennen aus:

   - **Sprache** - Nach Sprache gruppieren.
   - **Bibliothek** - Nach Bibliothek gruppieren.
7. Wählen Sie unter **Tags importieren** die Tagtypen aus, die auf importierte Kurse angewendet werden sollen.

   - **Sprache**
   - **Bibliothek**
   - **Betreff**
   - **Thema**
   - **Benutzerdefiniertes Tag**
8. Geben Sie im Feld **Benutzerdefiniertes Tag** ein benutzerdefiniertes Tag ein, das Sie zuweisen möchten. Trennen Sie mehrere Tags durch Kommas.

   ![](assets/linkedin-connector6.png)
   _Wählen Sie Filteroptionen aus, um die Daten aus dem LinkedIn Learning-Connector zu importieren_

9. Wenn Sie möchten, dass Teilnehmer die Registrierung für diese Kurse widerrufen können, wählen Sie **Benutzer können die Registrierung widerrufen**.
10. Wählen Sie **Speichern** aus, um den Filter anzuwenden und Einstellungen zu importieren.
