---
description: Adobe Learning Manager unterstützt mehrere Anmeldemethoden über mehrere SSO-Konfigurationen für interne und externe Benutzer.
title: Mehrere SSO-Anmeldungen
contentowner: saghosh
source-git-commit: d59e748472c77527c22b286aea5412f776f6441b
workflow-type: tm+mt
source-wordcount: '782'
ht-degree: 0%

---


# Mehrere SSO-Anmeldungen {#multiple-sso-logins}

Ein Administrator kann mehrere Anmeldemethoden für interne und externe Benutzer konfigurieren. Der Adobe Learning Manager unterstützt mehrere SSO-Anmeldungen, mit denen Administratoren die Anmeldemethode je nach ihren Anforderungen und Anwendungsfällen konfigurieren können.

Ziel ist es, Administratoren zu ermöglichen, unterschiedliche SSO für verschiedene Benutzergruppen basierend auf ihrem Speicherort, ihrer Organisation usw. zu konfigurieren.

Einem Konto können bis zu 20 SSO-Konfigurationen hinzugefügt werden. Diese können verwendet werden, um SSO sowohl für interne als auch für externe Benutzer einzurichten.

>[!NOTE]
>
>Beim Aktivieren von Multi-SSO können Sie Werte oder Benutzergruppen im Selbstregistrierungsprofil auswählen. Wenn Sie einen Wert auswählen, wird eine Benutzergruppe mit null Benutzern erstellt. Eine solche Benutzergruppe hat keinen Benutzer. Wenn die nächste CSV-Datei importiert wird, wird diese Benutzergruppe entfernt.

## Mehrere SSO aktivieren

Um mehrere SSO zu aktivieren, wählen Sie **Einstellungen** > **Anmeldemethoden**.

Aktivieren Sie auf der Einrichtungsseite das Kontrollkästchen &quot;Mehrere Single Sign-On (SSO) aktivieren&quot; für interne oder externe Benutzer.

Wenn Multi-SSO aktiviert ist, wird die für &quot;Standardanmeldemethode&quot; ausgewählte Anmeldungsmethode zum Standardanmeldetyp für Benutzergruppen/Profile, die nicht mit einer SSO-Konfiguration verknüpft sind. Die Standardanmeldung kann Adobe ID oder SSO oder ALM ID (externe Benutzer) sein.

Zum Konfigurieren eines SSO führen Sie die folgenden Schritte aus:

1. Klicken Sie auf Single Sign-on (SSO) konfigurieren.
1. Klicken Sie auf Neue SSO-Konfiguration hinzufügen .
1. Fügen Sie im Dialogfeld &quot;SSO-Konfiguration&quot; Folgendes hinzu:

   * Geben Sie den Namen des SSO ein.
   * Wählen Sie den Typ von SSO-IdP initiiert oder SP initiiert aus.

      * Wenn Sie &quot;IdP initiiert&quot; ausgewählt haben, geben Sie die IdP-URL ein. Hierbei handelt es sich um die URL, die der eindeutige Bezeichner für Ihre Anwendung ist. Dabei handelt es sich um Informationen, die von Ihrem IdP-Dienstanbieter bereitgestellt werden. Dies ist die URL, zu der alle Adobe Learning Manager-Benutzer nach der Anmeldung umgeleitet werden.
      * Laden Sie die IDP-Metadaten-XML-Datei von Ihrem IDP-Anbieter hoch. Diese Datei enthält Informationen zum IdP, mit denen der Adobe Learning Manager SAML-Zusicherungen von diesem akzeptieren kann.
      * Wenn Sie SP initiiert ausgewählt haben, geben Sie die Entitäts-ID ein. Die Entitäts-ID ist eine URL, die der Dienstanbieter (SP) bereitstellt.
      * Geben Sie die SP-Anmelde-URL ein. Diese URL wird von den Benutzern verwendet, um sich bei der Anwendung anzumelden.

1. Die SSO-Konfiguration wird der Liste hinzugefügt.

## Einrichten von SSO für interne Benutzer

