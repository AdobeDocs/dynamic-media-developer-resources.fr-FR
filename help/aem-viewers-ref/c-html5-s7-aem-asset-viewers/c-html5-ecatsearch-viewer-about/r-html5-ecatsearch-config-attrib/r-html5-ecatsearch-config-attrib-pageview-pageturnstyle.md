---
description: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2669c8e2-c942-420f-8262-9d76d5c499a2
TQID: 'https://experienceleague.adobe.com/aO-r0pyOX-Qv8OA1B6mqXHDl34kjZXqwPTlV7rU0fAA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 119
ht-degree: 2%

---

# PageView.pageturnstyle{#pageview-pageturnstyle}

[!DNL `[PageView.|<containerId>_pageView.]pageturnstyle= *`dialogWidth`*, *`dialogColor`*, *`dialogOpacity`*, *`borderOnOff`*, *`borderColor`*, *`fillColor`*`]

Contrôle l’aspect du composant lorsqu’un [!DNL `PageView.frametransition`] est défini sur [!DNL `turn`] ou sur [!DNL `auto`] sur des systèmes de bureau.

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

[!DNL `40,909090,1,1,909090,FFFFFF`]

## Exemples {#section-bb97b2aac37a43eba11d263ce7049363}

[!DNL `pageturnstyle=20,FF0000,1,1,00FF00,0000FF`]
