---
title: PageView.pageturnstyle
description: PageView.pageturnstyle
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 00706c64-c051-4b62-8194-61d0a1c565e9
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# PageView.pageturnstyle{#pageview-pageturnstyle}

` [PageView.|<containerId>_pageView.]pageturnstyle= *`dialogWidth`*, *`dialogColor`*, *`dialogOpacity`*, *`borderOnOff`*, *`borderColor`*, *`fillColor`*`

Contrôle l’aspect du composant lorsqu’un `PageView.frametransition` est défini sur `turn` ou sur `auto` sur des systèmes de bureau.

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> diviseurLargeur</span></span> </p> </td> 
   <td colname="col2"> <p> Largeur en pixels de l’ombre du séparateur de page qui sépare les pages de gauche et de droite dans la planche. Il contrôle également la largeur de l'ombre portée affichée à côté de la page tournante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">OpacitéDiviseur</span></span> </p> </td> 
   <td colname="col2"> <p> Couleur d’ombre au format RVB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">OpacitéDiviseur</span></span> </p> </td> 
   <td colname="col2"> <p>Opacité de l'ombre comprise entre <span class="codeph"> 0</span> et <span class="codeph"> 1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> Indicateur (<span class="codeph"> 0</span> ou <span class="codeph"> 1</span>) qui active et désactive la bordure autour de la page de démarrage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> Couleur de bordure au format RVB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> Couleur du remplissage uni de la zone du composant utilisée lors de l’animation de tournage de page, au format RVB. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-54c634116cfe4f17813318e07539264c}

Facultatif.

## Par défaut {#section-43fd13f639c2480c82658fafeeaf0846}

`40,909090,1,1,909090,FFFFFF`

## Exemples {#section-bb97b2aac37a43eba11d263ce7049363}

`pageturnstyle=20,FF0000,1,1,00FF00,0000FF`
