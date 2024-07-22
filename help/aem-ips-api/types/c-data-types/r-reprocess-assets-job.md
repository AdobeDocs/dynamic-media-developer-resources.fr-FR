---
description: Type de tâche pour permettre le retraitement des fichiers principaux précédemment chargés, y compris la réactualisation des PDF et la réoptimisation des images.
solution: Experience Manager
title: ReprocessAssetsJob
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b6078246-54e1-4119-b4f8-ba6a28577cff
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 2%

---

# [!DNL ReprocessAssetsJob]{#reprocessassetsjob}

Type de tâche pour permettre le retraitement des fichiers principaux précédemment chargés, y compris la réactualisation des PDF et la réoptimisation des images.

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Poignée de ressource. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> readyForPublish</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Si les fichiers sont marqués comme prêts pour la publication. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preservePublishState</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Contrôle si l’état de publication d’une ressource existante est conservé lors du remplacement. Si elle n’est pas définie, le paramètre par défaut de l’entreprise est utilisé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Créer ou non un masque. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preserveCrop</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Contrôle la conservation de toute définition de recadrage existante. Vrai par défaut.</p> <p>Si vous fournissez le paramètre manualCropOptions et les valeurs correspondantes, les nouvelles valeurs (à l’exception de 0,0,0,0) sont appliquées à la ressource, quelle que soit la valeur preserveCrop .</p><p>Si vous ne fournissez pas <i>not</i> le paramètre manualCropOptions, la valeur de preserveCrop est conservée. Et, en cas de valeur true, les valeurs preserveCrop existantes sont conservées ; en cas de valeur false, les valeurs preserveCrop sont supprimées.</p><p>Par exemple :</p><p><p>&lt;preserveCrop&gt;false&lt;/preserveCrop&gt;<br />&lt;manualCropOptions&gt;<br />   &lt;left&gt;190&lt;/left&gt;<br />   &lt;right&gt;310&lt;/right&gt;<br />   &lt;top&gt;160&lt;/top&gt;<br />   &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualCropOptions&gt;</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types : ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de recadrage manuel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de recadrage automatique des images en fonction de la couleur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Supprime l’espace blanc des bords des images, en fonction de la transparence. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types : PhotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers Photoshop vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers PostScript vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:PDFOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de téléchargement de fichiers de PDF vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> mediaOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types : MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de fichier multimédia A/V. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers Illustrator vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>Options que vous pouvez spécifier lors d’un téléchargement. La visionneuse affecte la manière dont la couleur est gérée pour le chargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>Tableau de scripts de génération automatique de visionneuses à appliquer aux fichiers chargés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Tableau de projets gérés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Options des paramètres de courrier électronique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Indique s’il faut charger uniquement des fichiers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>URL de l’emplacement de téléchargement du fichier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Détails de la tâche pour une tâche de publication de diffusion d’image à exécuter une fois le transfert terminé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Détails de la tâche pour une tâche de publication de rendu d’image à exécuter une fois le transfert terminé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Détails de la tâche pour une tâche de publication vidéo à exécuter une fois le transfert terminé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers d’InDesign vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> KnockoutBackground</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types : KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>Masquez l’arrière-plan des images sélectionnées. Vous pouvez ainsi les superposer dans d’autres calques avec une transparence en dehors de l’objet. </p> <p>Facultatif. </p> <p>Voir<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types : UnsharpMaskOptions</span> </p> </td> 
   <td colname="col3"> <p>Options permettant de contrôler les paramètres de masquage flou lors de la création d’un fichier TIF pyramid optimisé. Utilisez ces paramètres pour améliorer la netteté de l’image. </p> <p>Voir <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Notes**

Les choix pour `*CropOptions` incluent :

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Les choix pour `*PublishJob` incluent :

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`
