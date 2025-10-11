---
title: Benutzerdefinierte Rolle mit Ankündigungsberechtigungen mit Umfang
jcr-language: en_us
description: Erfahren Sie, wie Sie eine benutzerdefinierte Rolle in Adobe Learning Manager erstellen, die Ankündigungen nur für ausgewählte Kataloge und Benutzergruppen zulässt.
source-git-commit: 85eeebb33a67bf5528c88b26941345e00e98e0d3
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 0%

---


# Benutzerdefinierte Rolle mit Ankündigungsberechtigungen mit Umfang

Administratoren können benutzerdefinierte Rollen mit Ankündigungsberechtigungen erstellen, die auf bestimmte Kataloge und Benutzergruppen beschränkt sind. Dies stellt sicher, dass Ankündigungen zielgerichtet, relevant und nur für die gewünschten Teilnehmer sichtbar sind. Durch Ankündigungen mit Umfang wird sichergestellt, dass die richtigen Benutzer eine relevante Ankündigung erhalten, ohne Details an andere zu senden.

## Erstellen einer benutzerdefinierten Rolle mit einem bestimmten Umfang

Der Administrator kann eine benutzerdefinierte Rolle mit Ankündigungsberechtigungen erstellen, die auf einen bestimmten Katalog und eine bestimmte Benutzergruppe beschränkt sind.

So erstellen Sie eine benutzerdefinierte Rolle mit einem bestimmten Umfang:

1. Melden Sie sich bei Adobe Learning Manager als Administrator an.
2. Wählen Sie im linken Navigationsbereich **[!UICONTROL Benutzer]** aus.

   ![](assets/select-uses-admin.png)
   _Anwendern benutzerdefinierte Rollen für zielgerichtete Berechtigungen und Verantwortlichkeiten in Adobe Learning Manager zuweisen_

3. Wählen Sie Benutzerdefinierte Rollen aus.
4. Wählen Sie Benutzerdefinierte Rolle erstellen aus.

   ![](assets/create-custom-roles.png)
   _Benutzern benutzerdefinierte Rollen zuweisen, um Berechtigungen anzupassen und die administrative Steuerung für bestimmte Benutzergruppen oder Kataloge zu optimieren_

5. Geben Sie den Namen und die Beschreibung der benutzerdefinierten Rolle ein.
6. Wählen Sie Ankündigung unter Kontoberechtigungen aus.

   ![](assets/select-announcement.png)
   _Aktivieren Sie die Ankündigungsberechtigungen unter &quot;Kontoberechtigungen&quot;, damit benutzerdefinierte Administratoren die zielgerichtete Kommunikation innerhalb des Bereichs verwalten können_

7. Wählen Sie unter Umfang für Funktionsberechtigungen Zugriff pro Katalog festlegen und wählen Sie den Katalog aus.
8. Wählen Sie im selben Abschnitt Zugriff pro Benutzergruppe festlegen und wählen Sie die erforderlichen
Benutzergruppe.

   ![](assets/select-scope-announcement.png)
   _Legen Sie Benutzergruppen- und Katalogbereiche fest, um sicherzustellen, dass benutzerdefinierte Administratoren Berechtigungen verwalten und nur innerhalb ihrer zugewiesenen Bereiche auf sie zugreifen können_

9. Wählen Sie den Benutzer aus, dem Sie diese benutzerdefinierte Rolle zuweisen möchten, und fügen Sie ihn hinzu. Die zugewiesenen Benutzer können eine Ankündigung für ihren Bereich erstellen.

Ein benutzerdefinierter Administrator kann Ankündigungen erstellen, die auf die zugewiesenen Benutzergruppen und Kataloge beschränkt sind, um sicherzustellen, dass Nachrichten die richtige Zielgruppe erreichen, und um unnötige Benachrichtigungen zu vermeiden. Bei Benachrichtigungen und E-Mail-Ankündigungen können Administratoren zusätzliche Benutzergruppen hinzufügen, diese werden jedoch nur von Benutzern innerhalb des definierten Bereichs empfangen. Für Ankündigungen von Empfehlungen und Mastertiteln können Sie nur Benutzergruppen innerhalb des zugewiesenen Bereichs auswählen.

## Ankündigung für den zugewiesenen Bereich erstellen

Ein benutzerdefinierter Administrator kann Ankündigungen erstellen, die auf die zugewiesenen Benutzergruppen und Kataloge beschränkt sind, um sicherzustellen, dass Nachrichten die richtige Zielgruppe erreichen, und um unnötige Benachrichtigungen zu vermeiden.

So erstellen Sie eine Ankündigung für den zugewiesenen Bereich:

1. Melden Sie sich bei Adobe Learning Manager als benutzerdefinierter Administrator an.
2. Wählen Sie im linken Navigationsbereich **[!UICONTROL Ankündigung]** aus.
3. Wählen Sie **[!UICONTROL Hinzufügen]** aus.

   ![](/help/migrated/assets/create-add-announcement.png)
   _Seite &quot;Ankündigungen&quot; in Adobe Learning Manager, auf der Administratoren Ankündigungen für Zielbenutzergruppen erstellen und verwalten können_

