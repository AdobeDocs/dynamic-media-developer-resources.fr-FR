---
description: Indique la direction de l’animation des diapositives pour le de boutons.
seo-description: Indique la direction de l’animation des diapositives pour le de boutons.
seo-title: FavorisMenu.wing
solution: Experience Manager
title: FavorisMenu.wing
topic: Dynamic media
uuid: badc02ef-2724-41bb-9b00-c65966be8577
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FavorisMenu.wing{#favoritesmenu-bearing}

Indique la direction de l’animation des diapositives pour le de boutons.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Haut|Bas|Gauche|Droite|Ajuster-vertical|Ajuster-latéral</span> </p> </td> 
   <td colname="col2"> <p> Lorsqu’il est défini sur <span class="codeph"> Haut</span>, <span class="codeph"> Bas</span>, <span class="codeph"></span><span class="codeph"> gaucheou droite, le panneau se déploie dans une direction spécifiée sans vérification supplémentaire des limites, ce qui entraîne l’écrêtage du panneau par un  externe.</span> </p> <p>Lorsqu’il est <span class="codeph"> ajusté à la verticale</span>, le composant déplace d’abord la position du panneau de base vers le bas du menu Favoris et tente de déployer le panneau dans l’une des directions suivantes à partir de cet emplacement de base : en bas, à droite, à gauche. A chaque tentative, le composant vérifie si le panneau est coupé par un  externe. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et de répéter les tentatives de déploiement depuis le haut, la droite et la gauche. </p> <p>Lorsqu’il est défini sur <span class="codeph"> ajusté latéral</span>, le composant utilise une logique similaire. La base est déplacée vers la droite en premier, en essayant à droite, en bas et en haut des directions. Ensuite, il déplace la base vers la gauche, en essayant de se diriger vers la gauche, vers le bas et vers le haut. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
