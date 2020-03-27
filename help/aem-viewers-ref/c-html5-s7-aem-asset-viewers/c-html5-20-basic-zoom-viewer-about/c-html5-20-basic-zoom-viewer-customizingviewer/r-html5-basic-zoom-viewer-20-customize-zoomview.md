---
description: Le  principal est constitué de l’image agrandie.
seo-description: Le  principal est constitué de l’image agrandie.
seo-title: de zoom
solution: Experience Manager
title: de zoom
topic: Dynamic media
uuid: 06464e36-8c9c-4d3c-b4e5-5911f002568c
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Zoom view{#zoom-view}

Le  principal est constitué de l’image agrandie.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect de la zone d’affichage est contrôlé par le sélecteur de classe CSS suivant :

```
.s7basiczoomviewer .s7zoomview
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
   <td colname="col2"> <p>Le curseur s’affiche sur le  principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour rendre le principal transparent.

```
.s7basiczoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

Sur les systèmes de bureau, le composant prend en charge le sélecteur d’ `cursortype` attributs qui peut être appliqué à la `.s7zoomview` classe et contrôle le type de curseur en fonction de l’état du composant et de l’action de l’utilisateur. The following `cursortype` values are supported:

<table id="table_BC9FC40DA27B4A85995F4E9431AABF33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valeur </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> par défaut </span> </p> </td> 
   <td colname="col2"> <p>S’affiche lorsque l’image n’est pas zoomable en raison d’une résolution d’image réduite, de paramètres de composant ou des deux paramètres. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomine </span> </p> </td> 
   <td colname="col2"> <p>S’affiche lorsque vous pouvez zoomer sur l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> réinitialiser </span> </p> </td> 
   <td colname="col2"> <p>S’affiche lorsque l’image atteint le niveau de zoom maximal et peut être redéfinie à son état initial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> glisser </span> </p> </td> 
   <td colname="col2"> <p>S’affiche lorsqu’un utilisateur effectue un panoramique sur l’image qui fait l’objet d’un zoom avant. </p> </td> 
  </tr> 
 </tbody> 
</table>

