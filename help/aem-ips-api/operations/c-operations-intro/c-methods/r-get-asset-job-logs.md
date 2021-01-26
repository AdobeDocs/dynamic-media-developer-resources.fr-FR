---
description: Récupère les journaux de tâches d’un fichier. Les éléments renvoyés dans le tableau contiennent des informations détaillées sur chaque entrée du journal des tâches pour cette ressource. Le champ de réponse logMessage est localisé en fonction du champ authHeader.
seo-description: Récupère les journaux de tâches d’un fichier. Les éléments renvoyés dans le tableau contiennent des informations détaillées sur chaque entrée du journal des tâches pour cette ressource. Le champ de réponse logMessage est localisé en fonction du champ authHeader.
seo-title: getAssetJobLogs
solution: Experience Manager
title: getAssetJobLogs
topic: Dynamic Media Image Production System API
uuid: 7ea81baf-769b-4c73-bbc6-f52c89c98d50
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 8%

---


# getAssetJobLogs{#getassetjoblogs}

Récupère les journaux de tâches d’un fichier. Les éléments renvoyés dans le tableau contiennent des informations détaillées sur chaque entrée du journal des tâches pour cette ressource. Le champ de réponse logMessage est localisé en fonction du champ authHeader.

Syntaxe

## Types d’utilisateur autorisés {#section-72b98cdb0f6f47f5aabdc183a45ea577}

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
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société à laquelle appartient le fichier. |
| `*`assetHandle`*` | `xsd:string` | Oui | Poignée de ressource avec les journaux de tâches à récupérer. |

**Sortie (getAssetJobLogsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`jobLogArray`*` | `types:AssetJobLogArray` | Oui | Tableau du journal des tâches. |

## Exemples {#section-f03d7f3ec5d043d38227f926fb7609f6}

Cet exemple de code récupère les journaux des tâches d’une ressource spécifique. La réponse renvoie un tableau du journal des tâches contenant des informations détaillées sur toutes les tâches dans lesquelles la ressource a été utilisée.

**Request**

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

