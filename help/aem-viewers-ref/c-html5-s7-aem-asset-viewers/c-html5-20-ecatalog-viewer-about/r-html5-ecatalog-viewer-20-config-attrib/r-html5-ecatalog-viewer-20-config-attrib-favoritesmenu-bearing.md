---
title: FavoritesMenu.bearing
description: Indique la direction de l’animation de la diapositive pour le conteneur de boutons.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: f08545fd-f039-41a1-ad0b-430ce7c1bdd1
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 1%

---

# FavoritesMenu.bearing{#favoritesmenu-bearing}

Indique la direction de l’animation de la diapositive pour le conteneur de boutons.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> haut|bas|gauche|droite|ajuster-vertical|ajuster-latéral</span> </p> </td> 
   <td colname="col2"> <p> Lorsqu’il est défini sur <span class="codeph"> haut</span>, <span class="codeph"> bas</span>, <span class="codeph"> gauche</span> ou <span class="codeph"> droite</span>, le panneau se déploie dans la direction spécifiée sans vérification supplémentaire des limites, ce qui entraîne l’écrêtage du panneau par un conteneur extérieur. </p> <p>Lorsqu’il est défini sur <span class="codeph"> ajuster verticalement</span>, le composant déplace d’abord la position du panneau de base vers le bas du menu Favoris. Il tente de déployer le panneau dans l’une des directions suivantes à partir de cet emplacement de base : en bas, à droite, à gauche. À chaque tentative, le composant vérifie si le panneau est clipsé par un conteneur extérieur. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et de répéter les tentatives de déploiement dans les directions haut, droite et gauche. </p> <p>Lorsqu’il est défini sur l’ajustement <span class="codeph"></span>latéral, le composant utilise une logique similaire. La base est d’abord décalée vers la droite, en essayant les directions de déploiement vers la droite, vers le bas et vers le haut. Ensuite, il déplace la base vers la gauche, en essayant de déplacer les directions vers la gauche, vers le bas et vers le haut. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
