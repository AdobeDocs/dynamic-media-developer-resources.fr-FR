---
title: Lecteur vidéo
description: Le lecteur vidéo est la zone rectangulaire où le contenu vidéo est affiché dans la visionneuse.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 2f92d76e-3104-4ad8-9426-662275492251
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# Lecteur vidéo{#video-player}

Le lecteur vidéo est la zone rectangulaire où le contenu vidéo est affiché dans la visionneuse.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Si les dimensions de la vidéo en cours de lecture ne correspondent pas aux dimensions du lecteur vidéo, le contenu vidéo est centré dans la zone d’affichage rectangulaire du lecteur vidéo.

Le sélecteur de classe CSS suivant contrôle l’aspect du lecteur vidéo :

```
.s7mixedmediaviewer .s7videoplayer
```

**Propriétés CSS du lecteur vidéo**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Couleur d’arrière-plan du lecteur vidéo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le message d’erreur qui s’affiche si le système ne parvient pas à lire la vidéo peut être localisé. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) pour plus d’informations.

Exemple - Pour rendre le lecteur vidéo transparent :

```
.s7mixedmediaviewer .s7videoplayer { 
 background-color: transparent; 
}
```

Les sous-titres sont placés dans un conteneur interne à l’intérieur du lecteur vidéo. La position de ce conteneur est contrôlée par les opérateurs de positionnement WebVTT pris en charge. Le texte de la légende lui-même se trouve à l’intérieur de ce conteneur ; son style est contrôlé par le sélecteur de classe CSS suivant :

```
.s7mixedmediaviewer .s7videoplayer .s7caption
```

**Propriétés CSS des légendes**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
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
   <td colname="col2"> <p>Épaisseur de la police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille de police. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famille de police </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour définir le texte de la légende sur un Arial gris clair de 14 pixels® sur un arrière-plan noir semi-transparent :

```
.s7mixedmediaviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

L’aspect de l’animation de mise en mémoire tampon est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7mixedmediaviewer .s7videoplayer .s7waiticon
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
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p> Hauteur de l’icône de l’animation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge gauche </span> </p> </td> 
   <td colname="col2"> <p> Icône d’animation Marge gauche, normalement moins la moitié de la largeur de l’icône. </p> </td> 
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

Exemple - Pour configurer une animation de mise en mémoire tampon sur une largeur de 101 pixels et une hauteur de 29 pixels :

```
.s7mixedmediaviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
