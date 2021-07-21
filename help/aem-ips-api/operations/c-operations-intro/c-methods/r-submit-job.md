---
description: Envoie une tâche au système.
solution: Experience Manager
title: submitJob
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: b1dc7a0e-da9a-4086-822b-5274bd62eadf
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 12%

---

# submitJob{#submitjob}

Envoie une tâche au système.

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

**Entrée (submitJobParam)**

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> <p>Poignée de la société. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Gérer l’utilisateur qui a envoyé la tâche. </p> <p> <p>Remarque : Le système envoie le courrier électronique à l’utilisateur spécifié par <span class="codeph"> userHandle</span>. Si <span class="codeph"> userHandle</span> n’est pas fourni, la personne qui a envoyé la tâche reçoit les e-mails. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> <p>Nom de la tâche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Paramètre régional utilisé pour les détails du journal des tâches et la localisation des emails. </p> <p>Les paramètres régionaux sont spécifiés sous la forme <span class="codeph"> &lt;code_langue&gt;</span> et <span class="codeph"> [&lt;code_pays&gt;]</span>, où le code de langue est un code à deux lettres en minuscules, comme spécifié par ISO-639, et le code de pays facultatif est un code à deux lettres majuscules, comme spécifié par ISO-3166. Par exemple, la chaîne du paramètre régional pour l’anglais (États-Unis) serait : en-US. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Date et heure d’exécution de la tâche. </p> <p>Remarque :  Indiquez le fuseau horaire avec la requête. Les fuseaux horaires sont ajustés au fuseau horaire du serveur IPS cible. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execSchedule</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détermine le moment d’exécution de la tâche. </p> <p> Peut être une chaîne <span class="codeph"> cron</span> qui exécute la tâche de manière récurrente. </p> <p>Le planning est toujours relatif au fuseau horaire local du serveur. Consultez la documentation IPS pour connaître le format de planification personnalisé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> description</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Description de la tâche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ExportJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Exportez les fichiers précédemment téléchargés. </p> <p>Voir <a href="../../../types/c-data-types/r-exportjob.md#reference-1ce423f7b2d54507b90b67233c588665" format="dita" scope="local"> ExportJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une tâche de publication de diffusion d’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageRenderingPublishJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une tâche de publication de rendu d’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:VideoPublishJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une tâche de publication vidéo. </p> <p>Voir <a href="../../../types/c-data-types/r-video-publish-job.md#reference-e99e60d38fe94a07914eefcd7beef2e0" format="dita" scope="local"> VideoPublishJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ServerDirectoryPublishJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une tâche de publication de répertoire de serveur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadDirectoryJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:UploadDirectoryJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une tâche de téléchargement de répertoire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:UploadUrlsJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une tâche de téléchargement d’URL. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:OptimizeImagesJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:RipPdfsJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ReprocessAssetsJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> AutomatedSetGenerationJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AutomatedSetGenerationJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Traitez une liste de ressources en ensembles à l’aide de scripts de visionneuse automatisés. </p> <p>Voir <a href="../../../types/c-data-types/r-automated-set-generation-job.md#reference-ab0b3c5408eb41b98c49898b2197cf5a" format="dita" scope="local"> AutomatedSetGenerationJob</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Sortie (submitJobReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`jobHandle`*` | `xsd:string` | Oui | Poignée de tâche. |

## Exemples {#section-40ac77d14adf4588ba2575be6879b2d2}

Cet exemple de code envoie une tâche de publication de diffusion d’image à IPS et renvoie un gestionnaire de tâche. Sélectionnez un seul type de tâche dans la requête. Comme `userHandle` a été omis, des notifications par courrier électronique sont envoyées à l’utilisateur qui a envoyé la tâche. Cet exemple de tâche s’exécute immédiatement car `execTime` et `execSchedule` ont été omis.

**Request**

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

Vous pouvez spécifier au plus l’une des valeurs `execTime` et `execSchedule`. Si aucun des deux n’est transmis, la tâche s’exécute immédiatement. Vous ne pouvez utiliser que l’une des méthodes suivantes :

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`
