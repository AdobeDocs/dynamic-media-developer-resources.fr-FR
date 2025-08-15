---
title: setAsset
description: JavaScript référence de l’API pour la visionneuse vidéo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: e5d71393-fcae-4bd4-8e78-a451b2f05ffc
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# setAsset{#setasset}

JavaScript référence de l’API pour la visionneuse vidéo.

`setAsset(asset[, data])`

Définit la nouvelle ressource et les données de ressource supplémentaires facultatives. Vous pouvez appeler ce paramètre à tout moment, avant ou après `init()`. Si elle est appelée après `init()`, la visionneuse échange la ressource au moment de l’exécution.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Paramètres {#section-e030b401b966469cb5dd121501161c2a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> atout </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">{ String </span>} nouvel ID de ressource. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> données </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">{ JSON </span>} Objet JSON avec les champs facultatifs suivants (respect de la casse) : </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> posterimage </span> - Image à afficher sur la première image avant que la vidéo ne commence à jouer. Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_BBFF3965B69A4AC8A469FDB69097B25A"> <span class="codeph"> caption </span> - emplacement du nouveau fichier de sous-titrage. Si le fichier n’est pas spécifié, le bouton de sous-titrage n’est pas visible dans l’interface utilisateur. </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> navigation </span> - URL ou chemin d’accès au contenu de navigation WebVTT. Le fichier WebVTT doit être servi par Image Serving </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourne {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/Glacier_Climber_MP4")
```
