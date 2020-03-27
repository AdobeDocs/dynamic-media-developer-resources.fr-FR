---
description: type de tâche pour permettre le retraitement des fichiers originaux précédemment téléchargés, y compris la réimpression des fichiers PDF et la réoptimisation des images.
seo-description: type de tâche pour permettre le retraitement des fichiers originaux précédemment téléchargés, y compris la réimpression des fichiers PDF et la réoptimisation des images.
seo-title: ReprocessAssetsJob
solution: Experience Manager
title: ReprocessAssetsJob
topic: Scene7 Image Production System API
uuid: 5b4aa838-0fb4-4ae8-be5a-8ce1e1487127
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# ReprocessAssetsJob{#reprocessassetsjob}

type de tâche pour permettre le retraitement des fichiers originaux précédemment téléchargés, y compris la réimpression des fichiers PDF et la réoptimisation des images.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nom </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> type:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Poignée de ressource. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> readyForPublish</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Si les fichiers sont marqués comme prêts pour la publication. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preservePublishState</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Contrôle si l’état de publication d’un fichier existant est conservé lors du remplacement. Si elle n’est pas définie, le paramètre par défaut du  est utilisé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Indique s’il faut créer un masque. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preserveCrop</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3">Contrôle la préservation de toute définition de culture existante. La valeur par défaut est <span class="codeph"> true</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manuelCropOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> type:ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de recadrage manuel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> type:AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de recadrage automatique des images en fonction de la couleur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> type:AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Supprime l’espace blanc des bords des images en fonction de la transparence. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> photoshopOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> type:PhotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers Photoshop vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> type:PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de téléchargement de fichiers PostScript vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:PDFOoptions</span> </p> </td> 
   <td colname="col3"> <p>Options de téléchargement de fichiers PDF vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> mediaOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> type:MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de fichier multimédia A/V. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> type:IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers Illustrator vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> type:ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>Options que vous pouvez spécifier lors d’un téléchargement. Le jeu affecte la manière dont la couleur est gérée pour le téléchargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoSetCreationOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> type:AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>Tableau de scripts de génération automatique d’ensembles à appliquer aux fichiers téléchargés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projetHandleArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> type:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Tableau de gestionnaires de projet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> paramètre</span> de courrier électronique </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Options des paramètres de courrier électronique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Indique s’il faut télécharger uniquement des fichiers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>URL vers l’emplacement de téléchargement du fichier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> type:ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Détails de la tâche pour une tâche de publication de diffusion d’images à exécuter une fois le téléchargement terminé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> type:ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Détails de la tâche pour une tâche de publication de rendu d’image à exécuter une fois le transfert terminé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> type:VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Détails de la tâche pour une tâche de publication vidéo à exécuter une fois le téléchargement terminé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> type:InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers InDesign vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> masquageArrière-plan</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> type:KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>Masque l’arrière-plan des images sélectionnées. Vous pouvez ainsi les superposer dans d’autres calques avec une transparence en dehors de l’image du sujet. </p> <p>Facultatif. </p> <p>Voir<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> unsharpMaskOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> type:UnsharpMaskOptions</span> </p> </td> 
   <td colname="col3"> <p>Options permettant de contrôler les paramètres de masquage flou lors de la création d’un fichier TIF de pyramide optimisé. Utilisez ces paramètres pour améliorer la netteté de l’image. </p> <p>Voir <a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_unsharp_mask_options.html"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Remarques**

Les choix `*CropOptions` incluent :

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Les choix `*PublishJob` incluent :

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`

