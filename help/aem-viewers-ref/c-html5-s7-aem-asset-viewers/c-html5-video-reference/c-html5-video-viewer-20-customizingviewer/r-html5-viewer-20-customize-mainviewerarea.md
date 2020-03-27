---
description: La principale zone  est occupée par la vidéo. Il est généralement configuré pour s’adapter à l’écran du périphérique disponible lorsqu’aucune taille n’est spécifiée.
seo-description: La principale zone  est occupée par la vidéo. Il est généralement configuré pour s’adapter à l’écran du périphérique disponible lorsqu’aucune taille n’est spécifiée.
seo-title: Zone du lecteur principal
solution: Experience Manager
title: Zone du lecteur principal
topic: Dynamic media
uuid: f395b22d-55b8-4422-9aa4-9dd4b7a24063
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Zone du lecteur principal{#main-viewer-area}

La principale zone  est occupée par la vidéo. Il est généralement configuré pour s’adapter à l’écran du périphérique disponible lorsqu’aucune taille n’est spécifiée.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Le sélecteur de classe CSS suivant contrôle l’aspect de la zone d’affichage :

```
.s7videoviewer 
```

## Propriétés CSS de la zone de visionneuse principale {#css-properties-of-the-main-viewer-area}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
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
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan au format hexadécimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-e8caea0a303c425a8a637c2a47c06355}

Pour configurer une visionneuse de vidéos avec un arrière-plan blanc (#FFFFFF) et lui donner une taille de 512 x 288 pixels :

```
.s7videoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

