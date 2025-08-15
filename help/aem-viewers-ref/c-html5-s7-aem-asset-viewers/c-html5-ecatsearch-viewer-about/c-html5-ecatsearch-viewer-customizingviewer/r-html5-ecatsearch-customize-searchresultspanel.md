---
title: Search panneau Résultats
description: Le panneau des résultats de la recherche se compose de la zone de saisie de recherche en haut et de la zone principale où les messages d’information ou les résultats de recherche sont affichés.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ffbbc2ae-60da-4c3d-a350-6dbcb64e189d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '938'
ht-degree: 0%

---

# Search panneau Résultats{#search-results-panel}

Le panneau des résultats de la recherche se compose de la zone de saisie de recherche en haut et de la zone principale où les messages d’information ou les résultats de recherche sont affichés.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone principale de la visionneuse**

Lorsque le panneau est actif, l’interface utilisateur de la visionneuse est recouverte d’un remplissage semi-transparent. La couleur et l’opacité de ce remplissage sont contrôlées par le sélecteur de classe CSS suivant :

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
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Couleur du recouvrement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacité </span> </p> </td> 
   <td colname="col2"> <p>Opacité de la couleur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le panneau des résultats de la recherche occupe toujours toute la hauteur de visionneuse disponible. Vous pouvez toutefois configurer la largeur. Vous pouvez définir la largeur sur une valeur absolue en pixels, qui est un paramètre par défaut pour les points d’arrêt de taille moyenne et grande. Vous pouvez également définir la largeur sur 100 % pour que le panneau des résultats de la recherche occupe toute la zone de visionneuse. La largeur du panneau est contrôlée par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchresultspace
