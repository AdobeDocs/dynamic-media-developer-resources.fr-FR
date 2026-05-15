---
title: Définir l’indicateur
description: Définir l’indicateur est une série de points rendus sur des échantillons lorsqu’une visionneuse est utilisée sur un appareil tactile. Les points aident les utilisateurs à parcourir les pages de miniatures lorsque les boutons de défilement ne sont pas disponibles.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: b1e6734e-a341-45d7-b771-daeb0527cd00
TQID: 'https://experienceleague.adobe.com/y4QBgUjYMAh5-FlbA32Zgg0Peve1FcO-qhDxc0Ypv4M'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 263
ht-degree: 0%

---

# Définir l’indicateur{#set-indicator}

Définir l’indicateur est une série de points rendus sur des échantillons lorsqu’une visionneuse est utilisée sur un appareil tactile. Les points aident les utilisateurs à parcourir les pages de miniatures lorsque les boutons de défilement ne sont pas disponibles.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de l’indicateur défini**

L’aspect du conteneur d’indicateurs définis est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7zoomviewer .s7setindicator
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
   <td colname="col2"> <p>Couleur d’arrière-plan au format hexadécimal de l’indicateur défini. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour créer un indicateur défini avec un arrière-plan blanc :

```
.s7zoomviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

L’aspect d’un point d’indicateur défini individuel est contrôlé par le sélecteur de classe CSS :

`.s7zoomviewer .s7setindicator .s7dot`

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
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur du point indicateur défini. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la marge de gauche </span> </p> </td> 
   <td colname="col2"> <p>Marge de gauche en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de la marge supérieure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Marge supérieure en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> de la marge droite </p> </td> 
   <td colname="col2"> <p>Marge de droite en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de la marge inférieure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Marge inférieure en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de rayon de bordure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Rayon de la bordure en pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan au format hexadécimal </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Définir le point d’indicateur prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de miniature. En particulier, `state="selected"` correspond à la page de miniatures en cours, `state="unselected"` correspond à l’état de point par défaut.

Exemple - Pour créer un point indicateur défini de 15 x 15 pixels, avec une marge horizontale de 2 pixels, une marge supérieure de 5 pixels, une marge inférieure de 1 pixel, un rayon de 12 pixels, une couleur par défaut #D5D3D3 et #939393 couleur active :

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
