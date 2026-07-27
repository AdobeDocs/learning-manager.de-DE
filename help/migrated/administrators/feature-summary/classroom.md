---
title: Standorte für Klassenzimmer hinzufügen
description: Hier erfahren Sie, wie Administratoren Einstellungen konfigurieren und Standorte für Klassenzimmer in Adobe Learning Manager hinzufügen, migrieren, bearbeiten und löschen und wie Sie Standorte für Klassenzimmer hinzufügen.
source-git-commit: 6f2b9abf305665fe0b66007411455bd2210ee248
workflow-type: tm+mt
source-wordcount: '1641'
ht-degree: 3%

---


# Standorte für Klassenzimmer hinzufügen

Administratoren können eine Bibliothek mit Speicherorten für Klassenzimmer erstellen und verwalten, die beim Einrichten von Schulungsveranstaltungen mit Kursleiter im Modul &quot;Klassenzimmer&quot; und &quot;Virtuelle Klassenzimmer&quot; wiederverwendet werden kann. Für jeden Speicherort können Sie Details wie den Positionsnamen, die Sitzplatzbeschränkung und zusätzliche Informationen, einschließlich einer Standort-URL, definieren. Autoren können diese vordefinierten Speicherorte dann auswählen, wenn sie einen Kurs erstellen.

Standardmäßig verwendet Adobe Learning Manager ein Speicherortformat für ein einzelnes Feld. Für Organisationen, die Standorte für Klassenzimmer in mehreren Ländern und Sprachen verwalten, unterstützt Learning Manager auch ein strukturiertes Vierfeldformat, das **Land**, **Land/Provinz/Region**, **Stadt** und **Standortname** enthält. Dieses Format bietet zusätzliche Funktionen wie standortbasierte Filterung und Sprachunterstützung für einzelne Standorte. Administratoren können durch eine einmalige Migration zum Format mit vier Feldern wechseln.

