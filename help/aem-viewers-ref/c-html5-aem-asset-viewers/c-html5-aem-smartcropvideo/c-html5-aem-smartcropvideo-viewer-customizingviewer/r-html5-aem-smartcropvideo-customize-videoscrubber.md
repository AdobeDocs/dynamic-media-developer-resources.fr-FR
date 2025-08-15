---
title: Nettoyeur vidéo
description: La barre vidéo est la commande de curseur horizontal qui permet à un utilisateur de rechercher dynamiquement n’importe quelle position temporelle dans la vidéo en cours de lecture.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 9f7e3fec-8303-4114-86b2-fb75d041701d
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 0%

---

# Nettoyeur vidéo{#video-scrubber}

La barre vidéo est la commande de curseur horizontal qui permet à un utilisateur de rechercher dynamiquement n’importe quelle position temporelle dans la vidéo en cours de lecture.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Le « bouton » de la barre de défilement se déplace également lors de la lecture de la vidéo pour indiquer la position temporelle actuelle de la vidéo pendant la lecture. La barre de défilement prend toujours toute la largeur de la barre de contrôle. Il est possible d’appliquer une peau à la barre vidéo, de modifier sa hauteur et sa position verticale à l’aide de CSS.

L’aspect général de la barre vidéo est contrôlé par le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7videoscrubber 
.s7smartcropvideoviewer .s7videoscrubber .s7videotime 
.s7smartcropvideoviewer .s7videoscrubber .s7knob
```

**Propriétés CSS de la barre vidéo**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> inférieur </span> </p> </td> 
   <td colname="col2"> <p> Position à partir de la bordure inférieure, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la barre vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur de la barre vidéo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les sélecteurs de classe CSS suivants effectuent le suivi des indicateurs d’arrière-plan, de lecture et de chargement :

```
.s7smartcropvideoviewer .s7videoscrubber .s7track 
.s7smartcropvideoviewer .s7videoscrubber .s7trackloaded 
.s7smartcropvideoviewer .s7videoscrubber .s7trackplayed
```

**Propriétés CSS de la piste**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la piste correspondante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur de la piste correspondante. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le sélecteur de classe CSS suivant contrôle le bouton :

```
.s7smartcropvideoviewer .s7videoscrubber .s7knob
```

**Propriétés CSS du bouton**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Décalage vertical du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur du bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Oeuvre d'art de bouton. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le sélecteur de classe CSS suivant contrôle la bulle de durée de lecture :

```
.s7smartcropvideoviewer .s7videoscrubber .s7videotime
```

**Propriétés CSS de la bulle de temps de lecture**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> famille de polices </p> </td> 
   <td colname="col2"> <p> Famille de polices à utiliser pour le texte d’affichage de l’heure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de taille de police </span> </p> </td> 
   <td colname="col2"> <p> Taille de police à utiliser pour le texte d’affichage temporel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de couleur </span> </p> </td> 
   <td colname="col2"> <p> Couleur de police à utiliser pour le texte d’affichage temporel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p>Largeur de la zone de bulle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la zone de bulle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de marge intérieure </span> </p> </td> 
   <td colname="col2"> <p>Marge intérieure de la zone de bulle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Illustration Bubble. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la position de l’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Positionnez à l’intérieur d’un sprite d’illustration si des sprites CSS sont utilisés. </p> <p>Voir <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> des </a> Sprites CSS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> d’alignement de texte </p> </td> 
   <td colname="col2"> <p>Alignement du texte sur la zone de bulle. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’info-bulle de la barre vidéo peut être localisée. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) pour plus d’informations.

**Exemple** - Pour configurer une visionneuse de vidéos avec une barre vidéo dotée de couleurs de piste personnalisées qui fait dix pixels de haut. Enfin, faites-le positionner à 10 pixels et 35 pixels des bords supérieur et gauche de la barre de contrôle.

```
.s7smartcropvideoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7smartcropvideoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7smartcropvideoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7smartcropvideoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```
