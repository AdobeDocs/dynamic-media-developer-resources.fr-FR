---
title: Vue Zoom
description: En mode de zoom continu, la vue principale correspond à l’image zoomable lorsque la ressource actuelle est une image unique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0252436b-ba96-4273-b796-d1772fc093b0
TQID: 'https://experienceleague.adobe.com/xfQKn46HParEFKYh1jrrVxbmkUKQHJbcWlJ7LWHIsc0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 195
ht-degree: 0%

---

# Vue Zoom{#zoom-view}

En mode de zoom continu, la vue principale correspond à l’image zoomable lorsque la ressource actuelle est une image unique.

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
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan au format hexadécimal de la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> du curseur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Curseur affiché sur la vue principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour rendre la vue de zoom transparente.

```
.s7mixedmediaviewer .s7zoomview { 
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
