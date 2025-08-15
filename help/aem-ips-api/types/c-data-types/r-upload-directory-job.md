---
description: Télécharge des fichiers à partir de répertoires de serveur spécifiés de façon récurrente.
solution: Experience Manager
title: Tâche d’annuaire de téléchargement
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a23f1bc2-aa6a-4c1d-aab5-7f6dbd08682c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 1%

---

# [!DNL UploadDirectoryJob]{#uploaddirectoryjob}

Télécharge des fichiers à partir de répertoires de serveur spécifiés de façon récurrente.

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
   <td colname="col1"> <span class="codeph"><span class="varname"> Options</span> de couleur automatique </span> </td> 
   <td colname="col2"> <span class="codeph"> types :AutoColorOptions</span> </td> 
   <td colname="col3"> <p>Options de recadrage automatique de l’image (en fonction de la couleur). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Options</span> de création automatique </span> </td> 
   <td colname="col2"> <span class="codeph"> types :AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>Tableau de scripts de génération automatique d’ensembles à appliquer aux fichiers téléchargés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> AutoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>Supprime l’espace blanc des bords des images en fonction de la transparence. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Options</span> de gestion des couleurs </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>Options que vous pouvez spécifier lors d’un téléchargement. L’ensemble affecte la manière dont la couleur est gérée pour le téléchargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Créer un masque</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :booléen</span> </td> 
   <td colname="col3"> <p>S’il convient de créer un masque lors du téléchargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Dossier destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>Dossier IPS pour les fichiers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Définition du</span> courriel </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>Choix des paramètres d’email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Options</span> illustrator </span> </td> 
   <td colname="col2"> <span class="codeph"> types :IllustratorOptions</span> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers Illustrator vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Inclure les sous-dossiers</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>Inclure ou non des sous-dossiers lors du téléchargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :InDesignOptions</span> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers InDesign vers le serveur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Arrière-plan masqué</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>Masquer l’arrière-plan des images sélectionnées. Cela vous permet de les superposer dans d’autres calques avec une transparence en dehors de l’image du sujet. </p> <p>Facultatif. </p> <p>Voir <a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ManualCropOptions</span> </td> 
   <td colname="col3"> <p>Options de recadrage manuel de l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Options</span> médias </span> </td> 
   <td colname="col2"> <span class="codeph"> types :MediaOptions</span> </td> 
   <td colname="col3"> <p>Options qui vous permettent de définir une miniature de la vidéo. </p> <p>Voir <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> écraser</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>Options de remplacement du téléchargement de fichier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Options</span> pdf </span> </td> 
   <td colname="col2"> <span class="codeph"> types : PDFOptions</span> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers PDF vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Options</span> photoshop </span> </td> 
   <td colname="col2"> <span class="codeph"> types :PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers Photoshop vers le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>URL de la destination du téléchargement du fichier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> postImageRenderingPublish</span> </span>Travail </td> 
   <td colname="col2"> <span class="codeph"> types :ImageRendingPublishJob</span> </td> 
   <td colname="col3"> <p>Détails d’une tâche de publication de rendu d’image qui s’exécute une fois le téléchargement terminé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> PostImageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ImageServingPublishJob</span> </td> 
   <td colname="col3"> <p>Informations sur une tâche de publication Image Server qui s’exécute une fois le téléchargement terminé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Fichiers postJobOnlyIfFiles</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :booléen</span> </td> 
   <td colname="col3"> <p>Faut-il télécharger uniquement des fichiers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Options</span> postScript </span> </td> 
   <td colname="col2"> <span class="codeph"> types :PostScriptOptions</span> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers de script Post sur le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> PostVideoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :VideoPublishJob</span> </td> 
   <td colname="col3"> <p>Détails d’une tâche de publication vidéo qui s’exécute une fois le téléchargement terminé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> PreserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :booléen</span> </td> 
   <td colname="col3"> <p>Contrôle la préservation de toute définition de culture existante. La valeur par défaut est « true ». </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :booléen</span> </td> 
   <td colname="col3"> <p>Contrôle si l’état de publication d’une ressource existante est conservé lors de l’écrasement. S’il n’est pas défini, le paramètre par défaut de l’entreprise est utilisé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Fichiers de métadonnées</span> de processus </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>S’il est nécessaire de traiter des fichiers XML de métadonnées distincts pour cette tâche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> ProjectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :HandleArray</span> </td> 
   <td colname="col3"> <p>Tableau de descripteurs de projet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Prêt pour la publication</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :booléen</span> </td> 
   <td colname="col3"> <p>Détermine si les fichiers sont marqués comme prêts pour publication. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> serverDir</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> <p>Répertoire de chargement source. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :UnCompressOptions</span> </td> 
   <td colname="col3"> <p>Extract et traiter le contenu des fichiers TAR/ZIP transférés avec ces paramètres facultatifs. </p> <p>Voir <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Options</span> de masquage flou </span> </td> 
   <td colname="col2"> <span class="codeph"> types :UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>Options qui vous permettent de contrôler les paramètres de masquage flou lors de la création d’un fichier TIF pyramidal optimisé. Utilisez ces paramètres pour améliorer la netteté de l’image. </p> <p>Voir <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> Options de masquage</a> flou. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Mots-clés xmp.</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd :chaîne</span> </p> </td> 
   <td colname="col3"> <p>Une option de métadonnées supplémentaire pour l’ensemble des éléments de la tâche de téléchargement </p> </td> 
  </tr> 
 </tbody> 
</table>

## Remarques {#section-637405ff7e0b4a71b83fd359b92fa0c2}

Pour `CropOptions`, vous ne pouvez choisir qu’une seule des options suivantes :

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Pour `PublishJob`, vous ne pouvez choisir qu’une seule des options suivantes :

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`
