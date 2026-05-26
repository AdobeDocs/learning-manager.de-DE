---
description: API-Änderungen in ALM
jcr-language: en_us
title: API-Änderungen in der Patch-Version Mai 2026
source-git-commit: 24f54599749bce60916a57634144b0ca7f6a6d10
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# API-Änderungen in der Patch-Version Mai 2026

## API-Erweiterung für GET/learningObjects

Die GET/learningObjects-API enthält jetzt ein neues startDate-Attribut in der learningObjectInstance-Ressource, wenn die Instanzbeziehung einbezogen wird.

**Endpunkt**
GET /learningObjects/{id}?include=instances

**Änderung**
Ein neues Feld, startDate, wurde hinzugefügt unter:
included[].attributes.startDate

**Beschreibung**
startDate stellt das geplante Startdatum und die geplante Startzeit einer Lernobjektinstanz dar.

**Beispiel**
https://learningmanagerstage1.adobe.com/primeapi/v2/learningObjects/course:13209797?include=instances
Beispielantwort (abgeschnitten)

```
{
  "id": "course:13209797_16226533",
  "type": "learningObjectInstance",
  "attributes": {
    "dateCreated": "2026-05-20T04:35:46.000Z",
    "isAET": false,
    "isDefault": true,
    "isFlexible": false,
    "startDate": "2026-10-06T18:29:59.000Z",
    "state": "Active",
    "timeZoneCode": "IST"
  }
}
```

**Hinweise**

* Das Feld wird nur für die entsprechenden Lernobjektinstanzen zurückgegeben.
* Der Wert wird im Datum-Zeit-Format nach ISO 8601 UTC zurückgegeben.
* Bestehende Integrationen bleiben abwärtskompatibel.
