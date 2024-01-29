---
jcr-language: en_us
title: Adobe Learning Manager-Referenzsite-Paket (ALM-Referenzsite) für AEM Sites
description: Adobe Learning Manager (ALM) ist mit Adobe Experience Manager-Sites (AEM) integriert. Dies ermöglicht es Ihnen, Ihre eigene Website und Responsive-Mobilschnittstellen für Adobe Learning Manager mit minimalem Coding-Aufwand zu erstellen. Mit dieser Integration können Sie benutzerdefinierte Lernerlebnisse für Ihre Benutzer erstellen.
contentowner: saghosh
source-git-commit: 0ec031398f93c8396c0c9d49d172d62b2711481b
workflow-type: tm+mt
source-wordcount: '2146'
ht-degree: 0%

---


# Adobe Learning Manager-Referenzsite-Paket (ALM-Referenzsite) für AEM Sites

Adobe Learning Manager (ALM) ist mit Adobe Experience Manager-Sites (AEM) integriert. Dies ermöglicht es Ihnen, Ihre eigene Website und Responsive-Mobilschnittstellen für Adobe Learning Manager mit minimalem Coding-Aufwand zu erstellen. Mit dieser Integration können Sie benutzerdefinierte Lernerlebnisse für Ihre Benutzer erstellen.

Um eine solche Erfahrung zu erstellen, stellt ALM ein Adobe Learning Manager-Referenzsite-Paket (ALM-Referenzsite-Paket) für AEM Sites in Form einer ZIP-Datei bereit, die Sie auf Ihrer AEM Sites-Instanz installieren können.

Das Paket enthält AEM Sites-Webseitenvorlagen und -Websitekomponenten zusammen mit integrierbaren Widgets, z. B. Lernkatalog, integrierbare Widgets, Kalender usw.

Nachdem Sie das ALM-Referenzsite-Paket installiert haben, können Sie mit dem Erstellen einer Website für den Adobe Learning Manager beginnen, die Sie auf Ihrer AEM Sites-Instanz hosten können. Ihre Benutzer können dann die Komponenten per Drag &amp; Drop auf die Website ziehen.

ALM Referenz-Site-Paket installieren

## Voraussetzungen

* Lizenzen für AEM Sites und Adobe Commerce.
* AEM On-Premise 6.5 oder Adobe Experience Manager - Cloud Service
* Adobe Commerce 2.4.3

Nachdem Sie Ihre Umgebung von AEM Sites gesichert haben, müssen Sie das ALM-Referenzsite-Paket installieren. Dieses Paket enthält AEM Webseiten und Websitekomponenten, die zum Erstellen der Lernplattform beitragen.

