---
title: Zone principale de la visionneuse
description: La zone de visualisation principale est occupée par la vidéo. En règle générale, elle est configurée pour s’adapter à l’écran disponible du périphérique lorsqu’aucune taille n’est spécifiée.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 7d1379c1-7746-4f61-92df-e8ac4ab7d506
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# Zone principale de la visionneuse{#main-viewer-area}

La zone de visualisation principale est occupée par la vidéo. En règle générale, elle est configurée pour s’adapter à l’écran disponible du périphérique lorsqu’aucune taille n’est spécifiée.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Le sélecteur de classe CSS suivant contrôle l’apparence de la zone d’affichage :

```
.s7videoviewer 
```

## Propriétés CSS de la zone principale de la visionneuse {#css-properties-of-the-main-viewer-area}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Couleur de fond au format hexadécimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-e8caea0a303c425a8a637c2a47c06355}

Pour configurer une visionneuse de vidéo avec un arrière-plan blanc (#FFFFFF) et faire en sorte qu’elle fasse 512 x 288 pixels :

```
.s7videoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
