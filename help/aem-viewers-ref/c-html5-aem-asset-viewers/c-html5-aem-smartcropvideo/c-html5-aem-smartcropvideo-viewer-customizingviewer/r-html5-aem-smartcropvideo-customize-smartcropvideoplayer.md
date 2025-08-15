---
title: Lecteur vidéo
description: Le lecteur vidéo avec recadrage intelligent est la zone rectangulaire où le contenu vidéo est affiché dans la visionneuse.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Lecteur vidéo{#video-player}

Le lecteur vidéo avec recadrage intelligent est la zone rectangulaire où le contenu vidéo est affiché dans la visionneuse.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Si les dimensions de la vidéo en cours de lecture ne correspondent pas aux dimensions du lecteur de vidéo avec recadrage intelligent, le contenu vidéo est centré dans la zone d’affichage rectangulaire du lecteur de vidéo avec recadrage intelligent.

Le sélecteur de classe CSS suivant contrôle l’apparence du lecteur vidéo avec recadrage intelligent :

```
.s7smartcropvideoviewer .s7smartcropvideoplayer
```

**Propriétés CSS du lecteur vidéo avec recadrage intelligent**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la vue principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le message d’erreur qui s’affiche si le système n’est pas capable de lire la vidéo peut être localisé. Pour plus d’informations, voir [Localisation des éléments](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) de l’interface utilisateur.

Exemple - Pour configurer une visionneuse de vidéos avec recadrage intelligent avec la taille du lecteur vidéo avec recadrage intelligent définie sur 512 x 288 pixels.

```
.s7smartcropvideoviewer .s7smartcropvideoplayer{ 
background-color: transparent; 
}
```

Les sous-titres codés sont placés dans un conteneur interne à l’intérieur du lecteur vidéo avec recadrage intelligent. La position de ce conteneur est contrôlée par les opérateurs de positionnement WebVTT pris en charge. Le texte de la légende lui-même se trouve à l’intérieur de ce conteneur et son style est contrôlé par le sélecteur de classe CSS suivant :

`. s7smartcropvideoviewer .s7videoplayer .s7caption`

**Propriétés CSS du sous-titrage**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Arrière-plan du texte du sous-titrage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte de la légende. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> épaisseur de police </span> </p> </td> 
   <td colname="col2"> <p> Graisse de police des sous-titres. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de police </span> </p> </td> 
   <td colname="col2"> <p> Taille de police des sous-titres. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famille de police </span> </p> </td> 
   <td colname="col2"> <p>Police des sous-titres. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour définir le texte du sous-titrage afin qu’il soit de 14 pixels, gris clair, arial®, sur un fond noir semi-transparent :

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

L’aspect de l’animation de mise en mémoire tampon est contrôlé par le sélecteur de classe CSS suivant :

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
   <td colname="col1"> <p> <span class="codeph"> Largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur de l’icône d’animation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p> Hauteur de l’icône de l’animation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge gauche </span> </p> </td> 
   <td colname="col2"> <p> Icône d’animation Marge gauche, normalement moins la moitié de la largeur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge haut </span> </p> </td> 
   <td colname="col2"> <p> Marge supérieure de l’icône d’animation, normalement moins la moitié de la hauteur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p> Illustration de bouton. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une animation de mise en mémoire tampon de 101 pixels de large, 29 pixels de haut :

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
