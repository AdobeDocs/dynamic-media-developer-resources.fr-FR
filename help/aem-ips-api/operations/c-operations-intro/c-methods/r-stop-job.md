---
description: Arrête une tâche en cours.
solution: Experience Manager
title: Tâche d’arrêt
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 90e61cf1-11f1-4504-8007-126ba4fe436a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 18%

---

# Tâche d’arrêt{#stopjob}

Arrête une tâche en cours.

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

**Input (stopJobParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| CompanyHandle | `xsd:string` | Oui | Pseudo de l’entreprise. |
| Poignée de tâche | `xsd:string` | Oui | Gérez la tâche que vous souhaitez arrêter. |

**Output (stopJobReturn0**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-f7e07fa09ae24dc89685533f20ab3b81}

**Demander**

```java
<stopJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</stopJobParam>
```

**Réponse**

Aucune
