---
title: Temps de la vidéo
description: L’heure de la vidéo est l’affichage numérique qui indique l’heure et la durée actuelles de la vidéo en cours de lecture.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 90ec189e-6de4-44b3-8760-1e8636b919ba
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 2%

---

# Temps de la vidéo{#video-time}

L’heure de la vidéo est l’affichage numérique qui indique l’heure et la durée actuelles de la vidéo en cours de lecture.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La famille de polices, la taille de police et la couleur de la police de l’heure de la vidéo font partie des propriétés que CSS peut contrôler. Il peut également être positionné, par rapport à la barre de contrôle qui le contient, par CSS.

L’aspect de l’heure de la vidéo est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7interactivevideoviewer .s7videotime
```

## Propriétés CSS du temps vidéo {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droite </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure droite, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Largeur du contrôle de l’heure de la vidéo. Cette propriété est requise pour qu’Internet Explorer 8 ou version ultérieure fonctionne correctement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices à utiliser pour l’affichage du texte temporel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Taille de police à utiliser pour le texte d’affichage temporel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Couleur de police à utiliser pour le texte d’affichage de l’heure. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-e8caea0a303c425a8a637c2a47c06355}

Définissez la durée de la vidéo sur gris clair (hexadécimal `#BBBBBB`), dimensionnée à 12 pixels, positionnée à 15 pixels du haut de la barre de contrôle et à 80 pixels des bords supérieur et droit de la barre de contrôle.

```
.s7interactivevideoviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
