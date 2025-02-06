---
description: Hier erfahren Sie, wie Sie die Benutzeroberflächensprache mit SAML konfigurieren.
jcr-language: en_us
title: Benutzeroberflächensprache über SAML einrichten
contentowner: chandrum
source-git-commit: 448119eda15c8d7dfe10150c09fbbe7c530f35e8
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 0%

---


# Benutzeroberflächensprache über SAML einrichten

Adobe Learning Manager (ALM) akzeptiert jetzt ein SAML-Attribut für die Sprache. Dieses Attribut wird dann der Benutzeroberfläche und den Spracheinstellungen des Inhalts zugeordnet, um eine reibungslose Interaktion mit dem LMS in der gewünschten Sprache zu gewährleisten. Die Konfiguration dieser Spracheinstellungen wird über die Plattform Identity and Access Management (IAM) verwaltet und verwendet SAML für Single-Sign-on (SSO). Dies unterstützt sowohl vom Service Provider (SP) initiierte als auch vom Identity Provider (IdP) initiierte Anmeldungen, sodass Benutzer die Oberfläche und den Inhalt in der gewünschten Sprache sehen können. Der Arbeitsablauf ist wie folgt:

1. Anwendung in Okta erstellen
2. Hinzufügen eines Benutzers in Okta
3. Konfigurieren von SSO in ALM

## Anwendung in Okta erstellen

Führen Sie die folgenden Schritte aus, um eine Anwendung in Okta zu erstellen:

