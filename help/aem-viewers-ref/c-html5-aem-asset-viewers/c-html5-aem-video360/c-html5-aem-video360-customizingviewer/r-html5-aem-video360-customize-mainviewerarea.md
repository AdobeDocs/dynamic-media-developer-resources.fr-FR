---
description: La zone principale de la vue est la zone occupée par la vidéo 360. Il est généralement configuré pour s'adapter à l'écran du périphérique disponible lorsqu'aucune taille n'est spécifiée.
seo-description: La zone principale de la vue est la zone occupée par la vidéo 360. Il est généralement configuré pour s'adapter à l'écran du périphérique disponible lorsqu'aucune taille n'est spécifiée.
seo-title: Zone du lecteur principal
solution: Experience Manager
title: Zone du lecteur principal
topic: Dynamic Media
uuid: ec321901-f077-4f71-a48c-20cae11c41d1
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---


# Zone du lecteur principal{#main-viewer-area}

La zone principale de la vue est la zone occupée par la vidéo 360. Il est généralement configuré pour s&#39;adapter à l&#39;écran du périphérique disponible lorsqu&#39;aucune taille n&#39;est spécifiée.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visualisation principale**

L’aspect de la zone d’affichage est contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
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
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan au format hexadécimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-ee18025b182a42dc98052de5f133ddfe}

Pour configurer une visionneuse avec un arrière-plan blanc ( `#FFFFFF`) et lui donner une taille de 512 x 288 pixels.

```
.s7video360viewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

