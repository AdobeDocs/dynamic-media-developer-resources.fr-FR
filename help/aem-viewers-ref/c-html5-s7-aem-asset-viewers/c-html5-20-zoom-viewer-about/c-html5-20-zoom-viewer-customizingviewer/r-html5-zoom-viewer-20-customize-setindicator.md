---
title: Indicateur de définition
description: L’indicateur de définition est une série de points affichés au-dessus des échantillons lorsqu’une visionneuse est utilisée sur un appareil tactile. Les points aident les utilisateurs à parcourir les pages des miniatures lorsque les boutons de défilement ne sont pas disponibles.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: b1e6734e-a341-45d7-b771-daeb0527cd00
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# Indicateur de définition{#set-indicator}

L’indicateur de définition est une série de points affichés au-dessus des échantillons lorsqu’une visionneuse est utilisée sur un appareil tactile. Les points aident les utilisateurs à parcourir les pages des miniatures lorsque les boutons de défilement ne sont pas disponibles.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de l’indicateur défini**

L’aspect du conteneur d’indicateur défini est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7zoomviewer .s7setindicator
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan au format hexadécimal de l’indicateur défini. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour créer un indicateur d&#39;ensemble avec un arrière-plan blanc :

```
.s7zoomviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

L’aspect d’un point indicateur de définition individuel est contrôlé à l’aide du sélecteur de classe CSS :

`.s7zoomviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
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
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p>Marge gauche en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p>Marge supérieure en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan au format hexadécimal. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>L’indicateur Set prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de miniature. En particulier, `state="selected"` correspond à la page actuelle des miniatures, `state="unselected"` correspond à l’état du point par défaut.

Exemple : pour créer un point d’indicateur fixe de 15 x 15 pixels, avec une marge horizontale de 2 pixels, une marge supérieure de 5 pixels, une marge inférieure de 1 pixel, un rayon de 12 pixels, #D5D3D3 couleur par défaut et #939393 couleur active :

```
.s7zoomviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7zoomviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```