Das Paket für die Referenz-Site wird auf der [**GitHub-Repository**](https://github.com/adobe/adobe-learning-manager-reference-site/releases/tag/1.0.0).

Weitere Informationen finden Sie in der README-Datei.

## Erstellen Sie eine Anwendung in [!DNL Adobe Learning Manager]

Nach der Installation des AEM Sitepakets müssen Sie eine ALM-Anwendung konfigurieren, um Ihr Lernportal mit der AEM zu verbinden.

Dieses Szenario gilt, wenn AEM mit [!DNL Adobe Learning Manager].

Führen Sie die folgenden Schritte aus:

1. Klicken Sie als Integrationsadministrator auf **[!UICONTROL Anwendungen]**.
1. Um eine neue Anwendung zu erstellen, klicken Sie in der rechten oberen Ecke der Seite auf **[!UICONTROL Registrieren]**.
1. Geben Sie auf der Seite Neue Anwendung registrieren die folgenden Details ein:

   1. Anwendungsname: Der Name der Anwendung, die Sie erstellen.
   1. URL: Die URL Ihrer Organisation.
   1. Domänen umleiten: Die Hostingdomänen der AEM-Website. Sie können auch Jokerzeichen angeben.
   1. Beschreibung: Die Beschreibung der Anwendung.
   1. Bereiche: Wählen Sie Lesezugriff auf die Teilnehmerrolle und Schreibzugriff auf die Teilnehmerrolle aus.
   1. Nur für dieses Konto?: Wählen Sie Ja aus, wenn Sie die Anwendung für das vorhandene ALM-Konto verwenden möchten.

1. Nachdem Sie die Änderungen vorgenommen haben, klicken Sie auf Speichern.

Notieren Sie sich die Anwendungsanmeldeinformationen auf dem Bildschirm.

![](assets/application-credentials.png)
*Anmeldeinformationen für die Anwendung*

Klicken Sie zum Genehmigen der Anwendung auf **[!UICONTROL Genehmigen]**.

## Token abrufen

1. Klicken Sie auf der Registerkarte Entwicklerressourcen auf **[!UICONTROL Zugriffstoken für Tests und Entwicklung]**.

   ![](assets/access-tokens.png)

   *Wählen Sie Zugriffstoken für Tests und Entwicklung.*

1. Geben Sie die folgenden Details ein:

   ![](assets/access-token-details.png)
   *Token-Details eingeben*

   1. OAuth-Code abrufen: Geben Sie die Client-ID aus dem vorherigen Abschnitt ein und ändern Sie den Umfang. Klicken Sie auf Senden , um den OAuth-Code zu erhalten.
   1. Aktualisierungstoken abrufen: Geben Sie die Client-ID und den Schlüssel aus dem vorherigen Abschnitt ein. Geben Sie außerdem den OAuth-Code ein, den Sie aus dem vorherigen Schritt erhalten haben. Klicken Sie auf Senden.
   1. Zugriffstoken abrufen: Geben Sie die Client-ID und den Schlüssel aus dem vorherigen Abschnitt ein. Geben Sie außerdem das Aktualisierungstoken ein, das Sie aus dem vorherigen Schritt bezogen haben. Klicken Sie auf Senden.
   1. Details zum Zugriffstoken abrufen: Geben Sie das Zugriffstoken aus dem vorherigen Schritt ein. Klicken Sie auf Senden.

1. Sie können die Details aus der folgenden JSON-Antwort abrufen. Die Antwort besteht aus dem Zugriffstoken, dem Aktualisierungstoken, der Benutzerrolle, der Konto-ID, der Benutzer-ID und der Zeit bis zum Ablauf. Notieren Sie sich das Aktualisierungstoken, da Sie es wiederverwenden.

## Konfigurieren des ALM-Kontos in AEM

1. Starten Sie Ihre AEM.
1. Klicken Sie auf Einstellungen > Cloud Service.
1. Klicken Sie auf Adobe Learning Manager-Konfiguration.

   ![](assets/alm-configuration.png)
   *Adobe Learning Manager-Konfiguration auswählen*

1. Klicken Sie auf Erstellen > Konfigurationsordner. Benennen Sie Ihren Ordner.

   ![](assets/create-folder.png)
   *Konfiguration erstellen*

1. Wählen Sie im Lernprojekt die Konfiguration aus, die Sie erstellt haben.

1. Geben Sie die Details der Konfiguration ein.

   ![](assets/account-congiguration.png)
   *Konfigurationsordner erstellen*

   1. Adobe-Lern-Manager-Modus: Wählen Sie aus, wie das Lernerlebnis für angemeldete und nicht angemeldete Teilnehmer gestaltet werden soll.
   1. Adobe-Lern-Manager-URL: Geben Sie die URL der ALM-Instanz ein, in der die Lern-Services gehostet werden.
   1. Konto-ID: Die ID des ALM-Kontos.
   1. Client-ID, geheimer Clientschlüssel und Token für die Autorenaktualisierung: Geben Sie die Anmeldeinformationen ein, die Sie beim Erstellen der Anwendung in ALM erhalten haben.
   1. Anpassung des Widgets: Weitere Informationen finden Sie unter [Mit AEM integrieren](/help/migrated/integrate-aem-learning-manager.md) `.`

1. Speichern und schließen Sie die Konfiguration.

### AEM + Adobe Learning Manager (angemeldete/nicht angemeldete Benutzer)

Mit dem Adobe Learning Manager können Sie jetzt Ihre Produkte und Schulungen Ihren bestehenden und potenziellen Kunden und Partnern präsentieren, ohne dass eine Kontoerstellung oder Anmeldung erforderlich ist. Diese Funktion unterstützt Sie bei der Einführung von Produkten und Schulungen, indem sie Teilnehmern eine schnelle und einfache Vorschau der Schulung bietet, mit der Sie Produktfunktionen hervorheben und fördern können. So könnt ihr eure Produkte und Angebote effektiv präsentieren, insbesondere bei potenziellen Kunden und Partnern, was zu einem erhöhten Produktbewusstsein führt. Der einfache Zugriff und die bessere Erreichbarkeit führen zu erhöhtem Interesse, was dazu beiträgt, dass sich Schulungsanmeldungen und Lernressourcen stärker durchsetzen.

Mit diesem Arbeitsablauf kann ein Teilnehmer eine Vorschau einer Schulung anzeigen, auf Schulungsinformationen zugreifen oder nach Schulungen suchen, ohne sich beim Adobe Learning Manager anzumelden. Dieser Arbeitsablauf gilt nicht für die native Lern-Manager-Oberfläche (gilt NUR für AEM Sites und andere Headless-Oberflächen).

**Konfigurieren und Aktivieren des Lernplattform-Connectors**

In diesem Abschnitt werden die Schritte hervorgehoben, die zum Konfigurieren und Aktivieren des folgenden Connectors erforderlich sind:

**Zugriff auf Schulungsdaten**

Dieser Connector ermöglicht es Ihrer AEM Sites-basierten oder einer anderen benutzerdefinierten Headless-Benutzeroberfläche, Schulungsinformationen abzurufen und für die Teilnehmer zu rendern und eine nahtlose Suche nach Schulungsinformationen durchzuführen, bevor oder nachdem sich ein Teilnehmer anmeldet.

Dieser Connector ist nur erforderlich, wenn Sie AEM Sites-basierte oder andere Headless-Schnittstellen verwenden.

Der Connector exportiert Schulungsmetadaten in eine Datenspeicher- und Abruflösung sowie ein Suchaktivierungssystem. Daher können Sie Ihre AEM Sites-basierte oder eine andere benutzerdefinierte Headless-Benutzeroberfläche konfigurieren, um diese beiden Dienste zu verwenden, um Schulungsdaten abzurufen, Webseiten zu rendern und den Teilnehmern eine optimierte Schulungssuche bereitzustellen. Beispielsweise kann eine nicht angemeldete, auf AEM Sites basierende Benutzeroberfläche die exportierten Metadaten verwenden, um einem Teilnehmer beim Suchen, Durchsuchen und Zugreifen auf Schulungsseiten zu helfen, die Schulungsinformationen anzeigen.

Aktivieren Sie diesen Connector, um Ihre AEM Sites-basierten Webseiten zu erstellen und zu rendern und Ihren Teilnehmern sowohl vor als auch nach der Anmeldung benutzerdefinierte Erlebnisse zu bieten. Aktivieren Sie diesen Connector, um Ihre AEM Sites-basierten Webseiten zu erstellen und zu rendern und Ihren Teilnehmern sowohl vor als auch nach der Anmeldung benutzerdefinierte Erlebnisse zu bieten.

* Adobe Learning Manager cdn Basis-URL: Geben Sie die Basis-URL des Datenabruf-CDN-Dienstpfads von der Verbindungsseite für den Schulungsdatenzugriff ein.
* Admin-Aktualisierungstoken : Geben Sie das Aktualisierungstoken ein, das Sie im vorherigen Abschnitt festgelegt haben.
* URL der Schulungsmetadatenbasis : Geben Sie die Basis-URL der Suchfunktion und des Dienstpfads für den Datenabruf über die Schulungsdatenzugriffsseite ein.
* Adobe-Lern-Manager-Registrierungs-URL: Geben Sie die vom Integrationsadministrator für das Konto generierte Selbstregistrierungs-URL ein, die von den Teilnehmern für die Registrierung für die Schulung verwendet wird.

### AEM + Adobe-Lern-Manager + Adobe Commerce (angemeldete/nicht angemeldete Benutzer)

Adobe Learning Manager bietet jetzt Lösungen, die Sie bei der nahtlosen Integration der Lernplattform mit Adobe Commerce unterstützen. Mit dieser Version können Sie Ihre nativen, AEM Sites basierten oder anderen Headless-Learning Manager-Schnittstellen ganz einfach mit Adobe Commerce verbinden. Mit dieser Integration können Sie E-Commerce-Funktionen innerhalb Ihrer Lernplattform realisieren. Sie können Ihren Kunden und Geschäftspartnern jetzt kostenpflichtige Schulungen anbieten und Schulungskäufe ganz einfach auf nativen und nicht nativen Lernmanager-Schnittstellen ermöglichen. Ein Teilnehmer kann auch eine Vorschau einer Schulung anzeigen, auf Schulungsinformationen zugreifen oder nach Schulungen suchen, ohne sich beim Adobe Learning Manager anzumelden.

Ein Benutzer kann die bereits AEM Anwendung verwenden und sie genehmigen, anstatt eine zu erstellen.

* Adobe Learning Manager cdn Basis-URL: Geben Sie die Basis-URL des Datenabruf-CDN-Dienstpfads von der Adobe Commerce-Verbindungsseite ein.
* Adobe Commerce-URL: Geben Sie die URL der Adobe Commerce-Instanz ein, die Sie verwenden.
* GraphQL-Proxypfad - Die clientseitigen Learning Manager-Komponenten greifen direkt auf den Adobe Commerce GraphQL-Endpunkt zu, sodass ein CORS-Fehler auftreten kann. Um diesen Fehler zu vermeiden, müssen alle Aufrufe entweder vom gleichen Endpunkt wie AEM oder über einen Proxy, der CORS-Header hinzufügt, bereitgestellt werden.
* Adobe Commerce-Store-Name : Geben Sie den Adobe Commerce-Store-Namen ein, den Sie im vorherigen Abschnitt festgelegt haben.
* Adobe Commerce-Kundentoken-Lebensdauer (in Sekunden) : Geben Sie die Kundentoken-Lebensdauer ein, die den vordefinierten Zeitraum für eine Anmeldesitzung angibt.
* Admin-Aktualisierungstoken : Geben Sie das Aktualisierungstoken ein, das Sie im vorherigen Abschnitt festgelegt haben.

## Webseiten anpassen

Passen Sie Ihre Webseiten mithilfe der Website mit den AEM Referenzen und der verfügbaren Widgets an.

1. Starten Sie Ihre AEM.
1. Klicken Sie auf Sites und öffnen Sie die Konfigurationsseite.
1. Klicken **[!UICONTROL Lernsite]** > **[!UICONTROL Sprachmaster]** > **[!UICONTROL Englisch]**. Alle Webseiten des Projekts sind in diesem Ordner enthalten.

   ![](assets/list-webpages.png)
   *Alle Webseiten anzeigen*

1. Wählen Sie eine beliebige Vorlage aus und klicken Sie auf **[!UICONTROL Bearbeiten]**.

1. Klicken Sie auf der Seite auf die Schaltfläche &quot;Komponenteneinstellungen&quot; und ändern Sie die Eigenschaften der Komponente.

   ![](assets/settings-button.png)
   *Schaltfläche &quot;Einstellungen auswählen&quot;*

1. Zeigen Sie eine Vorschau Ihrer Änderungen an oder veröffentlichen Sie die Seite.

## Erstellen von Webseiten

Neben den Vorlagen, die Sie verwenden können und die vom Referenzsitepaket bereitgestellt werden, können Sie auch Webseiten erstellen, die auf den Vorlagen in AEM basieren.

1. Klicken Sie auf der AEM auf &quot;Erstellen&quot; > &quot;Seite&quot;.

1. Wählen Sie die Vorlage aus, die Sie anpassen möchten. Klicken Sie auf Weiter.

1. Geben Sie die Seiteneigenschaften ein.

   ![](assets/page-properties.png)
   *Seiteneigenschaften*

1. Klicken Sie zum Erstellen der Seite auf **[!UICONTROL Erstellen]**.

1. Wählen Sie die neue Seite aus und klicken Sie auf **[!UICONTROL Bearbeiten]**.

1. Fügen Sie eine Komponente auf der Seite ein, z. B. **Learning - Inhalt**.

   ![](assets/learning-content.png)
   *Nach Site filtern*

1. Wählen Sie die erforderlichen Katalogfilter aus, die auf der Seite angezeigt werden.

## Website aus Blueprint erstellen

Das ALM Referenz-Site-Paket bietet einen &quot;Learning Site Blueprint&quot;, mit dem Sie eine Website für Ihre Lernplattform erstellen können. Mit AEM Blaupausen können Sie Webseiten direkt aus AEM Sites-Komponenten erstellen. Sie müssen keine Vorlagen verwenden.

1. Klicken Sie auf der AEM auf **[!UICONTROL Sites]**.

1. Klicken **[!UICONTROL Erstellen]** > **[!UICONTROL Site]**.

1. Klicken Sie auf &quot;Website-Blueprint&quot;.

   ![](assets/learning-site-blueprint.png)

   *Site aus Blueprint erstellen*

1. Klicken Sie auf Weiter.

1. Geben Sie auf der Eigenschaftenseite die Metadaten für die Seite ein. Klicken Sie auf Erstellen.

   ![](assets/blueprint-properties.png)
   *Schulungssite-Blueprint auswählen*

1. Klicken Sie auf den Hyperlink Start , um zur Startseite der von Ihnen erstellten Website zu navigieren. Auf dieser Seite können Sie die Widgets und Katalogkomponenten anpassen.

## Die Website coden.

Zusätzlich zu den integrierten Vorlagen und der Möglichkeit, mit den WYSIWYG-Komponenten eine Website von Grund auf neu zu erstellen, können Sie auch Code schreiben und die Website erstellen.

Der Code befindet sich im [GitHub-Repository der Referenzsite](https://github.com/adobe/adobe-learning-manager-reference-site) für Sie bereit.

Die Hauptbestandteile der Vorlage sind:

* core: Java-Paket, das alle Kernfunktionen wie OSGi-Dienste, Listener oder Scheduler sowie komponentenbezogenen Java-Code wie Servlets oder Anforderungsfilter enthält.
* ui.apps: enthält die /apps (und /etc)-Teile des Projekts, d. h. JS&amp;CSS-Client-Bibliotheken, Komponenten, Vorlagen.
* ui.content: enthält Beispielinhalte, die die Komponenten aus &quot;ui.apps&quot; verwenden
* ui.frontend: enthält React-Komponenten.

Der gesamte Code ist im Repo enthalten, damit Sie sofort loslegen können.

## Importieren Sie Lern-Manager-Komponenten und fügen Sie sie vorhandenen Webseiten oder Vorlagen hinzu

Durch Installieren AEM Referenzsite-Pakets werden die Learning Manager-Komponenten zu Ihrer AEM Sites-Instanz hinzugefügt. Standardmäßig können Sie diese Komponenten der Lernwebsite für das Webprojekt (Website) hinzufügen, die wir sofort bereitstellen. Diese Komponenten sind auch auf der Website verfügbar, die Sie mit dem Blueprint für die Lernsite erstellen.

Wenn Sie diese neu hinzugefügten Learning Manager-Komponenten jedoch in Ihr vorhandenes Webprojekt oder Ihre Website verwenden möchten, sollten Sie sie wie folgt importieren.

1. Installieren Sie das ALM-Referenzsite-Paket.

1. Öffnen Sie das Webprojekt und navigieren Sie zur HTML-Datei (für die Webseite oder die Webvorlage, der Sie die Lern-Manager-Komponenten hinzufügen möchten).
1. Teilnehmen an einem Meeting

   Öffnen Sie die HTML-Datei und fügen Sie der Seitenkomponente die folgenden Codefragmente hinzu, damit der ausgeführt wird, bevor die auf der Seite vorhandenen Lernkomponenten gerendert werden.

   *`<sly data-sly-use.configModel="com.adobe.learning.core.models.GlobalConfigurationModel"/>`*
   *`<meta name="cp-config" content="${configModel.config}" />`*

   Der vorangehende Code fügt die zugeordnete Konfiguration im Meta-Tag der Seite hinzu, das für das Rendern der Lernkomponenten erforderlich ist. Weitere Informationen finden Sie unter [Adobe Learning Manager-Referenzsitr](https://github.com/adobe/adobe-learning-manager-reference-site/blob/master/ui.apps/src/main/content/jcr_root/apps/learning/components/page/customheaderlibs.html).

1. Stellen Sie sicher, dass Sie die Konfiguration dem Webprojekt zugeordnet haben.
1. Öffnen Sie die AEM Sites-Vorlage, in die Sie die Learning Manager-Komponenten importieren möchten.
1. Navigieren Sie im Vorlagenseiteneditor zum Container Zulässige Komponenten und wählen Sie **Richtlinie**.
1. Navigieren Sie auf der Seite &quot;Richtlinie&quot; zu Eigenschaften > Zulässige Komponenten und wählen Sie die folgenden Komponenten: &quot;Lernen - Inhalt&quot;, &quot;Lernen - Formular&quot; und &quot;Lernen - Struktur&quot;

Mit dem folgenden Verfahren kann die Vorlage die Clientbibliotheksabhängigkeiten der importierten Learning Manager-Komponenten erfüllen.

Die Webseiten, die diese Komponenten enthalten, sollten diese Bibliotheken laden, damit die Komponenten erfolgreich gerendert und verwendet werden können.

1. Klicken Sie im Vorlagenseiteneditor auf Seiteninformationen und dann auf Seitenrichtlinie.
1. Navigieren Sie auf der Seite Richtlinie zu Eigenschaften > Client-Bibliotheken und fügen Sie diese zur Vorlagenseite hinzu:

   1. learning.site
   1. learning.ui
   1. learning.commerce

Nachdem Sie diese Vorlage gespeichert haben, können Sie die Learning Manager-Komponenten allen Webseiten hinzufügen, die von dieser Vorlage abgeleitet wurden.
