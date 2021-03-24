---
description: Utilise getActiveJobs pour effectuer le suivi des téléchargements de bureau.
solution: Experience Manager
title: TéléchargerPostJob
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 10%

---


# UploadPostJob{#uploadpostjob}

Utilise getActiveJobs pour effectuer le suivi des téléchargements de bureau.

Voir aussi [Téléchargement de fichiers au moyen de POST HTTP vers le téléchargement...](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d).

>[!NOTE]
>
>Toutes les demandes de POST pour une tâche de téléchargement doivent provenir de la même adresse IP.

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nom </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatoire? </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:AutoColorCropOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options de recadrage automatique des images en fonction de la couleur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Tableau de scripts de génération automatique de visionneuses à appliquer aux fichiers téléchargés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Supprime l’espace blanc des bords des images en fonction de la transparence. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options que vous pouvez spécifier lors d’un téléchargement. La visionneuse affecte la façon dont la couleur est gérée pour le téléchargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>Oui</b> </p> </td> 
   <td colname="col4"> <p>Indique s’il faut créer un masque. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p><b>Oui</b> </p> </td> 
   <td colname="col4"> <p>Choix des paramètres de courrier électronique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:InDesignOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options de téléchargement des fichiers d’InDesign sur le serveur Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:IllustratorOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options de téléchargement des fichiers Illustrator vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Masque l’arrière-plan des images sélectionnées. Vous pouvez ainsi les superposer dans d’autres calques avec une transparence en dehors de l’image objet. Facultatif. </p> <p>Voir <a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:ManualCropOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options de recadrage manuel des images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:MediaOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options qui vous permettent de définir une image miniature à partir de la vidéo. </p> <p>Voir <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> remplacer</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Oui</p> </td> 
   <td colname="col4"> <p>Indique s’il faut remplacer des fichiers lors du téléchargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:options PDFO</span> </td> 
   <td colname="col3"> <p>Non</p> </td> 
   <td colname="col4"> <p>Options de téléchargement de fichiers PDF vers le serveur Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options de téléchargement de fichiers Photoshop vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>URL de téléchargement des fichiers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:PostScriptOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options de téléchargement de fichiers PostScript vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Contrôle la préservation de toute définition de culture existante. Vrai par défaut.</p> <p>Si vous fournissez le paramètre manualCropOptions et les valeurs correspondantes, les nouvelles valeurs (à l’exclusion de 0,0,0,0) sont appliquées à la ressource, quelle que soit la valeur preserveCrop.</p><p>Si <i>ne fournit pas</i> le paramètre manualCropOptions, la valeur de preserveCrop est conservée. Et, dans le cas de true, les valeurs preserveCrop existantes sont conservées ; en cas de false, les valeurs preserveCrop sont supprimées.</p><p>Par exemple :</p><p><p>&lt;preservecrop&gt;false&lt;/preservecrop&gt;<br />&lt;manualcropoptions&gt;<br />    &lt;left&gt;190&lt;/left&gt;<br />    &lt;right&gt;310&lt;/right&gt;<br />    &lt;top&gt;160&lt;/top&gt;<br />    &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualcropoptions&gt;</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>Oui</b> </p> </td> 
   <td colname="col4"> <p>Contrôle si l’état de publication d’un fichier existant est conservé lors du remplacement. Si elle n’est pas définie, le paramètre par défaut de la société est utilisé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Tableau de gestionnaires de projet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>Oui</b> </p> </td> 
   <td colname="col4"> <p>Indique si les fichiers sont marqués comme prêts pour la publication. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:OptionsUnCompresser</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Extrayez et traitez le contenu des fichiers TAR/ZIP téléchargés avec ces paramètres facultatifs. </p> <p>Voir <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options permettant de contrôler les paramètres de masquage flou lors de la création d’un fichier TIF pyramidal optimisé. Utilisez ces paramètres pour améliorer la netteté de l’image. </p> <p>Voir <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Une option de métadonnées supplémentaire pour tout ce qui se trouve dans la tâche de téléchargement. </p> </td> 
  </tr> 
 </tbody> 
</table>

