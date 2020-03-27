---
description: Télécharge régulièrement des fichiers à partir de répertoires de serveur spécifiés.
seo-description: Télécharge régulièrement des fichiers à partir de répertoires de serveur spécifiés.
seo-title: UploadDirectoryJob
solution: Experience Manager
title: UploadDirectoryJob
topic: Scene7 Image Production System API
uuid: 6e6ae415-7c54-4bbb-aa98-ff9a77d956b0
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# UploadDirectoryJob{#uploaddirectoryjob}

Télécharge régulièrement des fichiers à partir de répertoires de serveur spécifiés.

Syntaxe

## Paramètres {#section-69c07f4e7b2e4a0fba143ffaa9f4d48f}

<table id="table_6E40A78846F444BDB8E437413B90CFCE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nom </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:AutoColorOptions</span> </td> 
   <td colname="col3"> <p>Options de recadrage automatique des images (en fonction de la couleur). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>Tableau de scripts de génération automatique d’ensembles à appliquer aux fichiers téléchargés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>Supprime l’espace blanc des bords des images en fonction de la transparence. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>Options que vous pouvez spécifier lors d’un téléchargement. Le jeu affecte la manière dont la couleur est gérée pour le téléchargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Indique s’il faut créer un masque lors du téléchargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>dossier IPS pour les fichiers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> paramètre</span> de courrier électronique </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Choix des paramètres de courrier électronique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustratorOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:IllustratorOptions</span> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers Illustrator vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> incluredes sous-dossiers</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Inclure ou non des sous-dossiers lors du téléchargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:InDesignOptions</span> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers InDesign vers le serveur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> masquageArrière-plan</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>Masque l’arrière-plan des images sélectionnées. Vous pouvez ainsi les superposer dans d’autres calques avec une transparence en dehors de l’image du sujet. </p> <p>Facultatif. </p> <p>Voir <a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manuelCropOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:ManualCropOptions</span> </td> 
   <td colname="col3"> <p>Options de recadrage manuel des images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:MediaOptions</span> </td> 
   <td colname="col3"> <p>Options qui vous permettent de définir une image miniature à partir de la vidéo. </p> <p>Voir <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> Options</a>multimédia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> écraser</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Options de remplacement du téléchargement de fichier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:PDFOoptions</span> </td> 
   <td colname="col3"> <p>Options de téléchargement de fichiers PDF vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers Photoshop vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>URL de la destination du téléchargement du fichier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublish</span> </span>Job </td> 
   <td colname="col2"> <span class="codeph"> type:ImageRendingPublishJob</span> </td> 
   <td colname="col3"> <p>Détails d’une tâche de publication de rendu d’image qui s’exécute une fois le téléchargement terminé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageServingPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:ImageServingPublishJob</span> </td> 
   <td colname="col3"> <p>Détails d’une tâche de publication de diffusion d’images qui s’exécute une fois le téléchargement terminé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Indique s’il faut télécharger uniquement des fichiers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:PostScriptOptions</span> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers PostScript vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postVideoPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:VideoPublishJob</span> </td> 
   <td colname="col3"> <p>Détails d’une tâche de publication de vidéo qui s’exécute une fois le téléchargement terminé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Contrôle la préservation de toute définition de culture existante. La valeur par défaut est true. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Contrôle si l’état de publication d’un fichier existant est conservé lors du remplacement. Si elle n’est pas définie, le paramètre par défaut du  est utilisé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> processMetadataFiles</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Le traitement des fichiers XML de métadonnées distincts pour cette tâche doit-il être effectué ? </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projetHandleArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:HandleArray</span> </td> 
   <td colname="col3"> <p>Tableau de gestionnaires de projet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Détermine si les fichiers sont marqués comme prêts pour la publication. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDir</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Répertoire de téléchargement source. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:AnnulerCompresserOptions</span> </td> 
   <td colname="col3"> <p>Extrayez et traitez le contenu des fichiers TAR/ZIP téléchargés avec ces paramètres facultatifs. </p> <p>Voir <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> Annuler les options</a>de compression. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>Options permettant de contrôler les paramètres de masquage flou lors de la création d’un fichier TIF de pyramide optimisé. Utilisez ces paramètres pour améliorer la netteté de l’image. </p> <p>Voir <a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_unsharp_mask_options.html"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> xmpKeywords</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Une option de métadonnées supplémentaire pour tous les éléments de la tâche de téléchargement </p> </td> 
  </tr> 
 </tbody> 
</table>

## Remarques {#section-637405ff7e0b4a71b83fd359b92fa0c2}

Pour `CropOptions`cela, vous ne pouvez choisir que l’une des options suivantes :

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Pour `PublishJob`cela, vous ne pouvez choisir que l’une des options suivantes :

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`

