---
title: Défilement vidéo
description: La barre de défilement vidéo est la commande de curseur horizontale qui permet à un utilisateur de rechercher dynamiquement n’importe quelle position temporelle dans la vidéo en cours de lecture.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3e9c8800-fda2-41d1-8436-b2de7952652c
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# Défilement vidéo{#video-scrubber}

La barre de défilement vidéo est la commande de curseur horizontale qui permet à un utilisateur de rechercher dynamiquement n’importe quelle position temporelle dans la vidéo en cours de lecture.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La barre de défilement se déplace également au fur et à mesure que la vidéo est lue pour indiquer la position de l’heure actuelle de la vidéo pendant la lecture. La barre de défilement vidéo prend toujours toute la largeur de la barre de contrôle. Il est possible d’appliquer un habillage à la barre de défilement vidéo et de modifier sa hauteur et sa position verticale à l’aide de CSS.

L’aspect général de la barre de défilement vidéo est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7mixedmediaviewer .s7videoscrubber 
.s7mixedmediaviewer .s7videoscrubber .s7videotime 
.s7mixedmediaviewer .s7videoscrubber .s7knob
```

**Propriétés CSS de la barre de défilement vidéo**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p> Position à partir de la bordure inférieure, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la barre de défilement vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Couleur de la barre de défilement vidéo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les sélecteurs de classe CSS suivants effectuent le suivi des indicateurs d’arrière-plan, de lecture et de chargement :

```
.s7mixedmediaviewer .s7videoscrubber .s7track 
.s7mixedmediaviewer .s7videoscrubber .s7trackloaded 
.s7mixedmediaviewer .s7videoscrubber .s7trackplayed
```

**Propriétés CSS du track**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du suivi correspondant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Couleur du suivi correspondant. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le sélecteur de classe CSS suivant contrôle le bouton :

```
.s7mixedmediaviewer .s7videoscrubber .s7knob
```

**Propriétés CSS du bouton**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Décalage vertical des boutons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Obtenir une illustration. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le sélecteur de classe CSS suivant contrôle la bulle de durée de lecture :

```
.s7mixedmediaviewer .s7videoscrubber .s7videotime
```

**Propriétés CSS de la bulle de durée de lecture**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p> Famille de polices à utiliser pour l’affichage du texte temporel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p> Taille de police à utiliser pour le texte d’affichage temporel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Couleur de police à utiliser pour le texte d’affichage de l’heure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la zone de bulle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la bulle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure de la zone bulle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Illustrations à bulles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position dans l’objet d’illustration, si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Alignement du texte avec la zone de bulle. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’info-bulle de la barre de défilement vidéo peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) pour plus d’informations.

## Exemple {#section-e8caea0a303c425a8a637c2a47c06355}

Configurez une visionneuse de médias mixtes avec un défilement vidéo avec des couleurs de suivi personnalisées de 10 pixels de haut et positionnées de 10 et 35 pixels à partir des bords supérieur et gauche de la barre de contrôle.

```
.s7mixedmediaviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7mixedmediaviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7mixedmediaviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7mixedmediaviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```
