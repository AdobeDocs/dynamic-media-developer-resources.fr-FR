---
title: Bouton Supprimer les favoris
description: La position du bouton Supprimer les favoris est entièrement gérée par le menu Favoris .
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4bf4b055-598c-41b9-bc98-c51926c4785f
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---

# Bouton Supprimer les favoris{#remove-favorite-button}

La position du bouton Supprimer les favoris est entièrement gérée par le menu Favoris .

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspect du bouton Supprimer le favori est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7removefavoritebutton
```

**Propriétés CSS du bouton Supprimer le favori**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge les deux `state` et `selected` sélecteurs d’attributs, qui peuvent être utilisés pour appliquer différents habillages à différents états de bouton. En particulier, `selected='true'` correspond à l’état dans lequel un utilisateur peut ajouter une nouvelle icône Favori en cliquant ou en appuyant sur . Et `selected='false'` correspond au mode de fonctionnement normal lorsqu’un utilisateur peut zoomer, effectuer un panoramique et permuter des pages.

L’info-bulle de bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : pour configurer un bouton Supprimer le favori de 28 x 28 pixels et afficher une image différente pour chacun des quatre états de bouton différents lorsqu’il est sélectionné ou non.

```
.s7ecatalogsearchviewer .s7removefavoritebutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7removefavoritebutton[selected='false'][state='up'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7removefavoritebutton[selected='false'][state='over'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7removefavoritebutton[selected='false'][state='down'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7removefavoritebutton[selected='false'][state='disabled'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_disabled.png); 
} 
.s7ecatalogsearchviewer .s7removefavoritebutton[selected='true'][state='up'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7removefavoritebutton[selected='true'][state='over'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7removefavoritebutton[selected='true'][state='down'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7removefavoritebutton[selected='true'][state='disabled'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_disabled.png); 
}
```
