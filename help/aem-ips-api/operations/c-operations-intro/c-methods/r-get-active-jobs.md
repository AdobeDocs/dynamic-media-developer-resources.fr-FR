---
description: Obtient toutes les tâches actuellement actives.
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 55e92ebc-d153-49b5-bf2e-c69d042e15b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 14%

---

# getActiveJobs{#getactivejobs}

Obtient toutes les tâches actuellement actives.

Syntaxe

## Types d’utilisateurs autorisés {#section-125557a6ea7b4fc894d4bb468cd02118}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-29018fba6bf34c1e80dcd479dd24f3b5}

**Input (getActiveJobsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Non | La poignée de la société. |
| jobHandle | `xsd:string` | Non | La poignée de la tâche. |
| originalName | `xsd:string` | Non | Nom de la tâche d’origine. |

**Output (getActiveJobsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| jobArray | `xsd:string` | Oui | Tableau des tâches actives. |

## Exemples {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

Cet exemple de code renvoie toutes les tâches actives d’une société s’exécutant dans IPS. Dans ce cas, la réponse est inhabituelle, car le coordinateur de planification IPS est désactivé et aucune tâche active n’est en cours d’exécution. Dans des circonstances normales, la réponse renverrait un certain nombre de tâches actives.

**Requête**

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
