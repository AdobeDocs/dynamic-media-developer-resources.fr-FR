---
description: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2669c8e2-c942-420f-8262-9d76d5c499a2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# PageView.pageturnstyle{#pageview-pageturnstyle}

[!DNL `[PageView.|<containerId>_pageView.]pageturnstyle= *`dividerWidth`*, *`dividerColor`*, *`dividerOpacity`*, *`borderOnOff`*, *`borderColor`*, *`fillColor`*`]

Contrôle l’aspect du composant lorsqu’un [!DNL `PageView.frametransition`] est défini sur [!DNL `turn`] ou sur [!DNL `auto`] sur les systèmes de bureau.

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dividerWidth</span></span> </p> </td> 
   <td colname="col2"> <p> Largeur en pixels de l’ombre du séparateur de page qui sépare les pages de gauche et de droite dans la planche. Il contrôle également la largeur de l’ombre qui s’affiche en regard de la page tournante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Opacité du séparateur</span></span> </p> </td> 
   <td colname="col2"> <p> Couleur de l’ombre au format RRGGBB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Opacité du séparateur</span></span> </p> </td> 
   <td colname="col2"> <p>Opacité de <span class="codeph"> l’ombre comprise entre 0</span> et <span class="codeph"> 1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> Indicateur ( <span class="codeph"> 0</span> ou <span class="codeph"> 1</span>) qui active et désactive la bordure autour de la page qui tourne. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Couleur de bordure</span></span> </p> </td> 
   <td colname="col2"> <p> Couleur de la bordure au format RRGGBB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Couleur de remplissage</span></span> </p> </td> 
   <td colname="col2"> <p> Couleur du remplissage plein de la zone de composant utilisée pendant l’animation du changement de page, au format RRGGBB. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-54c634116cfe4f17813318e07539264c}

Facultatif.

## Par défaut {#section-43fd13f639c2480c82658fafeeaf0846}

[!DNL `40,909090,1,1,909090,FFFFFF`]

## Exemples {#section-bb97b2aac37a43eba11d263ce7049363}

[!DNL `pageturnstyle=20,FF0000,1,1,00FF00,0000FF`]
