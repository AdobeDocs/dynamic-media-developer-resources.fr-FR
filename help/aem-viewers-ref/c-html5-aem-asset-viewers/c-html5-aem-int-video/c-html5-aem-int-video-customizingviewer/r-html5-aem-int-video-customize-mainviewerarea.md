---
description: Le  principal est la zone occupée par les échantillons interactifs. Il est généralement configuré pour s’adapter à l’écran du périphérique disponible lorsqu’aucune taille n’est spécifiée.
seo-description: Le  principal est la zone occupée par les échantillons interactifs. Il est généralement configuré pour s’adapter à l’écran du périphérique disponible lorsqu’aucune taille n’est spécifiée.
seo-title: Zone du lecteur principal
solution: Experience Manager
title: Zone du lecteur principal
topic: Dynamic media
uuid: 3e04c578-dcb2-4034-8809-dc949be80097
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Zone du lecteur principal{#main-viewer-area}

Le  principal est la zone occupée par les échantillons interactifs. Il est généralement configuré pour s’adapter à l’écran du périphérique disponible lorsqu’aucune taille n’est spécifiée.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect de la zone d’affichage est contrôlé par le sélecteur de classe CSS suivant :

```
.s7interactivevideoviewer
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
   <td colname="col2"> <p>Hauteur du lecteur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan au format hexadécimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-ee18025b182a42dc98052de5f133ddfe}

Configuration d’une visionneuse avec un arrière-plan blanc ( `#FFFFFF`) et création d’une taille de 512 x 288 pixels.

```
.s7interactivevideoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