### Benutzer aus einer CSV-Datei

Führen Sie die folgenden Schritte aus:

1. Importieren Sie die CSV-Datei, die die aktiven Felder und deren Werte enthält.
1. Klicken Sie auf Einstellungen > Anmeldemethoden.
1. Aktivieren Sie das Kontrollkästchen Mehrere Single Sign-on (SSO) für die Anmeldung aktivieren .
1. Ordnen Sie die SSO-Konfigurationen den Werten des aktiven Felds zu.
1. Speichern Sie die Einstellungen. Importieren Sie die CSV-Datei erneut.

### Einzelbenutzer

Führen Sie die folgenden Schritte aus:

1. Klicken Sie auf Einstellungen > Anmeldemethoden.
1. Aktivieren Sie das Kontrollkästchen Mehrere Single Sign-on (SSO) für die Anmeldung aktivieren .
1. Wählen Sie ein aktives Feld für ein SSO aus.
1. Verknüpfen Sie die SSO-Konfigurationen mit den Werten des Felds.
1. Speichern Sie die Einstellungen. Fügen Sie einen einzelnen Benutzer hinzu und weisen Sie einen Wert für das aktive Feld zu.

### Selbstregistrierte Benutzer

Führen Sie die folgenden Schritte aus:

1. Klicken Sie auf Einstellungen > Anmeldemethoden.
1. Aktivieren Sie das Kontrollkästchen Mehrere Single Sign-on (SSO) für die Anmeldung aktivieren .
1. Verknüpfen Sie die SSO-Konfigurationen mit den Werten des Felds.
1. Speichern Sie die Einstellungen. Fügen Sie einen einzelnen Benutzer hinzu und weisen Sie einen Wert für das aktive Feld zu.
1. Selbstregistrierungsprofil hinzufügen
1. Wählen Sie einen Wert für das konfigurierte SSO-Feld aus.

Nach dem Speichern der Profileinstellungen leitet die kopierte URL die Benutzer zu dem SSO weiter, das mit dem für das Profil ausgewählten Wert verknüpft ist.

### Einrichten von SSO für externe Benutzer

Führen Sie die folgenden Schritte aus:

1. Erstellen Sie ein externes Profil.
1. Klicken Sie auf Einstellungen > Anmeldemethoden.
1. Aktivieren Sie das Kontrollkästchen Mehrere Single Sign-on (SSO) für die Anmeldung aktivieren .
1. Verknüpfen Sie die SSO-Konfiguration mit dem erstellten externen Profil.
1. Speichern Sie die Einstellungen.

Nach dem Speichern der Profileinstellungen werden die Benutzer nach dem Speichern über die URL des externen Profils zu dem SSO umgeleitet, das mit dem Profil verknüpft ist.

## Häufig gestellte Fragen

+++ Wer kann mehrere SSOs für Benutzer aktivieren?

Der Administrator und der benutzerdefinierte Administrator können mehrere SSOs aktivieren.
+++

+++Kann ich ein vorhandenes oder ein neues aktives Feld mit einem Wert verwenden?

Ja, Sie können ein vorhandenes oder ein neues aktives Feld mit einem einzelnen Wert verwenden, um mehrere SSOs einzurichten.
+++

+++Wenn eine CSV-Datei deaktivierte Felder enthält, schlägt die Einrichtung mehrerer SSOs fehl?

Nein, dies hat keine Auswirkungen auf die Einrichtung der SSOs. Benutzer werden zu einem bereits konfigurierten SSO umgeleitet.
+++

+++Kann ein Administrator dem aktiven Feld auf der Seite beim Einrichten von Multi-SSO neue Werte hinzufügen?

Ja, ein Administrator kann den aktiven Feldern neue Werte hinzufügen.
+++

+++Kann ich mit SSO verknüpfte Felder deaktivieren oder löschen?

Ja, Sie können mit SSO verknüpfte Felder deaktivieren oder löschen, bis Sie die Verknüpfung der Felder auf der SSO-Einrichtungsseite aufheben.
+++
