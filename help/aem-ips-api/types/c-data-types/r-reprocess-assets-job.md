---
description: Type de tâche pour permettre le retraitement des fichiers primaires précédemment téléchargés, y compris l’extraction de fichiers PDF et la ré-optimisation des images.
solution: Experience Manager
title: Tâche de retraitement des ressources
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b6078246-54e1-4119-b4f8-ba6a28577cff
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 2%

---

# [!DNL ReprocessAssetsJob]{#reprocessassetsjob}

Type de tâche pour permettre le retraitement des fichiers primaires précédemment téléchargés, y compris l’extraction de fichiers PDF et la ré-optimisation des images.

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
   <td colname="col1"> <p><span class="codeph"><span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Gestion des ressources. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Prêt pour la publication</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd :booléen</span> </p> </td> 
   <td colname="col3"> <p>Si les fichiers sont marqués comme prêts pour publication. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> preservePublishState</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd :booléen</span> </p> </td> 
   <td colname="col3"> <p>Contrôle si l’état de publication d’une ressource existante est conservé lors de l’écrasement. S’il n’est pas défini, le paramètre par défaut de l’entreprise est utilisé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Créer un masque</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd :booléen</span> </p> </td> 
   <td colname="col3"> <p>S’il faut créer un masque. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> PreserveCrop</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd :booléen</span> </p> </td> 
   <td colname="col3"> <p>Contrôle la préservation de toute définition de culture existante. Vrai par défaut.</p> <p>Si vous fournissez le paramètre manualCropOptions et les valeurs correspondantes, les nouvelles valeurs (à l’exclusion de 0,0,0,0) sont appliquées à la ressource quelle que soit la valeur preserveCrop.</p><p>Si vous ne <i>fournissez pas</i> le paramètre manualCropOptions, la valeur de preserveCrop est conservée. Et, si la valeur est true, les valeurs preserveCrop existantes sont conservées ; en cas de valeur false, les valeurs preserveCrop sont supprimées.</p><p>Par exemple :</p><p><p>&lt;preserveCrop&gt;faux&lt;/preserveCrop&gt;<br />&lt;manualCropOptions&gt;<br />   &lt;left&gt;190&lt;/left&gt;<br />   &lt;right&gt;310&lt;/right&gt;<br />   &lt;top&gt;160&lt;/top&gt;<br />   &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualCropOptions&gt;</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de recadrage manuel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> AutoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de recadrage automatique des images en fonction des couleurs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> AutoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Supprime l’espace blanc des bords des images en fonction de la transparence. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Options</span> photoshop </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :PhotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers Photoshop vers le serveur Image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Options</span> postScript </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers PostScript vers le serveur Image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Options</span> pdf </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types : PDFOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers PDF vers le serveur Image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Options</span> médias </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de fichier multimédia A/V. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Options</span> illustrator </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers Illustrator sur le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Options</span> de gestion des couleurs </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>Options que vous pouvez spécifier lors d’un téléchargement. L’ensemble affecte la manière dont la couleur est gérée pour le téléchargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Options</span> de création automatique </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>Tableau de scripts de génération automatique d’ensembles à appliquer aux fichiers téléchargés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> ProjectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Tableau de poignées de projet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Définition du</span> courriel </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd :chaîne</span> </p> </td> 
   <td colname="col3"> <p>Options des paramètres de courrier électronique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Fichiers postJobOnlyIfFiles</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd :booléen</span> </p> </td> 
   <td colname="col3"> <p>Faut-il télécharger uniquement des fichiers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd :chaîne</span> </p> </td> 
   <td colname="col3"> <p>URL vers l’emplacement de téléchargement du fichier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> PostImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Détails de la tâche pour une tâche de publication Image Server à exécuter une fois le téléchargement terminé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> PostImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Détails de la tâche pour la tâche de publication de rendu d’image à exécuter après la fin du téléchargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> PostVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Détails de la tâche de publication de vidéo à exécuter une fois le téléchargement terminé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers InDesign sur le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Arrière-plan masqué</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>Masquer l’arrière-plan des images sélectionnées. Cela vous permet de les superposer dans d’autres calques avec une transparence en dehors de l’image du sujet. </p> <p>Facultatif. </p> <p>Voir<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Options</span> de masquage flou </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :UnsharpMaskOptions</span> </p> </td> 
   <td colname="col3"> <p>Options qui vous permettent de contrôler les paramètres de masquage flou lors de la création d’un fichier TIF pyramidal optimisé. Utilisez ces paramètres pour améliorer la netteté de l’image. </p> <p>Voir <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> Options de masquage</a> flou. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Notes**

Choix pour `*CropOptions` inclure :

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Choix pour `*PublishJob` inclure :

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`
