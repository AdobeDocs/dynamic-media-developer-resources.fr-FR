---
description: Obtient toutes les tâches actuellement principales.
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 15%

---


# getActiveJobs{#getactivejobs}

Obtient toutes les tâches actuellement principales.

Syntaxe

## Types d’utilisateur autorisés {#section-125557a6ea7b4fc894d4bb468cd02118}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-29018fba6bf34c1e80dcd479dd24f3b5}

**Entrée (getActiveJobsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Non | La poignée de la société. |
| `*`jobHandle`*` | `xsd:string` | Non | La poignée de la tâche. |
| `*`originalName`*` | `xsd:string` | Non | Nom de la tâche d’origine. |

**Output (getActiveJobsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`jobArray`*` | `xsd:string` | Oui | Tableau des tâches principales. |

## Exemples {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

Cet exemple de code renvoie toutes les tâches principales d&#39;une société s&#39;exécutant dans IPS. Dans ce cas, la réponse est inhabituelle car le coordinateur de planification IPS est désactivé sans que les tâches principales soient en cours d&#39;exécution. Dans des circonstances normales, la réponse renverrait un certain nombre d&#39;emplois principaux.

**Request**

```java
<ns1:getActiveJobsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getActiveJobsParam>
```

**Réponse**

```java
<getActiveJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray></jobArray>
</getActiveJobsReturn>
```

