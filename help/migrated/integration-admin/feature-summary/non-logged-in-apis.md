---
description: Erfahre mehr über die nicht angemeldeten APIs zur Entwicklung der Headless-Benutzeroberfläche.
jcr-language: en_us
title: Nicht angemeldete APIs
source-git-commit: 21e2a4a5e73fcbddb64e0afec0a896b315e38688
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 0%

---

# Nicht angemeldete APIs

Erfahrt in diesem Artikel mehr über die Adobe Learning Manager-APIs, die Daten für headless- oder nicht angemeldete Erlebnisse bereitstellen.
Public Search API

## Public Search API

### Daten mit Public ES filtern

Mit dem Public Search API erhaltet ihr Filterdaten, die mit den grundlegenden Such-API zum Filtern der Kurse verwendet werden können. Dieses API bietet alle Filter, die bei der Suche API verwendet werden können.

**Curl-Beispiel**

Verwende die GET-Methode, um die folgende Anfrage zu stellen: Ersetze &lt;Base_URL> deine basis URL im unten stehenden Befehl &quot;Locken&quot;. &lt;/Base_URL> Die &lt;Base_URL> Seite &quot;Training Data Access Connector&quot; findest du auf der Seite &quot;Training Data Access Connector&quot;.&lt;/Base_URL>

```
curl --location '<Base_URL>/filterableData'
```

**Beispielantwort**

```
{
    "terms": {
        "loSkillLevels": [
            "1"
        ],
        "catalogNames": [
            "Default Catalog"
        ],
"catalogLabelIds": [
            "0000_1111"
        ],
        "loType": [
            "course"
        ],
        "availability": [
            "waitlistAvailable",
            "seatAvailable"
        ],
        "loSkillNames": [
            "General"
        ],
        "tags": [
            "course_tag"
        ],
        "authors": [
            "author_1"        
]
    },
    "range": {
        "duration": [
            "0"
        ],
        "dateCreated": [
            "2024-06-13T04:32:17.000Z"
        ],
        "price": [
            "0.0"
        ],
        "sessionEndTime": [
            "2024-06-18T20:30:00.000Z"
        ],
        "averageRating": [
            "0.0"
        ],
        "sessionStartTime": [
            "2024-06-18T19:30:00.000Z"
        ],
        "publishDate": [
            "2024-06-13T04:32:51.000Z"
        ],
        "ratingsCount": [
            "0"
        ]
    },
    "term": {}
}
```

**Filteroptionen**

| Optionen | Beschreibung |
| --- | --- |
| `loSkillLevels` | er kenntnisse, die für die Anmeldung zum Kurs erforderlich sind. |
| `catalogNames` | Liste der verfügbaren Katalognamen |
| `loType` | Arten von verfügbaren Lernobjekten. |
| `availability` | Verfügbarkeit von Sitzen und Verfügbarkeit von Wartelisten. |
| `loSkillNames` | Die Kompetenznamen, die den Lernobjekten hinzugefügt wurden. |
| `tags` | Die Tags, die den Lernobjekten zugeordnet sind. |
| `authors` | Name der Lernobjekte des Autors |
| `duration` | Die Dauer der Lernobjekte. |
| `dateCreated` | Das Datum, an dem das Lernobjekt erstellt wurde. |
| `sessionEndTime` | Zum Ende der Session. |
| `averageRating` | Die durchschnittliche Sternbewertung der Lernobjekte. |
| `sessionStartTime` | Beginn der Session. |
| `publishDate` | Das Datum der Veröffentlichung des Lernobjekts. |
| `ratingsCount` | Die Anzahl der Bewertungen zählt für das Lernobjekt. |

### API durchsuchen

Mit dem öffentlichen Search API könnt ihr anhand der bereitgestellten Daten grundlegende Suchdaten abrufen.

**Sample Curl**

Verwende die POST-Methode, um die folgende Anfrage zu stellen: Ersetze &lt;Base_URL> deine basis URL im unten stehenden Befehl &quot;Locken&quot;. &lt;/Base_URL> Die &lt;Base_URL> Seite &quot;Training Data Access Connector&quot; findest du auf der Seite &quot;Training Data Access Connector&quot;.&lt;/Base_URL>

```
curl --location '<Base_URL>/search?size=1000' \
--header 'content-type: application/json' 

--data '{
   "query": "",
   
    "sort": {
        "name": "publishDate",
        "order": "desc"
    },
    "lang": [
        "en-US"
    ],
    "filters": {
        "terms": {
            "loType": [
                "course",
                "learningProgram",
                "certification"
            ],
            "availability": [
                "seatAvailable",
                "waitlistAvailable"
            ]
        },
        "term": {
            "enrollmentDeadlinePassed": "true"
        },
        "range": {
                "dateCreated": [
                    {
                        "gte": "2024-05-02T02:48:51.000Z"
                    }
                ],
            "sessionStartTime": [
                {
                   "gte": "2024-06-18T19:30:00.000Z"
                }
            ],
            "sessionEndTime": [
                {
                   "lte": "2024-06-20T09:30:00.000Z"     
                }
            ]
        }
    }
}'
```

