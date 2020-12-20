---
description: L’icône de lecture est superposée sur la zone de vue vidéo. Il s’affiche lorsque la vidéo est en pause ou lorsque la fin de la vidéo est atteinte, et dépend également du paramètre iconeffect.
seo-description: L’icône de lecture est superposée sur la zone de vue vidéo. Il s’affiche lorsque la vidéo est en pause ou lorsque la fin de la vidéo est atteinte, et dépend également du paramètre iconeffect.
seo-title: Effet d’icône du lecteur vidéo
solution: Experience Manager
title: Effet d’icône du lecteur vidéo
topic: Dynamic media
uuid: 5d59c4b2-a7a1-49e1-84c7-0e127a571c4f
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 1%

---


# Effet d’icône du lecteur vidéo {#video-player-icon-effect}

L’icône de lecture est superposée sur la zone de vue vidéo. Il s’affiche lorsque la vidéo est en pause ou lorsque la fin de la vidéo est atteinte, et dépend également du paramètre iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspect de l’icône de lecture est contrôlé par le sélecteur de classe CSS suivant :

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
```

**Propriétés CSS de l’icône de lecture**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour l’icône de lecture. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p> Positionnez l’objet à l’intérieur de l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Largeur de l’icône de lecture. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’icône de lecture. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’effet Icône prend en charge le sélecteur d’attributs `state`. `state="play"` est utilisée lorsque la vidéo est en pause au milieu de la lecture et  `state="replay"` est utilisée lorsque la tête de lecture se trouve à la fin du flux.

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

