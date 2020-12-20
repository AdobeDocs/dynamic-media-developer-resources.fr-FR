---
description: Le panneau des résultats de la recherche se compose de la zone d’entrée de la recherche en haut et de la zone principale dans laquelle s’affichent les messages d’information ou les résultats de la recherche.
seo-description: Le panneau des résultats de la recherche se compose de la zone d’entrée de la recherche en haut et de la zone principale dans laquelle s’affichent les messages d’information ou les résultats de la recherche.
seo-title: Panneau Résultats de la recherche
solution: Experience Manager
title: Panneau Résultats de la recherche
topic: Dynamic media
uuid: 43d8e003-79f7-4e41-98d7-b362ab7180ea
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '952'
ht-degree: 1%

---


# Panneau des résultats de la recherche{#search-results-panel}

Le panneau des résultats de la recherche se compose de la zone d’entrée de la recherche en haut et de la zone principale dans laquelle s’affichent les messages d’information ou les résultats de la recherche.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visualisation principale**

Lorsque le panneau est principal, l’interface utilisateur du lecteur est recouverte d’un remplissage semi-transparent. La couleur et l’opacité de ce remplissage sont contrôlées à l’aide du sélecteur de classe CSS suivant :

```
.s7ecatalogviewer .s7searchpanel .s7backoverlay
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
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p>Couleur de l’incrustation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacité  </span> </p> </td> 
   <td colname="col2"> <p>Opacité de la couleur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le panneau des résultats de la recherche occupe toujours toute la hauteur de visionneuse disponible. Cependant, vous pouvez configurer la largeur. Vous pouvez définir la largeur sur une valeur en pixels absolus, ce qui est un paramètre par défaut pour les points d’arrêt de taille moyenne et grande. Vous pouvez également définir la largeur sur 100 % pour que le panneau des résultats de la recherche occupe l’intégralité de la zone de visualisation. La largeur du panneau est contrôlée par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchresultspace
```

**Propriété CSS de l’espace de résultats de la recherche**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Largeur de l’espace de résultats de la recherche. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer un panneau de résultats de recherche de 250 pixels de large sur des points d’arrêt de taille large et moyenne et utiliser un panneau de taille réelle sur un point d’arrêt de taille réduite :

```
.s7ecatalogsearchviewer.s7size_large .s7searchpanel .s7searchresultspanel, .s7ecatalogsearchviewer.s7size_medium .s7searchpanel .s7searchresultspanel { 
 width:250px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7searchpanel .s7searchresultspanel { 
 width:100%; 
}
```

La partie supérieure du panneau des résultats de la recherche est consacrée à la zone d’entrée de la recherche. Le remplissage sur les côtés de la zone de saisie est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputcontainer
```

**Propriétés CSS du conteneur d’entrée de recherche**

<table id="table_A1B96108542742DC8DCBCC9064F9E90B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure autour de la zone de saisie. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le champ de saisie de recherche est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput
```

**Propriétés CSS du champ de saisie de la recherche**

<table id="table_9FB5E89847BF4C889DC22AD7E842C0F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du champ de saisie de la recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage-gauche  </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure entre les limites du champ de saisie et le texte de saisie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p>Bordure du champ de saisie de la recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>Marge du champ de saisie de la recherche </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Taille de la police de texte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour configurer un champ de saisie de recherche avec une hauteur de 0 pixel et une police de texte de 14 pixels :

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput { 
 padding-left:5px; 
 height:30px; 
 font-size:14px; 
}
```

Le bouton de recherche situé à gauche du champ de saisie de la recherche sous la forme du &quot;miroir&quot; par défaut est contrôlé par le sélecteur de classe CSS suivant :

```
 .s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton
```

**Propriétés CSS du bouton d’entrée de recherche**

<table id="table_CDD818B40BB1416CB47B7C52F799DE0C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton d’entrée de recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur  </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton d’entrée de recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p>URL de l’icône "en forme de verre". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p>Taille de l'icône "en verre". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p>Bordure du bouton d’entrée de recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge  </span> </p> </td> 
   <td colname="col2"> <p>Marge du bouton d’entrée de recherche. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour configurer un bouton de recherche avec une icône &quot;en verre&quot; de 26 x 26 pixels ; Taille de 30 pixels avec bordure de 1 pixel :

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton { 
 width:30px; 
 height:30px; 
 background-size:26px 26px; 
 background-image: url(images/v2/Search_form_field.png); 
 font-size:14px; 
 border: 1px solid #696969; 
}
```

