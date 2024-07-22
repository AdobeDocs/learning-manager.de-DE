---
title: Native Erweiterbarkeit
description: Richten Sie benutzerdefinierte Erlebnisse in der nativen Version von Adobe Learning Manager ein, sodass Sie Headless-Erlebnisse nicht für weniger komplizierte Fälle verwenden können.
exl-id: 510bd00f-4f52-4705-817e-4ee73380ca90
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 48%

---

# Native Erweiterbarkeit

Sie können benutzerdefinierte Erfahrungen in der nativen Version von Adobe Learning Manager einrichten, sodass Sie für weniger komplizierte Fälle nicht Headless nutzen müssen. Sie können auch benutzerdefinierte Apps erstellen und sie an verschiedenen Punkten in der nativen Version der Workflows für Teilnehmende, Manager(innen), Administrator(inn)en, Autor(inn)en oder Kursleiter(inn)en platzieren.

Adobe Learning Manager unterstützt 15 Aufrufpunkte in der Administrator(inn)en-, Autor(inn)en-, Teilnehmenden-, Manager(innen) und Kursleiter(inn)en-App.

## Erstellen einer Erweiterung

1. Wählen Sie als Administrator(in) im linken Bereich **[!UICONTROL Native Erweiterungen]**.
1. Wählen Sie Erweiterung hinzufügen.
1. Geben Sie den Namen der Erweiterung in das Feld **[!UICONTROL Name]** ein.
1. Geben Sie die Beschreibung der Erweiterung in das Feld **[!UICONTROL Beschreibung]** ein.
1. Wählen Sie einen Aufrufpunkt aus. Ein Aufrufpunkt ist eine beliebige Stelle in Adobe Learning Manager, an der ein Link oder eine Schaltfläche in eine benutzerdefinierte App eingefügt werden kann. Die folgenden Aufrufpunkte sind verfügbar:

   Wählen Sie für dieses Beispiel **[!UICONTROL Admin]**, **[!UICONTROL Autor: Kurs]**, **[!UICONTROL Lernpfad]** - **[!UICONTROL Instanzen]** - **[!UICONTROL Instanzzeile]**.

   ![Erweiterungsbild](assets/list-native-extensions.png)
   *Aufrufpunkt auswählen*

1. Geben Sie die Erweiterungsbezeichnung ein, die auf der Benutzeroberfläche im Feld **[!UICONTROL Erweiterungsbezeichnung]** angezeigt wird.
1. Geben Sie die URL, unter der Sie die Erweiterung hosten möchten, in das Feld **[!UICONTROL URL]** ein.
1. Wählen Sie in der Dropdown-Liste Öffnen in aus, ob die Erweiterung in einem modalen oder in einem neuen Register gestartet werden soll.
1. Wählen Sie die Größe des modalen Fenster aus. Die Optionen sind verfügbar, wenn Sie im vorherigen Schritt *In-App* modal ausgewählt haben.

   Um die Barrierefreiheit im Popup beizubehalten, muss die Erweiterungs-App an das Ereignis gesendet werden, sobald sie sich auf dem letzten fokussierbaren Element auf ihrer Website befinden, und dann wählt der Benutzer die TAB-TASTE aus. Dies ist erforderlich, um den Fokus im Popup-Fenster zu halten und die Barrierefreiheit zu unterstützen.

   ```
   window.parent.postMessage({*}
   
   { type: 'ALM_EXTENSION_APP', eventType: 'trapFocusInModal' }
   
   ,{}'');
   ```

1. Legen Sie den Umfang der Erweiterung fest. Folgende Bereiche stehen zur Verfügung:

   * **[!UICONTROL Alle Kurse, Lernpfade und Zertifizierungen]**: Diese Erweiterung ist für alle Kurse, Lernpfade und Zertifizierungen aktiviert. Zusammen mit Administratoren können Autoren sie für einige Kurse, Lernpläne und Zertifizierungen deaktivieren.
   * **[!UICONTROL Ausgewählte Kurse, Lernpfade und Zertifizierungen]**: Diese Erweiterung ist für alle Kurse, Lernpfade und Zertifizierungen deaktiviert. Zusammen mit Administratoren können Autoren sie für einige Kurse, Lernpfade und Zertifizierungen aktivieren.

1. Wählen Sie den Umschalter **[!UICONTROL Aktivieren]**, um die Erweiterung zu aktivieren. Sobald die Erweiterung aktiv ist, wird sie entsprechend dem Gültigkeitsbereich am angegebenen Aufrufpunkt angezeigt.
1. Wählen Sie in der rechten oberen Ecke der Seite **[!UICONTROL Speichern]**, um die Erweiterung zu erstellen.

