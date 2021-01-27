---
description: La barre de contrôle est la zone rectangulaire qui contient et se trouve derrière tous les contrôles de l’interface utilisateur disponibles pour la visionneuse de vidéos, tels que le bouton Lecture/Pause, les commandes de volume, etc.
seo-description: La barre de contrôle est la zone rectangulaire qui contient et se trouve derrière tous les contrôles de l’interface utilisateur disponibles pour la visionneuse de vidéos, tels que le bouton Lecture/Pause, les commandes de volume, etc.
seo-title: Barre de contrôle
solution: Experience Manager
title: Barre de contrôle
topic: Dynamic Media
uuid: 7b7dccb3-6c64-4342-aac7-82c769561902
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 1%

---


# Barre de contrôle{#control-bar}

La barre de contrôle est la zone rectangulaire qui contient et se trouve derrière tous les contrôles de l’interface utilisateur disponibles pour la visionneuse de vidéos, tels que le bouton Lecture/Pause, les commandes de volume, etc.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La barre de contrôle prend toujours toute la largeur de visionneuse disponible. Il est possible de modifier sa couleur, sa hauteur et sa position verticale en CSS, par rapport au conteneur de la visionneuse de vidéos.

Le sélecteur de classe CSS suivant contrôle l’aspect de la barre de contrôle :

```
.s7mixedmediaviewer .s7controlbar
```

## Propriétés CSS de la barre de contrôle {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la barre de contrôle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la barre de contrôle. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-e8caea0a303c425a8a637c2a47c06355}

Configuration d’une visionneuse de supports variés avec une barre de contrôle grise de 30 pixels.

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

