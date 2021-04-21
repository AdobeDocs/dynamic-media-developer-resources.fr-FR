---
description: L’heure de la vidéo est l’affichage numérique qui montre l’heure et la durée actuelles de la vidéo en cours de lecture.
solution: Experience Manager
title: Durée de la vidéo
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 90ec189e-6de4-44b3-8760-1e8636b919ba
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 2%

---

# Durée de la vidéo{#video-time}

L’heure de la vidéo est l’affichage numérique qui montre l’heure et la durée actuelles de la vidéo en cours de lecture.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La famille de polices, la taille de police et la couleur de police de l’heure de la vidéo font partie des propriétés que CSS peut contrôler. Il peut également être positionné, par rapport à la barre de contrôle qui la contient, par CSS.

L’aspect de l’heure de la vidéo est contrôlé par le sélecteur de classe CSS suivant :

```
.s7interactivevideoviewer .s7videotime
```

## Propriétés CSS de l’heure de la vidéo {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure, y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> droite </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure droite, y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Largeur du contrôle de l’heure de la vidéo. Cette propriété est requise pour qu’Internet Explorer 8 ou version ultérieure fonctionne correctement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Famille de polices à utiliser pour le texte d’affichage temporel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Taille de police à utiliser pour le texte d’affichage temporel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Couleur de police à utiliser pour le texte d’affichage temporel. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-e8caea0a303c425a8a637c2a47c06355}

Définissez le temps de la vidéo sur gris clair (hexadécimal `#BBBBBB`), de taille 12 pixels, positionné à 15 pixels du haut de la barre de contrôle et à 80 pixels du haut et du bord droit de la barre de contrôle.

```
.s7interactivevideoviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
