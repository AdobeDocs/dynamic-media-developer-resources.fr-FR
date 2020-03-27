---
description: Le lecteur vidéo est la zone rectangulaire dans laquelle le contenu vidéo est affiché dans la visionneuse.
seo-description: Le lecteur vidéo est la zone rectangulaire dans laquelle le contenu vidéo est affiché dans la visionneuse.
seo-title: Lecteur vidéo
solution: Experience Manager
title: Lecteur vidéo
topic: Dynamic media
uuid: 2748c3d3-b974-4e54-8218-a2ec9e31a668
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Video player{#video-player}

Le lecteur vidéo est la zone rectangulaire dans laquelle le contenu vidéo est affiché dans la visionneuse.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Si les dimensions de la vidéo en cours de lecture ne correspondent pas à celles du lecteur vidéo, le contenu vidéo est centré dans la zone d’affichage du rectangle du lecteur vidéo.

Le sélecteur de classe CSS suivant contrôle l’aspect du lecteur vidéo :

```
.s7videoviewer .s7videoplayer
```

**Propriétés CSS du lecteur vidéo**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan du  principal du. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le message d’erreur affiché si le système n’est pas en mesure de lire la vidéo peut être localisé. Pour plus d’informations, voir [des éléments](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) de l’interface utilisateur.

Exemple : pour configurer une visionneuse de vidéos dont la taille du lecteur vidéo est définie sur 512 x 288 pixels.

```
.s7videoviewer .s7videoplayer{ 
background-color: transparent; 
}
```

Les sous-titres sont placés dans un interne  dans le lecteur vidéo. La position de cet  est contrôlée par les opérateurs de positionnement WebVTT pris en charge. Le texte de la légende lui-même se trouve à l’intérieur de ce et son style est contrôlé à l’aide du sélecteur de classe CSS suivant :

`. s7videoviewer .s7 videoplayer .s7caption`

**Propriétés CSS du sous-titrage**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Arrière-plan du texte de la légende fermée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte de la légende de fermeture. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font- </span> </p> </td> 
   <td colname="col2"> <p>  de police de la légende fermée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p> Taille de police de la légende fermée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Police de sous-titrage fermée. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour définir le texte d’une légende fermée sur 14 pixels, gris clair, Arial, sur un arrière-plan noir semi-transparent :

```
.s7videoviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

L’aspect de l’animation de mise en mémoire tampon est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7videoviewer .s7videoplayer .s7waiticon
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Largeur de l’icône d’animation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Hauteur de l’icône d’animation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge-gauche </span> </p> </td> 
   <td colname="col2"> <p> Marge gauche de l’icône d’animation, normalement moins la moitié de la largeur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge-haut </span> </p> </td> 
   <td colname="col2"> <p> Marge supérieure de l’icône d’animation, normalement moins la moitié de la hauteur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-image </span> </p> </td> 
   <td colname="col2"> <p> Touchez l’illustration. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une animation de mise en mémoire tampon avec une largeur de 101 pixels et une hauteur de 29 pixels :

```
.s7videoviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```

