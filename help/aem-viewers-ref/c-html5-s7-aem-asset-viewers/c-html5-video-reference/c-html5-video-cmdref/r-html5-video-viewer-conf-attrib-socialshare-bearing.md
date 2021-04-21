---
description: Attribut de configuration pour la visionneuse de vidéos.
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---


# SocialShare.bearing{#socialshare-bearing}

Attribut de configuration pour la visionneuse de vidéos.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-latéral</span> </p> </td> 
   <td colname="col2"> <p> Indique la direction de l'animation de la diapositive pour le conteneur des boutons. </p> <p> Lorsqu’il est défini sur <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span> ou <span class="codeph"> right</span>, le panneau se déploie dans une direction spécifiée sans vérification des limites supplémentaires, ce qui peut entraîner l’écrêtage du panneau par un conteneur externe. </p> <p>Lorsqu’il est défini sur <span class="codeph"> fit-vertical</span>, le composant déplace d’abord la position du panneau de base vers le bas de SocialShare et tente de déployer le panneau depuis le bas, la droite ou la gauche de cet emplacement de base. A chaque tentative, le composant vérifie si le panneau est coupé par un conteneur extérieur. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et de répéter les tentatives de déploiement en haut, à droite et à gauche. </p> <p>Lorsqu'il est défini sur <span class="codeph"> raccord-latéral</span>, le composant utilise une logique similaire. Cependant, il déplace d'abord la base vers la droite, en essayant à droite, vers le bas et vers le haut les directions de déploiement, puis déplace la base vers la gauche, en essayant à gauche, vers le bas et vers le haut les directions de déploiement. </p> </td> 
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

