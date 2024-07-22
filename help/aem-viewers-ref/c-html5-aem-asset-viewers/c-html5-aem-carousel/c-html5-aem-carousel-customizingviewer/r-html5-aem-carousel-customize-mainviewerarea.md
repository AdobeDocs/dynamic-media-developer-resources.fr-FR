---
title: Zone de visionneuse principale
description: La zone d’affichage principale est la zone occupée par l’image de bannière de carrousel. Il est défini pour s’adapter à l’écran de l’appareil disponible lorsqu’aucune taille n’est spécifiée.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: bdac54f5-79e3-4d3d-9c7e-d9a7cec61c73
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# Zone de visionneuse principale{#main-viewer-area}

La zone d’affichage principale est la zone occupée par l’image de bannière de carrousel. Il est défini pour s’adapter à l’écran de l’appareil disponible lorsqu’aucune taille n’est spécifiée.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect de la zone d’affichage est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7carouselviewer
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan au format hexadécimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une visionneuse avec un arrière-plan blanc ( `#FFFFFF`) et faire sa taille de 1 174 x 500 pixels.

```
.s7carouselviewer { 
 background-color: #FFFFFF; 
 width: 1174px; 
 height: 500px;  
}
```
