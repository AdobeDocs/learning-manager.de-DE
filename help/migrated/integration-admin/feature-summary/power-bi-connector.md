---
description: Erfahren Sie, wie Sie den Power BI-Connector mit Adobe Learning Manager integrieren
jcr-language: en_us
title: Power BI-Connector
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '1074'
ht-degree: 4%

---


# Power BI-Anschluss in Adobe Learning Manager

## Einführung

Über den Power BI-Connector können Sie Adobe Learning Manager mit Microsoft Power BI (kommerzielle Lizenz) integrieren, sodass Sie Ihre Lerndaten analysieren, visualisieren und freigeben können.

Mit dieser Integration kann der Integrationsadministrator Live-Datensätze wie Teilnehmertranskripte, Benutzerkenntnisse und xAPI-Aktivitätsberichte automatisch direkt in einen bestimmten Power BI-Arbeitsbereich exportieren.

Sobald die Verbindung hergestellt ist, können Sie alle Funktionen von Power BI nutzen, um benutzerdefinierte Dashboards und Berichte zu erstellen. Dies hilft Ihrem Unternehmen, tiefere Einblicke in den Fortschritt der Teilnehmer, die erreichten Qualifikationen und die Wirksamkeit der Schulung zu gewinnen und fundierte Entscheidungen auf der Grundlage von Echtzeit-Lerndaten zu treffen.

>[!NOTE]
>
>Adobe Learning Manager unterstützt nur die Integration mit der kommerziellen Version von Microsoft Power BI. Die Integration mit der Version von Government Cloud wird nicht unterstützt.

## Voraussetzungen

- Nur Microsoft Power BI mit einer **kommerziellen Lizenz** wird unterstützt.
- Stellen Sie sicher, dass Sie über die Berechtigung zum Erstellen von Power BI-Apps und -Arbeitsbereichen verfügen.
- **Mandantenname**, **App-Client-ID**, **App-Client-Geheimnis** und **Arbeitsbereich-ID** (optional) abrufen.

## Konfigurieren des Power BI-Anschlusses

Anschluss von ALM an Power BI:

1. Melden Sie sich bei Adobe Learning Manager als Integrationsadministrator an.
2. Bewegen Sie den Mauszeiger über die Kachel des **Power BI**-Connectors und wählen Sie **Verbinden** aus.

   ![](assets/power-bi-connector1.png)
   _Wählen Sie &quot;Verbinden&quot; aus, um den Power BI-Connector zu konfigurieren_

3. Geben Sie die folgenden Details ein:

   - Client-ID
   - Client-Geheimnis
   - Mandantenname
   - Arbeitsbereich-ID (optional)

   ![](assets/power-bi-connector2.png)
   _Geben Sie die erforderlichen Details zum Konfigurieren des Powers BI ein_

4. Wählen Sie **Verbinden**.

## Registrieren Sie die Power BI-App

So registrieren Sie die Power BI-App:

