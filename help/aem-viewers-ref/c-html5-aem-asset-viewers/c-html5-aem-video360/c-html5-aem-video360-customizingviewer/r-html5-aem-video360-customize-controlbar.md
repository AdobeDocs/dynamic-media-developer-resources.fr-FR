---
description: La barre de contrôle est la zone rectangulaire qui contient et se trouve derrière tous les contrôles de l’interface utilisateur disponibles pour la visionneuse de vidéos, tels que le bouton Lecture/Pause, les commandes de volume, etc.
solution: Experience Manager
title: Barre de contrôle
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéo 360 VR
role: Développeur, Professionnel
exl-id: 06078310-8aeb-449f-919a-ce88ddc8c4b3
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---

# Barre de contrôle{#control-bar}

La barre de contrôle est la zone rectangulaire qui contient et se trouve derrière tous les contrôles de l’interface utilisateur disponibles pour la visionneuse de vidéos, tels que le bouton Lecture/Pause, les commandes de volume, etc.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La barre de contrôle prend toujours toute la largeur de visionneuse disponible. Il est possible de modifier sa couleur, sa hauteur et sa position verticale en CSS, par rapport au conteneur de la visionneuse de vidéos.

Le sélecteur de classe CSS suivant contrôle l’aspect de la barre de contrôle :

```
.s7video360viewer .s7controlbar
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
   <td colname="col1"> <p> <span class="codeph"> arrière-plan-couleur  </span> </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la barre de contrôle. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple**  : pour configurer une visionneuse de vidéos avec une barre de contrôle grise de 30 pixels et située en haut du conteneur de la visionneuse de vidéos.

```
.s7video360viewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
