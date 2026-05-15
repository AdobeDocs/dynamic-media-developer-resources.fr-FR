---
title: Bouton Rechercher
description: Bouton Rechercher
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ede7d887-526b-4e00-9885-166dc37627aa
TQID: 'https://experienceleague.adobe.com/4isGidoN0mJG46pDeAmgLqLr-8SZihdjUBEJ4HkBKVU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 191
ht-degree: 0%

---

# Bouton Rechercher{#search-button}

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect du bouton est contrôlé avec le sélecteur de classe CSS suivant :

`.s7ecatalogsearchviewer .s7searchbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de la marge supérieure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Décalage par rapport au haut de la barre de contrôle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la marge de gauche </span> </p> </td> 
   <td colname="col2"> <p> Distance par rapport au bouton suivant à gauche, ou sur le côté gauche de la barre de contrôle si ce bouton est le premier d’une ligne. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge les sélecteurs d&#39;attributs `state` et `selected`, qui peuvent être utilisés pour appliquer différents habillages à différents états de bouton.
>
>En particulier, `selected='false'` correspond à l&#39;état initial du bouton de défilement, et `selected='true'` correspond à l&#39;état lorsque le panneau de recherche est actif.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : pour configurer un bouton de recherche de 28 x 28 pixels qui affiche une image différente pour chacun des quatre états de bouton, qu’il soit sélectionné ou non.

```
.s7ecatalogsearchviewer .s7searchbutton{ 
 margin-top: 4px; 
 margin-left: 10px; 
 width:28px; 
 height:28px;  
 display: inline-block; 
 background-size:contain; 
} 
 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/Search_dark_up.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/Search_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/Search_dark_down.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/Search_dark_disabled.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/Search_dark_over.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/Search_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/Search_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/Search_dark_disabled.png);  
}
```
