---
jcr-language: en_us
title: Adobe Learning Manager mit AEM integrieren
description: Erfahren Sie, wie Sie den Adobe Learning Manager mit Adobe Experience Manager integrieren (AEM)
contentowner: saghosh
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---



# Learning Manager mit AEM integrieren

## Übersicht {#overview}

Learning Manager ist ein Learning Management System mit einem integrierten Learning Content Management System. Benutzer verwalten ihre Lerninhalte, indem sie sie in den Lern-Manager hochladen, sodass der Lern-Manager die Versionierung, die Zuweisung zu Kursen, die Definition der Sichtbarkeit für Teilnehmer, die Verfolgung der Nutzung und die Berichterstattung an Administratoren durchführt.

Es gibt jedoch Benutzer, die ihre Inhalte auf Asset-Management-Systemen speichern und verwalten. Der Inhalt wird dann für verschiedene andere Funktionen neu verwendet.

Die verschiedenen Streifen in der Teilnehmer-App können in die AEM eingebettet werden. Jeder Teilnehmer, der sich bei der AEM anmeldet, sieht seine spezifischen Schulungsdaten in diesen Streifen.

## Herunterladen des Inhaltspakets {#downloadthecontentpackage}

Das Installationsprogramm wird als AEM-Inhaltspaket geliefert. [***Paket herunterladen***](https://github.com/adobe/captivate-prime-aem-components/releases).

Das Inhaltspaket ist als ZIP-Datei verfügbar und ist mit AEM 6.4 und AEM 6.5 kompatibel.

## Installieren der Lern-Manager-Komponente {#installcaptivateprimecomponent}

Installieren Sie das Learning Manager-Inhaltspaket mit dem AEM Package Manager:

>[!NOTE]
>
>Informationen zum Installieren von Paketen finden Sie unter  [***Mit Paketen arbeiten***](https://experienceleague.adobe.com/docs/experience-manager-65/administering/contentmanagement/package-manager.html?lang=en#how-to-work-with-packages).

1. Öffnen Sie als AEM den AEM Package Manager.

1. Klicken Sie auf die Schaltfläche **Paket hochladen**.

1. Klicken **[!UICONTROL Durchsuchen]** und laden Sie das Inhaltspaket hoch.
1. Klicken **[!UICONTROL Hochladen]**.
1. Nachdem das Paket hochgeladen wurde, installieren Sie das Inhaltspaket, indem Sie es auswählen und auf **[!UICONTROL Installieren]**.

   ![](assets/install-package.jpg)

## Generieren des Aktualisierungstokens {#generatetherefreshtoken}

Der AEM benötigt ein Aktualisierungstoken aus dem Learning Manager-Konto. Der Learning Manager-Integrationsadministrator generiert das Aktualisierungstoken.

1. Genehmigen Sie die empfohlene AEM Sites-App.

   Klicken **[!UICONTROL Anwendungen]** > **[!UICONTROL Highlights]** > **[!UICONTROL Adobe Experience Manager - Sites]**.

   ![](assets/launch-aem.jpg)

1. Klicken **[!UICONTROL Anwendungen]** > **[!UICONTROL Highlights]**, und öffnen Sie die Anwendung AEM Sites.

   Kopieren Sie die Anwendungs-ID und die Beschreibung.

1. Klicken **[!UICONTROL Ressourcen für Entwickler]** > **[!UICONTROL Zugriffstoken]**.

   ![](assets/click-tokens.jpg)

1. Geben Sie die folgenden Details ein:

   * Client-ID, die Anwendungs-ID.
   * Client-Geheimnis, das in der Beschreibung vorhanden ist.

1. Abrufen des OAuth-Codes Sie müssen die v2-API im Umleitungs-URI verwenden.
1. Klicken **[!UICONTROL Senden]** und rufen Sie das Aktualisierungstoken ab.

## Konfigurieren Sie das Widget in AEM {#configurethewidgetinaem}

Für die Widgetkonfiguration benötigt der AEM nur das Aktualisierungstoken, das vom Learning Manager-Integrationsadministrator bereitgestellt wird.

Sie können auch mehrere Kontokonfigurationen auf mehreren Seiten festlegen.

1. Klicken **[!UICONTROL Tools]** > **[!UICONTROL Cloud Service]** > **[!UICONTROL Captivate Learning Manager Widget-Konfiguration]**.
1. Klicken **[!UICONTROL Erstellen]**.
1. Geben Sie hier das Aktualisierungstoken ein. Richten Sie die anderen Einstellungen ein.
1. Der Hostname sollte für EU-Regionen in &quot;learningManagereu&quot; geändert werden.
1. Speichern und schließen Sie die Konfiguration.
1. Wählen Sie eine Konfiguration aus und veröffentlichen Sie die Konfiguration.

## Autor AEM {#aemauthor}

Der AEM muss zuerst die Komponente in AEM Vorlage hinzufügen.

Der AEM-Autor kann dann die Adobe Learning Manager-Komponente per Drag &amp; Drop ziehen und entsprechend konfigurieren.

Für die Lern-Manager-Komponente muss die im obigen Schritt erstellte Konfiguration der Seite zugeordnet werden.  Der Autor kann die Konfiguration zuordnen, indem er unter Seiteneigenschaften bearbeiten **[!UICONTROL Erweitert]** > **[!UICONTROL Konfiguration]** > **[!UICONTROL Cloud-Konfiguration]** und geben Sie den Konfigurationspfad an. Auf diese Weise kann der Autor Konfigurationen für mehrere Learning Manager-Konten erstellen und jedes Konto verschiedenen Sites zuordnen. Wenn eine Konfiguration nicht der Seite zugeordnet ist, liest die Komponente die Konfiguration von der übergeordneten Seite rekursiv, bis sie eine findet.

## Teilnehmer {#learner}

Der Teilnehmer kann die Kurse von der Seite aus absolvieren.

Um auf das Lern-Manager-Widget zugreifen zu können, sollte der Teilnehmer ein angemeldeter AEM Benutzer sein. Auch Eigenschaft **email** muss im Knoten &quot;/profile&quot; des Knoten rep:User des Teilnehmers vorhanden sein. Diese E-Mail-Adresse muss genau mit der im Learning Manager-Konto vorhandenen übereinstimmen.

Der Teilnehmer kann die Kurse von der Seite aus absolvieren.

Der Kursfortschritt wird ebenfalls gespeichert.

Die folgenden Widgets werden bereitgestellt:

1. Gamification
1. Lernkalender
1. Sozial-Widget
1. Katalog-Widget
1. Eigenes Lernen
1. Empfehlung auf der Grundlage von Peer Learning
1. Recommendations durch Administrator
1. Auf den Interessen der Teilnehmer basierende Empfehlung

Wenn keine Empfehlungen vorliegen, wird das Widget leer angezeigt.

## Unterstützung für Skyline

Skyline ist die Cloud-Version von AEM. Sie müssen zuerst Skyline über den Paketmanager installieren. Um die Skyline-Komponente in AEM zu verwenden, muss ein Benutzer im Learning Manager-Konto vorhanden sein. Mit anderen Worten, die E-Mail-Adresse des Benutzers muss im Konto vorhanden sein.

## Skyline bereitstellen

Die Schritte zum Konfigurieren von Skyline sind im Abschnitt  [GitHub-Repository](https://github.com/adobe/captivate-prime-aem-components).

## Katalog-Widget

Das Katalog-Widget zeigt einem Benutzer Schulungen aus einem bestimmten oder einem Satz von Katalogen an. Wählen Sie im Abschnitt &quot;Eigenschaften&quot; auf der Eigenschaftsseite einen Katalog aus den aufgeführten Optionen aus.

![](assets/catalog-widget.png)

Das Katalog-Widget enthält die folgenden Optionen:

* **[!UICONTROL Katalog-ID]:** Durch Kommas getrennte Katalog-IDs, für die die Schulung angezeigt werden muss.
* **[!UICONTROL Sortieren]:** Sortierreihenfolge für die Schulung Die Optionen sind: Name, Datum, dateCreated, dateEnrolled usw.
* **[!UICONTROL Teilnehmerstatus]:** Gibt alle Schulungen zurück, die die folgenden Filter verwenden: Registriert, Begonnen, Abgeschlossen und Nicht registriert. Die Suchergebnisse werden nicht angezeigt, wenn die Sortieroption dateEnrolled, dueDate oder dateEnrolled lautet.
* **[!UICONTROL Kenntnisname]:** Die Fähigkeit, die zum Filtern der exakten Schulung verwendet wird.
* **[!UICONTROL Tag-Name]:** Das zum Filtern der genauen Ergebnisse verwendete Tag.

Im Folgenden finden Sie einige zusätzliche Komponenten, die Sie anpassen können:

**[!UICONTROL Typen von Lernobjekten]:** Filtern Sie nach dem Typ des Lernobjekts. Die unterstützten Typen sind: Kurs, Zertifizierung, jobAid und learningProgram.

AEM ist der Titel einer Karte in einem Streifen zunächst leer. Geben Sie in den Eigenschaften den Namen des Titels in die Datei widgets.html ein.

**Anpassung**

Sie können das Erscheinungsbild des Layouts mithilfe der Datei widgets.html anpassen. Sie können das Erscheinungsbild der angezeigten Karten ändern und das Design anpassen.

Im Dialogfeld &quot; **[!UICONTROL Allgemeine Einstellungen]** &quot; können Sie die primären und sekundären Farben für die Karten auswählen und die Eigenschaften zum Anpassen des Designs angeben.

```
\{ 
 "globalCssText":"@import url('https://fonts.googleapis.com/css2?family=Grandstander:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');", 
 "fontNames":"Grandstander", 
 "cardLayout":{ 
 "cardLayoutName":"compact", 
 "cardPrimaryColor":"#376BA4", 
 "cardSecondaryColor":"#F98EB0", 
 "startedStateTextColor":"#ffffff", 
 "continueStateTextColor":"#ffffff", 
 "revisitStateTextColor":"#ffffff", 
 "startedStateColor":"#a0a0a0", 
 "continueStateColor":"#f9a122", 
 "revisitedStateColor":"#7fbc64", 
 "textPrimaryColor":"#ffffff", 
 "textSecondaryColor":"#d93f3f", 
 "navIconColor":"#a0a0a0" 
 } 
}
```

### Höhere Reihenfolgen-LO-Registrierung ignorieren

Wenn die Option **[!UICONTROL Höhere Reihenfolgen-LO-Registrierung ignorieren]** aktiviert ist und ein Benutzer direkt für ein Lernprogramm oder eine Zertifizierung registriert wird, werden die Kurse für diese Zertifizierung oder dieses Lernprogramm für den Benutzer in den Widgets angezeigt.

Wenn das Kontrollkästchen deaktiviert ist, werden die Kurse im Lernprogramm oder der Zertifizierung, für die sich der Benutzer nicht direkt registriert hat, nicht angezeigt.

![](assets/higher-order-lo.png)

Die Einstellung wird dann auf das Widget angewendet.

### Sicherheit

Die Felder &quot;Client-ID&quot; und &quot;Client-Geheimnis&quot; werden hinzugefügt. Darüber hinaus wird das Aktualisierungstoken maskiert. Wenn ein Benutzer die gesamte Konfiguration erstellt hat und der Benutzer die Konfiguration erneut öffnet, um sie zu bearbeiten, oder wenn ein anderer Benutzer diese Konfiguration öffnet, wird das Aktualisierungstoken maskiert.
