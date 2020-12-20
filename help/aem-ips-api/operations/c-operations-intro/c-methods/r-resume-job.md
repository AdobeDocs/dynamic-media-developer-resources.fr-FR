---
description: Redémarre une tâche suspendue.
seo-description: Redémarre une tâche suspendue.
seo-title: resumeJob
solution: Experience Manager
title: resumeJob
topic: Scene7 Image Production System API
uuid: 0ca5db75-cce0-4afc-9a58-c47c6229931e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '72'
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
| ` *`companyHandle`*` | `xsd:string` | Oui | Poignée vers la société avec la tâche que vous souhaitez redémarrer. |
| ` *`jobHandle`*` | `xsd:string` | Oui | Poignée de la tâche en pause. |

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
