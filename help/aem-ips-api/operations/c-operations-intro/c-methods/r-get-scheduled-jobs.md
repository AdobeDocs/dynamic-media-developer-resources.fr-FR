---
description: Obtient les tâches planifiées pour exécution.
solution: Experience Manager
title: getScheduledJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7920637e-b289-410c-ae5c-e67cd7b21aba
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 20%

---

# getScheduledJobs{#getscheduledjobs}

Obtient les tâches planifiées pour exécution.

Syntaxe

## Types d’utilisateurs autorisés {#section-bd1835ab508a429f8143b3bdb811d6a4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-2af604ff8282460990b9237158187f8f}

**Input (getScheduledJobsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | La poignée de la société. |
| jobHandle | `xsd:string` | Non | Traitement du traitement. |
| originalName | `xsd:string` | Non | Nom spécifié par `submitJob`. |

**Output (getScheduledJobsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| jobArray | `types:ScheduledJobArray` | Oui | Tableau des tâches planifiées. |

## Exemples {#section-e79e7da86ba848fd9996aa36de462e6c}

Cet exemple de code renvoie toutes les tâches planifiées dans un tableau de tâches. Le tableau lui-même contient des informations détaillées sur les tâches.

**Requête**

```java
<getScheduledJobsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>0</companyHandle>
</getScheduledJobsParam>
```

**Réponse**

```java
<getScheduledJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray>
      <items>
         <companyHandle>0</companyHandle>
         <jobHandle>0|Cleanup|</jobHandle>
         <name>Cleanup</name>
         <originalName></originalName>
         <type>Cleanup</type>
         <submitUserEmail>default@scene7.com</submitUserEmail>
         <execSchedule>00 00 00 * * </execSchedule>
         <nextFireTime>2007-10-13T00:00:00.000-07:00</nextFireTime>
         <timeZone>PST</timeZone>
         <triggerState>Paused</triggerState>
      </items>
   </jobArray>
</getScheduledJobsReturn>
```
