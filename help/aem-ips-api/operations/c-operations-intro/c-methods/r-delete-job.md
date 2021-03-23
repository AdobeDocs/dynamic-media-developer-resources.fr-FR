---
description: Supprime une tâche en cours ou planifiée.
seo-description: Supprime une tâche en cours ou planifiée.
seo-title: deleteJob
solution: Experience Manager
title: deleteJob
uuid: c1109cae-a3ca-40db-b641-9a6fc116c964
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 11%

---


# deleteJob{#deletejob}

Supprime une tâche en cours ou planifiée.

Syntaxe

## Types d’utilisateur autorisés {#section-1b959679dc8147c291126ddf7e061742}

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
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société à laquelle appartient la tâche. |
| `*`jobHandle`*` | `xsd:string` | Oui | Poignée de la tâche à supprimer. |

**Sortie**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-732d21d4dad04337b7a5ae1a0cc00eba}

Cet exemple de code supprime une tâche en cours d&#39;exécution ou dont l&#39;exécution est planifiée dans IPS. Il nécessite une poignée de travail, que vous devez obtenir d&#39;une autre opération.

**Request**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**Réponse**

Aucune
