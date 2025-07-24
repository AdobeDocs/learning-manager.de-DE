---
jcr-language: en_us
title: Unterstützung für benutzerdefinierte Domäne
description: Benutzerdefinierte Domänen werden in einer Azure-Instanz von Learning Manager nicht unterstützt.
contentowner: saghosh
exl-id: 162ce268-48e3-4c7e-acb1-5181cebbb18d
source-git-commit: 411c171c314a3aa9ad9cc10d46c2f0d447e2c0a3
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 65%

---

# Unterstützung für benutzerdefinierte Domäne

Benutzerdefinierte Domänen werden in einer Azure-Instanz von Learning Manager nicht unterstützt.

## Überblick {#overview}

Die Unterstützung benutzerdefinierter Domänen ermöglicht den Kunden, die vollständige Kontrolle über den Domänennamen zu erhalten, den sie für ihr Konto in Learning Manager verwenden können. Ein Kunde muss die benutzerdefinierte Domäne separat erwerben und mit dem Adobe-Team zusammenarbeiten, um sie als Anmelde-URL für seine Lernplattform einzurichten.

Dadurch kann der Kunde die Anmelde- und Zugriffsbenutzeroberfläche mit einem White Label versehen, sodass Adobe oder Adobe Learning Manager für Benutzende unsichtbar bleibt.

Sie möchten beispielsweise Ihre Domäne so anpassen, dass die Benutzererfahrung der in der Adobe-Domäne entspricht. Wenn ABC Inc ihre Kunden schulen möchte, sollen sie auf einer Domäne namens `abc.com/mylearning` statt `learningmanager.adobe.com/abc-inc/mylearning` landen.

>[!NOTE]
>
>Als Voraussetzung müssen Sie die Domäne registrieren, und dann führt Adobe Sie durch das Anpassen der URL.


Die Funktion für benutzerdefinierte Domänen ist gegen einen Aufpreis verfügbar. Wenden Sie sich an Ihren Customer Success Manager, um weitere Informationen zu erhalten.

* Für die Teilnehmerrolle beginnt die Domäne mit `https://cdn.<customer_custom_domain>/`. Beispiel: `https://cdn.elearningstage1.cpdomaintest.in/`
* Für alle anderen Rollen beginnt die Domäne mit `https://<customer_custom_domain>/`. Beispiel: `https://elearningstage1.cpdomaintest.in/`
* Die tatsächliche Anmelde-URL ist `https://<customer_custom_domain>/acapindex` oder `https://<customer_custom_domain>/login`. Ersetzen Sie `<customer_custom_domain>` durch die eigentliche Domäne Ihrer Organisation.

`<customer_custom_domain>` ist der anpassbare Teil.

## Einrichten einer benutzerdefinierten Domäne für ein Konto {#howtosetupacustomdomainonanaccount}

Voraussetzung dafür ist, dass ein Kunde einen Domänennamen besitzt und die Domäne von einem Anbieter kauft.

Nehmen wir an, ein Kunde besitzt eine fiktive Domäne **acme.com**. Der Kunde wünscht, dass Learning Manager-Inhalte von **learning.acme.com** bereitgestellt werden.

Führen Sie die folgenden Schritte aus, um eine benutzerdefinierte Domäne einzurichten.

1. Der Kunde muss **drei CNAME-Datensätze** in der Domäne hinzufügen:

   * **learning.acme.com:** Von Adobe freigegebener öffentlicher ALB-Endpunkt des Learning Managers
   * **lrs.learning.acme.com:** Öffentlicher ALB-Endpunkt, auf den learning.acme.com verweist
   * **cdn.learning.acme.com:** CDN-Endpunkt von Adobe freigegeben

1. Der Kunde muss SSL-Zertifikate für diese Domänen bereitstellen:

   * learning.acme.com
   * lrs.learning.acme.com
   * cdn.learning.acme.com

1. Adobe lädt diese SSL-Zertifikate in AWS ALB hoch, um Anfragen an die Domänen zu senden.
1. Adobe fügt learning.acme.com in ihr SAN-Zertifikat ein.
1. Adobe generiert die SP-Metadaten für den Kunden, da die Metadaten die benutzerdefinierten Domänen-URLs enthalten.

   * Wenn der Kunde eine Anmeldung mittels sozialer Medien wünscht, muss Adobe die Umleitungs-URL-Muster der sozialen Medien in die Liste der zulässigen URLs aufnehmen.
   * Wenn der Kunde SSO aktiviert hat, muss er mit seinem IDP zusammenarbeiten, um seine Domänen in die Umleitungs-URLs aufzunehmen. Der Kunde muss die IDP-Metadaten-XML-Datei mit Adobe teilen. Adobe muss dann die SSO-Einstellungen des Kundenkontos aktualisieren.

1. Adobe ändert dann die S3 CORS-Regeln, um die Domäne des Kunden einzubeziehen.