Le panneau des résultats de la recherche peut afficher une invite textuelle lors du premier appel de la fonction. Il affiche également un message à l’utilisateur lorsque sa recherche n’a retourné aucun résultat. Dans tous les cas, le texte apparaît dans la partie principale du panneau des résultats de la recherche et est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo
```

**Propriétés CSS des informations de recherche**

<table id="table_1DF5A12A21584FCC8C25F170078FEFE6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Couleur du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nom de la police de texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align  </span> </p> </td> 
   <td colname="col2"> <p>Alignement horizontal du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Taille du texte de la police. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce panneau de texte prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents styles à différents messages texte. En particulier, `state='prompt'` correspond à l’invite de texte affichée lorsque le panneau est appelé pour la première fois ; `state='results'` correspond au texte contenant des informations sur les accès à la recherche ; et `state='no_results'` correspond au texte affiché lorsque la requête de recherche ne renvoyait aucun résultat.

Le texte du message peut être localisé. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple - pour configurer un panneau de texte qui utilise une police grise de 18 pixels :

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo { 
 font-size: 18px; 
 color: #696969; 
}
```

Les résultats de la recherche sont affichés sous la forme d’une seule colonne ou d’une seule ligne de miniatures pour les pages avec accès à la recherche. L’espacement entre les miniatures des résultats de la recherche est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell
```

**Propriétés CSS des cellules de miniature**

<table id="table_26974E509F6943BB98CBC1E4BAE62D68"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge  </span> </p> </td> 
   <td colname="col2"> <p> Taille de la marge verticale autour de chaque miniature. L’espacement réel des miniatures correspond à la somme des marges supérieure et inférieure définies pour <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour configurer l’espacement de 10 pixels :

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

L’aspect des miniatures individuelles est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb
```

**Propriétés CSS de la miniature**

<table id="table_00829E44F75040A4B2AE19ACD550DA1E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur  </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p>Bordure de la miniature. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer des miniatures de 215 x 129 pixels, avec une bordure par défaut gris clair et une bordure sélectionnée gris foncé :

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb { 
 width: 215px; 
 height: 129px; 
}
```

L’aspect du libellé de la miniature est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
 .s7ecatalogsearchviewer 
.s7searchpanel .s7swatches .s7label
```

**Propriétés CSS du libellé**

<table id="table_CA669F6AE7574FF389BF725B3F768E5E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p> Couleur du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nom de la police de texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Taille de la police de texte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour configurer des libellés qui utilisent une police Helvetica de 12 pixels, grise, grise :

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7label { 
 font-family: Helvetica,sans-serif; 
 color: #4c4c4c; 
 font-size: 12px; 
}
```

Sur les systèmes qui utilisent la saisie de la souris, deux boutons de défilement s’affichent au bas du panneau des résultats de la recherche pour permettre à l’utilisateur de faire défiler les résultats de la recherche. L’aspect des boutons de défilement vers le haut et vers le bas est contrôlé par les sélecteurs de classe CSS suivants :

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton
```

Il n’est pas possible de positionner les boutons de défilement à l’aide des propriétés CSS top, left, bottom et right. Au lieu de cela, la logique du lecteur les positionne automatiquement.

**Propriétés CSS des boutons de défilement vers le haut et vers le bas**

<table id="table_11063C7F428D4707A8138F17650F8F5F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur  </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p> Positionnez l’objet à l’intérieur de l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages aux états de bouton `"up"`, `"down"`, `"over"` et `"disabled"`.

Les info-bulles des boutons peuvent être localisées. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : pour configurer un bouton de défilement vers le haut de 125 x 35 pixels et dont l’illustration est différente pour chaque état :

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_disabled.png);
```

