---
description: Arrête une tâche en cours.
seo-description: Arrête une tâche en cours.
seo-title: stopJob
solution: Experience Manager
title: stopJob
topic: Dynamic Media Image Production System API
uuid: 698c1652-5afa-4a2c-819a-1ba6ffc6aacf
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 20%

---


# stopJob{#stopjob}

Arrête une tâche en cours.

Syntaxe

## Types d’utilisateur autorisés {#section-b222f561143747f6ad089aadc0b274d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-2b64f074e37c4c38849994f3bc65342a}

**Entrée (stopJobParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de société. |
| `*`jobHandle`*` | `xsd:string` | Oui | Traitez la tâche que vous souhaitez arrêter. |

**Output (stopJobReturn0)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-f7e07fa09ae24dc89685533f20ab3b81}

**Request**

```java
<stopJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</stopJobParam>
```

**Réponse**

Aucune
