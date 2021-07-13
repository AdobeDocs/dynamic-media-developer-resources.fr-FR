---
description: Le lecteur vidéo est la zone rectangulaire dans laquelle le contenu vidéo est affiché dans la visionneuse.
solution: Experience Manager
title: Lecteur vidéo
feature: Dynamic Media Classic,Visionneuses,SDK/API,Vidéos interactives
role: Developer,User
exl-id: 9cfeceff-f6bd-42d9-9b85-456bbaa278fd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 1%

---

# Lecteur vidéo{#video-player}

Le lecteur vidéo est la zone rectangulaire dans laquelle le contenu vidéo est affiché dans la visionneuse.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Si les dimensions de la vidéo en cours de lecture ne correspondent pas aux dimensions du lecteur vidéo, le contenu vidéo est centré dans la zone d’affichage rectangle du lecteur vidéo.

Le sélecteur de classe CSS suivant contrôle l’aspect du lecteur vidéo :

```
.s7interactivevideoviewer .s7videoplayer
```

**Propriétés CSS du lecteur vidéo**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la vue principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Vous pouvez localiser le message d’erreur qui s’affiche lorsque le système ne parvient pas à lire la vidéo.

Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Exemple : pour configurer une visionneuse de vidéos avec une taille de lecteur vidéo définie sur 512 x 288 pixels.

```
.s7interactivevideoviewer .s7videoplayer{ 
background-color: transparent; 
}
```

Les sous-titres codés sont placés dans un conteneur interne du lecteur vidéo. La position de ce conteneur est contrôlée par les opérateurs de positionnement WebVTT pris en charge. Le texte de la légende se trouve à l’intérieur de ce conteneur et son style est contrôlé à l’aide du sélecteur de classe CSS suivant :

`.s7interactivevideoviewer .s7videoplayer .s7caption`

**Propriétés CSS du sous-titrage codé**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p>Arrière-plan du texte de la légende codée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Couleur du texte de la légende de fermeture. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p> Poids de police des sous-titres codés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p> Taille de police de la légende fermée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Police de la légende fermée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-5b82913ff3c44b7b8187969cb15e9560}

Pour configurer le texte des sous-titres à 14 pixels, gris clair, Arial, sur un arrière-plan noir semi-transparent :

```
.s7interactivevideoviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

L’aspect de l’animation de mise en mémoire tampon est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon
```

**Propriétés CSS de l’icône d’attente**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>propriété CSS </p> </th> 
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
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p> Marge gauche de l’icône d’animation, normalement moins la moitié de la largeur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> Marge supérieure de l’icône d’animation, normalement moins la moitié de la hauteur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Obtenir une illustration. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une animation de mise en mémoire tampon d’une largeur de 101 pixels et d’une hauteur de 29 pixels :

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
