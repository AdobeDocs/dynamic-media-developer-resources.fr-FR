---
title: Définir l’indicateur
description: L’indicateur défini est une série de points rendus au-dessus des échantillons principaux lorsqu’une visionneuse est utilisée sur un appareil tactile. Les points aident les utilisateurs à naviguer dans les pages de vignettes lorsque les boutons de défilement ne sont pas disponibles.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 53ee058a-cb8c-4b1f-bb9b-caaecc12c947
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Définir l’indicateur{#set-indicator}

Définir l’indicateur est une série de points rendus sur les échantillons principaux lorsqu’une visionneuse est utilisée sur un appareil tactile. Les points aident les utilisateurs à parcourir les pages de miniatures lorsque les boutons de défilement ne sont pas disponibles.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de l’indicateur défini**

L’aspect du conteneur indicateur défini est contrôlé par le sélecteur de classe CSS suivant :

```
.s7mixedmediaviewer .s7setindicator
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
   <td colname="col2"> <p>Couleur d’arrière-plan au format hexadécimal de l’indicateur défini. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour créer un indicateur défini sur fond blanc :

```
.s7mixedmediaviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

L’aspect d’un point indicateur défini individuel est contrôlé par le sélecteur de classe CSS :

`.s7mixedmediaviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du point indicateur défini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du point indicateur défini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge gauche </span> </p> </td> 
   <td colname="col2"> <p>Marge gauche en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge haut </span> </p> </td> 
   <td colname="col2"> <p>Marge supérieure en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge droite </span> </p> </td> 
   <td colname="col2"> <p>Marge de droite en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de la marge inférieure </span> </p> </td> 
   <td colname="col2"> <p>Marge inférieure en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rayon de bordure </span> </p> </td> 
   <td colname="col2"> <p>Rayon de bordure en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Couleur de fond au format hexadécimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Le point indicateur défini prend en charge le sélecteur d’attributs `state` , qui peut être utilisé pour appliquer différents habillages à différents états de miniature. En particulier, `state="selected"` correspond à la page actuelle des miniatures, `state="unselected"` correspond à l’état de point par défaut.

Exemple - Pour créer un point indicateur défini de 15 x 15 pixels, avec une marge horizontale de deux pixels, une marge supérieure de cinq pixels, une marge inférieure d’un pixel, un rayon de 12 pixels #D5D3D3 couleur par défaut et une couleur active #939393 :

```
.s7mixedmediaviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7mixedmediaviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```
