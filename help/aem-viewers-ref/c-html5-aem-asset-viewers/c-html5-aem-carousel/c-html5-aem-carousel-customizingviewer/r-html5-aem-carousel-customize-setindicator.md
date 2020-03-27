---
description: L’indicateur Set est une série de points rendus au bas de la visionneuse. Il affiche la position actuelle dans l’ensemble.
seo-description: L’indicateur Set est une série de points rendus au bas de la visionneuse. Il affiche la position actuelle dans l’ensemble.
seo-title: Définir un indicateur
solution: Experience Manager
title: Définir un indicateur
topic: Dynamic media
uuid: 3f90a216-654f-44a9-947d-592bd5f342d4
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Définir un indicateur{#set-indicator}

L’indicateur Set est une série de points rendus au bas de la visionneuse. Il affiche la position actuelle dans l’ensemble.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de l’indicateur d’ensemble**

L’aspect du d’indicateur défini est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7carouselviewer .s7setindicator
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
   <td colname="col2"> <p>Couleur d’arrière-plan au format hexadécimal de l’indicateur défini. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>L’indicateur Set prend en charge le sélecteur d’attributs de mode, que vous pouvez utiliser pour appliquer différents styles aux modes d’opération numérique et en pointillé. correspond notamment `mode="numeric"` au mode de fonctionnement numérique; `mode="dotted"` correspond à l’état par défaut du point.

Exemple : pour définir un indicateur avec un arrière-plan blanc :

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

L’aspect d’un point d’indicateur d’ensemble individuel est contrôlé par le sélecteur de classe CSS. Il s’applique aux éléments en mode d’opération numérique et en mode pointillé.

`.s7carouselviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du point d’indicateur défini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du point d’indicateur défini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge-gauche </span> </p> </td> 
   <td colname="col2"> <p>Marge gauche en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge-haut </span> </p> </td> 
   <td colname="col2"> <p>Marge supérieure en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge-droite </span> </p> </td> 
   <td colname="col2"> <p>Marge droite en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-bottom </span> </p> </td> 
   <td colname="col2"> <p>Marge inférieure en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>Rayon de la bordure en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan au format hexadécimal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nom de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Taille de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Couleur de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alignement vertical </span> </p> </td> 
   <td colname="col2"> <p>Alignement vertical de l’index de bannière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du texte pour l’index de la bannière. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Les éléments d’indicateur prennent en charge le sélecteur d’ `state` attributs, qui peut être utilisé pour appliquer différents habillages à différents états de miniature. correspond notamment `state="selected"` à l’élément actif de l’ensemble; `state="unselected"` correspond à l’état de l’élément par défaut.

Exemple : pour configurer l’indicateur en mode pointillé pour que les systèmes de bureau soient positionnés à 20 pixels du bas de la visionneuse. Les points non sélectionnés sont noirs avec une transparence de 50 %, 15 x 15 pixels avec des coins arrondis de 7 pixels. Les points sélectionnés sont noirs avec 90 % de transparence, 18 x 18 pixels avec 9 pixels aux coins arrondis. L’espacement entre les points est de 5 pixels.

```
.s7carouselviewer.s7mouseinput .s7setindicator { 
 bottom: 20px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot{ 
 width:15px; 
 height:15px; 
 margin-left:2.5px; 
 margin-right:2.5px; 
 margin-top:2.5px; 
 margin-bottom:2.5px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='selected'] {  
 width:18px; 
 height:18px; 
 background-color: #000000; 
 opacity: 0.9; 
 border-radius:9px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='unselected'] {  
 width:15px; 
 height:15px; 
 background-color: #000000; 
 opacity: 0.5; 
 border-radius:7px; 
}
```

