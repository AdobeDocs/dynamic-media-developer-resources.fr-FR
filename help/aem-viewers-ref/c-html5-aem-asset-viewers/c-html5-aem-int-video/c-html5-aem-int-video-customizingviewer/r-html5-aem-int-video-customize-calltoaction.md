---
description: Le panneau Appel à l’action s’affiche à la fin de la vidéo et affiche toutes les nuances interactives associées à la vidéo en question.
seo-description: Le panneau Appel à l’action s’affiche à la fin de la vidéo et affiche toutes les nuances interactives associées à la vidéo en question.
seo-title: Appel à l'action
solution: Experience Manager
title: Appel à l'action
topic: Dynamic media
uuid: 04a042d8-7329-4f1d-b3b9-312d620b1f29
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '1298'
ht-degree: 3%

---


# Appel à l&#39;action{#call-to-action}

Le panneau Appel à l’action s’affiche à la fin de la vidéo et affiche toutes les nuances interactives associées à la vidéo en question.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Le panneau se compose d’une zone d’en-tête présentant le titre de la vidéo, d’un bouton de relecture dans le coin supérieur droit et de nuances interactives réelles affichées sous la forme d’une grille défilante. Vous pouvez désactiver le panneau à l’aide de l’attribut de configuration [callToActionRecap](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-calltoactionrecap.md#reference-3720b68800684ddabf523e9d81644ce6).

Le panneau d’appel à l’action prend toujours la totalité de la zone de visualisation disponible.

<!--<a id="section_3A619BE925C04AFA87A6B7846C5C7E2B"></a>-->

Le sélecteur de classe CSS suivant contrôle l’aspect de la couleur d’arrière-plan dans le panneau d’appel à l’action :

```
.s7interactivevideoviewer .s7calltoaction
```

## Propriétés CSS de la couleur d’arrière-plan du panneau d’appel à l’action {#css-properties-of-the-background-color-of-the-call-to-action-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan du panneau d’appel à l’action. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#example}

Pour configurer un panneau d’appel à l’action avec un arrière-plan gris foncé :

```
.s7interactivevideoviewer .s7calltoaction { 
    background-color: #222222; 
}
```

<!--<a id="section_AD18C770788B49989BEDAA608ECA804C"></a>-->

Le sélecteur de classe CSS suivant contrôle l’aspect de l’en-tête dans le panneau d’appel à l’action :

```
.s7interactivevideoviewer .s7calltoaction .s7header
```

## Propriétés CSS de l&#39;en-tête du panneau d&#39;appel à l&#39;action {#css-properties-of-the-call-to-action-panel-header}

<table id="table_DAA1770AB3074845B5E1B700CD6FC18A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de l’en-tête. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de l’en-tête. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-bottom  </span> </p> </td> 
   <td colname="col2"> <p>Bordure inférieure de l’en-tête. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#example-1}

Pour configurer un en-tête de 70 pixels de haut, avec un arrière-plan gris foncé et une bordure de deux pixels légèrement grise le long du bas :

```
.s7interactivevideoviewer .s7calltoaction .s7header { 
    height: 70px; 
    border-bottom: 2px solid #444444; 
    background-color: #222222; 
}
```

<!--<a id="section_B0333FC1A2CC4E089C68D34B839E5156"></a>-->

Le sélecteur de classe CSS suivant contrôle l’aspect du titre d’en-tête dans le panneau d’appel à l’action :

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title
```

## Propriétés CSS du titre de l’en-tête dans le panneau d’appel à l’action :  {#css-properties-of-the-header-title-in-the-call-to-action-panel}

<table id="table_A5E36A5C4C664346B6DAE9A02B36C3D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Couleur du texte dans la bannière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ligne-hauteur  </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la ligne. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p> Famille de polices. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alignement de texte  </span> </p> </td> 
   <td colname="col2"> <p>Alignement du texte dans la bannière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage-gauche  </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure gauche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage-droit  </span> </p> </td> 
   <td colname="col2"> <p> Marge intérieure droite pour laisser de l’espace au bouton Lecture. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#example-2}

Pour configurer un titre de vidéo avec une hauteur de ligne de 70 pixels, une taille de police de 25 pixels, une couleur blanche et un alignement à gauche :

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title { 
    line-height: 70px; 
    font-size: 25px; 
    color: #ffffff; 
    text-align: left; 
}
```

<!--<a id="section_D23A6D4BA0614286A060982B359E3C08"></a>-->

Le sélecteur de classe CSS suivant contrôle l’aspect du bouton de fermeture dans le panneau d’appel à l’action :

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton
```

## Propriétés CSS du bouton de fermeture dans le panneau d’appel à l’action : {#css-properties-of-the-close-button-in-the-call-to-action-panel}

<table id="table_CB0BCBE70DB447BC8D31034A96308924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p>Position à partir du haut de l’en-tête, y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droite </span> </p> </td> 
   <td colname="col2"> <p>Position à droite de l’en-tête, y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur  </span> </p> </td> 
   <td colname="col2"> <p> Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p>Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p>Positionnez l’objet d’illustration à l’intérieur de l’image-objet, si des images-objets CSS sont utilisées. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de bouton.

## Exemple {#example-3}

Pour configurer un bouton de relecture de 28 x 28 pixels, positionné à 20 pixels du haut et du bord droit de l’en-tête ; affiche une image différente pour chacun des quatre états de bouton différents ; prend l’illustration de l’image d’image-objet du composant :

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton { 
 top: 20px; 
 right: 20px; 
 background-size: 336px; 
 width: 28px; 
 height: 28px;  
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state] { 
 background-image: url(images/v2/PlayPauseButton_sprite.png); 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='up'] { 
 background-position: -28px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='over'] { 
 background-position: -0px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='down'] { 
 background-position: -28px -1232px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='disabled'] { 
 background-position: -0px -1232px; 
}
```

<!--<a id="section_3975B58E78DE4E81B469372FB8A3A348"></a>-->

Le sélecteur de classe CSS suivant contrôle l’aspect de la vue de grille de miniature dans le panneau d’appel à l’action :

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview
```

## Propriétés CSS de la vue de grille de miniature dans le panneau d’appel à l’action :  {#css-properties-of-the-thumbnail-grid-view-in-the-call-to-action-panel}

<table id="table_A0DDD21C84944D48A639F51FCC8DF065"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la zone des miniatures. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#example-4}

Pour configurer une zone de miniatures avec un arrière-plan gris foncé :

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview { 
    background-color: #222222; 
}
```

<!--<a id="section_D2E5AADFCE0345468DC0D2977E2765D2"></a>-->

Le sélecteur de classe CSS suivant contrôle l’aspect de la cellule de pouce dans le panneau d’appel à l’action :

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell
```

## Propriétés CSS de la cellule de miniature dans le panneau d’appel à l’action : {#css-properties-of-the-thumbcell-in-the-call-to-action-panel}

<table id="table_9CEBEF6FC7024F02840A581AEEF612B4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Taille de la marge horizontale et verticale autour de chaque miniature. </p> <p>L’espacement réel des miniatures horizontales est égal à la somme des marges gauche et droite définies pour <span class="codeph"> .s7thumbcell </span>. La même règle s'applique également à l'espacement vertical. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#example-5}

Pour définir un espacement horizontal de 24 pixels et un espacement vertical de 18 pixels :

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell { 
 margin-top: 9px; 
 margin-bottom: 9px; 
 margin-left: 12px; 
 margin-right: 12px; 
}
```

<!--<a id="section_D06CF9F709A3447F83DC6E1CE7CA58B5"></a>-->

Le sélecteur de classe CSS suivant contrôle l’aspect de la miniature dans le panneau d’appel à l’action :

```
.s7interactivevideoviewer .s7calltoaction .s7thumb
```

## Propriétés CSS de la miniature dans le panneau d’appel à l’action : {#css-properties-of-the-thumbnail-in-the-call-to-action-panel}

<table id="table_ECD7477F4BE94BA8943210FA8B6B8D01"> 
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

>[!NOTE]
>
>La miniature prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages à différents états de miniature. `state="selected"` correspond en particulier à la vignette de l’image actuellement sélectionnée ; `state="default"` correspond au reste des miniatures ; `state="over"` est utilisé lors du survol de la souris.

## Exemple {#example-6}

Pour configurer des miniatures de 94 x 100 pixels :

```
.s7interactivevideoviewer .s7calltoaction .s7thumb { 
 width:94px; 
 height:100px; 
}
```

<!--<a id="section_F1B7E3FA3ABD4D71848586A3B308F9E2"></a>-->

Le sélecteur de classe CSS suivant contrôle l’aspect du libellé de la miniature dans le panneau d’appel à l’action :

```
.s7interactivevideoviewer .s7calltoaction .s7label
```

## Propriétés CSS du libellé de la miniature dans le panneau d’appel à l’action : {#css-properties-of-the-thumbnail-label-in-the-call-to-action-panel}

<table id="table_E2C9F21EBD9140FD9D20A4BBAD117E2F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p> Couleur du texte de l’étiquette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alignement de texte  </span> </p> </td> 
   <td colname="col2"> <p>Alignement horizontal du libellé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nom de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#example-7}

Pour configurer des libellés de couleur blanche, aligner le centre sur 15 pixels et utiliser une police Arial :

```
.s7interactivevideoviewer .s7calltoaction .s7label { 
 text-align: center; 
 color: #ffffff; 
  font-family: Arial,Helvetica,sans-serif; 
  font-size: 15px; 
}
```

<!--<a id="section_2C011101EB804513B942EFB4CBD38E62"></a>-->

S’il y a plus de miniatures que celles qui peuvent tenir verticalement à la vue, les miniatures génèrent une barre de défilement verticale sur le côté droit. Par défaut, le panneau d’appel à l’action affiche une toute petite barre verticale sans boutons de pouce et de défilement. Il est toutefois possible de personnaliser la barre en modifiant le fichier CSS de la visionneuse.

Le sélecteur de classe CSS suivant contrôle l’aspect de la zone de barre de défilement dans le panneau d’appel à l’action :

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar
```

## Propriétés CSS de la zone de la barre de défilement dans le panneau d’appel à l’action : {#css-properties-of-the-scroll-bar-area-in-the-call-to-action-panel}

<table id="table_6D3A4A68BFDB44259A6E2E632B9195F3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> Largeur de la barre de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p>Décalage de la barre de défilement verticale à partir du haut de la zone des miniatures. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bas </span> </p> </td> 
   <td colname="col2"> <p>Décalage de la barre de défilement verticale à partir du bas de la zone des miniatures. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droite </span> </p> </td> 
   <td colname="col2"> <p> Décalage de la barre de défilement horizontale par rapport au bord droit de la zone des vignettes. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#example-8}

Pour configurer une barre de défilement de 22 pixels de large et ne présentant aucune marge du haut, de la droite ou du bas de la zone des miniatures :

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:22px; 
}
```

<!--<a id="section_E27B7253441543278E1081D70BA46122"></a>-->

La barre de défilement est la zone située entre les boutons de la barre de défilement supérieure et inférieure. Le composant définit automatiquement la position et la hauteur de la piste.

Le sélecteur de classe CSS suivant contrôle l’aspect du suivi de la barre de défilement dans le panneau d’appel à l’action :

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack
```

## Propriétés CSS de la barre de suivi de défilement {#css-properties-of-the-scroll-track-bar}

<table id="table_7A7D40C332F4461FAAC623196C00D5A8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la barre de suivi de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la barre de suivi. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#example-9}

Pour configurer une piste de barre de défilement de 22 pixels de large et de couleur grise :

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:22px; 
 background-color:#222222; 
}
```

<!--<a id="section_4A5D8C1A9C9D4E7B8AC0CD5BC6F3772D"></a>-->

Le curseur de la barre de défilement se déplace verticalement dans la zone de suivi de défilement. Sa position verticale est entièrement contrôlée par la logique des composantes; toutefois, la hauteur du curseur ne change pas de manière dynamique en fonction de la quantité de contenu.

Le sélecteur de classe CSS suivant contrôle l’aspect de la hauteur du pouce et d’un autre aspect :

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb
```

## Propriétés CSS de la hauteur du curseur dans le panneau d’appel à l’action : {#css-properties-of-the-thumb-height-in-the-call-to-action-panel}

<table id="table_1F39948FC3924FA4B7F851B65B2D860B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Largeur du pouce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur  </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du pouce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage-haut  </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure verticale entre le haut de la piste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> remplissage-bas  </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure verticale entre le bas de la piste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p>Rayon de la bordure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p>Couleur du pouce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p> Image affichée pour un état de pouce donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p> Positionnez l’objet à l’intérieur de l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb prend en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages aux différents états de pouce suivants : `"up"`, `"down"`, `"over"` et `"disabled"`.

## Exemple {#example-10}

Pour configurer un pouce de barre de défilement de 6 x 167 pixels, avec trois pixels aux coins arrondis et une couleur de gris :

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state] { 
 width:6px; 
 height:167px; 
 background-color:#666666; 
 background-image:none; 
 border-radius:3px 3px 3px 3px; 
}
```

<!--<a id="section_C393B59763344E70A3BBD0601110F8DD"></a>-->

Le sélecteur de classe CSS suivant contrôle l’aspect des boutons de défilement supérieur et inférieur :

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton 
 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton
```

Il n’est pas possible de positionner les boutons de défilement à l’aide des propriétés CSS top, left, bottom ou right ; la logique du lecteur les positionne automatiquement. Le panneau d’appel à l’action de la visionneuse de vidéos interactive n’utilise pas ces boutons dans la barre de défilement. Par conséquent, leur taille est définie sur 0 pixel dans le CSS par défaut.

## Propriétés CSS des boutons de défilement supérieur et inférieur dans le panneau d’appel à l’action :  {#css-properties-of-the-top-and-bottom-scroll-buttons-in-the-call-to-action-panel}

<table id="table_FE17D19E0545424EADB0256524361359"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur  </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p>Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position  </span> </p> </td> 
   <td colname="col2"> <p> Positionnez l’objet à l’intérieur de l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ces boutons prennent en charge le sélecteur d’attributs `state`, qui peut être utilisé pour appliquer différents habillages aux différents états de pouce suivants : `"up"`, `"down"`, `"over"` et `"disabled"`.

Les info-bulles des boutons peuvent être localisées. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Exemple {#example-11}

Désactivez les boutons de défilement en définissant leur taille sur 0 et en les masquant :

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
}
```

