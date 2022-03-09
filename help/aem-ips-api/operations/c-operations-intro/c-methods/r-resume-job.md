---
description: Redémarre une tâche suspendue.
solution: Experience Manager
title: resumeJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ba8818ff-3040-463c-80d3-b7cfd1e01f77
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 17%

---

# resumeJob{#resumejob}

Redémarre une tâche suspendue.

Syntaxe

## Types d’utilisateurs autorisés {#section-eab49f4b6d1041179000326a10fee889}

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
| companyHandle | `xsd:string` | Oui | La gestion de la société avec la tâche que vous souhaitez redémarrer. |
| jobHandle | `xsd:string` | Oui | Gestion de la tâche suspendue. |

**Sortie (resumeJobReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

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
