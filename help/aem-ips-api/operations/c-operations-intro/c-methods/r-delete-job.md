---
description: Supprime une tâche en cours ou planifiée.
seo-description: Supprime une tâche en cours ou planifiée.
seo-title: deleteJob
solution: Experience Manager
title: deleteJob
topic: Scene7 Image Production System API
uuid: c1109cae-a3ca-40db-b641-9a6fc116c964
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

**Input (deleteJobParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Poignée du auquel appartient la tâche. |
| ` *`jobHandle`*` | `xsd:string` | Oui | Identifiant de la tâche à supprimer. |

**Sortie**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-732d21d4dad04337b7a5ae1a0cc00eba}

Cet exemple de code supprime une tâche en cours d’exécution ou qui est planifiée pour être exécutée dans IPS. Il nécessite une poignée de tâche, que vous devez obtenir d’une autre opération.

**Request**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**Réponse**

Aucune