1. Wechseln Sie zu [Registrieren Sie die Power BI-App](https://app.powerbi.com/embedsetup).
2. Wählen Sie **Für Ihre Organisation einbetten** und melden Sie sich bei Ihrem Microsoft-Konto an.
3. Geben Sie einen Namen für die Anwendung ein.
4. Wählen Sie unter **App-Typ** die **Server-seitige Web-App** aus.
5. Wählen Sie im Abschnitt **URL umleiten** die Option **Benutzerdefinierte URL verwenden** aus, und geben Sie [diese URL ein](https://learningmanager.adobe.com/ctr/app/azure/_callback): (Ersetzen Sie bei Bedarf die Domäne für Ihre Umgebung.)
6. Geben Sie im Feld **Home URL** [diese URL](https://learningmanager.adobe.com/) ein.
7. Wählen Sie im Abschnitt **Berechtigungen** die Option **Alle Datensätze lesen** und **Alle Datensätze lesen und schreiben** aus.
8. Wenden Sie sich an Ihren Power BI-Administrator, um den **Mandantennamen** zu erhalten.
9. Wenn Sie keine Arbeitsbereich-ID haben, erstellen Sie einen Arbeitsbereich in Power BI (erfordert Power BI Pro) und kopieren Sie die ID aus der URL.
10. Wählen Sie **App registrieren** aus und speichern Sie die **Client-ID** und **Client-Geheimnis** zur späteren Verwendung.

>[!NOTE]
>
>Wenn Sie die Verbindung später erneut autorisieren müssen, erstellen Sie eine neue Power BI-App und verwenden Sie die richtige Umleitungs-URL für Ihre Umgebung.

## Berichte in den Power BI exportieren

Nach dem Konfigurieren der Verbindung können Sie diese Berichte exportieren:

- **Teilnehmertranskripte**
- **Benutzerkenntnisse**
- **xAPI-Aktivitätsberichte**
- **Vereinheitlichte Berichte** (eine Kombination aus mehreren Berichten)

### Teilnehmertranskript

#### Exporte planen

1. Wählen Sie im linken Bereich **Teilnehmertranskripte** aus.
2. Wählen Sie **Zeitplan aktivieren** auf der Seite Exportieren aus.
3. Wählen Sie das **Startdatum** und **Uhrzeit** aus.
4. Definieren Sie das **Intervall** für die Häufigkeit der Exportwiederholung (täglich, wöchentlich usw.).

   ![](assets/power-bi-connector3.png)
   _Zeitplanexport für Teilnehmertranskript aktivieren_

5. Wählen Sie **Speichern**.

#### On-Demand-Export

- Sie können Berichte manuell generieren, indem Sie das **Startdatum** angeben und einen On-Demand-Export ausführen.
- Der Bericht enthält Daten vom angegebenen Datum bis zum aktuellen Tag.

### Benutzerkenntnisse

#### Exporte planen

1. Wählen Sie im linken Bereich **Benutzerkenntnisse** aus.
2. Wählen Sie **Zeitplan aktivieren** auf der Seite Exportieren aus.
3. Wählen Sie das **Startdatum** und **Uhrzeit** aus.
4. Definieren Sie das **Intervall** für die Häufigkeit der Exportwiederholung (täglich, wöchentlich usw.).

   ![](assets/power-bi-connector4.png)
   _Zeitplanexport des Benutzerkenntnisberichts aktivieren_

5. Wählen Sie **Speichern**.

#### On-Demand-Export

- Sie können Berichte manuell generieren, indem Sie das **Startdatum** angeben und einen On-Demand-Export ausführen.
- Der Bericht enthält Daten vom angegebenen Datum bis zum aktuellen Tag.

### xAPI-Aktivitätsberichte verwalten

**xAPI-Anweisungen** können auch in den Power BI exportiert werden.

#### Konfigurieren von xAPI-Exporten

1. Wählen Sie **xAPI-Aktivitätsbericht exportieren** aus.
2. Wählen Sie im linken Fensterbereich **Konfiguration** aus.

   - Füllen Sie JSON-Pfadfelder aus, um sie an Ihre CSV-Spalten anzupassen.
   - Wählen Sie **Hinzufügen** aus, um weitere Pfade einzuschließen.
   - Verwenden Sie **Bearbeiten**, um Felder zu aktualisieren.
3. Wählen Sie **Speichern**.

#### Exporte planen

1. Wählen Sie **Zeitplan konfigurieren**.
2. Wählen Sie **Export von xAPI-Anweisungen über diese Verbindung aktivieren**.
3. Legen Sie das **Startdatum**, **Zeit** und **Intervall** fest.
4. Wählen Sie **Speichern**.

#### On Demand-Export

1. Wählen Sie **On Demand**.
2. Geben Sie das **Startdatum** an.
3. Wählen Sie **Ausführen**.

>[!NOTE]
>
>Wenn einigen xAPI-Anweisungen im Learning Record Store (LRS) konfigurierte JSON-Pfade fehlen, werden ihre Werte im Power BI als N/A angezeigt.

#### Ausführungsstatus anzeigen

- Verwenden Sie **Ausführungsstatus**, um den Verlauf der Exporte anzuzeigen, einschließlich Startzeit, Dauer und Status.
- Ein Warnsymbol zeigt an, dass die Ausführung fehlgeschlagen ist. Klicken Sie auf den Link, um die Fehlerberichte als .CSV herunterzuladen.

### Vereinheitlichte Berichte

**Vereinheitlichte Berichte** kombinieren Daten aus:

- Teilnehmertranskript
- Gamification
- Feedbackbericht
- Anmelden/Zugriff
- Benutzerkenntnisse
- Benutzerbericht
- Schulungsbericht

So können Sie leistungsfähigere Dashboards erstellen, indem Sie Daten in Power BI zusammenführen.

#### Erstellen einer einheitlichen Berichtskonfiguration

1. Wählen Sie **Unified Reports** und anschließend **Configuration**.
2. Geben Sie einen eindeutigen Namen in das Feld **Datensatzname** ein.
3. Wählen Sie unter **Berichte für Datenexport auswählen** einen oder mehrere Berichte aus, die in diesem Dataset enthalten sein sollen.

   - Teilnehmertranskript
   - Anmelden/Zugriff
   - Schulungsbericht
   - Gamification
   - Benutzerkenntnisse
   - Feedbackbericht
   - Benutzerbericht
4. Verwenden Sie das Feld **Benutzergruppenfilter hinzufügen**, um die Daten der Benutzergruppen auszuwählen, die Sie exportieren möchten. Standardmäßig ist **Alle Benutzer** ausgewählt.
5. Verwenden Sie das Feld **Inhaltskatalogfilter hinzufügen**, um Berichte nach Inhaltskatalog zu filtern.
6. Die Filtertabelle zeigt an, welche Berichte die Filter **Benutzergruppe**, **Katalog** oder **Zeit** unterstützen.

   ![](assets/power-bi-connector5.png)
   _Konfiguration für vereinheitlichte Berichte erstellen_

7. Wählen Sie nach der Auswahl von Berichten und Filtern oben rechts **Speichern**.

#### Teilnehmertranskripte nach Status filtern

- **Alle:** Alle Datensätze im Datumsbereich
- **Abgeschlossen:** Nur abgeschlossene Lernaktivitäten
- **Wird ausgeführt:** Nur fortlaufende Aktivitäten
- **Nicht gestartet:** Ausgeschlossen Datensätze, die noch nicht gestartet wurden
- **Registrierung aufgehoben:** Enthält nicht registrierte Datensätze

## Herunterladen von Power BI-Vorlagen

Adobe bietet gebrauchsfertige Power BI-Vorlagen, die Ihnen den schnellen Einstieg erleichtern.

- Laden Sie Vorlagen herunter, importieren Sie Ihre Berichte und passen Sie sie nach Bedarf an.
- Verwendet Vorlagen, um ansprechende Dashboards zu erstellen, ohne bei Null anfangen zu müssen.

## Einstellungen für den Lernpfad

Wie **Lernpfade** in Ihren Berichten angezeigt werden, hängt von Ihren Administratoreinstellungen ab:

- **Vorhandene Verbindungen:**

   - Wenn **Lernpfad** deaktiviert ist, sind keine verknüpften Zeilen oder Spalten enthalten.
   - Wenn diese Option aktiviert ist, enthält der Bericht den Lernpfad (höhere Ebene) für registrierte Teilnehmer.

- **Neue Verbindungen:**

   - Wenn &quot;Lernpfad&quot; deaktiviert ist, werden folgende Spalten angezeigt:

      - **Eingebetteter Pfad:** Name des Lernprogramms.
      - **ID des eingebetteten Pfads:** ID für das Lernprogramm.
      - **Eingebettete Kurs-ID:** IDs von Kursen im Lernpfad.
   - Wenn diese Option aktiviert ist, verwendet die Spalte &quot;**Typ**&quot; ggf. den Lernpfad (höhere Ebene).
   - Bei neuen Verbindungen gelten die Änderungen nach 30 Tagen.

### Wo eure Daten zu sehen sind**

Alle exportierten Daten werden als Datensätze unter Ihrem Power BI-Konto angezeigt. Verwenden Sie diese, um benutzerdefinierte Dashboards und Visualisierungen zu erstellen.
