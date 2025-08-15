---
title: Table des matières
description: La table des matières est un bouton situé dans la barre de contrôle principale. Lorsque cette option est activée, un menu déroulant s’affiche, avec une liste d’index et d’étiquettes de pages.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 9b61e269-201d-4083-9c47-0b73d55aa6ed
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 0%

---

# Table des matières{#table-of-contents}

La table des matières est un bouton situé dans la barre de contrôle principale. Lorsque cette option est activée, un menu déroulant s’affiche, avec une liste d’index et d’étiquettes de pages.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

En fonction de la configuration, la liste peut contenir toutes les pages présentes dans le catalogue ou uniquement celles qui ont des étiquettes explicites définies. Sur les ordinateurs de bureau, si la liste est plus longue que l’espace disponible à l’écran, une barre de défilement est affichée sur la droite.

La position et la taille du bouton Table des matières dans l’interface utilisateur de la visionneuse sont contrôlées par le sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7tableofcontents
```

**Propriétés CSS de la table des matières**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge haut </span> </p> </td> 
   <td colname="col2"> <p> Décalage par rapport au haut de la barre de contrôle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge gauche </span> </p> </td> 
   <td colname="col2"> <p> Distance jusqu’au bouton suivant à gauche ou à gauche de la barre de contrôle, s’il s’agit du premier bouton d’une rangée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur du bouton Table des matières. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p> Hauteur du bouton Table des matières. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état donné du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites </a>CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state` , qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton peut être localisée. Pour plus d’informations, voir [Localisation des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) de l’interface utilisateur.

Exemple : pour configurer un bouton Table des matières positionné à 4 pixels du bas et à 43 pixels à gauche de la barre de contrôle principale. La taille est de 28 x 28 pixels, et une image différente est affichée pour chacun des quatre états de bouton différents :

```
.s7ecatalogviewer .s7tableofcontents { 
margin-top: 4px; 
margin-left: 10px; width: 28px; 
 height: 28px; 
} 
.s7ecatalogviewer .s7tableofcontents[state='up'] { 
background-image:url(images/v2/TableOfContents_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='over'] { 
background-image:url(images/v2/TableOfContents_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='down'] { 
background-image:url(images/v2/TableOfContents_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='disabled'] { 
background-image:url(images/v2/TableOfContents_dark_disabled.png); 
}
```

L’aspect du menu déroulant est contrôlé par le sélecteur de classe CSS suivant :

```
 .s7ecatalogviewer .s7tableofcontents .s7panel
```

**Propriétés CSS du panneau déroulant**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan du menu déroulant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p> Décalage interne entre les limites du panneau et le contenu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ombre-boîte </span> </p> </td> 
   <td colname="col2"> <p> Ombre portée autour du panneau. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il n’est pas possible de contrôler la taille ou la position du panneau déroulant à partir de CSS ; Le composant gère sa mise en page par programmation.

Exemple : configurez un menu déroulant avec un arrière-plan noir semi-transparent, une marge de 5 pixels autour du contenu et une ombre portée :

```
.s7ecatalogviewer .s7tableofcontents .s7panel { 
 background-color: rgba(0, 0, 0, 0.5); 
 margin: 5px; 
 box-shadow: 2px 2px 3px #c0c0c0; 
}
```

L’apparence de l’élément individuel est contrôlée par le sélecteur de classe CSS suivant :

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7item
```

**Propriétés CSS de l’élément**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famille de police </span> </p> </td> 
   <td colname="col2"> <p>Nom de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’élément. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rembourrage </span> </p> </td> 
   <td colname="col2"> <p>Rembourrage interne. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>L’élément de liste déroulante prend en charge le sélecteur d’attributs `state` , qui peut être utilisé pour appliquer différents habillages aux états de survol et d’élément sélectionnés.

Exemple : configurez un élément déroulant avec une police Helvetica® de 14 pixels et une hauteur de 19 pixels. Lorsqu’il est sélectionné, un élément a un arrière-plan gris foncé au survol et un arrière-plan gris clair :

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item { 
font-family: Helvetica,sans-serif; 
font-size: 14px; 
height: 19px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item[state="over"] { 
background-color: rgb(102, 102, 102); 
} 
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item[state="selected"] { 
background-color: rgb(178, 178, 178); 
}
```

