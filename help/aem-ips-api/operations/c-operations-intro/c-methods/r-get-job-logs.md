---
description: Obtient les logs de traitement spécifiés pour l'entreprise sélectionnée. Vous pouvez trier par caractères, sens, dates de début et de fin, et nombre de lignes.
solution: Experience Manager
title: getJobLogs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6239c3c4-bdbc-4e69-82d4-48a76f080eff
TQID: 'https://experienceleague.adobe.com/lerbQ3ibPCI3zqkrmgPrwTAYp1w6dWxIWYRt2Ij51oA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 184
ht-degree: 10%

---

# getJobLogs{#getjoblogs}

Obtient les logs de traitement spécifiés pour l&#39;entreprise sélectionnée. Vous pouvez trier par caractères, sens, dates de début et de fin, et nombre de lignes.

Syntaxe

## Types d’utilisateurs autorisés {#section-9df82972265d44c9ad91504a17c3ffa6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-8cfdc7994da24678a45edcb37e9a2166}

**Input (getJobLogsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Non | La gestion de l&#39;entreprise. |
| userHandle | `xsd:string` | Non | Obtient les journaux des tâches envoyées par un utilisateur spécifique. |
| sortBy | `xsd:string` | Non | Permet de sélectionner des champs de tri. |
| sortDirection | `xsd:string` | Non | Ordre de tri (croissant ou décroissant). |
| startDate | `xsd:dateTime` | Non | Date et heure de début du log de traitement. Indiquez le fuseau horaire avec la requête pour ce champ. |
| endDate | `xsd:dateTime` | Non | Date et heure de la fin du log de traitement. Indiquez le fuseau horaire avec la requête pour ce champ. |
| numRows | `xsd:int` | Non | Nombre maximum de lignes à retourner. |

**Output (getJobLogsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| jobLogArray | `types: JobLogArray` | Oui | Tableau des logs de traitement. |

## Exemples {#section-35871c94b4a44559912577efddbc46a6}

Cet exemple de code renvoie des journaux de tâches IPS pour une société spécifique. Vous pouvez également l’utiliser pour renvoyer les journaux de tâches d’un utilisateur, d’une entreprise et d’un utilisateur spécifiques.

**Requête**

```java
<ns1:getJobLogsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getJobLogsParam>
```

**Réponse**

```java
<getJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobLogArray>
      <items>
         <companyHandle>47</companyHandle>
         <jobHandle>47||Add_2007-09-14-15:04:34</jobHandle>
         <jobName>Add_2007-09-14-15:04:34</jobName>
         <submitUserEmail>kmagnusson@adobe.com</submitUserEmail>
         <logType>BeginUpload</logType>
         <startDate>2007-09-14T22:04:58.536-07:00</startDate>
         <fileSuccessCount>2</fileSuccessCount>
         <fileErrorCount>0</fileErrorCount>
         <fileWarningCount>205</fileWarningCount>
         <fileDuplicateCount>0</fileDuplicateCount>
         <fileUpdateCount>0</fileUpdateCount>
         <totalFileCount>0</totalFileCount>
         <fatalError>false</fatalError>
       </items>
   </jobLogArray>
</getJobLogsReturn>
```
