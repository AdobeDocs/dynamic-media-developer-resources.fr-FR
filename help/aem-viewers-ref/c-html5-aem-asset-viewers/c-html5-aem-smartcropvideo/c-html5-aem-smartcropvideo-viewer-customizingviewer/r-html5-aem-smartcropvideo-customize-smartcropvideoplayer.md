---
title: Lecteur vidéo
description: Le lecteur vidéo de recadrage intelligent est la zone rectangulaire où le contenu vidéo est affiché dans la visionneuse.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 07380e01e4eed6a65ba8821eee3db6fd9bb19639
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Lecteur vidéo{#video-player}

Le lecteur vidéo de recadrage intelligent est la zone rectangulaire où le contenu vidéo est affiché dans la visionneuse.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Si les dimensions de la vidéo en cours de lecture ne correspondent pas à celles du lecteur vidéo de recadrage intelligent, le contenu vidéo est centré dans la zone d’affichage rectangle du lecteur vidéo de recadrage intelligent.

Le sélecteur de classe CSS suivant contrôle l’aspect du lecteur vidéo de recadrage intelligent :

```
.s7smartcropvideoviewer .s7smartcropvideoplayer
```

**Propriétés CSS du lecteur vidéo de recadrage intelligent**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la vue principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le message d’erreur qui s’affiche si le système n’est pas en mesure de lire la vidéo peut être localisé. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) pour plus d’informations.

Exemple - Pour configurer une visionneuse de vidéos avec recadrage intelligent dont la taille du lecteur vidéo est définie sur 512 x 288 pixels.

```
.s7smartcropvideoviewer .s7smartcropvideoplayer{ 
background-color: transparent; 
}
```

Les sous-titres sont placés dans un conteneur interne à l’intérieur du lecteur vidéo de recadrage intelligent. La position de ce conteneur est contrôlée par des opérateurs de positionnement WebVTT pris en charge. Le texte de légende lui-même se trouve à l’intérieur de ce conteneur et son style est contrôlé par le sélecteur de classe CSS suivant :

`. s7smartcropvideoviewer .s7videoplayer .s7caption`

**Propriétés CSS des légendes**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Arrière-plan du texte de légende. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte de la légende. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> d’épaisseur de police </span> </p> </td> 
   <td colname="col2"> <p> Épaisseur de la police des sous-titres. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de taille de police </span> </p> </td> 
   <td colname="col2"> <p> Taille de police des légendes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> famille de polices </p> </td> 
   <td colname="col2"> <p>Police des sous-titres. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour configurer le texte des sous-titres afin qu’il fasse 14 pixels, gris clair, Arial®, sur un arrière-plan noir semi-transparent :

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

L’aspect de l’animation de mise en mémoire tampon est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon
```

**Propriétés CSS de l’icône d’attente**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur de l’icône d’animation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p> Hauteur de l’icône d’animation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la marge de gauche </span> </p> </td> 
   <td colname="col2"> <p> Icône d’animation : marge gauche, normalement moins la moitié de la largeur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de la marge supérieure </span> </p> </td> 
   <td colname="col2"> <p> Icône d’animation Marge supérieure : normalement, moins la moitié de la hauteur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> le </span> image d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Oeuvre d'art de bouton. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour configurer une animation de mise en mémoire tampon sur une largeur de 101 pixels et une hauteur de 29 pixels :

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
