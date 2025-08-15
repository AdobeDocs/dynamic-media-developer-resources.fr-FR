---
title: Durée vidéo
description: L’heure de la vidéo est l’affichage numérique qui indique l’heure actuelle et la durée de la vidéo en cours de lecture.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 78657fd2-e805-4047-be0a-592143025986
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# Durée vidéo{#video-time}

L’heure de la vidéo est l’affichage numérique qui indique l’heure actuelle et la durée de la vidéo en cours de lecture.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La famille de polices de l’heure de la vidéo, la taille de police et la couleur de la police font partie des propriétés que CSS peut contrôler. Il peut également être positionné, par rapport à la barre de contrôle qui le contient, par CSS.

L’aspect de l’heure de la vidéo est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7video360viewer .s7videotime
```

## Propriétés CSS de l’heure vidéo {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droit </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure droite, marge intérieure incluse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largeur </span> </p> </td> 
   <td colname="col2"> <p> Largeur du contrôle temporel vidéo. Cette propriété est requise pour qu'Internet Explorer 8 ou version ultérieure fonctionne correctement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> famille de polices </p> </td> 
   <td colname="col2"> <p>Famille de polices à utiliser pour le texte d’affichage de l’heure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de taille de police </span> </p> </td> 
   <td colname="col2"> <p>Taille de police à utiliser pour le texte d’affichage temporel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur de police à utiliser pour le texte d’affichage temporel. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Définissez l’heure de la vidéo sur gris clair (`#BBBBBB` hexadécimal), dimensionnée à 12 pixels, positionnée à 15 pixels du haut de la barre de contrôle et à 80 pixels des bords supérieur et droit de la barre de contrôle.

```
.s7video360viewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