```

**Propriété CSS de l’espace de résultats de la recherche**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur de l’espace des résultats de la recherche. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer un panneau de résultats de recherche de 250 pixels de large sur des points d’arrêt de grande et moyenne taille et utiliser un panneau pleine grandeur sur un point d’arrêt de petite taille :

```
.s7ecatalogsearchviewer.s7size_large .s7searchpanel .s7searchresultspanel, .s7ecatalogsearchviewer.s7size_medium .s7searchpanel .s7searchresultspanel { 
 width:250px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7searchpanel .s7searchresultspanel { 
 width:100%; 
}
```

La partie supérieure du panneau des résultats de la recherche est dédiée à la zone de saisie de recherche. Le remplissage sur les côtés de la zone de saisie est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputcontainer
```

**Propriétés CSS du conteneur d’entrées de recherche**

<table id="table_A1B96108542742DC8DCBCC9064F9E90B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rembourrage </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure autour de la zone de saisie. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le champ de saisie de recherche est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput
```

**Propriétés CSS du champ de saisie de recherche**

<table id="table_9FB5E89847BF4C889DC22AD7E842C0F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du champ de saisie de recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Remplissage gauche </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure entre les limites du champ de saisie et le texte d’entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> frontière </span> </p> </td> 
   <td colname="col2"> <p>Bordure du champ de saisie de recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p>Marge du champ de saisie de recherche </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille de la police du texte. </p> </td> 
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

Le bouton de recherche situé à gauche du champ de saisie de recherche sous la forme du « miroir » est contrôlé par défaut par le sélecteur de classe CSS suivant :

```
 .s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton
```

**Propriétés CSS du bouton de saisie de recherche**

<table id="table_CDD818B40BB1416CB47B7C52F799DE0C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton de saisie de recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton de saisie de recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>URL de l’icône « miroir ». </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de fond </span> </p> </td> 
   <td colname="col2"> <p>Taille de l’icône « miroir ». </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> frontière </span> </p> </td> 
   <td colname="col2"> <p>Bordure du bouton de saisie de la recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p>Marge du bouton de saisie de la recherche. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour configurer un bouton de recherche avec une icône « miroir » de 26 x 26 pixels ; Une taille de 30 pixels avec une bordure de 1 pixel :

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

Le panneau des résultats de la recherche peut afficher une invite textuelle lorsque la fonctionnalité est appelée pour la première fois. Il affiche également un message lorsque la recherche d’un utilisateur ne renvoie aucun résultat. Dans tous les cas, le texte apparaît dans la partie principale du panneau des résultats de la recherche et est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo
```

**Propriétés CSS des informations de recherche**

<table id="table_1DF5A12A21584FCC8C25F170078FEFE6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famille de police </span> </p> </td> 
   <td colname="col2"> <p>Nom de la police de texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alignement de police </span> </p> </td> 
   <td colname="col2"> <p>Alignement de texte horizontal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille du texte de police. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce panneau de texte prend en charge le sélecteur d’attributs `state` , qui peut être utilisé pour appliquer différents styles à différents messages texte. En particulier, `state='prompt'` correspond à l’invite de texte affichée lorsque le panneau est appelé pour la première fois. Le `state='results'` correspond au texte avec des informations sur les résultats de recherche. Enfin, le `state='no_results'` correspond au texte affiché lorsque la requête de recherche n’a renvoyé aucun résultat.

Le texte du message peut être localisé. Pour plus d’informations, voir [Localisation des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) de l’interface utilisateur.

Exemple - Pour configurer un panneau de texte qui utilise une police grise de 18 pixels :

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo { 
 font-size: 18px; 
 color: #696969; 
}
```

Search résultats sont rendus sous la forme d’une seule colonne ou d’une seule ligne de miniatures pour les pages contenant des résultats de recherche. L’espacement entre les miniatures des résultats de recherche est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell
```

**Propriétés CSS des cellules de miniature**

<table id="table_26974E509F6943BB98CBC1E4BAE62D68"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p> Taille de la marge verticale autour de chaque miniature. L’espacement réel des vignettes est égal à la somme des marges supérieure et inférieure définies pour <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour configurer l’espacement des dix pixels :

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

L’apparence des miniatures individuelles est contrôlée par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb
```

**Propriétés CSS de la miniature**

<table id="table_00829E44F75040A4B2AE19ACD550DA1E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> frontière </span> </p> </td> 
   <td colname="col2"> <p>Bordure de la miniature. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple – Pour configurer des miniatures de 215 x 129 pixels, avoir une bordure par défaut gris clair et une bordure sélectionnée gris foncé :

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb { 
 width: 215px; 
 height: 129px; 
}
```

L’apparence du libellé de la miniature est contrôlée par le sélecteur de classe CSS suivant :

```
 .s7ecatalogsearchviewer 
.s7searchpanel .s7swatches .s7label
```

**Propriétés CSS du libellé**

<table id="table_CA669F6AE7574FF389BF725B3F768E5E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur de texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famille de police </span> </p> </td> 
   <td colname="col2"> <p>Nom de la police de texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille de la police du texte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour configurer des étiquettes utilisant la police Helvetica® grise, 12 pixels :

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7label { 
 font-family: Helvetica,sans-serif; 
 color: #4c4c4c; 
 font-size: 12px; 
}
```

Sur les systèmes qui utilisent l’entrée de la souris, deux boutons de défilement apparaissent en bas du panneau des résultats de la recherche pour permettre à un utilisateur de faire défiler les résultats de la recherche. L’aspect des boutons de défilement vers le haut et vers le bas est contrôlé par les sélecteurs de classe CSS suivants :

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton
```

Il n’est pas possible de positionner les boutons de défilement à l’aide des propriétés CSS haut, gauche, bas et droite. Au lieu de cela, la logique de la visionneuse les positionne automatiquement.

**Propriétés CSS des boutons de défilement vers le haut et vers le bas**

<table id="table_11063C7F428D4707A8138F17650F8F5F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état donné du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Position à l’intérieur du sprite de l’illustration, si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites </a>CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state` , qui peut être utilisé pour appliquer différents habillages aux `"up"`états , `"down"`, `"over"`et `"disabled"` bouton.

Les info-bulles des boutons peuvent être localisées. Pour plus d’informations, voir [Localisation des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) de l’interface utilisateur.

Exemple - Pour configurer un bouton de défilement vers le haut de 125 x 35 pixels avec une illustration différente pour chaque état :

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