>[!NOTE]
>
>Wenn das Format für Speicherorte mit vier Feldern nicht aktiviert ist, können Autoren und Teilnehmer die Speicherorte für Klassenzimmer wie gewohnt weiterhin verwenden. Das vorhandene Speicherortformat für einzelne Felder bleibt verfügbar und es sind keine Änderungen erforderlich. Weitere Informationen finden Sie unter [Migrieren zur Methode mit vier Feldern](#migrate-classroom-locations-to-the-four-field-format).

## Konfigurieren der Klassenzimmerstandorteinstellungen

Administratoren können steuern, ob Autoren Speicherorte für Klassenzimmer erstellen und verwalten können. Verwenden Sie die Einstellungen **Standorte im Klassenzimmer**, um die Zugriffsebene zu definieren, die Autoren zur Verfügung steht.

So konfigurieren Sie **Klassenzimmerspeicherorte**-Einstellungen:

1. Melden Sie sich bei der Adobe Learning Manager als **Administrator** an.
1. Wählen Sie **Einstellungen** > **Standorte für Klassenzimmer**.

   Dadurch wird die Seite **Speicherort des Klassenzimmers** angezeigt.

1. Wählen Sie die Registerkarte **Einstellungen** aus.

   ![Registerkarte &quot;Einstellungen&quot; für Standorte im Klassenzimmer](assets/classroom-locations-settings-tab.png)

   *Aktivieren Sie auf der Registerkarte **Einstellungen**&#x200B;die Autorenberechtigungen für Standorte im Klassenzimmer und im virtuellen Klassenzimmer.*

1. Wählen Sie **Bearbeiten**.

   Der Schalter kann bearbeitet werden, sodass Sie die folgenden Einstellungen aktualisieren können:

   | **Einstellung** | **Beschreibung** |
   |---|---|
   | **Autoren das Erstellen von Speicherorten erlauben** | Aktivieren Sie diese Option, damit Autoren beim Erstellen von Schulungssitzungen mit Kursleiter Speicherorte für Klassenzimmer- und virtuelle Klassenzimmermodule erstellen können. |
   | **Autoren das Ändern und Löschen von Speicherorten erlauben** | Aktivieren Sie diese Option, damit Autoren die Speicherorte für Klassenzimmer und virtuelle Klassenzimmer bearbeiten oder löschen können. |

1. Wählen Sie **Speichern**.

## Erstellen und Verwalten von Speicherorten für Klassenzimmer

Administratoren können Standorte für Klassenzimmer erstellen und verwalten, die Autoren beim Erstellen von Schulungssitzungen im Klassenzimmer und virtuellen Klassenzimmer wiederverwenden können. Adobe Learning Manager unterstützt zwei Speicherortformate:

* **Einzelfeldformat**: Jeder Klassenzimmerstandort wird durch ein einzelnes Feld **Standortname** identifiziert. Weitere Informationen finden Sie unter [Hinzufügen eines Klassenzimmerstandorts mit einem Einzelfeldformat](#add-a-classroom-location-using-a-single-field-format).
* **Vierfeldformat**: Jeder Klassenzimmerstandort ist in **Land**, **Bundesland/Provinz/Region**, **Stadt** und **Standortname** organisiert, wodurch die Verwaltung von Standorten in mehreren Regionen vereinfacht wird. Wenn Ihr Konto derzeit das Einzelfeldformat verwendet, schließen Sie die einmalige Migration ab, bevor Sie zum Vierfeldformat wechseln. Weitere Informationen finden Sie unter [Migrieren zur Methode mit vier Feldern](#migrate-classroom-locations-to-the-four-field-format).

### Fügen Sie einen Speicherort für das Klassenzimmer mithilfe eines Einzelfeldformats hinzu

Sie können einen Speicherort für ein Klassenzimmer hinzufügen, indem Sie das Format für einzelne Felder verwenden:

1. Melden Sie sich bei der Adobe Learning Manager als **Administrator** an.
1. Wählen Sie **Einstellungen** > **Standorte für Klassenzimmer**.
1. Wählen Sie **Hinzufügen** > **Neuer Speicherort**.
1. Geben Sie die folgenden Details im Dialogfeld &quot;**Speicherort des Klassenzimmers**&quot; ein:

   1. Geben Sie den **Standortnamen** ein. Verwenden Sie einen eindeutigen Namen. Andernfalls zeigt Learning Manager eine Fehlermeldung an.
   1. Geben Sie die Positionsbeschreibung in das Feld **Standortinformationen** ein. Dieses Feld ist optional.
   1. Geben Sie die **URL des Standorts** an. Die Teilnehmer können diese Informationen in den Details des Klassenzimmers sehen. Bei Bedarf kann die URL auch eine URL für den Kartenstandort sein. Dies ist ein optionales Feld.
   1. Geben Sie den Standort **Region** ein, und wählen Sie ihn aus. Dieses Feld ist optional.
   1. Geben Sie die Anzahl der verfügbaren Lizenzen in das Feld **Sitzplatzbeschränkung** ein. Dies gibt die Sitzplatzkapazität des Klassenzimmers an. Dieser Wert kann beim Erstellen des tatsächlichen Schulungsereignisses mit Kursleiter geändert werden.
      ![Hinzufügen eines Klassenzimmerspeicherorts mithilfe des Formats für ein einzelnes Feld](assets/add-classroom-location-single-field-format.jpeg)
      *Fügen Sie einen Speicherort für das Klassenzimmer mithilfe des Formats für ein einzelnes Feld hinzu.*

### Migrieren von Speicherorten für Klassenzimmer in das Vierfeldformat

Wenn in Ihrem Konto das alte Format für den Speicherort des Klassenzimmers mit einem Feld verwendet wird, migrieren Sie die vorhandenen Speicherorte für Klassenzimmer, bevor Sie das Format mit vier Feldern aktivieren. Das Vierfeldformat organisiert Standortdaten in **Land**, **Bundesland/Provinz/Region**, **Stadt** und **Standortname**, wodurch die Verwaltung von Standorten in mehreren Regionen vereinfacht wird.

Diese Migration ist ein einmaliger Prozess. Nachdem Sie zum Vierfeldformat gewechselt sind, können Sie das Konto nicht mehr auf das Einzelfeldformat zurücksetzen.

So migrieren Sie vorhandene Speicherorte:

1. Navigieren Sie zu **Admin** > **Speicherorte für Klassenzimmer** und wählen Sie die Registerkarte **Einstellungen** aus.
1. Wählen Sie im Abschnitt **Speicherortformatmigration** die Option **Export** aus.

   Eine CSV-Datei mit Ihren vorhandenen Speicherorten in Klassenzimmern wird heruntergeladen. Die folgenden Spalten sind verfügbar:

   1. **Raum-ID**: Eindeutiger Bezeichner für den Speicherort.
   1. **Gebietsschema**: Gebietsschema für den übersetzten Standortnamen und die Standortinformationen.
   1. **Name**: Name des Klassenzimmers.
   1. **Land**: Land, in dem sich das Klassenzimmer befindet.
   1. **Status**: Bundesland, Bundesland oder Region, in dem bzw. in der sich das Klassenzimmer befindet
   1. **Stadt**: Stadt, in der sich das Klassenzimmer befindet.
   1. **info**: Zusätzliche Details wie Name des Gebäudes, Stockwerk oder Zimmernummer.
   1. **url**: Mit dem Speicherort verknüpfte URL, z. B. ein Map-Link.
   1. **Sitzlimit**: Maximale Sitzplatzkapazität des Klassenzimmers.

   >[!NOTE]
   >
   >Die exportierte CSV-Datei enthält immer die Spalten des Speicherortformats mit vier Feldern, auch wenn das Format mit vier Feldern nicht aktiviert ist.

   ![Migrationsfortschritt überprüfen](assets/location-format-migration-progress.png)

   *Überprüfen Sie den Migrationsfortschritt, bevor Sie zum Speicherortformat mit vier Feldern wechseln.*

1. Aktualisieren Sie die CSV-Datei für jeden Spaltennamen mit den erforderlichen Informationen, z. B. Land, Bundesland, Stadt, zusammen mit allen anderen erforderlichen Informationen.
1. Wählen Sie **Importieren** aus und laden Sie dann die aktualisierte CSV-Datei hoch.

   Adobe Learning Manager validiert die Daten und aktualisiert den Migrationsfortschritt.

1. Wenn der Migrationsfortschrittsbalken 100 % erreicht, wählen Sie **Zu neuem Vierfeldformat wechseln**. Statusaktualisierungen des **Standortformats** auf **Migration abgeschlossen**.

   Status der Migration des Speicherortformats abgeschlossen ![1](assets/location-format-migration-complete.png)

   Die Migration des *Standortformats wird auf den Status &quot;Migration abgeschlossen&quot; aktualisiert.*

## Fügen Sie Klassenzimmerpositionen mithilfe eines Vierfeldformats hinzu

Nach Abschluss der einmaligen Migration können Administratoren Standorte für Klassenzimmer im Format mit vier Feldern erstellen. Autoren können diese Orte dann beim Erstellen von Schulungssitzungen mit Kursleiter wiederverwenden. Administratoren können einzelne Speicherorte für Klassenzimmer hinzufügen oder mehrere Speicherorte für Klassenzimmer aus einer CSV-Datei importieren.

### Klassenzimmerposition hinzufügen

Mit Standorten für Klassenzimmer können Sie Schulungsplätze standardisieren und die Sitzungsplanung für Autoren vereinfachen.

So fügen Sie einen Speicherort für ein Klassenzimmer hinzu:

1. Wählen Sie in der Admin-App **Einstellungen** > **Speicherorte für Klassenzimmer**.

   ![Registerkarte &quot;Alle Speicherorte&quot;](assets/all-locations-tab.png)

   *Wählen Sie die Registerkarte **Alle Speicherorte**&#x200B;aus, um einen Speicherort für ein Klassenzimmer hinzuzufügen.*

1. Wählen Sie **Hinzufügen** > **Neuer Speicherort** in der oberen rechten Ecke.

   Das Popup-Fenster &quot;**Speicherort des Klassenzimmers**&quot; wird angezeigt.

   ![Pop-up-Fenster &quot;Speicherort für Klassenzimmer&quot;](assets/classroom-location-popup-window.png)

   *Geben Sie die Details im Fenster &quot;Speicherort des Klassenzimmers&quot; ein.*

1. Geben Sie im Popup-Fenster &quot;**Speicherort des Klassenzimmers**&quot; die folgenden Details ein:

   | **Feld** | **Beschreibung** |
   |---|---|
   | **Land** | Wählen Sie das Land, in dem sich das Klassenzimmer befindet. |
   | **Bundesland/Provinz/Region** | Wählen Sie das Bundesland, das Bundesland oder die Region aus. |
   | **Stadt** | Wählen Sie die Stadt aus, in der sich das Klassenzimmer befindet. |
   | **Standortname** | Geben Sie den Namen des Klassenzimmers bzw. Raums ein. |
   | **Standortinformationen** | Geben Sie zusätzliche Details ein, z. B. den Namen des Gebäudes, die Etage oder die Raumnummer. |
   | **URL des Speicherorts** | Geben Sie eine URL für den Speicherort ein, z. B. einen Map-Link. |
   | **Sitzplatzbeschränkung** | Geben Sie die maximale Sitzplatzkapazität des Klassenzimmers ein. |

1. Wählen Sie **Speichern**.

   Der Speicherort des Klassenzimmers wird gespeichert und auf der Registerkarte **Alle Speicherorte** aufgeführt.

### Klassenzimmerspeicherorte gesammelt importieren

Verwenden Sie den Massenimport, um mehrere Klassenzimmerspeicherorte hinzuzufügen oder vorhandene Speicherorte mithilfe einer CSV-Datei zu aktualisieren.

So importieren Sie mehrere Klassenzimmerspeicherorte gleichzeitig:

1. Wählen Sie in der Admin-App **Einstellungen** > **Speicherorte für Klassenzimmer**.
1. Wählen Sie auf der Registerkarte **Alle Speicherorte** die Option **CSV** herunterladen.

   Eine CSV-Datei mit Ihren vorhandenen Klassenzimmerspeicherorten wird heruntergeladen. Die folgenden Spalten sind verfügbar:

   1. **Raum-ID**: Eindeutiger Bezeichner für den Speicherort.
   1. **Gebietsschema**: Gebietsschema für den übersetzten Standortnamen und die Standortinformationen.
   1. **Name**: Name des Klassenzimmers.
   1. **Land**: Land, in dem sich das Klassenzimmer befindet.
   1. **Status**: Bundesland, Bundesland oder Region, in dem bzw. in der sich das Klassenzimmer befindet
   1. **Stadt**: Stadt, in der sich das Klassenzimmer befindet.
   1. **info**: Zusätzliche Details wie Name des Gebäudes, Stockwerk oder Zimmernummer.
   1. **url**: Mit dem Speicherort verknüpfte URL, z. B. ein Map-Link.
   1. **Sitzlimit**: Maximale Sitzplatzkapazität des Klassenzimmers.

1. Aktualisieren Sie die CSV-Datei für jeden Spaltennamen mit den erforderlichen Informationen, z. B. Land, Bundesland, Stadt, zusammen mit allen anderen erforderlichen Informationen.
1. Wählen Sie **Hinzufügen** > **Speicherorte für Massenimport** in der oberen rechten Ecke aus.

   Das Popupfenster **Speicherorte in CSV-Datei importieren** wird angezeigt.

   ![CSV-Pop-up-Fenster &quot;Speicherorte importieren&quot;](assets/import-locations-csv-popup.png)

   *Ziehen Sie die CSV-Datei mit den aktualisierten Informationen per Drag &amp; Drop.*

1. Ziehen Sie die aktualisierte CSV-Datei in den Upload-Bereich.
1. Wählen Sie **Importieren**.

   Die Speicherorte für Klassenzimmer werden aktualisiert.

## Hinzufügen von Übersetzungen für einen Speicherort im Klassenzimmer

Fügen Sie Übersetzungen für die Felder &quot;**Location Name**&quot; und &quot;**Location Information**&quot; hinzu, um die Details zum Klassenzimmerstandort in den bevorzugten Sprachen der Teilnehmer anzuzeigen.

So fügen Sie Übersetzungen für einen Speicherort für ein Klassenzimmer hinzu:

1. Wählen Sie **Alle Speicherorte** > **Hinzufügen** aus den **Speicherorten für Klassenzimmer**.
1. Wählen Sie **Neuer Speicherort**.

   Das Popup-Fenster &quot;**Speicherort des Klassenzimmers**&quot; wird angezeigt.

1. Wählen Sie **Neue Sprache hinzufügen**.

   Das Popupfenster **Neue Sprache hinzufügen** wird angezeigt.

   ![Popup-Fenster &quot;Neue Sprache hinzufügen&quot;](assets/add-new-language-popup.png)

   *Wählen Sie die Sprachen im Popupfenster &quot;Neue Sprache hinzufügen&quot; aus.*

1. Wählen Sie **Speichern**.

   Die Übersetzungen werden gespeichert und den Benutzern angezeigt.

>[!NOTE]
>
>Übersetzungen werden nur von den Feldern &quot;**Location Name**&quot; und &quot;**Location Information**&quot; unterstützt. Standortdetails wie **Land**, **Land/Provinz/Region** und **Stadt** werden nicht übersetzt.

## Bearbeiten eines Klassenzimmerspeicherorts

Um einen Speicherort für ein Klassenzimmer zu bearbeiten, führen Sie die folgenden Schritte aus:

1. Wählen Sie in der Admin-App **Einstellungen** > **Speicherorte für Klassenzimmer**.
1. Bewegen Sie den Mauszeiger über den gewünschten Speicherort des Klassenzimmers, den Sie bearbeiten möchten.

   ![Symbol &quot;Bearbeiten&quot; für den Speicherort eines Klassenzimmers](assets/edit-classroom-location-icon.png)

   *Bewegen Sie den Mauszeiger über den erforderlichen Speicherort des Klassenzimmers und wählen Sie das Symbol &quot;Bearbeiten&quot; aus.*

1. Wählen Sie das Symbol **Speicherort des Klassenzimmers bearbeiten**.

   Das Popupfenster &quot;Position des Klassenzimmers&quot; wird angezeigt.

1. Ändern Sie den Speicherort des Klassenzimmers, und wählen Sie **Speichern**.

## Löschen eines Klassenzimmerspeicherorts

Um einen Speicherort für ein Klassenzimmer zu löschen, führen Sie die folgenden Schritte aus:

1. Wählen Sie in der Admin-App **Einstellungen** > **Speicherorte für Klassenzimmer**.
1. Bewegen Sie den Mauszeiger über den gewünschten Speicherort des Klassenzimmers, den Sie löschen möchten.
1. Wählen Sie das Symbol **Speicherort des Klassenzimmers löschen**.

   Das Popupfenster &quot;Bestätigung erforderlich&quot; wird angezeigt.

   ![Popup-Fenster &quot;Bestätigung erforderlich&quot;](assets/delete-classroom-location-confirmation.png)

   *Wählen Sie &quot;Löschen&quot; aus, um das Löschen eines Klassenzimmerstandorts zu bestätigen.*

1. Wählen Sie **Löschen** aus.

## Häufige Fragen

1. **Was passiert mit vorhandenen Standorten für Klassenzimmer nach Abschluss der Migration?**<br>
Sie können das Format für Speicherorte mit vier Feldern nur aktivieren, nachdem alle vorhandenen Speicherorte manuell oder über einen CSV-Upload migriert wurden. Sobald das Format mit vier Feldern aktiviert ist, werden in allen vorhandenen Kursen, die Speicherorte für Klassenzimmer verwenden, Speicherorte im neuen Format angezeigt.

1. **Muss ich die exportierte CSV-Datei manuell so umstrukturieren, dass sie dem vier Felder umfassenden Speicherortformat entspricht?**<br>
Nein. Die exportierte CSV-Datei verwendet immer das Speicherortformat mit vier Feldern, unabhängig davon, ob es derzeit aktiviert ist. Sie müssen nur fehlende Werte aktualisieren, bevor Sie die Datei importieren.

1. **Wirkt sich die Migration auf Adobe Learning Manager-Berichte aus?**<br>
Ja. Nach der Migration werden in Berichten, die Informationen zum Speicherort des Klassenzimmers enthalten, Speicherorte im folgenden Format angezeigt:

   **Land > Bundesland/Provinz/Region > Stadt > Ortsname**

   Dieses Format ersetzt den vorherigen Positionswert für ein einzelnes Feld.

1. **Was passiert, wenn ich das Speicherortformat für vier Felder nicht aktiviere?**<br>
Für Autoren oder Teilnehmer ändert sich nichts. Die Speicherorte für Klassenzimmer werden weiterhin wie gewohnt angezeigt und funktionieren unter Verwendung des vorhandenen Einzelfeldformats so lange, bis ein Administrator die Migration abschließt und das Vierfeldformat aktiviert.
