---
description: L’icône de lecture est superposée sur la zone de vue principale. Il s’affiche lorsque la vidéo est en pause ou lorsque la fin de la vidéo est atteinte, et dépend également du paramètre iconeffect.
solution: Experience Manager
title: Effet Icône
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéo
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 1%

---


# Effet Icône{#icon-effect}

L’icône de lecture est superposée sur la zone de vue principale. Il s’affiche lorsque la vidéo est en pause ou lorsque la fin de la vidéo est atteinte, et dépend également du paramètre iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspect de l’icône de lecture est contrôlé par le sélecteur de classe CSS suivant :

```
.s7videoviewer . s7videoplayer .s7iconeffect
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
   <td colname="col2"> <p> Positionnez l’objet à l’intérieur de l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
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
.s7videoviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7videoviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7videoviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```

