---
title: Page vue
description: La vue principale se compose de l’image du catalogue. Il peut être glissé pour accéder à une autre page ou agrandi.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d98babad-96c7-419a-abf2-3b6657d550eb
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 3%

---

# Page vue{#page-view}

La vue principale se compose de l’image du catalogue. Il peut être glissé pour accéder à une autre page ou agrandi.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect de la zone d’affichage est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7pageview
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
   <td colname="col2"> <p> Couleur d’arrière-plan de la vue principale au format hexadécimal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>Curseur affiché au-dessus de la vue principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour rendre la vue principale transparente.

```
.s7ecatalogsearchviewer .s7pageview { 
 background-color: transparent; 
}
```

Sur les systèmes de bureau, le composant prend en charge la variable `cursortype` sélecteur d’attributs qui peut être appliqué à `.s7pageview` et contrôle le type du curseur en fonction de l’état du composant et de l’action de l’utilisateur. Les éléments suivants `cursortype` sont prises en charge :

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Valeur </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> par défaut </span> </p> </td> 
   <td colname="col2"> <p>S’affiche lorsque l’image n’est pas agrandie en raison d’une petite résolution d’image, de paramètres de composant ou des deux. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p>S’affiche lorsque l’image peut être agrandie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> réinitialiser </span> </p> </td> 
   <td colname="col2"> <p>S’affiche lorsque l’image atteint le niveau de zoom maximal et peut être réinitialisée à l’état initial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> glisser </span> </p> </td> 
   <td colname="col2"> <p>Affiché lorsque l’utilisateur effectue un panoramique sur l’image agrandie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositive </span> </p> </td> 
   <td colname="col2"> <p>Affiché lorsque l’utilisateur effectue un changement d’image en effectuant un glissement ou un clic horizontal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le séparateur de page qui sépare visuellement les pages gauche et droite de l’étendue du catalogue est contrôlé à l’aide du sélecteur de classe CSS suivant :

`.s7ecatalogsearchviewer .s7pageview .s7pagedivider`

<table id="table_77EBC9A77BF14CF4974F8F43C709A207"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Largeur du séparateur de page. Définissez sur . <span class="codeph"> 0 </span> px pour masquer complètement le séparateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Image que vous souhaitez utiliser comme séparateur de page. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour un séparateur de page de 40 pixels de large avec une image semi-transparente.

```
.s7ecatalogsearchviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>Lorsque la variable `frametransition` le modificateur est défini sur `turn` ou `auto` (sur les systèmes de bureau), l’aspect du séparateur de page est contrôlé à l’aide de la fonction `pageturnstyle` et le `.s7pagedivider` La classe CSS est ignorée.

Il est possible de configurer l’affichage des curseurs de souris personnalisés sur la zone de visionneuse principale. Cette fonctionnalité est contrôlée avec les sélecteurs d’attributs supplémentaires appliqués à `.s7ecatalogsearchviewer .s7pageview` Classe CSS :

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> par défaut </span> </p> </td> 
   <td colname="col2"> <p> Normalement, une flèche s’affiche pour une image non zoomable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p> Indique à quel moment une image peut être agrandie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> réinitialiser </span> </p> </td> 
   <td colname="col2"> <p>Indique si une image atteint le zoom maximal et peut être réinitialisée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> glisser </span> </p> </td> 
   <td colname="col2"> <p>Affiche le moment où l’utilisateur effectue une opération de glisser sur l’image agrandie </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diapositive </span> </p> </td> 
   <td colname="col2"> <p>Affiche le moment où l’utilisateur effectue le changement d’image à l’aide d’un mouvement de diapositives </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : utilisez des curseurs de souris différents pour chaque type d’état de composant.

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
