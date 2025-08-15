---
title: Barre de contrôle
description: La barre de contrôle est la zone rectangulaire qui contient et se trouve derrière tous les contrôles d’interface utilisateur disponibles pour la visionneuse de vidéos, tels que le bouton lecture/pause et les commandes de volume.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2239307a-4a05-4392-b35c-a64ea6c938ad
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---

# Barre de contrôle{#control-bar}

La barre de contrôle est la zone rectangulaire qui contient et se trouve derrière tous les contrôles d’interface utilisateur disponibles pour la visionneuse de vidéos, tels que le bouton lecture/pause et les commandes de volume.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La barre de contrôle prend toujours toute la largeur de visionneuse disponible. Il est possible de modifier sa couleur, sa hauteur et sa position verticale par CSS, par rapport au conteneur de la visionneuse vidéo.

Le sélecteur de classe CSS suivant contrôle l’apparence de la barre de contrôle :

```
.s7videoviewer .s7controlbar
```

## Propriétés CSS de la barre de contrôle {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Retour au début </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure, y compris le rembourrage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fond </span> </p> </td> 
   <td colname="col2"> <p> Position à partir de la bordure inférieure, remplissage compris. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la barre de contrôle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> couleur d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la barre de contrôle. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-e8caea0a303c425a8a637c2a47c06355}

Pour configurer une visionneuse de vidéos avec une barre de contrôle grise de 30 pixels de haut située en haut du conteneur de la visionneuse vidéo.

```
.s7videoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
