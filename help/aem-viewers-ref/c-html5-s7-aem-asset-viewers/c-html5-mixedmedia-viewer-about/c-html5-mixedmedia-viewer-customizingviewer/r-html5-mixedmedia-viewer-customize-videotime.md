---
title: Temps de la vidéo
description: L’heure de la vidéo est l’affichage numérique qui indique l’heure et la durée actuelles de la vidéo en cours de lecture.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 5efae314-5f37-4afc-9b9e-3108a8529e50
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# Temps de la vidéo{#video-time}

L’heure de la vidéo est l’affichage numérique qui indique l’heure et la durée actuelles de la vidéo en cours de lecture.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La famille de polices, la taille de police et la couleur de la police de l’heure de la vidéo font partie des propriétés que CSS peut contrôler. Il peut également être positionné, par rapport à la barre de contrôle qui le contient, par CSS.

L’aspect de l’heure de la vidéo est contrôlé à l’aide du sélecteur de classe CSS suivant :

```
.s7mixedmediaviewer .s7videotime
```

## Propriétés CSS du temps vidéo {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droit </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure droite, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Largeur du contrôle de l’heure de la vidéo. Cette propriété est requise pour qu’Internet Explorer 8 ou version ultérieure fonctionne correctement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices à utiliser pour l’affichage du texte temporel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Taille de police à utiliser pour le texte d’affichage temporel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Couleur de police à utiliser pour le texte d’affichage de l’heure. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-e8caea0a303c425a8a637c2a47c06355}

Définissez le temps de la vidéo sur gris clair (hexadécimal `#BBBBBB`), dimensionné à 12 pixels, positionné 15 pixels à partir du haut de la barre de contrôle et 80 pixels à partir des bords droits de la barre de contrôle.

```
.s7mixedmediaviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
