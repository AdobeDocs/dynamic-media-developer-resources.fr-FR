---
description: Indique la direction de l'animation des diapositives pour le conteneur des boutons.
solution: Experience Manager
title: FavoritesMenu.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 2%

---


# FavoritesMenu.bearing{#favoritesmenu-bearing}

Indique la direction de l&#39;animation des diapositives pour le conteneur des boutons.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-latéral</span> </p> </td> 
   <td colname="col2"> <p> Lorsqu’il est défini sur <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span> ou <span class="codeph"> right</span>, le panneau se déploie dans la direction spécifiée sans vérification des limites supplémentaires, ce qui entraîne l’écrêtage du panneau par un conteneur extérieur. </p> <p>Lorsqu'il est défini sur <span class="codeph"> fit-vertical</span>, le composant déplace d'abord la position du panneau de base vers le bas du menu Favoris et tente de déployer le panneau dans l'une des directions suivantes à partir de cet emplacement de base : en bas, à droite, à gauche. A chaque tentative, le composant vérifie si le panneau est coupé par un conteneur extérieur. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et de répéter les tentatives de déploiement depuis le haut, la droite et la gauche. </p> <p>Lorsqu'il est défini sur <span class="codeph"> raccord-latéral</span>, le composant utilise une logique similaire. La base est déplacée vers la droite en premier, essayant à droite, vers le bas et vers le haut. Ensuite, il déplace la base vers la gauche, en essayant de délocaliser les directions vers la gauche, vers le bas et vers le haut. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