**Beispielantwort des API-Aufrufs**

```
{
    "results": [
        {
            "loId": "course:11332313",
            "loType": "course",
            "tags": [
                "course_tag"
            ],
            "authors": [
                "author1",
                "author2"
            ],
            "status": "Published",
            "duration": 0,
            "publishDate": "2024-06-13T04:32:51.000Z",
            "dateCreated": "2024-06-13T04:32:17.000Z",
            "name": "vc coursse to check ",
            "averageRating": 0.0,
            "ratingsCount": 0,
            "loSkillNames": [
                "General"
            ],
            "loSkillLevels": [
                "1"
            ],
            "loInstances": [
                {
                    "id": "14346696",
                    "name": "Default Instance",
                    "status": "Active",
                    "price": 0.0
                }
            ],
            "catalogInfo": [
                {
                    "id": "37779",
                    "name": "Default Catalog"
                }
            ]
        }
    ],
    "request": {
        "query": "",
        "filters": {
            "terms": {
                "loType": [
                    "course",
                    "learningProgram",
                    "certification"
                ],
                "loSkillNames": [
                    "General"
                ],
                "deliveryType": [],
                "availability": [
                    "seatAvailable",
                    "waitlistAvailable"
                ]
            },
            "term": {
                "enrollmentDeadlinePassed": "true"
            },
            "range": {
                "dateCreated": [
                    {
                        "gte": "2024-05-02T02:48:51.000Z"
                    }
                ],
                "sessionStartTime": [
                    {
                        "gte": "2024-06-18T19:30:00.000Z"
                    }
                ],
                "sessionEndTime": [
                    {
                        "lte": "2024-06-20T09:30:00.000Z"
                    }
                ]
            }
        },
        "sort": {
            "name": "publishDate",
            "order": "desc"
        },
        "lang": [
            "en-US"
        ]
    },
    "self": "<Base_URL>/search?page=0&size=1000",
    "count": 1
}
```

**Optionen zum Sortieren im Such-API**

Du kannst die folgenden Sortieroptionen auswählen, die auf die Ergebnisse angewendet werden sollen.

| Optionen | Beschreibung |
| --- | --- |
| `duration` | Die Dauer des Lernobjekts. |
| `publishDate` | Das Datum der Veröffentlichung des Lernobjekts. |
| `dateCreated` | Das Datum, an dem das Lernobjekt erstellt wurde. |
| `name_en` | Der Name des Lernobjekts. |
| `averageRating` | Durchschnittliche Sternbewertung der Teilnehmer. |
| `ratingsCount` | Die Anzahl der Bewertungen zählt für das Lernobjekt. |
| `relevance(default)` | Die relevanten Daten basieren auf den Suchbegriffen. |

### Lernobjektdaten mit öffentlichen Suchfunktionen API

Mit dem öffentlichen ES-Lernobjekt-API kannst du die Liste der Arten und IDs von Lernobjekten auf der Headless-Benutzeroberfläche abrufen.

**Curl-Beispiel**

Verwende die GET-Methode, um die folgende Anfrage zu stellen: Ersetze &lt;Base_URL> deine basis URL im unten stehenden Befehl &quot;Locken&quot;. &lt;/Base_URL> Die &lt;Base_URL> Seite &quot;Training Data Access Connector&quot; findest du auf der Seite &quot;Training Data Access Connector&quot;.&lt;/Base_URL>

```
curl --location '<Base_URL>/learningObjectIds'
```

**Beispielantwort für den API-Aufruf**

```
{
    "loIds": [
        "course:1132800",
"certification:126009",
"learningProgram:104433"
    ]
}
```

## Kursübersicht API

Die Kursübersicht API ermöglicht es Ihnen, detaillierte Informationen zu einem bestimmten Kurs abzurufen.

**Curl-Beispiel**

Verwende die GET-Methode, um die folgende Anfrage zu stellen: Ersetze &lt;Base_URL> deine basis URL im unten stehenden Befehl &quot;Locken&quot;. &lt;/Base_URL> Die &lt;Base_URL> Seite &quot;Training Data Access Connector&quot; findest du auf der Seite &quot;Training Data Access Connector&quot;. &lt;/Base_URL> &lt;Course_ID> Ersetze sie durch die kursspezifische ID.&lt;/Course_ID>

