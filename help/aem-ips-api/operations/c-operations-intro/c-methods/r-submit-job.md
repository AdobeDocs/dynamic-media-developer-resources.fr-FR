---
description: Envoie une tâche au système.
seo-description: Envoie une tâche au système.
seo-title: submitJob
solution: Experience Manager
title: submitJob
topic: Scene7 Image Production System API
uuid: d3a83b59-bcd7-4ae9-b1ee-e515fc3c9261
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> sociétéHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> <p> poignée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Traitez l’utilisateur qui a envoyé la tâche. </p> <p> <p>Remarque : Le système envoie un courrier électronique à l’utilisateur spécifié par <span class="codeph"> userHandle</span>. Si <span class="codeph"> userHandle</span> n’est pas fourni, la personne qui a envoyé la tâche reçoit les courriers électroniques. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> <p>Nom de la tâche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Paramètres régionaux utilisés pour les détails du journal des tâches et les  par courrier électronique. </p> <p>Les paramètres régionaux sont spécifiés sous la forme <span class="codeph"> &lt;code_langue&gt;</span> et <span class="codeph"> [&lt;code_pays&gt;]</span>, où le code de langue est un code en minuscules, à deux lettres, comme spécifié par ISO-639, et le code de pays facultatif est un code en majuscules, à deux lettres, comme spécifié par ISO-3166. Par exemple, la chaîne de paramètres régionaux pour l’anglais (Etats-Unis) serait : en-US. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execTime</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Date et heure d’exécution de la tâche. </p> <p>Remarque :  Indiquez le fuseau horaire avec la requête. Les fuseaux horaires sont ajustés au fuseau horaire du serveur IPS . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execSchedule</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détermine le moment d’exécution de la tâche. </p> <p> Il peut s’agir d’une <span class="codeph"> chaîne cron</span> qui exécute la tâche de manière récurrente. </p> <p>La planification dépend toujours du fuseau horaire local du serveur. Consultez la documentation IPS pour connaître le format de planification personnalisé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> description</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Description de la tâche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:ExportJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Exportez les fichiers précédemment téléchargés. </p> <p>Voir <a href="../../../types/c-data-types/r-exportjob.md#reference-1ce423f7b2d54507b90b67233c588665" format="dita" scope="local"> Tâche</a>d’exportation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ImageServingPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une tâche de publication de diffusion d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageRenderingPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:ImageRenderingPublishJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une tâche de publication de rendu d’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> Tâche <span class="varname"> de publication</span> vidéo </span> </td> 
   <td colname="col2"> <span class="codeph"> type:VideoPublishJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une tâche de publication vidéo. </p> <p>Voir <a href="../../../types/c-data-types/r-video-publish-job.md#reference-e99e60d38fe94a07914eefcd7beef2e0" format="dita" scope="local"> PublicationVidéoTâche</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:ServerDirectoryPublishJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une tâche de publication dans le répertoire du serveur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadDirectoryJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:UploadDirectoryJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une tâche de répertoire de téléchargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:UploadUrlsJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une tâche d’URL de téléchargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:OptimizeImagesJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:RipPdfsJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:ReprocessAssetsJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> automatiséSetGenerationJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:AutomatedSetGenerationJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Traitez un de ressources en jeux à l’aide de scripts d’ensemble automatisés. </p> <p>Voir <a href="../../../types/c-data-types/r-automated-set-generation-job.md#reference-ab0b3c5408eb41b98c49898b2197cf5a" format="dita" scope="local"> AutomatedSetGenerationJob</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (submitJobReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`jobHandle`*` | `xsd:string` | Oui | Poignée de tâche. |

## Exemples {#section-40ac77d14adf4588ba2575be6879b2d2}

Cet exemple de code envoie une tâche de publication de diffusion d’image à IPS et renvoie un nom d’utilisateur de tâche. Sélectionnez un seul type de tâche dans la requête. Etant donné que `userHandle` ce paramètre a été omis, des notifications par courrier électronique sont envoyées à l’utilisateur qui a envoyé la tâche. Cet exemple de tâche s’exécute immédiatement, car `execTime` et `execSchedule` a été omis.

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

Vous pouvez spécifier au maximum l’un des `execTime` et `execSchedule`. Si aucun des deux n’est transmis, la tâche s’exécute immédiatement. Vous ne pouvez utiliser que l’une des méthodes suivantes :

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`

