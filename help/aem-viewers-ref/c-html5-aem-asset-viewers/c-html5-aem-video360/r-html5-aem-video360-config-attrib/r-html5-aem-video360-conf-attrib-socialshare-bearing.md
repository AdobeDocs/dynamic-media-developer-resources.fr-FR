---
description: Attribut de configuration pour le lecteur vidéo360.
seo-description: Attribut de configuration pour le lecteur vidéo360.
seo-title: SocialPartager.aring
solution: Experience Manager
title: SocialPartager.aring
topic: Dynamic media
uuid: 43217e2e-71c5-4c58-94e0-c6ed38e25a5b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SocialPartager.aring{#socialshare-bearing}

Attribut de configuration pour le lecteur vidéo360.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Haut|Bas|Gauche|Droite|Ajuster-vertical|Ajuster-latéral</span> </p> </td> 
   <td colname="col2"> <p> Indique la direction de l’animation de la diapositive pour le de boutons. </p> <p> Lorsqu’il est défini sur <span class="codeph"> Haut</span>, <span class="codeph"> Bas</span>, <span class="codeph"></span><span class="codeph"> gaucheou droite, le panneau se déploie dans une direction spécifiée sans vérification supplémentaire des limites, ce qui peut entraîner l’écrêtage du panneau par un  externe.</span> </p> <p>Lorsqu’il est <span class="codeph"> ajusté à la verticale</span>, le composant déplace d’abord la position du panneau de base vers le bas de SocialShare et tente de déployer le panneau depuis le bas, la droite ou la gauche de cet emplacement de base. A chaque tentative, le composant vérifie si le panneau est coupé par un  externe. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et de répéter les tentatives de déploiement en haut, à droite et à gauche. </p> <p>Lorsqu’il est défini sur <span class="codeph"> ajusté latéral</span>, le composant utilise une logique similaire. Cependant, il déplace d’abord la base vers la droite, en essayant de suivre les directions de déploiement vers la droite, vers le bas et vers le haut, puis la base vers la gauche, en essayant de suivre les directions de déploiement vers la gauche, vers le bas et vers le haut. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
bearing=left
```

