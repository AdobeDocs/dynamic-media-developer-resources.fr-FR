---
description: La position du bouton Supprimer les favoris est entièrement gérée par le menu Favoris.
seo-description: La position du bouton Supprimer les favoris est entièrement gérée par le menu Favoris.
seo-title: Bouton Supprimer les favoris
solution: Experience Manager
title: Bouton Supprimer les favoris
uuid: c2e1929d-d859-49d5-8bdc-13507e25d02c
feature: Dynamic Media Classic, Visionneuses, SDK/API, Catalogue électronique
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---


# Supprimer le bouton favori{#remove-favorite-button}

La position du bouton Supprimer les favoris est entièrement gérée par le menu Favoris.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspect du bouton Supprimer les favoris est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7removefavoritebutton
```

**Propriétés CSS du bouton Supprimer les favoris**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p> Positionnez l’objet à l’intérieur de l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
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
>Ce bouton prend en charge les sélecteurs d&#39;attribut `state` et `selected`, qui peuvent être utilisés pour appliquer différents habillages à différents états de bouton. En particulier, `selected='true'` correspond à l’état lorsqu’un utilisateur peut ajouter une nouvelle icône Favori en cliquant ou en appuyant dessus. `selected='false'` correspond au mode de fonctionnement normal lorsqu’un utilisateur peut effectuer un zoom, effectuer un panoramique et permuter des pages.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : pour configurer un bouton Supprimer les favoris de 28 x 28 pixels et afficher une image différente pour chacun des quatre états de bouton différents si sélectionné ou non.

```
.s7ecatalogviewer .s7removefavoritebutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='false'][state='up'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_up.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='false'][state='over'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_over.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='false'][state='down'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_down.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='false'][state='disabled'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_disabled.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='true'][state='up'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_over.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='true'][state='over'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_over.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='true'][state='down'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_over.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='true'][state='disabled'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_disabled.png); 
}
```

