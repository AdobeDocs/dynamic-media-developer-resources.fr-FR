---
description: Charge les URL depuis l'emplacement où tu veux récupérer les fichiers.
solution: Experience Manager
title: UploadUrlsJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 28bca473-670f-4588-93fb-a6d6a692ce30
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 1%

---

# [!DNL UploadUrlsJob]{#uploadurlsjob}

Charge les URL depuis l&#39;emplacement où tu veux récupérer les fichiers.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> d’options : AutoColorCropOptions</span> </td> 
   <td colname="col3"> Options de recadrage automatique des images en fonction de la couleur. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de sous-domaines:AutoSetCreationOptions</span> </td> 
   <td colname="col3"> Tableau de scripts de génération de jeux automatiques à appliquer aux fichiers chargés. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de sous-domaines:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> Supprime l’espace blanc sur les bords des images en fonction de la transparence. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Permet de créer un masque. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> d’options :ColorManagementOptions</span> </td> 
   <td colname="col3"> Options que vous pouvez spécifier lors d’un chargement. Le jeu affecte la manière dont la couleur est gérée pour le chargement. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Choix des paramètres d’e-mail. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> d’images :IllustratorOptions</span> </td> 
   <td colname="col3"> Options de chargement des fichiers Illustrator sur le serveur d’images. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :InDesignOptions</span> </td> 
   <td colname="col3"> Options de chargement des fichiers InDesign sur le serveur. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :KnockoutBackgroundOptions</span> </td> 
   <td colname="col3">Masquez l’arrière-plan des images sélectionnées. Vous pouvez ainsi les superposer dans d’autres calques avec une transparence en dehors de l’image de l’objet. Facultatif. Voir <a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de sous-domaines:ManualCropOptions</span> </td> 
   <td colname="col3"> Options de recadrage manuel d’images. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :MediaOptions</span> </td> 
   <td colname="col3">Options permettant de définir une miniature de la vidéo. Voir <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numUrls</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3">Renvoie le nombre d’URL envoyées dans une tâche. Utilisé par <a href="../../operations/c-operations-intro/c-methods/r-get-active-jobs.md#reference-67483cbd71d04042b48434d886e8a7a0" format="dita" scope="local"> getActiveJobs</a> et <a href="../../operations/c-operations-intro/c-methods/r-get-scheduled-jobs.md#reference-2bab1861325f4bff84c879d1efa9146e" format="dita" scope="local"> getScheduledJobs</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> remplacer </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Permet de spécifier si les fichiers doivent être remplacés lors du chargement. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de sous-réseau :PDFOptions</span> </td> 
   <td colname="col3"> Options de chargement des fichiers PDF sur le serveur d’images. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de sous-réseau :PhotoshopOptions</span> </td> 
   <td colname="col3"> Options de chargement des fichiers Photoshop sur le serveur d’images. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> URL où les fichiers sont chargés. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> d’audience :ImageRendingPublishJob</span> </td> 
   <td colname="col3"> Détails d’une tâche de publication de rendu d’image qui s’exécute une fois le chargement terminé. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ImageServingPublishJob</span> </td> 
   <td colname="col3"> Toutes les options de média. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :PostScriptOptions</span> </td> 
   <td colname="col3"> Options de chargement de fichiers Post Script sur le serveur d’images. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :VideoPublishJob</span> </td> 
   <td colname="col3"> Informations détaillées sur une tâche de publication de vidéo qui s’exécute une fois le chargement terminé. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Contrôle la conservation de toute définition de culture existante. La valeur par défaut est « true » </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Contrôle si l’état de publication d’une ressource existante est conservé lors du remplacement. S’il n’est pas défini, le paramètre par défaut de la société est utilisé. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3"> Tableau des descripteurs de projet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Indique si les fichiers sont marqués comme prêts à être publiés. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :UnCompressOptions</span> </td> 
   <td colname="col3">Extrayez et traitez le contenu des fichiers TAR/ZIP chargés avec ces paramètres facultatifs. Voir <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> d’options de compression</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de sous-réseau:UnsharpMaskOptions</span> </td> 
   <td colname="col3">Options permettant de contrôler les paramètres de masquage flou lors de la création d’un fichier TIF pyramide optimisé. Utilisez ces paramètres pour améliorer la netteté de l’image. Voir <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> urlArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:UrlArray</span> </td> 
   <td colname="col3"> Tableau d’URL à charger. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmpKeywords </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Une option de métadonnées supplémentaire pour tout ce qui concerne la tâche de chargement. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Remarques {#section-637405ff7e0b4a71b83fd359b92fa0c2}

Par `CropOptions`, vous ne pouvez choisir que l’une des options suivantes :

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Par `PublishJob`, vous ne pouvez choisir que l’une des options suivantes :

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`
