---
title: Effet d’icône du lecteur vidéo
description: L’icône Lecture est superposée dans la zone d’affichage vidéo. Il s’affiche lorsque la vidéo est en pause ou lorsque la fin de la vidéo est atteinte, et cela dépend également du paramètre iconeffect.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1e0bd97f-20e9-41e6-95fc-d693644152da
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---

# Effet d’icône du lecteur vidéo{#video-player-icon-effect}

L’icône Lecture est superposée dans la zone d’affichage vidéo. Il s’affiche lorsque la vidéo est en pause ou lorsque la fin de la vidéo est atteinte, et cela dépend également du paramètre iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’apparence de l’icône de lecture est contrôlée par le sélecteur de classe CSS suivant :

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
```

**Propriétés CSS de l’icône de lecture**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour l’icône de lecture. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprites </a>CSS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur de l’icône de lecture. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’icône de lecture. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’effet d’icône prend en charge le sélecteur d’attributs `state` . Le sélecteur `state="play"` est utilisé lorsque la vidéo est interrompue au milieu de la lecture et `state="replay"` lorsque la tête de lecture se trouve à la fin du flux.

## Exemple {#section-e8caea0a303c425a8a637c2a47c06355}

Configurez une icône de lecture de 100 x 100 pixels.

```
.s7mixedmediaviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
