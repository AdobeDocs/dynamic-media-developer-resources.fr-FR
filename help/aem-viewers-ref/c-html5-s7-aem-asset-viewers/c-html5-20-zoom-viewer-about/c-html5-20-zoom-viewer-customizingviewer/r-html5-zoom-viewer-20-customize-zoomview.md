---
title: Vue Zoom
description: La vue principale se compose de l’image zoomable.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ae6c7f6f-5d71-49b5-adbb-782520961acf
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Vue Zoom{#zoom-view}

La vue principale se compose de l’image zoomable.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

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
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan au format hexadécimal de la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> du curseur </span> </p> </td> 
   <td colname="col2"> <p>Curseur affiché sur la vue principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour rendre la vue principale transparente.

```
.s7zoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

Sur les systèmes de bureau, le composant prend en charge `cursortype` sélecteur d’attributs qui peut être appliqué à la classe `.s7zoomview`. Il contrôle le type du curseur en fonction de l’état du composant et de l’action de l’utilisateur. Les valeurs `cursortype` suivantes sont prises en charge :

* `default`

  Affiché lorsque l’image ne peut pas faire l’objet d’un zoom en raison d’une faible résolution d’image, des paramètres de composant ou des deux.

* `zoomin`

  Affiché lorsque l’image peut faire l’objet d’un zoom avant.

* `reset`

  Affiché lorsque l’image est au niveau de zoom maximal et peut être réinitialisé à son état initial.

* `drag`

  Affiché lorsque l’utilisateur effectue un panoramique sur l’image qui fait l’objet d’un zoom avant.

* `slide`

  Affiché lorsque l’utilisateur permute des images en effectuant un balayage horizontal ou en cliquant dessus.
