---
description: Obtient les journaux de tâches spécifiés pour l’entreprise sélectionnée. Vous pouvez trier par caractères, direction, dates de début et de fin et nombre de lignes.
solution: Experience Manager
title: getJobLogs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6239c3c4-bdbc-4e69-82d4-48a76f080eff
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 10%

---

# getJobLogs{#getjoblogs}

Obtient les journaux de tâches spécifiés pour l’entreprise sélectionnée. Vous pouvez trier par caractères, direction, dates de début et de fin et nombre de lignes.

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
| CompanyHandle | `xsd:string` | Non | Gérez l’entreprise. |
| Poignée utilisateur | `xsd:string` | Non | Obtient les journaux des tâches envoyées par un utilisateur spécifique. |
| Tri par | `xsd:string` | Non | Permet de sélectionner des champs de tri. |
| sortDirection | `xsd:string` | Non | Ordre de tri (croissant ou décroissant). |
| Date de début | `xsd:dateTime` | Non | La date et l’heure du début du journal de travail. Indiquez le fuseau horaire contenant la demande pour ce champ. |
| Date de fin | `xsd:dateTime` | Non | date et heure de fin du journal de travail. Indiquez le fuseau horaire contenant la demande pour ce champ. |
| Rangées numériques | `xsd:int` | Non | Nombre maximum de lignes à renvoyer. |

**Output (getJobLogsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| jobLogArray | `types: JobLogArray` | Oui | Tableau de journaux de travail. |

## Exemples {#section-35871c94b4a44559912577efddbc46a6}

Cet échantillon de code renvoie les journaux de tâches IPS d’une entreprise spécifique. Vous pouvez également l’utiliser pour renvoyer les rapports d’un utilisateur spécifique ou d’une société et d’un utilisateur.

**Demander**

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
