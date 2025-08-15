---
title: Barre de contrôle
description: La barre de contrôle est la zone rectangulaire qui contient toutes les commandes de l’interface utilisateur disponibles pour la visionneuse de vidéos, telles que le bouton Lecture/Pause, les commandes de volume, etc., et se trouve derrière elles.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f0de655c-36f0-4ed4-806c-d486eed2201b
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Barre de contrôle{#control-bar}

La barre de contrôle est la zone rectangulaire qui contient toutes les commandes de l’interface utilisateur disponibles pour la visionneuse de vidéos, telles que le bouton Lecture/Pause, les commandes de volume, etc., et se trouve derrière elles.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La barre de contrôle utilise toujours toute la largeur de visionneuse disponible. Il est possible de modifier sa couleur, sa hauteur et sa position verticale par CSS, par rapport au conteneur de la visionneuse vidéo.

Le sélecteur de classe CSS suivant contrôle l’aspect de la barre de contrôle :

```
.s7mixedmediaviewer .s7controlbar
```

## Propriétés CSS de la barre de contrôle {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> de hauteur </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la barre de contrôle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la barre de contrôle. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-e8caea0a303c425a8a637c2a47c06355}

Pour configurer une visionneuse de médias mixtes avec une barre de contrôle grise de 30 pixels de haut.

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
