---
title: Effet Icône
description: L’icône de lecture est superposée sur la zone d’affichage principale. Il s’affiche lorsque la vidéo est mise en pause ou lorsque la fin de la vidéo est atteinte, et dépend également du paramètre d’effet iconique .
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: f4bf343a-4a78-470b-abe5-94e2d608f45d
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 1%

---

# Effet Icône{#icon-effect}

L’icône de lecture est superposée sur la zone d’affichage principale. Il s’affiche lorsque la vidéo est mise en pause ou lorsque la fin de la vidéo est atteinte, et dépend également du paramètre d’effet iconique .

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspect de l’icône de lecture est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7videoviewer . s7videoplayer .s7iconeffect
```

**Propriétés CSS de l’icône de lecture**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Image affichée de l’icône de lecture. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
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

L’effet d’icône prend en charge `state` sélecteur d’attributs. When `state="play"` est utilisée lorsque la vidéo est mise en pause au milieu de la lecture ; et `state="replay"` est utilisé lorsque la tête de lecture se trouve à la fin du flux.

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
