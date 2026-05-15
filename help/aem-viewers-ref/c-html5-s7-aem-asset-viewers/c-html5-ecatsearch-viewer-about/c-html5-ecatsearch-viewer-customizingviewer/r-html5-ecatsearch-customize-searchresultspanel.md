---
title: Panneau Résultats de la recherche
description: Le panneau des résultats de la recherche comprend la zone de saisie de la recherche en haut et la zone principale où s’affichent les messages d’information ou les résultats de la recherche.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ffbbc2ae-60da-4c3d-a350-6dbcb64e189d
TQID: 'https://experienceleague.adobe.com/VVRqhgxbkQOHlerVRDGNaHL-tM6elPDs-Vqotij43mg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 955
ht-degree: 0%

---

# Panneau Résultats de la recherche{#search-results-panel}

Le panneau des résultats de la recherche comprend la zone de saisie de la recherche en haut et la zone principale où s’affichent les messages d’information ou les résultats de la recherche.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

Lorsque le panneau est actif, l’interface utilisateur de la visionneuse est recouverte d’un remplissage semi-transparent. La couleur et l’opacité de ce remplissage sont contrôlées avec le sélecteur de classe CSS suivant :

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
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur du recouvrement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> d’opacité <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Opacité de la couleur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le panneau des résultats de recherche occupe toujours toute la hauteur de visionneuse disponible. Vous pouvez toutefois configurer la largeur. Vous pouvez définir la largeur sur une valeur absolue en pixels, qui est un paramètre par défaut pour les points d’arrêt de taille moyenne et grande. Vous pouvez également définir la largeur sur 100 % pour que le panneau des résultats de recherche occupe toute la zone de la visionneuse. La largeur du panneau est contrôlée par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchresultspace
```

**Propriété CSS de l’espace de résultats de recherche**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur de l’espace des résultats de recherche. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour configurer un panneau de résultats de recherche de 250 pixels de large sur des points d’arrêt de taille moyenne et grande et utiliser un panneau de taille réelle sur un point d’arrêt de petite taille :

```
.s7ecatalogsearchviewer.s7size_large .s7searchpanel .s7searchresultspanel, .s7ecatalogsearchviewer.s7size_medium .s7searchpanel .s7searchresultspanel { 
 width:250px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7searchpanel .s7searchresultspanel { 
 width:100%; 
}
```

La partie supérieure du panneau des résultats de la recherche est dédiée à la zone de saisie de la recherche. La marge intérieure sur les côtés de la zone de saisie est contrôlée par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputcontainer
```

**Propriétés CSS du conteneur d’entrée de recherche**

<table id="table_A1B96108542742DC8DCBCC9064F9E90B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> de marge intérieure <span class="codeph"> </p> </td> 
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
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur du champ de saisie de recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de marge intérieure gauche <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Marge intérieure entre les limites du champ de saisie et le texte saisi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de bordure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Bordure du champ de saisie de recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de la marge <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Marge du champ de saisie de recherche </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de taille de police <span class="codeph"> </p> </td> 
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

Le bouton de recherche situé à gauche du champ de saisie de recherche sous la forme du « miroir » est par défaut contrôlé par le sélecteur de classe CSS suivant :

```
 .s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton
```

**Propriétés CSS du bouton d’entrée de recherche**

<table id="table_CDD818B40BB1416CB47B7C52F799DE0C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton de saisie de la recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton de saisie de recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p>URL de l’image de l’icône en forme de « miroir ». </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la taille de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Taille de l’icône « Look Glass ». </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de bordure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Bordure du bouton de saisie de recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de la marge <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Marge du bouton de saisie de recherche. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour configurer un bouton de recherche avec une icône « Look Glass » de 26 x 26 pixels ; taille de 30 pixels avec une bordure de 1 pixel :

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

Le panneau des résultats de la recherche peut afficher une invite textuelle lors du premier appel de la fonction. Elle affiche également un message lorsque la recherche d’un utilisateur n’a renvoyé aucun résultat. Dans tous les cas, le texte s’affiche dans la partie principale du panneau des résultats de recherche et est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo
```

**Propriétés CSS des informations de recherche**

<table id="table_1DF5A12A21584FCC8C25F170078FEFE6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> de couleur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Couleur du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> famille de polices </p> </td> 
   <td colname="col2"> <p>Nom de la police de texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> d’alignement des polices </p> </td> 
   <td colname="col2"> <p>Alignement horizontal du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de taille de police <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Taille du texte de la police. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce panneau de texte prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents styles à différents messages de texte. En particulier, `state='prompt'` correspond à l’invite de texte affichée lorsque le panneau est appelé pour la première fois. La `state='results'` correspond au texte contenant des informations sur les accès de recherche. Enfin, la `state='no_results'` correspond au texte affiché lorsque la requête de recherche n’a renvoyé aucun résultat.

Le texte du message peut être localisé. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple - Pour configurer un panneau de texte qui utilise une police grise de 18 pixels :

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo { 
 font-size: 18px; 
 color: #696969; 
}
```

Les résultats de la recherche sont générés en une seule colonne ou une seule ligne de miniatures pour les pages comportant des accès de recherche. L’espacement entre les miniatures des résultats de recherche est contrôlé avec le sélecteur de classe CSS suivant :

```
.ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell
```

**Propriétés CSS des cellules des miniatures**

<table id="table_26974E509F6943BB98CBC1E4BAE62D68"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> de la marge <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Taille de la marge verticale autour de chaque miniature. L’espacement réel des miniatures est égal à la somme des marges supérieure et inférieure définies pour <span class="codeph">’</span> .s7thumbcell. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour configurer l’espacement de dix pixels :

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

L’aspect des miniatures individuelles est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb
```

**Propriétés CSS de la miniature**

<table id="table_00829E44F75040A4B2AE19ACD550DA1E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur de la miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de bordure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Bordure de la miniature. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour configurer des miniatures de 215 x 129 pixels, ayant une bordure par défaut gris clair et une bordure sélectionnée gris foncé :

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb { 
 width: 215px; 
 height: 129px; 
}
```

L’aspect du libellé de la miniature est contrôlé par le sélecteur de classe CSS suivant :

```
 .s7ecatalogsearchviewer 
.s7searchpanel .s7swatches .s7label
```

**Propriétés CSS du libellé**

<table id="table_CA669F6AE7574FF389BF725B3F768E5E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> de couleur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Couleur du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> famille de polices </p> </td> 
   <td colname="col2"> <p>Nom de la police de texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de taille de police <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Taille de la police du texte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour configurer des libellés qui utilisent une police Helvetica® grise de 12 pixels :

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7label { 
 font-family: Helvetica,sans-serif; 
 color: #4c4c4c; 
 font-size: 12px; 
}
```

Sur les systèmes qui utilisent la souris, deux boutons de défilement s’affichent au bas du panneau des résultats de recherche pour permettre à l’utilisateur ou à l’utilisatrice de faire défiler les résultats de la recherche. L’aspect des boutons de défilement vers le haut et vers le bas est contrôlé avec les sélecteurs de classe CSS suivants :

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton
```

Il n’est pas possible de positionner des boutons de défilement à l’aide des propriétés CSS haut, gauche, bas et droite. Au lieu de cela, la logique de la visionneuse les positionne automatiquement.

**Propriétés CSS des boutons de défilement vers le haut et vers le bas**

<table id="table_11063C7F428D4707A8138F17650F8F5F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d&#39;attributs de `state`, qui peut être utilisé pour appliquer différents habillages aux états des boutons `"up"`, `"down"`, `"over"` et `"disabled"`.

Les info-bulles des boutons peuvent être localisées. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

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
