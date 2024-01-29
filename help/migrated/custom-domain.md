---
jcr-language: en_us
title: Unterstützung für benutzerdefinierte Domäne
description: Benutzerdefinierte Domänen werden in einer Azure-Instanz von Learning Manager nicht unterstützt.
contentowner: saghosh
source-git-commit: 8635072782253cbac3f913953797cae7c0bc5ef4
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---



# Unterstützung für benutzerdefinierte Domäne

Benutzerdefinierte Domänen werden in einer Azure-Instanz von Learning Manager nicht unterstützt.

## Übersicht {#overview}

Mit der Unterstützung benutzerdefinierter Domänen erhalten Kunden die vollständige Kontrolle über den Domänennamen, den sie für ihr Konto in Learning Manager verwenden können. Ein Kunde muss die benutzerdefinierte Domäne separat erwerben und mit dem Adobe-Team zusammenarbeiten, um sie als Anmelde-URL für seine Lernplattform einzurichten.

Dadurch kann der Kunde die Anmelde- und Zugriffsbenutzeroberfläche mit einem White Label versehen, sodass keine Adobe oder Adobe Learning Manager vorhanden sind.

Sie möchten beispielsweise Ihre Domäne so anpassen, dass die Benutzererfahrung der in der Adobe-Domäne entspricht. Wenn ABC Inc ihre Kunden schulen möchte, sollen sie auf einer Domäne mit dem Namen `abc.com/mylearning`statt `learningmanager.adobe.com/abc-inc/mylearning`.

>[!NOTE]
>
>Als Voraussetzung müssen Sie die Domäne registrieren, und dann führt Adobe Sie durch das Anpassen der URL.


Die Funktion für benutzerdefinierte Domänen ist gegen einen Aufpreis verfügbar. Wenden Sie sich an Ihren Customer Success Manager, um weitere Informationen zu erhalten.

* Für die Teilnehmerrolle beginnt die Domäne mit `https://cdn.<customer_custom_domain>/` Beispiel: `https://cdn.elearningstage1.cpdomaintest.in/`
* Für alle anderen Rollen beginnt die Domäne mit `https://<customer_custom_domain>/`. Beispiel: `https://elearningstage1.cpdomaintest.in/`

`<customer_custom_domain>` ist der anpassbare Teil.

## Einrichten einer benutzerdefinierten Domäne für ein Konto {#howtosetupacustomdomainonanaccount}

Voraussetzung dafür ist, dass ein Kunde einen Domänennamen besitzt und die Domäne von einem Anbieter kauft.

Nehmen wir an, ein Kunde besitzt eine fiktive Domäne. **acme.com**. Der Kunde wünscht, dass Learning Manager-Inhalte von **learning.acme.com**.

Führen Sie die folgenden Schritte aus, um eine benutzerdefinierte Domäne einzurichten.

1. Der Kunde muss **drei CNAME hinzufügen** Datensätze in der Domäne:

   * **learning.acme.com:** Öffentlicher ALB-Endpunkt des Learning Managers, der von Adobe freigegeben wird
   * **lrs.learning.acme.com:** Öffentlicher ALB-Endpunkt, auf den learning.acme.com verweist
   * **cdn.learning.acme.com:** Von Adobe freigegebener CDN-Endpunkt

1. Der Kunde muss SSL-Zertifikate für diese Domänen bereitstellen:

   * learning.acme.com
   * lrs.learning.acme.com
   * cdn.learning.acme.com

1. Adobe lädt diese SSL-Zertifikate in AWS ALB hoch, um Anfragen an die Domänen zu senden.
1. Adobe fügt learning.acme.com in ihr SAN-Zertifikat ein.
1. Adobe generiert die SP-Metadaten für den Kunden, da die Metadaten die benutzerdefinierten Domänen-URLs enthalten.

   * Wenn der Kunde eine Anmeldung per Social Media wünscht, muss der Adobe die Umleitungs-URL-Muster der Social-Media-Websites in die Liste der zulässigen URLs aufnehmen.
   * Wenn der Kunde SSO aktiviert hat, muss er mit seinem IDP zusammenarbeiten, um seine Domänen in die Umleitungs-URLs aufzunehmen. Der Kunde muss die IDP-Metadaten-XML-Datei für Adobe freigeben. Adobe muss dann die SSO-Einstellungen des Kundenkontos aktualisieren.

1. Adobe ändert dann die S3 CORS-Regeln, um die Domäne des Kunden einzubeziehen.
