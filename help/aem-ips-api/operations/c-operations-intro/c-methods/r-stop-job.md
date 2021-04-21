---
description: Arrête une tâche en cours.
solution: Experience Manager
title: stopJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 19%

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
