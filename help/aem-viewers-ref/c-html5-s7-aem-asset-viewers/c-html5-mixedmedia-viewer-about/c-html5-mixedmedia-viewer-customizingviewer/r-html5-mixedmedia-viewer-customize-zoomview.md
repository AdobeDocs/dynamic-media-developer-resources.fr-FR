---
description: En mode de zoom continu, le  principal est constitué de l’image agrandie lorsque le fichier actif est une image unique.
seo-description: En mode de zoom continu, le  principal est constitué de l’image agrandie lorsque le fichier actif est une image unique.
seo-title: de zoom
solution: Experience Manager
title: de zoom
topic: Dynamic media
uuid: c9113275-eec6-4014-b7ad-3ae9f2cf01d9
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Zoom view{#zoom-view}

En mode de zoom continu, le  principal est constitué de l’image agrandie lorsque le fichier actif est une image unique.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect de la zone d’affichage est contrôlé par le sélecteur de classe CSS suivant :

```
.s7mixedmediaviewer .s7zoomview
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
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan au format hexadécimal du  principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> curseur </span> </p> </td> 
   <td colname="col2"> <p>Curseur affiché sur le  principal du. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour rendre le de zoom transparent.

```
.s7mixedmediaviewer .s7zoomview { 
 background-color: transparent; 
}
```

Sur les systèmes de bureau, le composant prend en charge le sélecteur d’ `cursortype` attributs qui peut être appliqué à la `.s7zoomview` classe. Il contrôle le type du curseur en fonction de l’état du composant et de l’action de l’utilisateur. The following `cursortype` values are supported:

* `default`

   S’affiche lorsque l’image n’est pas zoomable en raison d’une résolution d’image réduite, de paramètres de composant ou des deux paramètres.

* `zoomin`

   S’affiche lorsque vous pouvez zoomer sur l’image.

* `reset`

   S’affiche lorsque l’image atteint le niveau de zoom maximal et peut être redéfinie à son état initial.

* `drag`

   S’affiche lorsque l’utilisateur effectue un panoramique sur l’image qui fait l’objet d’un zoom avant.

* `slide`

   S’affiche lorsque l’utilisateur effectue une permutation d’image en effectuant un glissement ou un mouvement de balayage horizontal.

