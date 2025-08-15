---
title: SocialShare.bearing
description: Attribut de configuration pour la visionneuse vidéo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 391efc4e-23f6-4159-8b03-ad1c9a887ec3
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

Attribut de configuration pour la visionneuse vidéo.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> haut|bas|gauche|droite|ajuster-vertical|ajuster-latéral</span> </p> </td> 
   <td colname="col2"> <p> Indique la direction de l’animation de la diapositive pour le conteneur de boutons. </p> <p> Lorsqu’il est défini sur <span class="codeph"> haut</span>, <span class="codeph"> bas</span>, <span class="codeph"> gauche</span> ou <span class="codeph"> droite</span>, le panneau se déploie dans une direction spécifiée sans vérification supplémentaire des limites, ce qui peut entraîner l’écrêtage du panneau par un conteneur extérieur. </p> <p>Lorsqu’il est défini sur <span class="codeph"> ajuster verticalement</span>, le composant déplace d’abord la position du panneau de base vers le bas de SocialShare et tente de déployer le panneau du bas, de la droite ou de la gauche à partir de cet emplacement de base. À chaque tentative, le composant vérifie si le panneau est clipsé par un conteneur extérieur. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et de répéter les tentatives de déploiement en haut, à droite et à gauche. </p> <p>Lorsqu’il est défini sur l’ajustement <span class="codeph"></span>latéral, le composant utilise une logique similaire. Toutefois, il déplace d’abord la base vers la droite, en essayant les directions de déploiement vers la droite, vers le bas et vers le haut, puis déplace la base vers la gauche, en essayant les directions de déploiement vers la gauche, vers le bas et vers le haut. </p> </td> 
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
