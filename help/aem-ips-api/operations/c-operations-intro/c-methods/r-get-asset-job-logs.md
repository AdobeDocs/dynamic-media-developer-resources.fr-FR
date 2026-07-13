---
description: Obtient les logs de traitement d’une ressource. Les éléments renvoyés dans le tableau contiennent des informations détaillées sur chaque entrée du journal de tâches pour cette ressource. Le champ de réponse logMessage est localisé en fonction du champ authHeader .
solution: Experience Manager
title: getAssetJobLogs
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 88ec5cab-7eb4-48aa-914f-21311593e463
TQID: 'https://experienceleague.adobe.com/P8JrN-sCYIQmvFBJrNxiPdmp1Au8-8Tjdpd7DwpRS2I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 156
ht-degree: 8%

---

# getAssetJobLogs{#getassetjoblogs}

Obtient les logs de traitement d’une ressource. Les éléments renvoyés dans le tableau contiennent des informations détaillées sur chaque entrée du journal de tâches pour cette ressource. Le champ de réponse logMessage est localisé en fonction du champ authHeader .

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

**Input (getAssetJobLogsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société à laquelle appartient la ressource. |
| assetHandle | `xsd:string` | Oui | Identifiant de la ressource avec les logs de traitement à récupérer. |

**Output (getAssetJobLogsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| jobLogArray | `types:AssetJobLogArray` | Oui | Tableau de logs de traitement. |

## Exemples {#section-f03d7f3ec5d043d38227f926fb7609f6}

Cet exemple de code récupère les journaux de tâches d’une ressource spécifique. La réponse renvoie un tableau de logs de traitement avec des informations détaillées sur toutes les tâches dans lesquelles la ressource a été utilisée.

**Requête**

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

