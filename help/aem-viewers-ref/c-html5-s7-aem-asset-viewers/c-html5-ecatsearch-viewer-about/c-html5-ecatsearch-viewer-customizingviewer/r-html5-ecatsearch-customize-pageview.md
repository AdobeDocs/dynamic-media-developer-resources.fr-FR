---
title: Page vue
description: La vue principale se compose de l’image du catalogue. Il peut être balayé pour accéder à une autre page ou agrandi.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d98babad-96c7-419a-abf2-3b6657d550eb
TQID: 'https://experienceleague.adobe.com/IN5BJWNHvq-xzVmyu8gX-yIYCt-QvkgI3pvOp6nOP-Y'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 388
ht-degree: 1%

---

# Page vue{#page-view}

La vue principale se compose de l’image du catalogue. Il peut être balayé pour accéder à une autre page ou agrandi.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect de la zone d’affichage est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7pageview
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
   <td colname="col2"> <p> Couleur d’arrière-plan de la vue principale au format hexadécimal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> du curseur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Curseur affiché sur la vue principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour rendre la vue principale transparente.

```
.s7ecatalogsearchviewer .s7pageview { 
 background-color: transparent; 
}
```

Sur les systèmes de bureau, le composant prend en charge le sélecteur d’attributs `cursortype` qui peut être appliqué à `.s7pageview` classe et contrôle le type du curseur en fonction de l’état du composant et de l’action de l’utilisateur. Les valeurs `cursortype` suivantes sont prises en charge :

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valeur </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> par défaut </p> </td> 
   <td colname="col2"> <p>Affiché lorsque l’image ne peut pas faire l’objet d’un zoom en raison d’une résolution d’image réduite, des paramètres des composants ou des deux. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p>Affiché lorsque l’image peut faire l’objet d’un zoom avant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset </span> </p> </td> 
   <td colname="col2"> <p>Affiché lorsque l’image est au niveau de zoom maximal et peut être réinitialisé à l’état initial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> glisser </span> </p> </td> 
   <td colname="col2"> <p>Affiché lorsque l’utilisateur effectue un panoramique sur l’image qui fait l’objet d’un zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> de diapositives </p> </td> 
   <td colname="col2"> <p>Affiché lorsque l’utilisateur permute une image en effectuant un balayage horizontal ou un clic. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le séparateur de page qui sépare visuellement les pages gauche et droite de la page du catalogue est contrôlé par le sélecteur de classe CSS suivant :

`.s7ecatalogsearchviewer .s7pageview .s7pagedivider`

<table id="table_77EBC9A77BF14CF4974F8F43C709A207"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur du séparateur de page. Réglez-le sur <span class="codeph"> 0 </span> px pour masquer complètement le séparateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Image à utiliser comme séparateur de page. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour disposer d’un séparateur de page de 40 pixels de large avec une image semi-transparente.

```
.s7ecatalogsearchviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>Lorsque le modificateur `frametransition` est défini sur `turn` ou `auto` (sur les systèmes de bureau), l’aspect du séparateur de page est contrôlé par le modificateur `pageturnstyle` et la classe CSS `.s7pagedivider` est ignorée.

Il est possible de configurer l’affichage des curseurs de souris personnalisés sur la zone de visionneuse principale. Cette fonctionnalité est contrôlée avec les sélecteurs d’attributs supplémentaires appliqués à `.s7ecatalogsearchviewer .s7pageview` classe CSS :

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> par défaut </p> </td> 
   <td colname="col2"> <p> Normalement, une flèche s’affiche pour une image non zoomable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p> Indique à quel moment il est possible d’effectuer un zoom avant sur une image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset </span> </p> </td> 
   <td colname="col2"> <p>Indique à quel moment une image atteint le zoom maximal et peut être réinitialisée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> glisser </span> </p> </td> 
   <td colname="col2"> <p>Indique quand l’utilisateur effectue une opération de glisser-déposer sur une image agrandie </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> de diapositives </p> </td> 
   <td colname="col2"> <p>Indique quand l’utilisateur permute des images à l’aide du mouvement de diapositive </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : utilisez différents curseurs de souris pour chaque type d’état du composant.

```
.s7ecatalogsearchviewer .s7pageview[cursortype="default"] { 
cursor:auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="zoomin"] { 
cursor:url(images/zoomin_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="reset"] { 
cursor:url(images/zoomout_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview [cursortype="slide"] { 
cursor:url(images/slide_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="drag"] { 
cursor:url(images/drag_cursor.cur), auto; 
}
```
