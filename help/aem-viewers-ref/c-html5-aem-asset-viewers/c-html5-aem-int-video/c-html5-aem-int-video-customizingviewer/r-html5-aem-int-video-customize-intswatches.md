---
description: Le panneau Nuancier interactif s’affiche en regard du contenu vidéo si des données interactives ont été transmises à la visionneuse en configuration. Il s’agit d’une bannière en haut qui affiche le texte tel que "Cliquer pour", une colonne d’une ou de plusieurs nuances interactives et deux boutons de défilement (disponibles uniquement sur les ordinateurs de bureau).
seo-description: Le panneau Nuancier interactif s’affiche en regard du contenu vidéo si des données interactives ont été transmises à la visionneuse en configuration. Il s’agit d’une bannière en haut qui affiche le texte tel que "Cliquer pour", une colonne d’une ou de plusieurs nuances interactives et deux boutons de défilement (disponibles uniquement sur les ordinateurs de bureau).
seo-title: Nuances interactives
solution: Experience Manager
title: Nuances interactives
topic: Dynamic media
uuid: 9f9df764-3dd0-414e-a0db-4287f0019313
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Nuances interactives{#interactive-swatches}

Le panneau Nuancier interactif s’affiche en regard du contenu vidéo si des données interactives ont été transmises à la visionneuse en configuration. Il s’agit d’une bannière en haut qui affiche le texte tel que &quot;Cliquer pour&quot;, une colonne d’une ou de plusieurs nuances interactives et deux boutons de défilement (disponibles uniquement sur les ordinateurs de bureau).

<!--<a id="section_235621A1533A49AAADB64A7C3191F735"></a>-->

Sur les ordinateurs de bureau et les périphériques tactiles, en orientation paysage, les échantillons interactifs sont rendus verticalement à droite du contenu vidéo. Sur les périphériques tactiles en orientation portrait, ils apparaissent au bas de la visionneuse, sous la forme d’une rangée horizontale de nuances.

Le sélecteur de classe CSS suivant contrôle l’emplacement et l’orientation du panneau Nuancier interactif :

```
.s7interactivevideoviewer .s7interactiveswatches
```

## Propriétés CSS des échantillons interactifs {#css-properties-of-the-interactive-swatches}

<table id="table_352DAD495AE742E39B4F12629C43F712"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du panneau Nuancier interactif </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du panneau Nuancier interactif. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p>Position supérieure du panneau Nuancier interactif. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bas </span> </p> </td> 
   <td colname="col2"> <p>Position inférieure du panneau Nuancier interactif. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gauche </span> </p> </td> 
   <td colname="col2"> <p>Position gauche du panneau Nuancier interactif. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droite </span> </p> </td> 
   <td colname="col2"> <p>Position droite du panneau Nuancier interactif. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’emplacement et l’orientation d’exécution du panneau Nuancier interactif sont définis par une combinaison des propriétés CSS ci-dessus, comme suit :

* Pour rendre les échantillons interactifs horizontalement au bas de la visionneuse, définissez la hauteur sur une valeur absolue en pixels. gauche et bas à 0px; width, right et top to auto.
* Pour rendre les échantillons interactifs verticalement à droite du contenu vidéo, définissez la largeur sur un pixel absolu. droit et haut à 0px; hauteur, gauche et bas jusqu’à auto.

Il est possible d’utiliser des marqueurs CSS conjointement avec cette mise en forme pour obtenir le positionnement adaptatif du panneau des nuances interactives.

## Exemple {#example}

Pour configurer un panneau d’échantillons interactif afin qu’il s’affiche horizontalement en bas de la visionneuse sur des périphériques tactiles en orientation paysage et verticalement à droite du contenu vidéo dans tous les autres cas :

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7interactiveswatches, 
.s7interactivevideoviewer.s7mouseinput .s7interactiveswatches { 
 width:120px; 
 height:auto; 
 right:0px; 
 top:0px; 
 left:auto; 
 bottom:auto; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7interactiveswatches { 
 width:auto; 
 height:136px; 
 right:auto; 
 top:auto; 
 left:0px; 
 bottom:0px; 
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La taille et la position de la bannière sont gérées par le composant d’échantillons interactifs en fonction d’autres styles appliqués avec CSS et ne peuvent pas être définis explicitement.

Le sélecteur de classe CSS suivant contrôle l’aspect du panneau de bannière :

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner
```

## Propriétés CSS du panneau de bannière {#css-properties-of-the-banner-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan du panneau de bannière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte dans le panneau de bannière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p>Bordure autour du panneau de bannière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font- </span> </p> </td> 
   <td colname="col2"> <p>Le de police à utiliser pour le texte dans le panneau de bannière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Taille de police à utiliser pour le texte dans le panneau de bannière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices à utiliser pour le texte dans le panneau de bannière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align </span> </p> </td> 
   <td colname="col2"> <p>Alignement des polices à utiliser pour le texte dans le panneau de bannière. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’info-bulle de la bannière peut être localisée. Pour plus d’informations, voir [des éléments](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) de l’interface utilisateur.

## Exemple {#section-e8caea0a303c425a8a637c2a47c06355}

Pour configurer une bannière avec un arrière-plan gris foncé, une bordure gris clair de deux pixels et un texte blanc centré horizontalement :

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner { 
    background-color: #222222; 
    border-bottom: 2px solid #444444; 
    color: #ffffff; 
    text-align: center; 
}
```

Le sélecteur de classe CSS suivant contrôle l’aspect des échantillons :

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches
```

## Propriétés CSS de la zone de nuances {#css-properties-of-the-swatches-area}

<table id="table_45E98E96B07246CAA5D3076FAF62A0B3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la zone des échantillons. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-9cadd62a09fd44a280f55ff42437e416}

Pour configurer une zone de nuances avec un arrière-plan gris foncé :

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches { 
    background-color: #222222; 
}
```

Le sélecteur de classe CSS suivant contrôle l’espacement entre les miniatures d’échantillon :

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell`

## Propriétés CSS des nuances d’espacement des miniatures {#css-properties-of-the-swatches-thumbnail-spacing}

<table id="table_FE6A749EA3894956998D50EA4AB6497B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Taille de la marge horizontale et verticale autour de chaque miniature. L’espacement réel des miniatures est égal à la somme des marges gauche et droite définies pour <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-39fb270b7e494a9d99e6e8f6890ec53c}

Pour définir un espacement vertical de 10 pixels :

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

Le sélecteur de classe CSS suivant contrôle l’aspect des miniatures individuelles :

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb`

## Propriétés CSS de l’aspect des miniatures individuelles {#css-properties-of-the-appearance-of-individual-thumbnails}

<table id="table_FB760FE6BEA44E129C07DD912C86DE57"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p>Bordure de la vignette. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La miniature prend en charge le sélecteur d’ `state` attributs, que vous pouvez utiliser pour appliquer différents habillages à différents états de miniature. Correspond en particulier `state="selected"` à la vignette de l&#39;image actuellement sélectionnée ; correspond `state="default"` au reste des miniatures ; est `state="over"` utilisée lorsque vous passez la souris.

## Exemple {#section-69fec189ffaa440b97b6b846c320b75b}

Pour configurer des miniatures de 100 x 75 pixels :

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb { 
 width:100px; 
 height:75px; 
}
```

Le sélecteur de classe CSS suivant contrôle l’aspect du libellé de la miniature :

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label`

## Propriétés CSS de l’aspect du libellé de la miniature {#css-properties-of-the-appearance-of-the-thumbnail-label}

<table id="table_81B3209FB8124FFA9DB81FD35717900D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordure </span> </p> </td> 
   <td colname="col2"> <p>Bordure du libellé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Alignement horizontal du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nom de la police. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-eb141eb6c1154183baa69796edb90536}

Pour configurer les libellés de manière à ce qu’ils soient alignés à gauche, en blanc, sur 12 pixels, dans la police Helvetica et sur une bordure inférieure :

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label { 
 border-bottom: 1px solid #e9e9e9; 
 text-align: left; 
color: #ffffff; 
font-family: Helvetica,sans-serif; 
font-size: 12px; 
}
```

Le sélecteur de classe CSS suivant contrôle l’aspect des boutons de défilement Haut et Bas :

`.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton`

`.s7interactivevideoviewer .s7interactiveswatches .s7scrolldownbutton`

Il n’est pas possible de positionner les boutons de défilement à l’aide des propriétés CSS `top`, `left`, `bottom`et `right` ; au lieu de cela, la logique du lecteur les positionne automatiquement.

## Propriétés CSS de l’aspect des boutons de défilement vers le haut et vers le bas {#css-properties-of-the-appearance-of-the-up-and-down-scroll-buttons}

<table id="table_48AF27AFBB1543288D45449D6900675C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton de défilement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-image </span> </p> </td> 
   <td colname="col2"> <p>Image affichée pour un état de bouton donné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-position </span> </p> </td> 
   <td colname="col2"> <p>Position à l’intérieur de l’image-objet d’illustration, si des images-objets CSS sont utilisées. </p> <p>Voir aussi <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ce bouton prend en charge le sélecteur d’ `state` attributs, que vous pouvez utiliser pour appliquer différents habillages aux états du bouton : &quot; `up`&quot;, &quot; `down`&quot;, &quot; `over`&quot; et &quot; `disabled`&quot;.

Les info-bulles des boutons peuvent être localisées. Pour plus d’informations, voir [des éléments](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) de l’interface utilisateur.

## Exemple {#section-e6ce4fa084b84288bc7583342b2c510c}

Pour configurer un bouton de défilement vers le haut de 60 x 36 pixels, disposez d’une illustration différente pour chaque état et extrait cette illustration de l’image d’image-objet du composant :

```
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton { 
 background-size: 120px; 
 width: 60px; 
 height: 36px;  
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state] { 
 background-image: url(images/v2/InteractiveSwatches_light_sprite.png); 
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='up'] { background-position: -60px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='over'] { background-position: -0px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='down'] { background-position: -60px -648px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='disabled'] { background-position: -0px -648px; }
```