```
curl --location '<Base_URL>/loSummary?loId=course%3A<Course_ID>'
```

**Beispielantwort des API-Aufrufs**

```
{
    "results": [
        {
            "instanceId": "14336686",
            "courseId": "11312313",
            "accountId": "44355",
            "seatConsumed": 1,
            "seatLimit": 1,
            "waitlistLimit":1,
            "waitlistCount": 1,
            "seatAvailable": false,
            "waitlistAvailable": false
        }
    ],
    "count": 1
}
```

>[!NOTE]
>
>Wenn ein Kurs mehrere Instanzen hat, erhaltet ihr Details zu allen Instanzen.

## CDN JSON-API für Kursdetails

Die CDN JSON-API ermöglicht es Ihnen, die vollständigen Kursinformationen zu einem bestimmten Kurs abzurufen.

**Curl-Probe für Kurs**

Verwende die GET-Methode, um die folgende Anfrage zu stellen: Ersetze &lt;CDN_path> deine basis URL im unten stehenden Befehl &quot;Locken&quot;. &lt;/CDN_path> Die &lt;CDN_path> Seite &quot;Training Data Access Connector&quot; findest du auf der Seite &quot;Training Data Access Connector&quot;. &lt;/CDN_path> &lt;Course_ID> Ersetze sie durch die kursspezifische ID.&lt;/Course_ID>

```
curl --location '<CDN_path_URL>/course/<Course_ID>.json'
```

**Muster-Locken für den Lernpfad und die Zertifizierung**

```
curl --location '<CDN_path_URL>/learningProgram/<LearningProgram_ID>.json'
```

```
curl --location '<CDN_path_URL>/ certification /<Certification_ID>.json'
```

**Beispielantwort des API-Aufrufs**

