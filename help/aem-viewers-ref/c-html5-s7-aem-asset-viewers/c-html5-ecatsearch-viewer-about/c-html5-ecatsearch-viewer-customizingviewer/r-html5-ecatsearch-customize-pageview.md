---
description: Le principal est constitué de l’image du catalogue. Il peut être glissé pour accéder à une autre page ou faire l’objet d’un zoom.
seo-description: Le principal est constitué de l’image du catalogue. Il peut être glissé pour accéder à une autre page ou faire l’objet d’un zoom.
seo-title: ' de page'
solution: Experience Manager
title: ' de page'
topic: Dynamic media
uuid: f585bf57-c66a-4213-a2af-d9625beb5bed
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Page view{#page-view}

Le principal est constitué de l’image du catalogue. Il peut être glissé pour accéder à une autre page ou faire l’objet d’un zoom.

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
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan du principal  au format hexadécimal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> curseur </span> </p> </td> 
   <td colname="col2"> <p>Curseur affiché sur le  principal du. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour rendre le principal transparent.

```
.s7ecatalogsearchviewer .s7pageview { 
 background-color: transparent; 
}
```

Sur les systèmes de bureau, le composant prend en charge le sélecteur d’ `cursortype` attributs qui peut être appliqué à `.s7pageview` la classe et contrôle le type du curseur en fonction de l’état du composant et de l’action de l’utilisateur. The following `cursortype` values are supported:

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
   <td colname="col2"> <p>S’affiche lorsque l’image n’est pas agrandie en raison d’une résolution d’image réduite, de paramètres de composant ou des deux. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomine </span> </p> </td> 
   <td colname="col2"> <p>S’affiche lorsque vous pouvez zoomer sur l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> réinitialiser </span> </p> </td> 
   <td colname="col2"> <p>S’affiche lorsque l’image atteint le niveau de zoom maximal et peut être redéfinie à l’état initial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> glisser </span> </p> </td> 
   <td colname="col2"> <p>S’affiche lorsque l’utilisateur effectue un panoramique sur l’image qui fait l’objet d’un zoom avant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> glissière </span> </p> </td> 
   <td colname="col2"> <p>S’affiche lorsque l’utilisateur effectue une permutation d’image en effectuant un balayage horizontal ou un clic. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le séparateur de page qui sépare visuellement les pages de gauche et de droite de la planche de catalogue est contrôlé par le sélecteur de classe CSS suivant :

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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Largeur du séparateur de page. Définissez cette valeur sur <span class="codeph"> 0 </span> px pour masquer complètement le séparateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-image </span> </p> </td> 
   <td colname="col2"> <p>Image à utiliser comme séparateur de page. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour avoir un séparateur de page de 40 pixels de large avec une image semi-transparente.

```
.s7ecatalogsearchviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>Lorsque le `frametransition` modificateur est défini sur `turn` ou `auto` (sur les systèmes de bureau), l’aspect du séparateur de page est contrôlé avec le modificateur `pageturnstyle` et la classe `.s7pagedivider` CSS est ignorée.

Il est possible de configurer l’affichage des curseurs de souris personnalisés sur la zone de visualisation principale. Ceci est contrôlé avec les sélecteurs d’attributs supplémentaires appliqués à la classe `.s7ecatalogsearchviewer .s7pageview` CSS :

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> par défaut </span> </p> </td> 
   <td colname="col2"> <p> Normalement, une flèche s’affiche pour les images non zoomables. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomine </span> </p> </td> 
   <td colname="col2"> <p> Indique le moment où un zoom est possible sur une image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> réinitialiser </span> </p> </td> 
   <td colname="col2"> <p>Indique le moment où une image atteint le zoom maximum et peut être réinitialisée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> glisser </span> </p> </td> 
   <td colname="col2"> <p>Indique le moment où l’utilisateur effectue une opération de glisser-déplacer sur un zoom dans l’image </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> glissière </span> </p> </td> 
   <td colname="col2"> <p>Affiche le moment où l’utilisateur effectue un échange d’images à l’aide d’un mouvement de diapositive </p> </td> 
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

