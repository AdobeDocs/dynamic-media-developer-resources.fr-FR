---
title: Effet Icône
description: L’icône de lecture est superposée sur la zone d’affichage principale. Il s’affiche lorsque la vidéo est mise en pause ou lorsque la fin de la vidéo est atteinte, et dépend également du paramètre d’effet iconique .
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e25a3b9d-88ef-4214-9b6b-2527ebf0f145
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# Effet Icône{#icon-effect}

L’icône de lecture est superposée sur la zone d’affichage principale. Il s’affiche lorsque la vidéo est mise en pause ou lorsque la fin de la vidéo est atteinte, et dépend également du paramètre d’effet iconique .

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspect de l’icône de lecture est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7video360viewer . s7video360player .s7iconeffect
```

**Propriétés CSS de l’icône de lecture**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Image affichée de l’icône de lecture. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
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

L’effet d’icône prend en charge le sélecteur d’attributs `state`. Le sélecteur d’attributs `state="play"` est utilisé lorsque la vidéo est mise en pause au milieu de la lecture et `state="replay"` est utilisé lorsque la tête de lecture se trouve à la fin de la diffusion.

**Exemple** - Configurer une icône de lecture de 100 x 100 pixels.

```
.s7video360viewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7video360viewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7video360viewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
