---
description: Utilise getActiveJobs pour suivre les téléchargements de bureau.
solution: Experience Manager
title: UploadPostJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 60163016-fe96-4ac2-9208-da8192042d0f
TQID: 'https://experienceleague.adobe.com/HyBhZzT6yi-kgeyJmPZT4clh4FrdwhYqGCo1uZv1riI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 447
ht-degree: 6%

---

# [!DNL UploadPostJob]{#uploadpostjob}

Utilise getActiveJobs pour suivre les téléchargements de bureau.

Consultez également la section [Chargement de ressources au moyen de POST HTTP dans le fichier Charger...](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d).

>[!NOTE]
>
>Toutes les requêtes POST pour une tâche de chargement doivent provenir de la même adresse IP.

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nom </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatoire ? </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> d’options : AutoColorCropOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options de recadrage automatique des images en fonction de la couleur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de sous-groupes :AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Tableau de scripts de génération de jeux automatiques à appliquer aux fichiers chargés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de sous-domaines:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Supprime l’espace blanc sur les bords des images en fonction de la transparence. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> d’options :ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options que vous pouvez spécifier lors d’un chargement. Le jeu affecte la manière dont la couleur est gérée pour le chargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>Oui</b> </p> </td> 
   <td colname="col4"> <p>Permet de créer un masque. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p><b>Oui</b> </p> </td> 
   <td colname="col4"> <p>Choix des paramètres d’e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :InDesignOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options de chargement des fichiers InDesign sur le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> d’images :IllustratorOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options de chargement des fichiers Illustrator sur le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Masquez l’arrière-plan des images sélectionnées. Vous pouvez ainsi les superposer dans d’autres calques avec une transparence en dehors de l’image de l’objet. Facultatif. </p> <p>Voir <a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de sous-domaines:ManualCropOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options de recadrage manuel d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :MediaOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options permettant de définir une miniature de la vidéo. </p> <p>Voir <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> remplacer </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Oui</p> </td> 
   <td colname="col4"> <p>Permet de spécifier si les fichiers doivent être remplacés lors du chargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de sous-réseau :PDFOptions</span> </td> 
   <td colname="col3"> <p>Non</p> </td> 
   <td colname="col4"> <p>Options de chargement des fichiers PDF sur le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de sous-réseau :PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options de chargement des fichiers Photoshop sur le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>URL où les fichiers sont chargés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :PostScriptOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options de chargement de fichiers Post Script sur le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Contrôle la conservation de toute définition de culture existante. Vrai par défaut.</p> <p>Si vous fournissez le paramètre manualCropOptions et les valeurs correspondantes, les nouvelles valeurs (à l’exception de 0,0,0,0) sont appliquées à l’actif, quelle que soit la valeur preserveCrop.</p><p>Si vous ne fournissez <i>pas</i> le paramètre manualCropOptions, la valeur de preserveCrop est conservée. Si la valeur est true, les valeurs preserveCrop existantes sont conservées ; si la valeur est false, les valeurs preserveCrop sont supprimées.</p><p>Par exemple :</p><p><p>&lt;preserveCrop&gt;false&lt;/preserveCrop&gt;<br />&lt;manualCropOptions&gt;<br /> &lt;left&gt;190&lt;/left&gt;<br /> &lt;right&gt;310&lt;/right&gt;<br /> &lt;top&gt;160&lt;/top&gt;<br /> &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualCropOptions&gt;</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>Oui</b> </p> </td> 
   <td colname="col4"> <p>Contrôle si l’état de publication d’une ressource existante est conservé lors du remplacement. S’il n’est pas défini, le paramètre par défaut de la société est utilisé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Tableau des descripteurs de projet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>Oui</b> </p> </td> 
   <td colname="col4"> <p>Indique si les fichiers sont marqués comme prêts à être publiés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :UnCompressOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Extrayez et traitez le contenu des fichiers TAR/ZIP chargés avec ces paramètres facultatifs. </p> <p>Voir <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> d’options de compression</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de sous-réseau:UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Options permettant de contrôler les paramètres de masquage flou lors de la création d’un fichier TIF pyramide optimisé. Utilisez ces paramètres pour améliorer la netteté de l’image. </p> <p>Voir <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Une option de métadonnées supplémentaire pour tout ce qui concerne la tâche de chargement. </p> </td> 
  </tr> 
 </tbody> 
</table>

