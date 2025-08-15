---
title: Page vue
description: La vue principale se compose de l’image du catalogue. Il peut être glissé pour accéder à une autre page ou zoomé.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d3368115-15e7-4d9d-a417-a3c82c9a8a64
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 1%

---

# Page vue{#page-view}

La vue principale se compose de l’image du catalogue. Il peut être glissé pour accéder à une autre page ou zoomé.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone principale de la visionneuse**

L’aspect de la zone d’affichage est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7pageview
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
   <td colname="col2"> <p> Couleur d’arrière-plan de la vue principale au format hexadécimal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> curseur </span> </p> </td> 
   <td colname="col2"> <p>Curseur affiché sur le dessus de la fenêtre principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour rendre la vue principale transparente.

```
.s7ecatalogviewer .s7pageview { 
 background-color: transparent; 
}
```

Sur les ordinateurs de bureau, le composant prend en charge le `cursortype` sélecteur d’attributs qui peut être appliqué à `.s7pageview` la classe et contrôle le type du curseur en fonction de l’état du composant et de l’action de l’utilisateur. Les valeurs suivantes `cursortype` sont prises en charge :

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valeur </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> faire défaut </span> </p> </td> 
   <td colname="col2"> <p>Affiché lorsque l’image n’est pas zoomable en raison d’une résolution d’image réduite, des paramètres de composant, ou les deux. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Zoom avant </span> </p> </td> 
   <td colname="col2"> <p>S’affiche lorsque l’image peut être zoomée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> réinitialisation </span> </p> </td> 
   <td colname="col2"> <p>S’affiche lorsque l’image est au niveau de zoom maximal et peut être réinitialisée à l’état initial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> traîner </span> </p> </td> 
   <td colname="col2"> <p>S’affiche lorsque l’utilisateur effectue un panoramique de l’image avec zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> glisser </span> </p> </td> 
   <td colname="col2"> <p>S’affiche lorsque l’utilisateur permute d’image par balayage horizontal ou effleurement. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le séparateur de page qui sépare visuellement les pages gauche et droite de la planche du catalogue est contrôlé par le sélecteur de classe CSS suivant :

`.s7ecatalogviewer .s7pageview .s7pagedivider`

<table id="table_77EBC9A77BF14CF4974F8F43C709A207"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur du séparateur de page. Définissez le séparateur sur <span class="codeph"> 0 </span> px. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Image que vous souhaitez utiliser comme séparateur de page. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : avoir un séparateur de page de 40 pixels de large avec une image semi-transparente.

```
.s7ecatalogviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>Lorsque le `frametransition` modificateur est défini sur `turn` ou `auto` (sur les ordinateurs de bureau), l’apparence du séparateur de page est contrôlée par le `pageturnstyle` modificateur et la `.s7pagedivider` classe CSS est ignorée.

Il est possible de configurer l’affichage des curseurs personnalisés de la souris sur la zone principale de la visionneuse. Cette fonctionnalité est contrôlée par les sélecteurs d’attributs supplémentaires appliqués à `.s7ecatalogviewer .s7pageview` la classe CSS :

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> faire défaut </span> </p> </td> 
   <td colname="col2"> <p> Normalement, une flèche s’affiche pour les images non zoomables. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Zoom avant </span> </p> </td> 
   <td colname="col2"> <p> Indique les moments où une image peut être zoomée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> réinitialisation </span> </p> </td> 
   <td colname="col2"> <p>Indique quand une image atteint le zoom maximal et peut être réinitialisée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> traîner </span> </p> </td> 
   <td colname="col2"> <p>Indique quand l’utilisateur effectue une opération de glissement sur l’image avec un zoom avant </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> glisser </span> </p> </td> 
   <td colname="col2"> <p>Indique lorsque l’utilisateur permute l’image à l’aide d’un mouvement de glissement </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : avoir des curseurs de souris différents pour chaque type d’état de composant.

```
.s7ecatalogviewer .s7pageview[cursortype="default"] { 
cursor:auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="zoomin"] { 
cursor:url(images/zoomin_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="reset"] { 
cursor:url(images/zoomout_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview [cursortype="slide"] { 
cursor:url(images/slide_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="drag"] { 
cursor:url(images/drag_cursor.cur), auto; 
}
```
