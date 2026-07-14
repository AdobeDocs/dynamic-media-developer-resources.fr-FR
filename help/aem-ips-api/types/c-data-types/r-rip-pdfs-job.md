---
title: RipPdfJob
description: Processus de récupération d’une ressource PDF existante.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7a787b45-3cda-44f2-8357-8b6217b679e0
TQID: 'https://experienceleague.adobe.com/TdjReFUJR2N-XqrC1BXdH7PpI9Xqj5hbM6iA8bWCDzw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
  - id: ae478996-b206-4712-9b0c-dc78a2644453
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 198
ht-degree: 3%

---

# [!DNL RipPdfsJob]{#rippdfsjob}

Processus de récupération d’une ressource PDF existante.

>[!NOTE]
>
>Ce type de traitement est obsolète. Transition vers `ReprocessAssetsJob` pour toutes les intégrations futures.

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Gérez le tableau des fichiers PDF à extraire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Détermine si vous souhaitez créer un masque ou non. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> de sous-domaines:ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de recadrage manuel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> d’options : AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de recadrage automatique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> de rapports :PostTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> de sous-réseau :PDFOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> d’images :IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> d’options :ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Tableau de descripteurs de projet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Paramètres d’e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>URL vers laquelle les fichiers sont chargés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Détails de la tâche pour une image diffusant la tâche de publication à exécuter une fois le chargement terminé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Détails de la tâche pour une tâche de publication de rendu d’image à exécuter une fois le chargement terminé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Détails d’une tâche de publication vidéo à exécuter une fois le chargement terminé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Options de chargement des fichiers Adobe InDesign sur le serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> knockoutBackground </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>Masquez l’arrière-plan des images sélectionnées. Cette fonctionnalité vous permet de les superposer dans d’autres calques avec une transparence en dehors de l’image du sujet. </p> <p>Facultatif. </p> <p>Voir <a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Remarques {#section-0822e70fa4784131baa5ad0ba8c0fb3b}

Les choix pour `*CropOptions` incluent :

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Les choix pour `*PublishJob` incluent :

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`

