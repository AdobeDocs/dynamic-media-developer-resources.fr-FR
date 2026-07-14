---
title: Table des matières
description: La table des matières est un bouton situé dans la barre de contrôle principale. Une fois activé, un panneau déroulant s’affiche avec une liste d’index et de libellés de page.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: bc597c68-b86c-4577-9d24-6999eccada78
TQID: 'https://experienceleague.adobe.com/STVKP5765wmXV8odE0wkEvtlP2WFXLJzSDgN4zYec74'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 1110
ht-degree: 0%

---

# Table des matières{#table-of-contents}

La table des matières est un bouton situé dans la barre de contrôle principale. Une fois activé, un panneau déroulant s’affiche avec une liste d’index et de libellés de page.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Selon la configuration, la liste peut contenir toutes les pages présentes dans le catalogue ou uniquement les pages dont les libellés explicites sont définis. Sur les ordinateurs de bureau, si la liste est plus longue que l’écran disponible, une barre de défilement s’affiche à droite.

La position et la taille du bouton de la table des matières dans l’interface utilisateur de la visionneuse sont contrôlées avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7tableofcontents
```

**Propriétés CSS de la table des matières**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> de la marge supérieure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Décalage par rapport au haut de la barre de contrôle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la marge de gauche </span> </p> </td> 
   <td colname="col2"> <p> Distance par rapport au bouton suivant à gauche, ou sur le côté gauche de la barre de contrôle si ce bouton est le premier d’une ligne. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur du bouton Table des matières. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Hauteur du bouton de la table des matières. </p> </td> 
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
>Ce bouton prend en charge le sélecteur d&#39;attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple - Configurez un bouton de table des matières positionné à 4 pixels du bas et à 43 pixels de la gauche de la barre de contrôle principale. La taille est de 28 x 28 pixels et une image différente s’affiche pour chacun des quatre états de bouton différents :

```
.s7ecatalogsearchviewer .s7tableofcontents { 
margin-top: 4px; 
margin-left: 10px; width: 28px; 
 height: 28px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='up'] { 
background-image:url(images/v2/TableOfContents_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='over'] { 
background-image:url(images/v2/TableOfContents_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='down'] { 
background-image:url(images/v2/TableOfContents_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='disabled'] { 
background-image:url(images/v2/TableOfContents_dark_disabled.png); 
}
```

L’aspect du panneau déroulant est contrôlé avec le sélecteur de classe CSS suivant :

```
 .s7ecatalogsearchviewer .s7tableofcontents .s7panel
```

**Propriétés CSS du panneau déroulant**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan du panneau déroulant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de la marge <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Décalage interne entre les limites du panneau et le contenu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> d'ombre <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Ombre portée autour du panneau. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il n’est pas possible de contrôler la taille ou la position du panneau déroulant à partir de CSS ; le composant gère sa disposition par programmation.

Exemple - configurez un panneau déroulant avec un arrière-plan noir semi-transparent, une marge de 5 pixels autour du contenu et une ombre portée :

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel { 
 background-color: rgba(0, 0, 0, 0.5); 
 margin: 5px; 
 box-shadow: 2px 2px 3px #c0c0c0; 
}
```

L’aspect individuel de l’élément est contrôlé par le sélecteur de classe CSS suivant :

```
 .s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item
```

**Propriétés CSS de l’élément**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> famille de polices </p> </td> 
   <td colname="col2"> <p>Nom de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de taille de police <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’élément. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de marge intérieure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Marge intérieure interne. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Les éléments de liste déroulante prennent en charge le sélecteur d&#39;attributs `state`, qui peut être utilisé pour appliquer différents habillages aux états d&#39;éléments sélectionnés et survolés.

Exemple - configurez un élément déroulant avec une police Helvetica® de 14 pixels et de 19 pixels de hauteur. Un élément possède un arrière-plan gris foncé au survol et un arrière-plan gris clair lorsqu’il est sélectionné :

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item { 
font-family: Helvetica,sans-serif; 
font-size: 14px; 
height: 19px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item[state="over"] { 
background-color: rgb(102, 102, 102); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item[state="selected"] { 
background-color: rgb(178, 178, 178); 
}
```

Un élément qui affiche l’index de page est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7index
```

**Propriétés CSS de l’index de page**

<table id="table_FAA5072E4AAC48F4BE00B05D87FD9827"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> de largeur min. <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Largeur minimale de l’élément. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> largeur max. </p> </td> 
   <td colname="col2"> <p> Largeur maximale de l’élément. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de marge intérieure droite <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Distance entre l’index de page et le libellé de la page. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il est possible de masquer entièrement l’index de page en définissant `display:none` pour la classe CSS `s7index`.

Exemple 1 : configurez un index de page avec une largeur minimale de 40 pixels, une largeur maximale de 70 pixels et une marge de 5 pixels sur le côté droit :

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7index { 
max-width: 70px; 
min-width: 40px; 
padding-right: 5px; 
}
```

Exemple 2 - masquage de l’index de page :

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7index { 
display: none; 
}
```

Le libellé de la page est contrôlé avec le sélecteur de classe CSS suivant :

```
 .s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7label
```

**Propriétés CSS du libellé de la page**

<table id="table_A42E372D931D4F04855EE5AB5530CB12"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> de largeur min. <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Largeur minimale de l’élément. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> largeur max. </p> </td> 
   <td colname="col2"> <p> Largeur maximale de l’élément. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - configurez un index de page avec une largeur minimale de 40 pixels et une largeur maximale de 240 pixels :

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7label { 
min-width: 40px; 
max-width: 240px; 
}
```

S’il y a plus d’éléments que ne peut en contenir verticalement dans le panneau déroulant (le système est un bureau), le composant affiche une barre de défilement verticale sur le côté droit du panneau. L’aspect de la zone de la barre de défilement est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar
```

**Propriétés CSS de la barre de défilement**

<table id="table_D34A63AAE6324699ABDCC08355D33035"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur de la barre de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Décalage de la barre de défilement verticale par rapport au haut de la zone du panneau. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> inférieur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Barre de défilement verticale décalée par rapport au bas de la zone du panneau. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droit </span> </p> </td> 
   <td colname="col2"> <p> La barre de défilement horizontale se décale par rapport au bord droit de la zone du panneau. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - configurez une barre de défilement de 28 pixels de large ne comportant pas de marge pour la zone supérieure, droite ou inférieure du panneau :

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:28px; 
}
```

La piste de la barre de défilement est la zone située entre les boutons de défilement supérieur et inférieur. Le composant définit automatiquement la position et la hauteur de la piste. La piste est contrôlée avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolltrack
```

**Propriétés CSS de la piste de défilement**

<table id="table_E49EE04B3FF64AB2948E7C09DF3EA1B7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>La largeur de la piste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la piste. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - configurez une piste de barre de défilement de 28 pixels de large avec un arrière-plan gris semi-transparent :

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

Le pouce de la barre de défilement se déplace verticalement dans la zone de piste de défilement. Sa position verticale est contrôlée par la logique du composant. Cependant, la hauteur du pouce ne change pas dynamiquement en fonction de la quantité de contenu. Vous pouvez configurer la hauteur du pouce et d’autres aspects avec le sélecteur de classe CSS suivant :

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb
```

**Propriétés CSS du pouce de la barre de défilement**

<table id="table_D8DFBC2419BD4AB3B4892AC7B599C70A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>La largeur du pouce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>La hauteur du pouce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de remplissage supérieur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Marge intérieure verticale entre le haut de la piste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de marge intérieure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Marge intérieure verticale entre le bas de la piste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de pouce donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir aussi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb prend en charge le sélecteur d&#39;attributs `state`, qui peut être utilisé pour appliquer différents habillages aux états `up`, `down`, `over` et `disabled`.

Exemple - configurez une barre de défilement de 28 x 45 pixels avec des marges de 10 pixels en haut et en bas et des illustrations différentes pour chaque état :

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

L’aspect des boutons de défilement supérieur et inférieur est contrôlé avec les sélecteurs de classe CSS suivants :

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton
```

Il n’est pas possible de positionner les boutons de défilement à l’aide des propriétés CSS `top`, `left`, `bottom` et `right` ; à la place, la logique de la visionneuse les positionne automatiquement.

**Propriétés CSS du bouton de défilement vers le haut et vers le bas**

<table id="table_89561098E43D44C2865267687BBF38F4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>La largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
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
>Button prend en charge le sélecteur d&#39;attributs `state`, qui peut être utilisé pour appliquer différents habillages aux états de bouton `up`, `down`, `over` et `disabled`.

L’info-bulle du bouton peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) pour plus d’informations.

Exemple : configurez des boutons de défilement de 28 x 32 pixels avec des illustrations différentes pour chaque état :

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```
