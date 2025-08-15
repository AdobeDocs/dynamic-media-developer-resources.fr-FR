---
title: Vue de zoom
description: En mode zoom continu, la vue principale est constituée de l’image zoomable lorsque la ressource actuelle est une image unique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0252436b-ba96-4273-b796-d1772fc093b0
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Vue de zoom{#zoom-view}

En mode zoom continu, la vue principale est constituée de l’image zoomable lorsque la ressource actuelle est une image unique.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone principale de la visionneuse**

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
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan au format hexadécimal de la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> curseur </span> </p> </td> 
   <td colname="col2"> <p>Curseur affiché sur la vue principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : rendre l’affichage zoom transparent.

```
.s7mixedmediaviewer .s7zoomview { 
 background-color: transparent; 
}
```

Sur les ordinateurs de bureau, le composant prend en charge `cursortype` le sélecteur d’attributs qui peut être appliqué à la `.s7zoomview` classe. Il contrôle le type du curseur en fonction de l’état du composant et de l’action de l’utilisateur. Les valeurs suivantes `cursortype` sont prises en charge :

* `default`

  Affiché lorsque l’image n’est pas zoomable en raison d’une petite résolution d’image, ou des paramètres de composant, ou les deux.

* `zoomin`

  S’affiche lorsque l’image peut être zoomée.

* `reset`

  S’affiche lorsque l’image est au niveau de zoom maximal et peut être réinitialisée à son état initial.

* `drag`

  S’affiche lorsque l’utilisateur effectue un panoramique de l’image agrandie.

* `slide`

  S’affiche lorsque l’utilisateur effectue un balayage horizontal d’image.
