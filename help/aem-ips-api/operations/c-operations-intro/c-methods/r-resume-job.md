---
description: Redémarre une tâche suspendue.
solution: Experience Manager
title: resumeJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 16%

---


# resumeJob{#resumejob}

Redémarre une tâche suspendue.

Syntaxe

## Types d’utilisateur autorisés {#section-eab49f4b6d1041179000326a10fee889}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-6b2f8aa65d4d4ae1af0c9cee468b0a51}

**Entrée (resumeJobParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée vers la société avec la tâche que vous souhaitez redémarrer. |
| `*`jobHandle`*` | `xsd:string` | Oui | Poignée de la tâche en pause. |

**Sortie (resumeJobReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-d0524e031f1f43d89430eade19526162}

Cet exemple de code redémarre une tâche suspendue.

**Request**

```java
<resumeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</resumeJobParam>
```

**Réponse**

Aucune
