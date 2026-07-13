---
description: Soumet un traitement au système.
solution: Experience Manager
title: submitJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b1dc7a0e-da9a-4086-822b-5274bd62eadf
TQID: 'https://experienceleague.adobe.com/RtEWl0OGJGwGT-0CfZPNXr1-zCFt--3ZcJQshdBA6Nk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 393
ht-degree: 7%

---

# submitJob{#submitjob}

Soumet un traitement au système.

Syntaxe

## Types d’utilisateurs autorisés {#section-eb7024277bec43c79e03f396205be16f}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-31a07dbccf964850883e817384499459}

**Input (submitJobParam)**

<table id="table_9CB1F668E036422E8CE4E0BBA42EC44C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nom </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatoire </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> <p>Identifiant de la société. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Gérer vers l’utilisateur qui a envoyé le traitement. </p> <p> <p>Remarque : le système envoie un e-mail à l’utilisateur spécifié par <span class="codeph"> userHandle</span>. Si <span class="codeph"> userHandle</span> n’est pas fourni, la personne qui a envoyé le traitement reçoit les e-mails. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> <p>Nom du traitement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> paramètres régionaux </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Paramètres régionaux utilisés pour les détails du log de traitement et la localisation des e-mails. </p> <p>Les paramètres régionaux sont spécifiés <span class="codeph"> &lt;language_code&gt;</span> et <span class="codeph"> [&lt;country_code&gt;]</span>, où le code de langue est un code à deux lettres en minuscules spécifié par la norme ISO-639 et le code de pays facultatif est un code à deux lettres en majuscules spécifié par la norme ISO-3166. Par exemple, la chaîne de paramètres régionaux pour l’anglais (États-Unis) serait : en-US. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execTime </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Date et heure d’exécution du traitement. </p> <p>Remarque : indiquez le fuseau horaire de la requête. Les fuseaux horaires sont adaptés au fuseau horaire du serveur IPS cible. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execSchedule </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détermine quand exécuter la tâche. </p> <p> Il peut s’agir d’une chaîne <span class="codeph"> cron</span> qui exécute la tâche de manière récurrente. </p> <p>La planification est toujours relative au fuseau horaire local du serveur. Voir la documentation IPS pour le format de planning personnalisé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> description </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Description du traitement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ExportJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Exportez les fichiers précédemment chargés. </p> <p>Voir <a href="../../../types/c-data-types/r-exportjob.md#reference-1ce423f7b2d54507b90b67233c588665" format="dita" scope="local"> ExportJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ImageServingPublishJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une image diffusant la tâche de publication. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ImageRenderingPublishJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une tâche de publication de rendu d’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :VideoPublishJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une tâche de publication vidéo. </p> <p>Voir <a href="../../../types/c-data-types/r-video-publish-job.md#reference-e99e60d38fe94a07914eefcd7beef2e0" format="dita" scope="local"> VideoPublishJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ServerDirectoryPublishJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’un traitement de publication de répertoire serveur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadDirectoryJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de sous-réseau :UploadDirectoryJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une tâche de répertoire de chargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de sous-réseau :UploadUrlsJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une tâche d’URL de chargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizerImagesJob</span> </span> </td> 
   <td colname="col2"> types de <span class="codeph"> :OptimizeImagesJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span> </span> </td> 
   <td colname="col2"> Types de <span class="codeph"> : RipPdfsJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de sous-dossiers :ReprocessAssetsJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> automatedSetGenerationJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de sous-réseau :AutomatedSetGenerationJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Traitez une liste de ressources en visionneuses à l’aide de scripts de visionneuse automatisée. </p> <p>Voir <a href="../../../types/c-data-types/r-automated-set-generation-job.md#reference-ab0b3c5408eb41b98c49898b2197cf5a" format="dita" scope="local"> AutomatedSetGenerationJob</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (submitJobReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| jobHandle | `xsd:string` | Oui | Traitement du traitement. |

## Exemples {#section-40ac77d14adf4588ba2575be6879b2d2}

Cet exemple de code envoie une image diffusant la tâche de publication à IPS et renvoie un descripteur de tâche. Sélectionnez un seul type de traitement dans la requête. Comme `userHandle` a été omis, des notifications par e-mail sont envoyées à l’utilisateur qui a envoyé le traitement. Cet exemple de tâche s’exécute immédiatement, car `execTime` et `execSchedule` ont été omis.

**Requête**

```java
<submitJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobName>My Test Job</jobName>
   <imageServingPublishJob>
      <publishType>Full</publishType>
      <emailSetting>Error</emailSetting>
   </imageServingPublishJob>
</submitJobParam>
```

**Réponse**

```java
<submitJobReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobHandle>47|My Test Job|</jobHandle>
</submitJobReturn>
```

## Remarques {#section-0f3078e503a249aeb6f3d662a51f036a}

Vous pouvez spécifier au maximum l’une des options `execTime` et `execSchedule`. Si aucun des deux n’est transmis, la tâche s’exécute immédiatement. Vous ne pouvez utiliser que l’une des méthodes suivantes :

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`

