---
description: Weitere Informationen zur Konfiguration erweiterter Einstellungen in Adobe Learning Manager
jcr-language: en_us
title: Erweiterte Einstellungen in Adobe Learning Manager
source-git-commit: 03123dcd8d9066cdfcb0fe97e61acb3df625a23e
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 34%

---


# Erweiterte Einstellungen in Adobe Learning Manager

## Katalogbeschriftungen

Katalogbeschriftungen in Adobe Learning Manager werden verwendet, um Lernobjekte (Kurse, Zertifizierungen, Lernpfade usw.) mit Tags zu versehen mit bestimmten Feldern und Werten. Diese Beschriftungen helfen Ihnen und Autoren dabei, Inhalte effektiv zu kategorisieren und zu organisieren, sodass Sie Inhalte besser filtern, verfolgen und Berichte erstellen können.

Weitere Informationen finden Sie unter [Katalogbeschriftungen in Adobe Learning Manager](/help/migrated/administrators/feature-summary/catalog-labels.md).


>[!NOTE]
>
>* Obligatorische Beschriftungen: Sie können festlegen, dass Katalogbeschriftungen für Autoren während der Kurserstellung obligatorisch sein sollen.
>* Arbeitsablauf für Autoren: Autoren müssen beim Erstellen oder Bearbeiten von Kursen Compliance-Beschriftungen hinzufügen, um eine ordnungsgemäße Kategorisierung sicherzustellen.

## Inhaltsordner

Mit Inhaltsordnern können Sie Inhalte organisieren und verwalten, indem Sie private oder öffentliche Ordner erstellen. Diese Funktion stellt sicher, dass Inhalte nur für bestimmte Autoren oder Gruppen zugänglich sind, wodurch eine bessere Kontrolle über die Sichtbarkeit und Verwaltung von Inhalten ermöglicht wird.

**Wichtigste Punkte:**

Ein Ordner ist ein Repository mit Inhalten, die einer Teilmenge der gesamten Inhaltsbibliothek in einem Konto entsprechen, und verfügt über die folgenden Eigenschaften:

* Nur Sie (Administrator) können einen Ordner erstellen, bearbeiten oder löschen.
* Sie können den Zugriff auf Ordner steuern, indem Sie Rollen nur für benutzerdefinierte Administratoren definieren.
* Der Inhalt muss jederzeit mit mindestens einem Ordner verknüpft sein. Zunächst werden alle Inhalte mit dem öffentlichen Ordner verknüpft, was später geändert werden kann.
* Der Inhalt kann zum Zeitpunkt der Erstellung mit mehreren Ordnern verknüpft werden, was auch durch einen Kopiervorgang möglich ist.
* Alle Ordnernamen müssen innerhalb des Kontos eindeutig sein, da andernfalls ein Fehler beim Benennen eines Ordners auftritt.

Ordner steuern nur die Sichtbarkeit von Inhalten und erstellen keine Kopien von Inhalten. Daher wird die Bearbeitung des Inhalts in allen zugehörigen Ordnern widergespiegelt.

**Öffentlicher Ordner**

Jedes Konto enthält einen öffentlichen Ordner. Anfänglich befinden sich alle Inhalte in diesem Ordner. Später können Autoren Inhalte aus diesem Ordner in andere Ordner verschieben. Ein öffentlicher Ordner verfügt über die folgenden Eigenschaften:

* Alle Inhalte, die mit diesem Ordner verknüpft sind, sind standardmäßig für alle Arten von Autoren verfügbar.
* Inhalte, die Teil eines öffentlichen Ordners sind, können nicht Teil eines anderen Ordners sein. Das Gleiche gilt auch umgekehrt.

Dieser Ordner kann nicht Teil einer konfigurierbaren Rollendefinition sein. Wenn also ein öffentlicher Ordner nicht in einer konfigurierbaren Rollendefinition enthalten ist, wird der Zugriff auf den öffentlichen Ordner nicht eingeschränkt.

**Privater Ordner**

Jeder von Ihnen erstellte Ordner ist ein privater Ordner.

**Inhaltsordner hinzufügen**

Um einen Inhaltsordner hinzuzufügen, führen Sie die folgenden Schritte aus:

1. Wählen Sie **[!UICONTROL Einstellungen]** > **[!UICONTROL Inhaltsordner]**.
2. Wählen Sie **[!UICONTROL Hinzufügen]**, um einen neuen Ordner zu erstellen.
3. Geben Sie den Namen und die Beschreibung des zu erstellenden Ordners ein.

   ![Alternativtext](assets/advanced-settings-picture1.png)

4. Wählen Sie **[!UICONTROL Speichern]**, um den Ordner zu erstellen.

**Ordnervorgänge**

* **[!UICONTROL Ordner hinzufügen]**: Um einen Ordner hinzuzufügen, wählen Sie den Ordner aus und wählen Sie dann **[!UICONTROL Hinzufügen]** in der oberen rechten Ecke des Bildschirms aus.
* **[!UICONTROL Ordner löschen]**: Wählen Sie zum Löschen eines Ordners den zu löschenden Ordner aus, wählen Sie das Menü **[!UICONTROL Aktionen]** aus, und wählen Sie dann **[!UICONTROL Ordner löschen]** aus.

## Standorte für Klassenzimmer

Erstellen und verwalten Sie eine Bibliothek mit physischen oder virtuellen Schulungsräumen. Diese Standorte können von Autoren und Administratoren verwendet werden, um ILT-Veranstaltungen (Instructor-Led Training = Schulungen mit Kursleiter) einzurichten. Die Funktion stellt sicher, dass die Details zum Schulungsraum, wie z. B. Sitzbeschränkungen und Standortinformationen, vorkonfiguriert und leicht zugänglich sind.

Weitere Informationen finden Sie unter [Klassenzimmerspeicherorte in Adobe Learning Manager hinzufügen](/help/migrated/administrators/feature-summary/classroom.md).

## Berichte

In diesem Abschnitt können Sie die Kompatibilitäts- und Gruppenerfolg-Dashboards konfigurieren.

![Alternativtext](assets/advanced-settings-picture2.png)

Weitere Informationen finden Sie unter:

* [Kompatibilitäts-Dashboard](/help/migrated/administrators/feature-summary/reports.md#compliance-dashboard)
* [Dashboard für den Gruppenerfolg](/help/migrated/administrators/feature-summary/group-success-dashboard.md)