1. Erstellen Sie in Okta ein Entwicklerkonto mit Ihrer Unternehmens-E-Mail-Adresse und melden Sie sich bei Ihrem Konto an.
2. Wählen Sie **[!UICONTROL Anwendungen]** > **[!UICONTROL Programmintegration erstellen]**.
3. Wählen Sie **[!UICONTROL SAML 2.0]** und anschließend **[!UICONTROL Weiter]** aus.
4. Geben Sie einen Namen für die Anwendung ein und wählen Sie Weiter.
5. Konfigurieren Sie die folgenden Felder:

   * **[!UICONTROL URL für einmaliges Anmelden]**: Geben Sie die spezifische Domänen-URL ein, zu der Sie die Anwendung verknüpfen möchten (z. B. [https://learningmanagerstage.adobe.com/saml/SSO](https://learningmanagerstage.adobe.com/saml/SSO)). Ändern Sie gegebenenfalls die URL der Umgebung.
   * **[!UICONTROL Zielgruppen-URI (SP-Entitäts-ID)]**: Verwenden Sie dieselbe Umgebungs-URL wie oben.
   * **[!UICONTROL Name ID Format]**: Wählen Sie die E-Mail-Adresse aus.
   * **[!UICONTROL Anwendungsbenutzername]**: Wählen Sie Okta-Benutzername aus.

6. Fügen Sie unter &quot;Attributanweisungen&quot; Folgendes (bzw. ggf. zusätzliche Felder) hinzu:
   * **Name**: Gebietsschema
   * **Namensformat**: Nicht definiert
   * **Wert**: user.locale

7. Wählen Sie Weiter und dann Fertig stellen aus.
8. Scrollen Sie anschließend nach unten zu SAML-Signaturzertifikate:

   * Suchen Sie die Zeile mit dem Status &quot;**[!UICONTROL Aktiv]**&quot;.
   * Wählen Sie **[!UICONTROL Aktionen]** > **[!UICONTROL IdP-Metadaten anzeigen]**.
   * Dadurch wird eine XML-Datei auf einer neuen Registerkarte geöffnet. Kopieren Sie den XML-Code und speichern Sie ihn lokal als .xml-Datei.

## Hinzufügen eines Benutzers in Okta

Um einen Benutzer in Okta zu erstellen, führen Sie die folgenden Schritte aus:

1. Wählen Sie **[!UICONTROL Verzeichnis]** > **[!UICONTROL Personen]** und wählen Sie dann **[!UICONTROL Person hinzufügen]**.
2. Geben Sie die erforderlichen Details für den Benutzer ein und wählen Sie **[!UICONTROL Speichern]**.
3. Suchen Sie nach dem Benutzernamen des neuen Benutzers und wählen Sie ihn aus.
4. Wählen Sie **[!UICONTROL Anwendung zuweisen]**.
5. Wählen Sie die Anwendung aus, die Sie zuvor erstellt haben, und wählen Sie dann **[!UICONTROL Speichern]**.
6. Navigieren Sie zum Benutzerprofil und wählen Sie **[!UICONTROL Bearbeiten]**.
7. Geben Sie im Feld &quot;Gebietsschema&quot; den erforderlichen Wert ein (z. B. fr_FR, en_US) und wählen Sie **[!UICONTROL Speichern]**.

## Konfigurieren von SSO in ALM

Zum Konfigurieren von SSO in ALM führen Sie die folgenden Schritte aus:

1. Melden Sie sich als Administrator an.
2. Wählen Sie **[!UICONTROL Einstellungen]** > **[!UICONTROL Anmeldemethoden]**.
3. Wechseln Sie zur Registerkarte **[!UICONTROL Konfiguration für einmaliges Anmelden (SSO)]**.
4. Wählen Sie **[!UICONTROL Neue SSO-Konfiguration hinzufügen]**.

   ![](assets/sso-add.PNG)
   _SSO in ALM hinzufügen_

5. Konfigurieren Sie die folgenden Details und wählen Sie Speichern.
   * Geben Sie einen Namen für die Konfiguration ein.
   * Wählen Sie **[!UICONTROL IDP Initiated]** aus der Dropdown-Liste **[!UICONTROL Einstellungen für einmaliges Anmelden (SSO)]** aus.
   * Für **[!UICONTROL IDP-initiierte Authentifizierungs-URL]**:

      * Öffnen Sie die Metadaten-XML-Datei, die Sie zuvor heruntergeladen haben.
      * Suchen Sie nach dem Positionswert und kopieren Sie ihn.
      * Fügen Sie diesen Wert in das Feld IdP-Initiated Authentication URL ein.

   * Für **[!UICONTROL Metadaten-XML-Datei]**: Laden Sie die zuvor heruntergeladene XML-Datei hoch.

6. Wechseln Sie zurück zur Registerkarte **[!UICONTROL Setup]**.
7. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Konfiguration für einmaliges Anmelden]**.
8. Wählen Sie im Dropdownmenü **[!UICONTROL SSO-Setup]** den zuvor erstellten Konfigurationsnamen aus.
9. Wählen Sie **[!UICONTROL Speichern]**.

## Benutzeranmeldung und Spracheinstellung

Wenn sich ein Benutzer mit den Anmeldeinformationen über SSO anmeldet, wird das vom IdP übergebene Sprachattribut der Benutzeroberfläche und den Sprachfeldern für Inhalte in ALM zugeordnet. Die Spracheinstellungen werden sofort auf der Benutzeroberfläche und im Inhalt ohne Zwischenspeicherzeit übernommen.

Benutzer können ihre Spracheinstellungen im Abschnitt &quot;Benutzerprofil&quot; manuell aktualisieren. Diese manuell aktualisierten Spracheinstellungen bleiben in Kraft und werden von den IDP-Einstellungen bei zukünftigen Anmeldungen nicht überschrieben.

Wenn ein Benutzer aus ALM gelöscht wird, werden die Spracheinstellungen in der Datenbank beibehalten. Wenn derselbe Benutzer erneut hinzugefügt wird, wird die zuvor festgelegte Sprache wiederhergestellt.

Administratoren können die Berichte Benutzeraktivität, Lernzusammenfassung und Kompatibilitäts-Dashboard auf sprachspezifische Details überprüfen.


