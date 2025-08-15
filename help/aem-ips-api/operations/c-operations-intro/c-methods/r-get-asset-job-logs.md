---
description: Obtient les rapports des tâches d’une ressource. Les éléments renvoyés dans le tableau contiennent des informations détaillées sur chaque entrée dans le journal de travail de cette ressource. Le champ de réponse logMessage est localisé en fonction du champ authEn-tête.
solution: Experience Manager
title: getAssetJobLogs
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 88ec5cab-7eb4-48aa-914f-21311593e463
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 8%

---

# getAssetJobLogs{#getassetjoblogs}

Obtient les rapports des tâches d’une ressource. Les éléments renvoyés dans le tableau contiennent des informations détaillées sur chaque entrée dans le journal de travail de cette ressource. Le champ de réponse logMessage est localisé en fonction du champ authEn-tête.

Syntaxe

## Types d’utilisateurs autorisés {#section-72b98cdb0f6f47f5aabdc183a45ea577}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-9586617e124b4da4acb6b66b2a9adad8}

**Entrée (getAssetJobLogsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| CompanyHandle | `xsd:string` | Oui | Identifiant de l’entreprise à laquelle la ressource appartient. |
| AssetHandle | `xsd:string` | Oui | Poignée de la ressource contenant les journaux de tâche à récupérer. |

**Output (getAssetJobLogsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| jobLogArray | `types:AssetJobLogArray` | Oui | Tableau du journal des tâches. |

## Exemples {#section-f03d7f3ec5d043d38227f926fb7609f6}

Cet exemple de code récupère les journaux de tâches d’une ressource spécifique. La réponse renvoie un tableau de journal de tâche avec des informations détaillées sur toutes les tâches dans lesquelles la ressource a été utilisée.

**Demander**

```java
<getAssetJobLogsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetJobLogsParam>
```

**Réponse**

```java
<getAssetJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <jobLogArray>
      <items>
         <jobHandle>j|6||Add_2007-10-24-16:11:07</jobHandle>
         <jobName>Add_2007-10-24-16:11:07</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS</logMessage>
         <logType>UploadSuccess</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2007-10-24T16:12:32.297-07:00</logDate>
      </items>
      <items>
         <jobHandle>j|6||submitServerUploadJob40_2008-06-11-11:38</jobHandle>
         <jobName>submitServerUploadJob40_2008-06-11-11:38</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS.</logMessage>
         <logType>FileUpdated</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2008-06-11T11:38:48.547-07:00</logDate>
      </items>
   </jobLogArray>
</getAssetJobLogsReturn>
```