```
{
    "data": {
        "id": "course:11342313",
        "type": "learningObject",
        "attributes": {
            "authorNames": [
                "author1",
                "author2"
            ],
            "dateCreated": "2024-06-13T04:32:17.000Z",
            "datePublished": "2024-06-13T04:32:51.000Z",
            "dateUpdated": "2024-06-13T04:32:51.000Z",
            "duration": 0,
            "effectiveModifiedDate": "2024-06-13T04:32:51.000Z",
            "effectivenessIndex": 0,
            "enrollmentType": "Self Enroll",
            "hasOptionalLoResources": false,
            "hasPreview": false,
            "isExternal": false,
            "isMqaEnabled": false,
            "isPrerequisiteEnforced": false,
            "isSubLoOrderEnforced": false,
            "loResourceCompletionCount": 1,
            "loType": "course",
            "moduleResetEnabled": false,
            "state": "Published",
            "tags": [
                "course_tag"
            ],
            "unenrollmentAllowed": true,
            "localizedMetadata": [
                {
                    "description": "",
                    "locale": "en-US",
                    "name": "vc coursse to check "
                }
            ],
            "rating": {
                "averageRating": 0,
                "ratingsCount": 0
            }
        },
        "relationships": {
            "authors": {
                "data": [
                    {
                        "id": "13138897",
                        "type": "user"
                    }
                ]
            },
            "instances": {
                "data": [
                    {
                        "id": "course:11332313_14336696",
                        "type": "learningObjectInstance"
                    }
                ]
            },
            "skills": {
                "data": [
                    {
                        "id": "course:11332313_237719",
                        "type": "learningObjectSkill"
                    }
                ]
            }
        }
    },
    "included": [
        {
            "id": "237719",
            "type": "skill",
            "attributes": {
                "name": "General",
                "state": "Active"
            },
            "relationships": {
                "levels": {
                    "data": [
                        {
                            "id": "237719_1",
                            "type": "skillLevel"
                        }
                    ]
                }
            }
        },
        {
            "id": "course:11312313",
            "type": "learningObject",
            "attributes": {
                "authorNames": [
                    "m 41",
                    "rae"
                ],
                "dateCreated": "2024-06-13T04:32:17.000Z",
                "datePublished": "2024-06-13T04:32:51.000Z",
                "dateUpdated": "2024-06-13T04:32:51.000Z",
                "duration": 0,
                "effectiveModifiedDate": "2024-06-13T04:32:51.000Z",
                "effectivenessIndex": 0,
                "enrollmentType": "Self Enroll",
                "hasOptionalLoResources": false,
                "hasPreview": false,
                "isExternal": false,
                "isMqaEnabled": false,
                "isPrerequisiteEnforced": false,
                "isSubLoOrderEnforced": false,
                "loResourceCompletionCount": 1,
                "loType": "course",
                "moduleResetEnabled": false,
                "state": "Published",
                "tags": [
                    "course_tag"
                ],
                "unenrollmentAllowed": true,
                "localizedMetadata": [
                    {
                        "description": "",
                        "locale": "en-US",
                        "name": "course name "
                    }
                ],
                "rating": {
                    "averageRating": 0,
                    "ratingsCount": 0
                }
            },
            "relationships": {
                "authors": {
                    "data": [
                        {
                            "id": "13128897",
                            "type": "user"
                        }
                    ]
                },
                "instances": {
                    "data": [
                        {
                            "id": "course:11312313_14336696",
                            "type": "learningObjectInstance"
                        }
                    ]
                },
                "skills": {
                    "data": [
                        {
                            "id": "course:11312313_237719",
                            "type": "learningObjectSkill"
                        }
                    ]
                }
            }
        },
        {
            "id": "course:11312313_14336696_12034506_0",
            "type": "learningObjectResource",
            "attributes": {
                "externalReporting": false,
                "isExpiredSubmission": false,
                "loResourceType": "Content",
                "multipleAttemptEnabled": false,
                "previewEnabled": false,
                "resourceType": "Virtual Classroom",
                "submissionEnabled": false,
                "localizedMetadata": [
                    {
                        "description": "",
                        "locale": "en-US",
                        "name": "vc session"
                    }
                ]
            },
            "relationships": {
                "learningObject": {
                    "data": {
                        "id": "course:11312313",
                        "type": "learningObject"
                    }
                },
                "resources": {
                    "data": [
                        {
                            "id": "course:11312313_14336696_12034506_0_resource",
                            "type": "resource"
                        }
                    ]
                }
            }
        },
        {
            "id": "course:11312313_237719",
            "type": "learningObjectSkill",
            "attributes": {
                "credits": 1,
                "learningObjectId": "course:11312313"
            },
            "relationships": {
                "skillLevel": {
                    "data": {
                        "id": "237719_1",
                        "type": "skillLevel"
                    }
                }
            }
        },
        {
            "id": "13128897",
            "type": "user",
            "attributes": {
                "avatarUrl": "https://abccontents.adobe.com/public/images/default_user_avatar.svg",
                "binUserId": "1f8c01aa-7f58-42e9-bc40-11537eb6498d",
                "email": "manjusha+41re@adobetest.com",
                "enrollOnClick": false,
                "gamificationEnabled": true,
                "lastLoginDate": "2024-06-13T04:23:45.000Z",
                "name": "m 41",
                "pointsEarned": 0,
                "pointsRedeemed": 0,
                "preferredResolution": "AUTO",
                "profile": "admin",
                "roles": [
                    "Learner",
                    "Admin",
                    "Author",
                    "Instructor",
                    "Integration Admin"
                ],
                "state": "ACTIVE",
                "userType": "Internal"
            },
            "relationships": {
                "account": {
                    "data": {
                        "id": "44355",
                        "type": "account"
                    }
                }
            }
        },
        {
            "id": "course:11312313_14336696_12034506_0_resource",
            "type": "resource",
            "attributes": {
                "avatarUrls": [
                    "https://abccontents.adobe.com/public/images/default_user_avatar.svg"
                ],
                "completionDeadline": "2024-06-18T20:30:00.000Z",
                "contentType": "Virtual Classroom",
                "dateStart": "2024-06-18T19:30:00.000Z",
                "desiredDuration": 3600,
                "hasQuiz": false,
                "hasToc": false,
                "instructorNames": [
                    "instructor1"
                ],
                "isDefault": true,
                "locale": "en-US",
                "location": "http://google.com",
                "name": "vc session",
                "onlyQuiz": false,
                "reportingType": "NONE"
            }
        },
        {
            "id": "course:11312313_14336696",
            "type": "learningObjectInstance",
            "attributes": {
                "dateCreated": "2024-06-13T04:32:18.000Z",
                "isDefault": true,
                "isFlexible": false,
                "state": "Active",
                "localizedMetadata": [
                    {
                        "locale": "en-US",
                        "name": "Default Instance"
                    }
                ],
                "seatConsumed": 0,
                "waitlistCount": 0
            },
            "relationships": {
                "learningObject": {
                    "data": {
                        "id": "course:11312313",
                        "type": "learningObject"
                    }
                },
                "loResources": {
                    "data": [
                        {
                            "id": "course:11312313_14336696_12034506_0",
                            "type": "learningObjectResource"
                        }
                    ]
                }
            }
        },
        {
            "id": "237719_1",
            "type": "skillLevel",
            "attributes": {
                "level": "1",
                "maxCredits": 1,
                "name": "Level 1"
            },
            "relationships": {
                "skill": {
                    "data": {
                        "id": "237719",
                        "type": "skill"
                    }
                }
            }
        }
    ]
}
```
