---
description: Utilise getActiveJobs pour effectuer le suivi des téléchargements sur ordinateur.
solution: Experience Manager
title: UploadPostJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 60163016-fe96-4ac2-9208-da8192042d0f
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 5%

---

# [!DNL UploadPostJob]{#uploadpostjob}

Utilise getActiveJobs pour effectuer le suivi des téléchargements sur ordinateur.

Voir aussi [Téléchargement de ressources au moyen de HTTP POSTs vers le Télécharger...](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d).

>[!NOTE]
>
>Toutes POST demandes de tâche de téléchargement doivent provenir de la même adresse IP.

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
   <td colname="col1"> <span class="codeph"><span class="varname"> AutoColorCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :AutoColorCropOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options de recadrage automatique des images en fonction de la couleur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de sous-groupes :AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Tableau de scripts de génération automatique d’ensembles à appliquer aux fichiers téléchargés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> AutoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Supprime l’espace blanc des bords des images en fonction de la transparence. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Options</span> de gestion des couleurs </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options que vous pouvez spécifier lors d’un téléchargement. L’ensemble affecte la manière dont la couleur est gérée pour le téléchargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Créer un masque</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :booléen</span> </td> 
   <td colname="col3"> <p><b>Oui</b> </p> </td> 
   <td colname="col4"> <p>S’il faut créer un masque. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Définition du</span> courriel </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p><b>Oui</b> </p> </td> 
   <td colname="col4"> <p>Choix des paramètres d’email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :InDesignOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options de téléchargement des fichiers InDesign vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Options Illustrator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :IllustratorOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options de téléchargement des fichiers Illustrator sur le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Arrière-plan masqué</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Masquer l’arrière-plan des images sélectionnées. Cela vous permet de les superposer dans d’autres calques avec une transparence en dehors de l’image du sujet. Facultatif. </p> <p>Voir<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ManualCropOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options de recadrage manuel d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :MediaOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options qui vous permettent de définir une miniature de la vidéo. </p> <p>Voir <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> écraser</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :booléen</span> </td> 
   <td colname="col3"> <p>Oui</p> </td> 
   <td colname="col4"> <p>Faut-il écraser les fichiers lors du téléchargement ? </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Options</span> pdf </span> </td> 
   <td colname="col2"> <span class="codeph"> types : PDFOptions</span> </td> 
   <td colname="col3"> <p>Non</p> </td> 
   <td colname="col4"> <p>Options de téléchargement des fichiers PDF vers le serveur Image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Options</span> photoshop </span> </td> 
   <td colname="col2"> <span class="codeph"> types :PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options de téléchargement des fichiers Photoshop vers le serveur Image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>URL où les fichiers sont chargés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :PostScriptOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options de téléchargement des fichiers de script Post vers le serveur Image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> PreserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :booléen</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Contrôle la préservation de toute définition de culture existante. Vrai par défaut.</p> <p>Si vous fournissez le paramètre manualCropOptions et les valeurs correspondantes, les nouvelles valeurs (à l’exclusion de 0,0,0,0) sont appliquées à la ressource quelle que soit la valeur preserveCrop.</p><p>Si vous ne <i>fournissez pas</i> le paramètre manualCropOptions, la valeur de preserveCrop est conservée. Et, si la valeur est true, les valeurs preserveCrop existantes sont conservées ; en cas de valeur false, les valeurs preserveCrop sont supprimées.</p><p>Par exemple :</p><p><p>&lt;preserveCrop&gt;faux&lt;/preserveCrop&gt;<br />&lt;manualCropOptions&gt;<br />   &lt;left&gt;190&lt;/left&gt;<br />   &lt;right&gt;310&lt;/right&gt;<br />   &lt;top&gt;160&lt;/top&gt;<br />   &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualCropOptions&gt;</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :booléen</span> </td> 
   <td colname="col3"> <p><b>Oui</b> </p> </td> 
   <td colname="col4"> <p>Contrôle si l’état de publication d’une ressource existante est conservé lors de l’écrasement. S’il n’est pas défini, le paramètre par défaut de l’entreprise est utilisé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> ProjectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :HandleArray</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Tableau des descripteurs de projet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>Oui</b> </p> </td> 
   <td colname="col4"> <p>Si les fichiers sont marqués comme prêts pour publication. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :UnCompressOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Extract et traiter le contenu des fichiers TAR/ZIP transférés avec ces paramètres facultatifs. </p> <p>Voir <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Options</span> de masquage flou </span> </td> 
   <td colname="col2"> <span class="codeph"> types :UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options qui vous permettent de contrôler les paramètres de masquage flou lors de la création d’un fichier TIF pyramidal optimisé. Utilisez ces paramètres pour améliorer la netteté de l’image. </p> <p>Voir <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> Options de masquage</a> flou. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> Mots-clés xmp.</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Une option de métadonnées supplémentaire pour tout ce qui concerne la tâche de chargement. </p> </td> 
  </tr> 
 </tbody> 
</table>