## Zugriff auf die Erweiterung als Administrator(in)

1. Wählen Sie als Administrator(in) in der linken Symbolleiste **[!UICONTROL Lernpfade]**.
1. Wählen Sie einen Kurs > **[!UICONTROL Lernpfad anzeigen]**.
1. Wählen Sie im linken Bereich **[!UICONTROL Instanzen]**.
1. Wählen Sie im Abschnitt “Instanzen“ **[!UICONTROL Mehr]**. Die Erweiterung wird im Abschnitt “Instanzen“ angezeigt.

   ![Instanzenbild](assets/instances-extension.png)
   *Erweiterung auswählen*

   Wenn Sie die Erweiterung auswählen, wird sie im modalen Format angezeigt.

## Zugriff auf die Erweiterung als Autor(in)

1. Wählen Sie als Administrator(in) in der linken Symbolleiste **[!UICONTROL Lernpfade]**.
1. Wählen Sie einen Kurs > **[!UICONTROL Lernpfad anzeigen]**.
1. Wählen Sie im linken Bereich **[!UICONTROL Instanzen]**.
1. Wählen Sie im Abschnitt “Instanzen“ **[!UICONTROL Mehr]**. Die Erweiterung wird im Abschnitt “Instanzen“ angezeigt.

   ![Instanzenbild](assets/instances-extension.png)
   *Zugriff auf Erweiterung als Autor*

   Wenn Sie die Erweiterung auswählen, wird sie im modalen Format angezeigt.

## Anzeigen aller Erweiterungen

Als Administrator können Sie alle Erweiterungen auf der Seite Native Erweiterungen anzeigen. Um die Liste anzuzeigen, wählen Sie „Native Erweiterungen“ im linken Bereich der App aus.

![Ansichtserweiterungsabbild ](assets/view-extensions.png)
*Alle Erweiterungen anzeigen*

## Aktivieren oder Deaktivieren von Erweiterungen

Als Autor(in) können Sie auf der Seite “Einstellungen“ eines Kurses eine Erweiterung für einen Kurs, eine Zertifizierung oder einen Lernpfad aktivieren oder deaktivieren.

![Erweiterungsbild aktivieren](assets/activate-extension.png)
*Aktivieren einer Erweiterung*

## Freigeben eines Zugriffschlüssels

Sie müssen den Zugriffschlüssel freigeben, wenn Sie eine Registrierungserweiterung konfigurieren.

Dies ist wichtig, da die Authentifizierung für die Registrierung fehlschlägt, wenn dieser Schlüssel nicht generiert und in allen geteilt wird und die Teilnehmer sich nicht für die Kurse selbst registrieren können.

Der Zugriffsschlüssel muss für die Registrierung für einen Kurs oder einen Lernpfad und für Zertifikate gemeinsam genutzt werden.

Generieren Sie auf der Registerkarte &quot;Einstellungen&quot; den Schlüssel.

![Schlüsselbild freigeben](assets/share-extension.png)
*Freigeben des Zugriffsschlüssels*

## Herunterladen des Erweiterungsberichts

Es gibt zwei Möglichkeiten, diesen Bericht herunterzuladen.

**Erweiterungskonfigurationsbericht**

1. Wählen Sie auf der Seite “Native Erweiterungen“ **[!UICONTROL Erweiterungskonfigurationsbericht]**.

   ![Berichtsbild](assets/extension-config-report.png)
   *Erweiterungsbericht herunterladen*

   Der Bericht wird generiert.

1. Wählen Sie OK.

   ![Berichtsbild wird generiert](assets/generating-report.png)
   *Bericht wird generiert*

   Der Bericht enthält folgende Felder:

   * Name der Erweiterung
   * Aufrufungspunkt
   * Name
   * In URL öffnen
   * Umfang
   * Aktivieren
   * LO Eindeutige ID
   * Schulungs-ID
   * Schulungstyp
   * Schulungsname

**Berichtsseite**

1. Wählen Sie in **[!UICONTROL Berichte]** > **[!UICONTROL Benutzerdefinierte Berichte]** die Option **[!UICONTROL Erweiterungskonfigurationsbericht]** aus.

   ![meldet Seitenbild ](assets/extension-report-page.png)
   *Bericht von Seite &quot;Berichte&quot; herunterladen*

Der Status muss beim Konfigurieren des Registrierungsstatus im Bereich **0 - 4294967295** liegen.
