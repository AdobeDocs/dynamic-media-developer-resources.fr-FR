---
title: Définir l’indicateur
description: Définir l’indicateur est une série de points affichés en bas de la visionneuse. Elle affiche la position actuelle dans l’ensemble.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 7d0827c5-f420-4804-983c-5298ee92b276
TQID: 'https://experienceleague.adobe.com/VF5K2OQes7ej6M1YGwefbZ4LLnsHVuXed0MKXoX79u0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 354
ht-degree: 0%

---

# Définir l’indicateur{#set-indicator}

Définir l’indicateur est une série de points affichés en bas de la visionneuse. Elle affiche la position actuelle dans l’ensemble.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de l’indicateur défini**

L’aspect du conteneur d’indicateurs définis est contrôlé avec le sélecteur de classe CSS suivant :

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
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan au format hexadécimal de l’indicateur défini. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Définir l’indicateur prend en charge le sélecteur d’attributs de mode, que vous pouvez utiliser pour appliquer différents styles pour les modes d’opération numériques et en pointillés. En particulier, `mode="numeric"` correspond au mode de fonctionnement numérique; `mode="dotted"` correspond à l&#39;état point par défaut.

Par exemple, supposons que vous souhaitiez configurer un indicateur défini avec un arrière-plan blanc :

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

L’aspect d’un point indicateur défini individuel est contrôlé par le sélecteur de classe CSS. Elle s’applique aux éléments en mode de fonctionnement pointillé et numérique.

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
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> famille de polices </p> </td> 
   <td colname="col2"> <p>Nom de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de taille de police <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Taille de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de couleur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Couleur de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> un </span> d’alignement vertical </p> </td> 
   <td colname="col2"> <p>Alignement vertical de l’index de bannière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur de ligne <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur du texte de l’index de bannière. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Définir les éléments d’indicateur prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de miniature. En particulier, `state="selected"` correspond à l’élément actif de l’ensemble ; `state="unselected"` correspond à l’état d’élément par défaut.

Par exemple, supposons que vous souhaitiez configurer un indicateur de réglage en mode pointillé pour les ordinateurs de bureau. Vous souhaitez qu’il soit positionné à 20 pixels du bas de la visionneuse. De plus, vous souhaitez que les points non sélectionnés soient noirs avec 50 % de transparence, 15 x 15 pixels avec sept pixels arrondis. Les points sélectionnés sont noirs avec 90 % de transparence, 18 x 18 pixels avec neuf pixels d’angles arrondis. L’espacement entre les points est de cinq pixels.

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
