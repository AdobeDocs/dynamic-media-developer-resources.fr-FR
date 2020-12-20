---
description: La zone principale de la vue est la zone occupée par l'image de rotation. Il s'adapte généralement à l'écran du périphérique disponible lorsqu'aucune taille n'est spécifiée.
seo-description: La zone principale de la vue est la zone occupée par l'image de rotation. Il s'adapte généralement à l'écran du périphérique disponible lorsqu'aucune taille n'est spécifiée.
seo-title: Zone du lecteur principal
solution: Experience Manager
title: Zone du lecteur principal
topic: Dynamic media
uuid: 8395386b-4039-4a47-8d31-a341813c2647
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---


# Zone du lecteur principal{#main-viewer-area}

La zone principale de la vue est la zone occupée par l&#39;image de rotation. Il s&#39;adapte généralement à l&#39;écran du périphérique disponible lorsqu&#39;aucune taille n&#39;est spécifiée.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visualisation principale**

L’aspect de la zone d’affichage est contrôlé par le sélecteur de classe CSS suivant :

```
.s7spinviewer
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

Exemple : pour configurer une visionneuse avec un arrière-plan blanc ( `#FFFFFF`) et lui appliquer une taille de 512 x 288 pixels.

```
.s7spinviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

