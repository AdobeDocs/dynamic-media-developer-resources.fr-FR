---
description: Redémarre un traitement en pause.
solution: Experience Manager
title: resumeJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ba8818ff-3040-463c-80d3-b7cfd1e01f77
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 14%

---

# resumeJob{#resumejob}

Redémarre un traitement en pause.

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

**Input (resumeJobParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Le handle de la société avec le traitement que vous souhaitez redémarrer. |
| jobHandle | `xsd:string` | Oui | Poignée du traitement en pause. |

**Output (resumeJobReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-d0524e031f1f43d89430eade19526162}

Cet exemple de code redémarre un traitement en pause.

**Requête**

```java
<resumeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</resumeJobParam>
```

**Réponse**

Aucune
