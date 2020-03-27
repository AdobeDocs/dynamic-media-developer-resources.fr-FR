---
description: Le déroulant du menu Favoris apparaît dans la barre de contrôle. Il s’agit d’un bouton et d’un panneau qui se développe lorsqu’un utilisateur clique ou appuie sur un bouton. Le panneau contient des outils Favoris individuels.
seo-description: Le déroulant du menu Favoris apparaît dans la barre de contrôle. Il s’agit d’un bouton et d’un panneau qui se développe lorsqu’un utilisateur clique ou appuie sur un bouton. Le panneau contient des outils Favoris individuels.
seo-title: Menu Favoris
solution: Experience Manager
title: Menu Favoris
topic: Dynamic media
uuid: 46de2a74-690e-4010-8a71-54206dd02fd0
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Menu Favoris{#favorites-menu}

Le déroulant du menu Favoris apparaît dans la barre de contrôle. Il s’agit d’un bouton et d’un panneau qui se développe lorsqu’un utilisateur clique ou appuie sur un bouton. Le panneau contient des outils Favoris individuels.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La position et la taille du menu Favoris dans l’interface utilisateur du lecteur de contenu sont contrôlées à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7favoritesmenu
```

**Propriétés CSS du bouton du menu Favoris**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge-haut </span> </p> </td> 
   <td colname="col2"> <p> Décalage à partir du haut de la barre de contrôle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge-gauche </span> </p> </td> 
   <td colname="col2"> <p> Distance du bouton suivant à gauche ou du côté gauche de la barre de contrôle s’il s’agit du premier bouton d’une rangée. </p> </td> 
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

Exemple : configurez un menu Favoris positionné à 4 pixels du haut de la barre de contrôle et à 10 pixels du bouton le plus proche à gauche et de 28 x 28 pixels.

```
.s7ecatalogsearchviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

L’aspect du bouton du menu Favoris est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton
```

**Propriétés CSS du bouton Favoris**

<table id="table_970D62A1413145E0A964FA9D9F108579"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-image </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p> Positionnez-vous à l’intérieur de l’image-objet d’illustration, si des images-objets CSS sont utilisées. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’ `state` attributs, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton peut être localisée. Pour plus d’informations, voir [des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) de l’interface utilisateur.

Exemple : configurez un bouton de menu Favoris qui affiche une image différente pour chacun des quatre états de bouton.

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='up'] { 
background-image:url(images/v2/FavoritesMenu dark_up.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='over'] { 
background-image:url(images/v2/FavoritesMenu_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='down'] { 
background-image:url(images/v2/FavoritesMenu_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='disabled'] { 
background-image:url(images/v2/FavoritesMenu_dark_disabled.png); 
}
```

L’aspect du panneau contenant les icônes Favoris individuelles est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesmenupanel
```

**Propriétés CSS du panneau du menu Favoris**

<table id="table_B57B44C561E94F86BB1B0EC1671F26DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan du panneau. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : configurez un panneau pour obtenir une couleur transparente.

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```

