---
description: La vue principale est constituée de l’image agrandie.
seo-description: La vue principale est constituée de l’image agrandie.
seo-title: Vue de zoom
solution: Experience Manager
title: Vue de zoom
topic: Dynamic media
uuid: 34cb6c80-77eb-42b0-91dd-ae0369ea2881
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---


# Vue de zoom{#zoom-view}

La vue principale est constituée de l’image agrandie.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visualisation principale**

L’aspect de la zone d’affichage est contrôlé par le sélecteur de classe CSS suivant :

```
.s7zoomviewer .s7zoomview
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
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan au format hexadécimal de la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> curseur  </span> </p> </td> 
   <td colname="col2"> <p>Curseur affiché sur la vue principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour rendre la vue principale transparente.

```
.s7zoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

Sur les systèmes de bureau, le composant prend en charge le sélecteur d&#39;attributs `cursortype` qui peut être appliqué à la classe `.s7zoomview`. Il contrôle le type du curseur en fonction de l’état du composant et de l’action de l’utilisateur. Les valeurs `cursortype` suivantes sont prises en charge :

* `default`

   S’affiche lorsque l’image ne peut pas faire l’objet d’un zoom en raison d’une résolution d’image réduite, de paramètres de composant ou des deux.

* `zoomin`

   S’affiche lorsque vous pouvez zoomer sur l’image.

* `reset`

   S’affiche lorsque l’image atteint le niveau de zoom maximal et peut être redéfinie à son état initial.

* `drag`

   S’affiche lorsque l’utilisateur effectue un panoramique sur l’image dont l’état est zoomé.

* `slide`

   S’affiche lorsque l’utilisateur effectue une permutation d’images en effectuant un balayage horizontal ou un balayage horizontal.

