---
description: Indique la direction de l’animation des diapositives pour le conteneur de boutons.
solution: Experience Manager
title: FavoritesMenu.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2466a288-59c2-4a5e-b0bd-ff5b42dcacdb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---

# FavoritesMenu.bearing{#favoritesmenu-bearing}

Indique la direction de l’animation des diapositives pour le conteneur de boutons.

[!DNL `[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-latéral</span> </p> </td> 
   <td colname="col2"> <p> Lorsqu’il est défini sur <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span> ou <span class="codeph"> right</span>, le panneau se déploie dans la direction spécifiée sans vérification des limites supplémentaire, ce qui entraîne un écrêtage du panneau par un conteneur externe. </p> <p>Lorsqu’il est défini sur <span class="codeph"> ajusté vertical </span>, le composant déplace d’abord la position du panneau de base vers le bas du menu Favoris et tente de déployer le panneau dans l’une des directions suivantes à partir de cet emplacement de base : bas, droite, gauche. À chaque tentative, le composant vérifie si le panneau est tronqué par un conteneur externe. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et répète les tentatives de déploiement depuis le haut, la droite et la gauche. </p> <p>Lorsqu’il est défini sur <span class="codeph"> rationnel </span>, le composant utilise une logique similaire. La base est déplacée vers la droite d'abord, en essayant vers la droite, vers le bas et vers le haut. Ensuite, il déplace la base vers la gauche, en essayant à gauche, vers le bas et vers le haut en déployant des directions. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fit-vertical`]

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `bearing=left`]
