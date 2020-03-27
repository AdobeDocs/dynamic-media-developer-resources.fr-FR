---
description: Obtient les journaux de tâches spécifiés pour le  sélectionné. Vous pouvez trier par caractères, direction, dates de  et de fin et nombre de lignes.
seo-description: Obtient les journaux de tâches spécifiés pour le  sélectionné. Vous pouvez trier par caractères, direction, dates de  et de fin et nombre de lignes.
seo-title: getJobLogs
solution: Experience Manager
title: getJobLogs
topic: Scene7 Image Production System API
uuid: 850ccfad-6cdb-4eda-a20a-762fadadf8b2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getJobLogs{#getjoblogs}

Obtient les journaux de tâches spécifiés pour le  sélectionné. Vous pouvez trier par caractères, direction, dates de  et de fin et nombre de lignes.

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
| ` *`companyHandle`*` | `xsd:string` | Non |  poignée. |
| ` *`userHandle`*` | `xsd:string` | Non | Obtient les journaux des tâches envoyées par un utilisateur spécifique. |
| ` *`sortBy`*` | `xsd:string` | Non | Permet de sélectionner des champs de tri. |
| ` *`sortDirection`*` | `xsd:string` | Non | Ordre de tri (croissant ou décroissant). |
| ` *`startDate`*` | `xsd:dateTime` | Non | Date et heure du du journal des tâches. Indiquez le fuseau horaire avec la demande de ce champ. |
| ` *`endDate`*` | `xsd:dateTime` | Non | Date et heure de fin du journal des tâches. Indiquez le fuseau horaire avec la demande de ce champ. |
| ` *`numRows`*` | `xsd:int` | Non | Nombre maximal de lignes à renvoyer. |

**Output (getJobLogsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`jobLogArray`*` | `types: JobLogArray` | Oui | Tableau des journaux des tâches. |

## Exemples {#section-35871c94b4a44559912577efddbc46a6}

Cet exemple de code renvoie des journaux de tâches IPS pour un  spécifique. Vous pouvez également l’utiliser pour renvoyer des journaux de tâches pour un utilisateur ou un ou un utilisateur spécifique.

**Request**

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

