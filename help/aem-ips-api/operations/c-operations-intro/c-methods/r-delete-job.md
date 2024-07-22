---
description: Supprime une tâche en cours ou planifiée.
solution: Experience Manager
title: deleteJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d38dd1e2-668e-4956-b854-54bf466d6d45
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 11%

---

# deleteJob{#deletejob}

Supprime une tâche en cours ou planifiée.

Syntaxe

## Types d’utilisateurs autorisés {#section-1b959679dc8147c291126ddf7e061742}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-000c42bc93744b1a8e777f3ec3c272b0}

**Entrée (deleteJobParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gestionnaire de la société à laquelle appartient la tâche. |
| jobHandle | `xsd:string` | Oui | Gestionnaire de la tâche à supprimer. |

**Output**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-732d21d4dad04337b7a5ae1a0cc00eba}

Cet exemple de code supprime une tâche en cours d’exécution ou planifiée dans IPS. Elle nécessite une gestion de tâche, que vous devez obtenir d’une autre opération.

**Requête**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**Réponse**

Aucune
