---
title: Mode Zoom
description: En mode zoom continu, la vue principale est composée de l’image agrandie lorsque la ressource active est une seule image.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0252436b-ba96-4273-b796-d1772fc093b0
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Mode Zoom{#zoom-view}

En mode zoom continu, la vue principale est composée de l’image agrandie lorsque la ressource active est une seule image.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect de la zone d’affichage est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7mixedmediaviewer .s7zoomview
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
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan au format hexadécimal de la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>Curseur affiché au-dessus de la vue principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour rendre le zoom transparent.

```
.s7mixedmediaviewer .s7zoomview { 
 background-color: transparent; 
}
```

Sur les systèmes de bureau, le composant prend en charge `cursortype` sélecteur d’attributs qui peut être appliqué au `.s7zoomview` classe . Il contrôle le type de curseur en fonction de l’état du composant et de l’action de l’utilisateur. Les éléments suivants `cursortype` sont prises en charge :

* `default`

   S’affiche lorsque l’image n’est pas agrandie en raison d’une petite résolution d’image, de paramètres de composant ou des deux.

* `zoomin`

   S’affiche lorsque l’image peut être agrandie.

* `reset`

   S’affiche lorsque l’image atteint le niveau de zoom maximal et peut être réinitialisée à son état initial.

* `drag`

   Affiché lorsque l’utilisateur effectue un panoramique sur l’image qui est agrandie.

* `slide`

   Affiché lorsque l’utilisateur effectue un échange d’image à l’aide d’un glissement ou d’un clic horizontal.
