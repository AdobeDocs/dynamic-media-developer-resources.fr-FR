---
title: setVideo
description: Référence de l’API JavaScript pour la visionneuse de vidéos avec recadrage intelligent
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 5e735e11-e359-4b98-b4a9-2c69a8eb424a
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---

# setVideo{#setvideo}

Référence de l’API JavaScript pour la visionneuse de vidéos avec recadrage intelligent

`setVideo(videoUrl[, data])`

Définit une nouvelle vidéo externe et des données vidéo supplémentaires facultatives. Peut être appelé à tout moment, avant et après la `init()`. Si elle est appelée après `init()`, la visionneuse permute la vidéo au moment de l’exécution.

Voir aussi [init]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Paramètres {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} URL absolue de la nouvelle vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de données </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} Objet JSON avec les champs facultatifs suivants (sensibles à la casse) : </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> posterimage </span> - Image à afficher sur la première image avant que la vidéo ne commence à être lue. Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local">’</a> VideoPlayer.posterimage. </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> de sous-titres </span> - Emplacement du nouveau fichier de sous-titres. Si aucun fichier de sous-titres n’est spécifié, le bouton de sous-titres n’est pas affiché dans l’interface utilisateur. </li> 
      <li id="li_A43A1BAB6B0F4A7981F71408F08F07D1"> <span class="codeph"> de navigation </span> - URL ou chemin d’accès au contenu de navigation WebVTT. Le fichier WebVTT doit être diffusé par le service d’images. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

<!--
## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Scene7SharedAssets/Glacier_Climber_MP4")
```
-->