4. Wählen Sie im Dropdown-Menü den **[!UICONTROL Ankündigungstyp]** aus.
a. **[!UICONTROL Als Benachrichtigung]**
b. **[!UICONTROL Als Mastertitel]**
c. **[!UICONTROL Als Empfehlung]**
d. **[!UICONTROL Als E-Mail]**
5. Wählen Sie **[!UICONTROL Als Mastertitel]** aus.
6. Wählen Sie die Sprache aus und laden Sie ein Bild für den Mastertitel hoch.
7. Optional können Sie eine URL für die Aktionsschaltfläche hinzufügen.

   ![](/help/migrated/assets/announcement-screen.png)
   _Bildschirm &quot;Ankündigung erstellen&quot;, mit dem Administratoren den Ankündigungstyp festlegen, Anhänge hochladen und Aktionsschaltflächen hinzufügen können_

   Der zugewiesene Bereich ist im Abschnitt **[!UICONTROL Bereich]** vorausgewählt und kann von benutzerdefinierten Administratoren nicht geändert werden.

   >[!NOTE]
   >
   >**[!UICONTROL Für Benachrichtigungen]** und **[!UICONTROL E-Mail]**-Ankündigungen können sie zusätzliche Benutzergruppen und Kataloge enthalten, wenn diese sich mit ihrem zugewiesenen Bereich überschneiden.

8. Wählen Sie **[!UICONTROL Speichern]**.

Nur Teilnehmer im Bereich des benutzerdefinierten Administrators können die Ankündigung anzeigen. In diesem [Artikel](/help/migrated/administrators/feature-summary/announcements.md) erfahren Sie, wie Sie mehrere Arten von Ankündigungen erstellen.

## Zurücksetzen des Bereichs durch benutzerdefinierte Administratoren

Benutzerdefinierte Administratoren können den Bereich ihrer veröffentlichten Ankündigungen zurücksetzen, wenn ein Administrator den Bereich geändert hat. Sobald der Umfang zurückgesetzt wurde, wird der aktualisierte Umfang auf die Ankündigung angewendet und nur Teilnehmer innerhalb des neuen Bereichs können die Ankündigung sehen.

Zurücksetzen des Gültigkeitsbereichs:

1. Melden Sie sich bei Adobe Learning Manager als benutzerdefinierter Administrator an.
2. Wählen Sie im linken Navigationsbereich **[!UICONTROL Ankündigung]** aus.
3. Wählen Sie die Registerkarte **[!UICONTROL Veröffentlicht]** aus.
4. Wählen Sie eine beliebige Ankündigung und dann das Einstellungssymbol aus.
5. Wählen Sie **[!UICONTROL Bearbeiten]**.

   ![](/help/migrated/assets/select-edit-published-announcement.png)
   _Ankündigungsbildschirm mit den veröffentlichten Ankündigungen mit Bearbeitungs-, Veröffentlichungs- und anderen Optionen_

6. Wählen Sie **Zurücksetzen**.

   ![](/help/migrated/assets/reset-the-scope.png)
   _Ankündigung mit einer Benachrichtigung zur Bereichsänderung, wobei benutzerdefinierte Administratoren die Möglichkeit haben, die Bereichsauswahl zurückzusetzen und zu aktualisieren, um neue Zugriffsberechtigungen anzuzeigen_

Der Umfang wird aktualisiert und nur Benutzer innerhalb des aktualisierten Bereichs können die Ankündigung anzeigen.

## Ankündigung über die Administrator-Benutzeroberfläche bearbeiten

Administratoren können alle Ankündigungen bearbeiten und verwalten, die von benutzerdefinierten Administratoren erstellt wurden. Wenn ein Administrator versucht, eine Ankündigung zu bearbeiten, die von einem benutzerdefinierten Administrator mit einem bestimmten Bereich erstellt wurde, wird in der Ankündigung eine Warnmeldung mit der Meldung **[!UICONTROL Bereich entfernen]** angezeigt. Der Administrator kann den Bereich entfernen, um die Ankündigung allen zur Verfügung zu stellen. In diesem Fall erhält der benutzerdefinierte Administrator eine Warnung, dass der Umfang der Ankündigung geändert wurde.

So bearbeiten Sie die Ankündigung über die Administrator-Benutzeroberfläche:

1. Melden Sie sich bei Adobe Learning Manager als Administrator an.
2. Wählen Sie im linken Navigationsbereich **[!UICONTROL Ankündigung]** aus.
3. Wählen Sie die Registerkarte **[!UICONTROL Veröffentlicht]** aus.
4. Wählen Sie eine beliebige Ankündigung und dann das Einstellungssymbol aus.
5. Wählen Sie **[!UICONTROL Bearbeiten]**.

   ![](/help/migrated/assets/select-edit-published-announcement.png)
   _Ankündigungsbildschirm mit den veröffentlichten Ankündigungen mit Bearbeitungs-, Veröffentlichungs- und anderen Optionen_

6. Wählen Sie **[!UICONTROL Entfernen]** aus.

   ![](/help/migrated/assets/remove-the-scope.png)
   _Ankündigungsbildschirm, der angibt, dass der Bereich entfernt werden muss, damit Administratoren Ankündigungen bearbeiten können, die für Benutzergruppen mit Umfang erstellt wurden_

Der Administrator kann die Ankündigung bearbeiten, nachdem er den Bereich entfernt hat.