Un élément qui affiche l’index de page est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index
```

**Propriétés CSS de l’index de page**

<table id="table_FAA5072E4AAC48F4BE00B05D87FD9827"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur min. </span> </p> </td> 
   <td colname="col2"> <p> Largeur minimale de l’élément. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur max. </span> </p> </td> 
   <td colname="col2"> <p> Largeur maximale de l’élément. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Remplissage droit </span> </p> </td> 
   <td colname="col2"> <p> Distance entre l’index de page et le libellé de la page. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il est possible de masquer entièrement l’index de la page en définissant `display:none` la `s7index` classe CSS.

Exemple 1 - Configuration d’un index de page d’une largeur minimale de 40 pixels, d’une largeur maximale de 70 pixels et d’une marge de 5 pixels sur le côté droit :

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
max-width: 70px; 
min-width: 40px; 
padding-right: 5px; 
}
```

Exemple 2 - Masquer l’index de page :

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
display: none; 
}
```

Le libellé de la page est contrôlé par le sélecteur de classe CSS suivant :

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7label
```

**Propriétés CSS du libellé de page**

<table id="table_A42E372D931D4F04855EE5AB5530CB12"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur min. </span> </p> </td> 
   <td colname="col2"> <p> Largeur minimale de l’élément. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur max. </span> </p> </td> 
   <td colname="col2"> <p> Largeur maximale de l’élément. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : configurez un index de page d’une largeur minimale de 40 pixels et d’une largeur maximale de 240 pixels :

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7label { 
min-width: 40px; 
max-width: 240px; 
}
```

S’il y a plus d’éléments que ce qui peut tenir verticalement dans le panneau déroulant et que le système est un bureau, le composant affiche une barre de défilement verticale sur le côté droit du panneau. L’aspect de la zone de la barre de défilement est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar
```

**Propriétés CSS de la barre de défilement**

<table id="table_D34A63AAE6324699ABDCC08355D33035"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur de la barre de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Retour au début </span> </p> </td> 
   <td colname="col2"> <p> La barre de défilement verticale est décalée par rapport au haut de la zone du panneau. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fond </span> </p> </td> 
   <td colname="col2"> <p> La barre de défilement verticale est décalée par rapport au bas de la zone du panneau. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Droite </span> </p> </td> 
   <td colname="col2"> <p> La barre de défilement horizontale est décalée par rapport au bord droit du panneau. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : configurez une barre de défilement de 28 pixels de large sans marge pour la zone supérieure, droite ou inférieure du panneau :

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:28px; 
}
```

La piste de la barre de défilement correspond à la zone située entre les boutons de défilement supérieur et inférieur. Le composant définit automatiquement la position et la hauteur de la piste. La piste est contrôlée par le sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack
```

**Propriétés CSS de la piste de défilement**

<table id="table_E49EE04B3FF64AB2948E7C09DF3EA1B7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de voie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la piste. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - configurez une piste de barre de défilement de 28 pixels de large et avec un arrière-plan gris semi-transparent :

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

Le pouce de la barre de défilement se déplace verticalement dans la zone de piste de défilement. Sa position verticale est contrôlée par la logique du composant. Toutefois, la hauteur de miniature ne change pas dynamiquement en fonction de la quantité de contenu. Vous pouvez configurer la hauteur du pouce et d’autres aspects à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb
```

**Propriétés CSS du pouce de la barre de défilement**

<table id="table_D8DFBC2419BD4AB3B4892AC7B599C70A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du pouce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du pouce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Dessus de rembourrage </span> </p> </td> 
   <td colname="col2"> <p> Le rembourrage vertical entre le haut de la piste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Fond de rembourrage </span> </p> </td> 
   <td colname="col2"> <p>Remplissage vertical entre le bas de la piste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état numérique donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites </a>CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La miniature prend en charge le sélecteur d’attributs `state` , qui peut être utilisé pour appliquer différents habillages aux `up`états , `down`, `over`et `disabled` thumb.

Exemple : configurez une barre de défilement de 28 x 45 pixels, avec des marges de 10 pixels en haut et en bas et avec des illustrations différentes pour chaque état :

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

L’apparence des boutons de défilement supérieur et inférieur est contrôlée par les sélecteurs de classe CSS suivants :

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton
```

Il n’est pas possible de positionner les boutons de défilement à l’aide de CSS `top`, `left`, `bottom`et `right` de ses propriétés ; au lieu de cela, la logique de la visionneuse les positionne automatiquement.

**Propriétés CSS des boutons de défilement vers le haut et vers le bas**

<table id="table_89561098E43D44C2865267687BBF38F4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état donné du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites </a>CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Le bouton prend en charge le sélecteur d’attributs `state` , qui peut être utilisé pour appliquer différents habillages aux `up`états , `down`, `over`et `disabled` bouton.

L’info-bulle du bouton peut être localisée. Pour plus d’informations, voir [Localisation des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) de l’interface utilisateur.

Exemple : configurez des boutons de défilement de 28 x 32 pixels avec des illustrations différentes pour chaque état :

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```
