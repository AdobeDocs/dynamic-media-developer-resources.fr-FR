---
description: L’icône de lecture est superposée sur la zone d’affichage de la vidéo. Il s’affiche lorsque la vidéo est mise en pause ou lorsque la fin de la vidéo est atteinte, et dépend également du paramètre d’effet iconique .
solution: Experience Manager
title: Effet de l’icône du lecteur vidéo
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,User
exl-id: 1e0bd97f-20e9-41e6-95fc-d693644152da
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 1%

---

# Effet de l’icône du lecteur vidéo{#video-player-icon-effect}

L’icône de lecture est superposée sur la zone d’affichage de la vidéo. Il s’affiche lorsque la vidéo est mise en pause ou lorsque la fin de la vidéo est atteinte, et dépend également du paramètre d’effet iconique .

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspect de l’icône de lecture est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
```

**Propriétés CSS de l’icône de lecture**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Image affichée de l’icône de lecture. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
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

L’effet Icône prend en charge le sélecteur d’attributs `state`. `state="play"` est utilisée lorsque la vidéo est mise en pause au milieu de la lecture et  `state="replay"` est utilisée lorsque la tête de lecture se trouve à la fin de la diffusion.

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
