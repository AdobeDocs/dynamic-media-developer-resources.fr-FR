---
description: La barre de contrôle est la zone rectangulaire qui contient toutes les commandes de l’interface utilisateur disponibles pour la visionneuse de vidéos, telles que le bouton Lecture/Pause, les commandes de volume, etc.
seo-description: La barre de contrôle est la zone rectangulaire qui contient toutes les commandes de l’interface utilisateur disponibles pour la visionneuse de vidéos, telles que le bouton Lecture/Pause, les commandes de volume, etc.
seo-title: Barre de contrôle
solution: Experience Manager
title: Barre de contrôle
topic: Dynamic media
uuid: 5686b670-3c8c-4bef-b428-dc468f6ca05d
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Barre de contrôle{#control-bar}

La barre de contrôle est la zone rectangulaire qui contient toutes les commandes de l’interface utilisateur disponibles pour la visionneuse de vidéos, telles que le bouton Lecture/Pause, les commandes de volume, etc.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La barre de contrôle prend toujours la largeur totale de la visionneuse disponible. Il est possible de modifier sa couleur, sa hauteur et sa position verticale en CSS, par rapport au  de la visionneuse de vidéos.

Le sélecteur de classe CSS suivant contrôle l’aspect de la barre de contrôle :

```
.s7videoviewer .s7controlbar
```

## Propriétés CSS de la barre de contrôle {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure, y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bas </span> </p> </td> 
   <td colname="col2"> <p> Position à partir de la bordure inférieure, y compris le remplissage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hauteur de la barre de contrôle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la barre de contrôle. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-e8caea0a303c425a8a637c2a47c06355}

Configuration d’une visionneuse de vidéos avec une barre de contrôle grise de 30 pixels de haut et située en haut du  de la visionneuse de vidéos.

```
.s7videoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

