---
jcr-language: en_us
title: Aktivieren der vollständigen Kontrolle über den freigegebenen Katalog
description: Aktivieren der vollständigen Kontrolle über den freigegebenen Katalog im Adobe-Lernmanager
contentowner: saghosh
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---



# Aktivieren der vollständigen Kontrolle über den freigegebenen Katalog

## Katalog erstellen {#createcatalog}

Als Administrator können Sie einen Katalog mit Kursen, Lernprogrammen, Arbeitshilfen und Zertifizierungen erstellen.

Weitere Informationen finden Sie unter [Kataloge](/help/migrated/administrators/feature-summary/catalogs.md).

## Katalog freigeben {#sharecatalog}

Sie können die Kataloge für interne Benutzer einer Organisation oder für alle externen Benutzer freigeben. Die Freigabe erfolgt jedoch ausschließlich. Das heißt, dass ein intern freigegebener Katalog nicht für externe Gruppen freigegeben werden kann und umgekehrt.

Kurse, Lernprogramme, Arbeitshilfen und Zertifizierungen sind die unterstützten Lernobjekte für einen freigegebenen Katalog.

Weitere Informationen finden Sie unter [Kataloge freigeben](/help/migrated/administrators/feature-summary/catalogs.md).

## Aktivieren der vollständigen Kontrolle über den freigegebenen Katalog {#fullcontrol}

Sie können externen Konten vollen Zugriff auf Ihren Katalog gewähren. Der Administrator des Kontos kann dann den Katalog akzeptieren und dementsprechend Lerninhalte oder Module hinzufügen oder löschen.

So gewähren Sie einem externen Konto die vollständige Kontrolle:

1. Nachdem Sie einem Katalog Lernaktivitäten hinzugefügt haben, müssen Sie den Katalog für externe Benutzer freigeben.
1. Fügen Sie im Dialogfeld &quot;Externes Konto&quot; die Unterdomäne und die E-Mail-ID des Administrators der externen Organisation hinzu.
1. Aktivieren Sie in der Option Katalogsteuerung die Schaltfläche, um externen Benutzern die vollständige Kontrolle über den Katalog zu ermöglichen.

   ![](assets/catalog-control.png)

   *Vollständige Kontrolle über den freigegebenen Katalog zulassen*

   Wenn Sie die vollständige Katalogsteuerung zulassen, akzeptiert der Administrator der externen Organisation die Anforderung, Änderungen am Katalog zuzulassen. Der Autor der externen Organisation kann dann die Kurse bearbeiten oder Module hinzufügen.

   Weitere Informationen finden Sie in den folgenden Abschnitten.

## Administrator der externen Organisation {#administratorofexternalorganization}

Sobald der Administrator der vorherigen Organisation die vollständige Kontrolle über den Katalog aktiviert hat, akzeptiert der Administrator der externen Organisation die Anforderung, akzeptiert den Katalog und zeigt ihn an.

1. Klicken Sie auf das Benachrichtigungssymbol, um die Benachrichtigung anzuzeigen und den Katalog zu akzeptieren.

   <!--![](assets/notification-to-acceptcatalog.png)-->

1. Um die Einladung für den Katalog anzunehmen, klicken Sie auf &quot;Akzeptieren&quot;.
1. Wenn Sie in der Liste der Kataloge den Katalog starten, der für Sie freigegeben wurde, wird eine Meldung angezeigt, dass der Katalog jetzt die vollständige Kontrolle hat.

   ![](assets/catalog-details.png)

   *Katalogdetails anzeigen*

1. Sie können den Namen des Katalogs und die Beschreibung ändern.

## Katalog für Lernprogramm, Zertifizierung und Arbeitshilfen freigeben {#sharecatalogforlearningprogramcertificationandjobaids}

Wie die vollständige Katalogsteuerung für Kurse kann auch der Administrator die vollständige Katalogsteuerung für Folgendes gewähren:

* Lernprogramme
* Zertifikationen
* Arbeitshilfen

## Kurs zurücksetzen {#resetcourse}

1. Klicken Sie auf der Katalogkarte mit der fehlerhaften Verknüpfung auf **[!UICONTROL Kurs zurücksetzen]**.

