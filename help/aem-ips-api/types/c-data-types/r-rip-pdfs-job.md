---
title: RipPdfsJob
description: Processus d’extraction d’un fichier PDF existant.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7a787b45-3cda-44f2-8357-8b6217b679e0
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---

# [!DNL RipPdfsJob]{#rippdfsjob}

Processus d’extraction d’un fichier PDF existant.

>[!NOTE]
>
>Ce type de tâche est obsolète. Transition vers `ReprocessAssetsJob` pour toutes les intégrations futures.

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
   <td colname="col1"> <p><span class="codeph"><span class="varname"> HandleArray pdfHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Gérez la table des fichiers PDF à extraire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Créer un masque</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd :booléen</span> </p> </td> 
   <td colname="col3"> <p>Détermine si vous voulez créer un masque ou non. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de recadrage manuel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> AutoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de recadrage automatique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> AutoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :PostTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Options</span> postScript </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Options</span> pdf </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types : PDFOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Options</span> illustrator </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Options</span> de gestion des couleurs </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> ProjectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Tableau de poignées de projet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Définition du</span> courriel </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd :chaîne</span> </p> </td> 
   <td colname="col3"> <p>Paramètres de courrier électronique </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd :chaîne</span> </p> </td> 
   <td colname="col3"> <p>L’URL vers laquelle les fichiers sont téléchargés. </p> </td> 
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
   <td colname="col3"> <p>Détails de la tâche de publication vidéo à exécuter une fois le téléchargement terminé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de téléchargement des fichiers Adobe InDesign sur le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Arrière-plan masqué</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>Masquer l’arrière-plan des images sélectionnées. Cette capacité vous permet de les superposer dans d’autres calques avec une transparence en dehors de l’image du sujet. </p> <p>Facultatif. </p> <p>Voir<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Remarques {#section-0822e70fa4784131baa5ad0ba8c0fb3b}

Choix pour `*CropOptions` inclure :

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Choix pour `*PublishJob` inclure :

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`
