---
description: Tâche exécutée sur un serveur. Il s’agit également d’une instance d’une tâche planifiée.
seo-description: Tâche exécutée sur un serveur. Il s’agit également d’une instance d’une tâche planifiée.
seo-title: ActiveJob
solution: Experience Manager
title: ActiveJob
topic: Scene7 Image Production System API
uuid: d7120a88-6f3e-4844-aafa-83d419470fad
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# ActiveJob{#activejob}

Tâche exécutée sur un serveur. Il s’agit également d’une instance d’une tâche planifiée.

Il existe des tâches dans 3 états :

* Programmé pour exécution.
* En cours d’exécution.
* Exécution terminée (et avoir déjà écrit des informations dans un journal de tâches).

Spécifiez une valeur de type de tâche pour renvoyer le type de tâche. Vous pouvez renvoyer les tâches suivantes :

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> sociétéHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Pose le . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tâcheHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Traitement de la tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nom</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nom unique de la tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> originalName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Nom d’origine du type <span class="codeph"> ActiveJob</span> envoyé avec la tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Choix des types de tâche renvoyés par le système. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> state</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Choix des états actifs renvoyés par le système. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> adresse électronique de l’utilisateur qui a planifié la tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Paramètres régionaux des détails du journal des tâches et des  de messagerie électronique. <p>Spécifiez les paramètres régionaux comme <span class="codeph"> &lt;code_langue&gt;[-&lt;code_pays&gt;]</span>, où le code de langue est un code à deux lettres en minuscules, comme spécifié par ISO-639, et le code de pays facultatif est un code à deux lettres en majuscules, comme spécifié par ISO-3166. Par exemple, la chaîne de paramètres régionaux pour l’anglais (Etats-Unis) serait : <span class="codeph"> en-US</span>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> description</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Description de la tâche initialement spécifiée dans <span class="codeph"> submitJob</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nom du serveur exécutant la tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> startDate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Date, heure et fuseau horaire de la tâche active. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> totalSize</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Taille totale de la tâche active. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progression</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Progression de la tâche (c.-à-d. la distance entre la tâche et l’achèvement). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Message texte décrivant la progression de la tâche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Date, heure et fuseau horaire de la dernière mise à jour de progression. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tâcheProgressArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:TaskProgressArray</span> </td> 
   <td colname="col3"> asynchrone  des informations de progression. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ImageServingPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Détails de la tâche pour une tâche de publication de diffusion d’images. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingRenderJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:ImageServingRenderJob</span> </td> 
   <td colname="col3"> Détails de la tâche d’une tâche de publication de rendu d’image. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> Tâche <span class="varname"> de publication</span> vidéo </span> </td> 
   <td colname="col2"> <span class="codeph"> type:VideoPublishJob</span> </td> 
   <td colname="col3"> Détails de la tâche pour une tâche de publication vidéo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Détails de la tâche pour une tâche de publication dans le répertoire du serveur. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:UploadUrlsJob</span> </td> 
   <td colname="col3"> Détails de la tâche pour une tâche d’URL de téléchargement. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:RipPdfsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:OptimizeImagesJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:ReprocessAssetsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadPostJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:UploadPostJob</span> </td> 
   <td colname="col3"> Suivi des détails de la tâche lors du téléchargement sur le bureau. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:ExportJob</span> </td> 
   <td colname="col3">Autoriser l’exportation autorisée de fichiers précédemment téléchargés. Voir <a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exportjob.html" format="http" scope="external"> Exportation de tâche</a>. </td> 
  </tr> 
 </tbody> 
</table>