<!-- ![](assets/reset-course.png)-->

1. Nachdem Sie auf die Schaltfläche &quot;Zurücksetzen&quot; geklickt haben, wird eine Warnmeldung angezeigt. Kurs zurücksetzen:

   * Entfernt alle neu hinzugefügten Inhalte aus dem Katalog.
   * Aktualisiert den Katalog synchron mit dem ursprünglichen freigegebenen Katalog.
   * Stellt die Beziehung zum übergeordneten Lernobjekt wieder her.

   Das Zurücksetzen des Katalogs ist unumkehrbar. Die Änderungen, die Sie am Katalog vorgenommen haben, können nicht rückgängig gemacht werden.

1. Um die Änderungen zu akzeptieren, klicken Sie auf Ja.
1. Im Kurskatalog können Sie sehen, dass der Katalog nicht über die Meldung verfügt *Verknüpfung unterbrochen* noch.

   Wenn Sie die Katalogdetails anzeigen, können Sie sehen, dass der Katalog jetzt in seinem ursprünglichen Zustand wiederhergestellt wurde.

## Fügen Sie ein Lernobjekt erneut hinzu {#readdalearningobject}

Wenn Sie versehentlich einen Kurs, ein Lernprogramm, eine Zertifizierung oder eine Arbeitshilfe entfernt haben, können Sie sie wiederherstellen.

Um ein gelöschtes Lernobjekt wiederherzustellen, klicken Sie auf &quot;Neu hinzufügen&quot;.

Diese Aktion kehrt die Aktion um und stellt das Lernobjekt in der Katalogansicht wieder her.

![](assets/re-add-button.png)

*Erneutes Hinzufügen eines Lernobjekts*

Nachdem Sie auf die Schaltfläche Neu hinzufügen geklickt haben, wird eine Bestätigungsmeldung angezeigt, dass das Lernobjekt erfolgreich zum Katalog hinzugefügt wurde.

## Externe Organisation {#externalorganization}

Sobald der Administrator des externen Kontos den Katalog akzeptiert hat, kann der Autor jetzt Kurse und Lernprogramme hinzufügen.

1. Als Benutzer erhalten Sie eine Benachrichtigung, dass der Katalog jetzt in Ihrem Konto verfügbar ist.
1. Um die Liste der Kurse anzuzeigen, klicken Sie **[!UICONTROL Kurse]** im linken Navigationsbereich. Sie können alle von Ihnen erstellten und für Sie freigegebenen Kurse anzeigen.
1. Klicken Sie zum Anzeigen der Kursdetails auf **[!UICONTROL Kurs anzeigen]** auf der Kurskarte.

   <!--![](assets/view-course.png)-->

1. Auf der Seite mit den Kursdetails werden Informationen zum Kurs und die freigegebenen Module angezeigt. Um ein Modul hinzuzufügen, klicken Sie auf Module hinzufügen. Wenn Sie den vorhandenen Modulen Module hinzufügen, werden die neuen Module am Ende der vorhandenen Module angezeigt. Sie können die Module immer neu anordnen.
1. Nachdem Sie die Module hinzugefügt haben, klicken Sie auf &quot;Neu veröffentlichen&quot;.

   Nachdem Sie die Module erneut veröffentlicht haben, wird auf der Katalogkarte eine Meldung angezeigt *Verknüpfung unterbrochen*.

   Da Sie den ursprünglichen Katalog mit neuen Modulen aktualisiert haben, existiert die bestehende Beziehung zum erworbenen Kurs nicht mehr.

   Das Lernobjekt ist nicht mehr mit dem Quellkonto synchron, da der Inhalt des Lernobjekts geändert wurde.

   <!--![](assets/link-broken.png)-->

Wenn Sie nach dem Hinzufügen und erneuten Veröffentlichen des Moduls das Gefühl haben, dass Sie versehentlich einen Kurs im Katalog hinzugefügt oder gelöscht haben, können Sie das Modul zurücksetzen und den ursprünglichen Zustand des Moduls wiederherstellen, als es erstmals mit voller Kontrolle freigegeben wurde.
