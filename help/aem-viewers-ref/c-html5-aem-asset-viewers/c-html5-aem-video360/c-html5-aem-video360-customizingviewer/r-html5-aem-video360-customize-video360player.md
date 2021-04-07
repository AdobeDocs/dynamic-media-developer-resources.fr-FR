---
description: Le lecteur vidéo est la zone rectangulaire dans laquelle le contenu vidéo est affiché dans la visionneuse.
solution: Experience Manager
title: Lecteur vidéo360
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéo 360 VR
role: Développeur, Professionnel
exl-id: 54ccf872-2d24-4d3f-9808-6d0e2558f5a5
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 1%

---

# Lecteur vidéo360{#video-player}

Le lecteur vidéo est la zone rectangulaire dans laquelle le contenu vidéo est affiché dans la visionneuse.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Si les dimensions de la vidéo en cours de lecture ne correspondent pas à celles du lecteur vidéo, le contenu vidéo est centré dans la zone d’affichage rectangulaire du lecteur vidéo.

Le sélecteur de classe CSS suivant contrôle l’aspect du lecteur vidéo :

```
.s7video360viewer .s7video360player
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

Voir [Localisation des éléments de l’interface utilisateur](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

Exemple : pour configurer une visionneuse de vidéos dont la taille du lecteur vidéo est définie sur 512 x 288 pixels.

```
.s7video360viewer .s7video360player{ 
background-color: transparent; 
}
```

<!--<a id="section_5B82913FF3C44B7B8187969CB15E9560"></a>-->

L&#39;aspect de l&#39;animation de mise en mémoire tampon est contrôlé par le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7video360player .s7waiticon
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
   <td colname="col1"> <p> <span class="codeph"> marge-gauche  </span> </p> </td> 
   <td colname="col2"> <p> L’icône d’animation a la marge gauche, habituellement moins la moitié de la largeur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> Marge supérieure de l’icône d’animation, habituellement moins la moitié de la hauteur de l’icône. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image d’arrière-plan  </span> </p> </td> 
   <td colname="col2"> <p> Touchez l’illustration. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer une animation de mise en mémoire tampon d’une largeur de 101 pixels et d’une hauteur de 29 pixels :

```
.s7video360viewer .s7video360player .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
