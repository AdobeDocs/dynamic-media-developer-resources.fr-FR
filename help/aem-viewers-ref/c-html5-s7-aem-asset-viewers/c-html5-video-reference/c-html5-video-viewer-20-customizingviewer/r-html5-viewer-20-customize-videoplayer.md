---
title: Lecteur vidéo
description: Le lecteur vidéo est la zone rectangulaire où le contenu vidéo est affiché dans la visionneuse.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2741821f-78fe-44d4-8604-fee10086e0a0
TQID: 'https://experienceleague.adobe.com/mVDQWuBQZT9--O4V3XCrPRasFvG8x7fIsxqQLFsMpNU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 310
ht-degree: 0%

---

# Lecteur vidéo{#video-player}

Le lecteur vidéo est la zone rectangulaire où le contenu vidéo est affiché dans la visionneuse.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Si les dimensions de la vidéo lue ne correspondent pas à celles du lecteur vidéo, le contenu vidéo est centré dans la zone d’affichage en rectangle du lecteur vidéo.

Le sélecteur de classe CSS suivant contrôle l’aspect du lecteur vidéo :

```
.s7videoviewer .s7videoplayer
```

**Propriétés CSS du lecteur vidéo**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la vue principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le message d’erreur qui s’affiche si le système n’est pas en mesure de lire la vidéo peut être localisé. Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) pour plus d’informations.

Exemple - Pour configurer une visionneuse de vidéos avec une taille de lecteur vidéo définie sur 512 x 288 pixels.

```
.s7videoviewer .s7videoplayer{ 
background-color: transparent; 
}
```

Les sous-titres sont placés dans un conteneur interne au sein du lecteur vidéo. La position de ce conteneur est contrôlée par des opérateurs de positionnement WebVTT pris en charge. Le texte de légende lui-même se trouve à l’intérieur de ce conteneur et son style est contrôlé par le sélecteur de classe CSS suivant :

`. s7videoviewer .s7 videoplayer .s7caption`

**Propriétés CSS des légendes**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Arrière-plan du texte de légende. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de couleur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Couleur du texte de la légende. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> d’épaisseur de police <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Épaisseur de la police des sous-titres. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de taille de police <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Taille de police des légendes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> famille de polices </p> </td> 
   <td colname="col2"> <p>Police des sous-titres. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour configurer le texte des sous-titres afin qu’il fasse 14 pixels, gris clair, Arial®, sur un arrière-plan noir semi-transparent :

```
.s7videoviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

L’aspect de l’animation de mise en mémoire tampon est contrôlé avec le sélecteur de classe CSS suivant :

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
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur de l’icône d’animation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Hauteur de l’icône d’animation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> la marge de gauche </span> </p> </td> 
   <td colname="col2"> <p> Icône d’animation : marge gauche, normalement moins la moitié de la largeur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de la marge supérieure <span class="codeph"> </p> </td> 
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
.s7videoviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
