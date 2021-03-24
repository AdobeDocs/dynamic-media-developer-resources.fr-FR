---
description: Obtient les journaux de tâches spécifiés pour la société sélectionnée. Vous pouvez trier par caractères, direction, dates de début et de fin et nombre de lignes.
solution: Experience Manager
title: getJobLogs
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 10%

---


# getJobLogs{#getjoblogs}

Obtient les journaux de tâches spécifiés pour la société sélectionnée. Vous pouvez trier par caractères, direction, dates de début et de fin et nombre de lignes.

Syntaxe

## Types d’utilisateur autorisés {#section-9df82972265d44c9ad91504a17c3ffa6}

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

**Entrée (getJobLogsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Non | Poignée de société. |
| `*`userHandle`*` | `xsd:string` | Non | Récupère les journaux des tâches soumises par un utilisateur spécifique. |
| `*`sortBy`*` | `xsd:string` | Non | Permet de sélectionner des champs de tri. |
| `*`sortDirection`*` | `xsd:string` | Non | Ordre de tri (croissant ou décroissant). |
| `*`startDate`*` | `xsd:dateTime` | Non | Date et heure du début du journal des tâches. Indiquez le fuseau horaire avec la demande de ce champ. |
| `*`endDate`*` | `xsd:dateTime` | Non | Date et heure de fin du journal des tâches. Indiquez le fuseau horaire avec la demande de ce champ. |
| `*`numRows`*` | `xsd:int` | Non | Nombre maximal de lignes à renvoyer. |

**Output (getJobLogsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`jobLogArray`*` | `types: JobLogArray` | Oui | Tableau des journaux des tâches. |

## Exemples {#section-35871c94b4a44559912577efddbc46a6}

Cet exemple de code renvoie des journaux de tâches IPS pour une société spécifique. Vous pouvez également l’utiliser pour renvoyer des journaux de tâches pour un utilisateur ou une société et un utilisateur spécifiques.

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

