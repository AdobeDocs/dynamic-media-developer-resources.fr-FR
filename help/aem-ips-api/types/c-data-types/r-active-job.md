---
title: ActiveJob
description: Tâche exécutée sur un serveur. Il s’agit également d’une instance d’une tâche planifiée.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3d878207-99e4-4c75-ab12-b38a37c82fb7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 1%

---

# [!DNL ActiveJob]{#activejob}

Tâche exécutée sur un serveur. Il s’agit également d’une instance d’une tâche planifiée.

Il existe des emplois dans trois états :

* Planifié pour s’exécuter.
* En cours d’exécution.
* Exécution terminée (et avoir déjà écrit des informations dans un journal de travail).

Pour renvoyer le type de tâche, spécifiez une valeur de type de tâche. Vous pouvez renvoyer les tâches suivantes :

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublish`
* `JobUploadDirectoryJob`
* `uploadUrlsJob`

## Paramètres {#section-6590fe864a434000822b9ec384784512}

<table id="table_1C4DDAB4EB1341FDA92B6F14E0132F75"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> CompanyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Gérer vers la société. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Gérer jusqu’à la tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nom </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nom unique de la tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> originalName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Nom d’origine du type <span class="codeph"> ActiveJob</span> envoyé avec la tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Choix des types de tâches renvoyés par le système. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> état</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Choix des états de travail actifs renvoyés par le système. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> SubmitUserEmail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Adresse électronique de l’utilisateur qui a planifié la tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> paramètres régionaux</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3">Paramètres régionaux relatifs aux détails du journal des tâches et à la localisation des adresses électroniques. <p>Spécifiez les paramètres régionaux comme <span class="codeph"> &lt;code_langue&gt;[-&lt;code_pays&gt;]</span>, où le code de langue est un code à deux lettres en minuscules spécifié par la norme ISO-639 et le code de pays facultatif est un code à deux lettres en majuscules spécifié par la norme ISO-3166. Par exemple, la chaîne de paramètres régionaux pour l’anglais (États-Unis) serait : <span class="codeph"> en-US</span>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> description </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Description de la tâche initialement spécifiée dans <span class="codeph"> submitJob</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverName </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Nom du serveur exécutant le traitement. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> startDate </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Date, heure et fuseau horaire du traitement actif. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> totalSize </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Taille totale de la tâche active. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> progrès</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :int</span> </td> 
   <td colname="col3"> Progression de la tâche (c’est-à-dire à quel point la tâche est proche de la fin). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Message texte décrivant la progression de la tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Date, heure et fuseau horaire de la dernière mise à jour de la progression. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> taskProgressArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de tâches :TaskProgressArray</span> </td> 
   <td colname="col3"> Informations sur la progression d'une tâche asynchrone. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ImageServingPublishJob</span> </td> 
   <td colname="col3"> Détails de la tâche d’une tâche de publication Image Server. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Image ServingRenderJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ImageServingRenderJob</span> </td> 
   <td colname="col3"> Détails de la tâche de publication de rendu d’images. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Tâche</span> de publication vidéo </span> </td> 
   <td colname="col2"> <span class="codeph"> types :VideoPublishJob</span> </td> 
   <td colname="col3"> Détails de la tâche pour une tâche de publication vidéo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ImageServingPublishJob</span> </td> 
   <td colname="col3"> Détails d’une tâche de publication d’annuaire de serveur. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de sous-réseau :UploadUrlsJob</span> </td> 
   <td colname="col3"> Détails d’une tâche de chargement d’URL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span> </span> </td> 
   <td colname="col2"> Types de <span class="codeph"> : RipPdfsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizerImagesJob</span> </span> </td> 
   <td colname="col2"> types de <span class="codeph"> :OptimizeImagesJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Tâche</span> de retraitement des ressources </span> </td> 
   <td colname="col2"> <span class="codeph"> de sous-dossiers :ReprocessAssetsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadPostJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de rapports :UploadPostJob</span> </td> 
   <td colname="col3"> Détails du traitement, suivi du chargement du bureau. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Traitement d’exportation</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ExportJob</span> </td> 
   <td colname="col3">Autoriser l’exportation autorisée des fichiers précédemment téléchargés. Voir <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-exportjob.html" format="http" scope="external"> Tâche</a> d’exportation. </td> 
  </tr> 
 </tbody> 
</table>
