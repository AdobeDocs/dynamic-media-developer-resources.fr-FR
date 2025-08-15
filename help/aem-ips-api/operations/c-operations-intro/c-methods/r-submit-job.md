---
description: Envoie une tâche au système.
solution: Experience Manager
title: Tâche submitTask
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b1dc7a0e-da9a-4086-822b-5274bd62eadf
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 7%

---

# Tâche submitTask{#submitjob}

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
   <td colname="col1"> <span class="codeph"><span class="varname"> CompanyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> <p>Pseudo de l’entreprise. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Poignée</span> utilisateur </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Handle à l’utilisateur qui a envoyé la tâche. </p> <p> <p>Remarque : Le système envoie un courrier électronique à l’utilisateur spécifié par <span class="codeph"> userHandle</span>. Si <span class="codeph"> userHandle</span> n’est pas fourni, la personne qui a envoyé la tâche reçoit les courriers électroniques. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"></span> Nom de tâche </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> <p>Nom de la tâche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> paramètres régionaux</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Paramètres régionaux utilisés pour les détails du journal de la tâche et la localisation des adresses électroniques. </p> <p>Les paramètres régionaux sont spécifiés sous la forme <span class="codeph"> &lt;language_code&gt;</span> et <span class="codeph"> [&lt;country_code&gt;]</span>, où le code de langue est un code à deux lettres minuscules, conformément à la norme ISO-639, et le code pays facultatif est un code majuscule à deux lettres tel que spécifié par la norme ISO-3166. &lt;/country_code&gt;&lt;/language_code&gt; Par exemple, la chaîne du paramètre régional Anglais (États-Unis) serait : en-US. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"></span> Temps exécutif </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :dateTime</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Date et heure d’exécution de la tâche. </p> <p>Remarque : indiquez le fuseau horaire avec la demande. Les fuseaux horaires sont ajustés au fuseau horaire du serveur IPS cible. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> execSchedule</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détermine le moment de l’exécution de la tâche. </p> <p> Il peut s’agir d’une <span class="codeph"> chaîne cron</span> qui exécute la tâche de façon récurrente. </p> <p>La planification dépend toujours du fuseau horaire local du serveur. Voir la documentation IPS pour connaître le format de planification personnalisé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> description</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Description d’emploi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Traitement d’exportation</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ExportJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Exportez les fichiers précédemment téléchargés. </p> <p>Voir <a href="../../../types/c-data-types/r-exportjob.md#reference-1ce423f7b2d54507b90b67233c588665" format="dita" scope="local"> ExportJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Image ServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ImageServingPublishJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une tâche de publication Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Tâche de publication de rendu d’image</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ImageRenderingPublishJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une tâche de publication de rendu d’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Tâche</span> de publication vidéo </span> </td> 
   <td colname="col2"> <span class="codeph"> types :VideoPublishJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une tâche de publication vidéo. </p> <p>Voir <a href="../../../types/c-data-types/r-video-publish-job.md#reference-e99e60d38fe94a07914eefcd7beef2e0" format="dita" scope="local"> VideoPublishJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ServerDirectoryPublishJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Informations sur une tâche de publication de répertoire de serveur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Tâche d’annuaire</span> de téléchargement </span> </td> 
   <td colname="col2"> <span class="codeph"> types :UploadDirectoryJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Informations détaillées sur une tâche dans le répertoire de téléchargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types : UploadUrlsJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Détails d’une tâche de téléchargement d’URL. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Tâche d’optimisation des</span> images </span> </td> 
   <td colname="col2"> <span class="codeph"> types :OptimizeImagesJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Tâche ripPdfsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :RipPdfsJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Tâche</span> de retraitement des ressources </span> </td> 
   <td colname="col2"> <span class="codeph"> types :Reprocess AssetsJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Tâche de génération de visionneuse</span> automatisée </span> </td> 
   <td colname="col2"> <span class="codeph"> types : AutomatedSetGenerationJob</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Traitez une liste de fichiers en ensembles à l’aide des scripts d’ensemble automatisés. </p> <p>Voir <a href="../../../types/c-data-types/r-automated-set-generation-job.md#reference-ab0b3c5408eb41b98c49898b2197cf5a" format="dita" scope="local"> AutomatedSetGenerationJob</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (submitJobReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Poignée de tâche | `xsd:string` | Oui | Gestion de la tâche. |

## Exemples {#section-40ac77d14adf4588ba2575be6879b2d2}

Cet exemple de code envoie une tâche de publication de serveur d’images à IPS et renvoie une poignée de tâche. Choisissez un seul type de tâche dans la demande. Comme `userHandle` elle a été omise, des notifications électroniques sont envoyées à l’utilisateur qui a envoyé la tâche. Cet exemple de tâche s’exécute immédiatement car `execTime` et `execSchedule` ont été omis.

**Demander**

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

Vous pouvez spécifier au moins l’un des `execTime` et `execSchedule`. Si aucun des deux n’est réussi, la tâche s’exécute immédiatement. Vous ne pouvez utiliser qu’un seul des types suivants :

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`
