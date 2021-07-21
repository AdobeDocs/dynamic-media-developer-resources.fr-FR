---
description: Arrête un traitement en cours.
solution: Experience Manager
title: stopJob
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 90e61cf1-11f1-4504-8007-126ba4fe436a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 20%

---

# stopJob{#stopjob}

Arrête un traitement en cours.

Syntaxe

## Types d’utilisateurs autorisés {#section-b222f561143747f6ad089aadc0b274d8}

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
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société. |
| `*`jobHandle`*` | `xsd:string` | Oui | Gérez la tâche que vous souhaitez arrêter. |

**Sortie (stopJobReturn0**

L’API IPS ne renvoie pas de réponse pour cette opération.

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
