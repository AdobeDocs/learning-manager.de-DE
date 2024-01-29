---
jcr-language: en_us
title: Soziale Anmeldung in Learning Manager
description: Soziale Anmeldung in Learning Manager
contentowner: saghosh
preview: true
source-git-commit: ccdb222228f76fdae63ebb0a808824ad6ac1db7f
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---



# Soziale Anmeldung in Learning Manager

Sie können Ihre Facebook-, LinkedIn- oder Twitter-Anmeldeinformationen verwenden, um sich beim Lernmanager anzumelden.

## Social Login einrichten {#setupsociallogin}

1. Wenden Sie sich an Ihren Customer Success Manager, wenn Sie möchten, dass er das Konto einrichtet.

   Andernfalls führen Sie die folgenden Schritte aus.

1. Suchen Sie nach dem Konto, für das Sie die Anmeldung per Social Media einrichten möchten.
1. Ändern Sie die Anmeldung in SSO.
1. Klicken Sie auf Erweitert. Geben Sie die folgende JSON an.

   ```
   \{"linkedIn":true,"microsoft":true,"twitter":true,"facebook":true,"editingAllowed":true
   ```

   Wenn es sich um eine falsche JSON handelt, wird eine Ausnahme angezeigt.

   Diese Social-Login-Funktion wird nur für INTERNE Benutzer verwendet.

