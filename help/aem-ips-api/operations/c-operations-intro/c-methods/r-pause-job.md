---
description: Interrompt un principal travail.
solution: Experience Manager
title: pauseJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 17%

---


# pauseJob{#pausejob}

Interrompt un principal travail.

Syntaxe

## Types d’utilisateur autorisés {#section-f2bf306ab4574871bd21f9f7dd681033}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-7aedb924cf8b4e05a0dc927636d537a0}

**Entrée (pauseJobParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Pose la société. |
| `*`jobHandle`*` | `xsd:string` | Oui | Traitez la tâche que vous souhaitez mettre en pause. |

**Sortie (PauseJobReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-ee4914f9496f4bd88556728a48fb22c1}

Cet exemple de code interrompt une tâche principale.

**Request**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**Réponse**

Aucune
