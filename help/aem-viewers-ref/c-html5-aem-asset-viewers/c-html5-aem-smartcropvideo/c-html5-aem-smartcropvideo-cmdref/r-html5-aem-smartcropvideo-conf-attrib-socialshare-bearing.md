---
description: Attribut de configuration de la visionneuse de vidéos avec recadrage intelligent.
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 391efc4e-23f6-4159-8b03-ad1c9a887ec3
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

Attribut de configuration de la visionneuse de vidéos avec recadrage intelligent.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-latéral</span> </p> </td> 
   <td colname="col2"> <p> Indique la direction de l’animation de diapositives pour le conteneur de boutons. </p> <p> Lorsque la variable est définie sur <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span>ou <span class="codeph"> right</span>, le panneau se déploie dans une direction spécifiée sans vérification des limites supplémentaire, ce qui peut entraîner un écrêtage du panneau par un conteneur externe. </p> <p>Lorsque la variable est définie sur <span class="codeph"> ajusté vertical</span>, le composant déplace d’abord la position du panneau de base vers le bas de SocialShare et tente de déployer le panneau depuis le bas, la droite ou la gauche de cet emplacement de base. À chaque tentative, le composant vérifie si le panneau est tronqué par un conteneur externe. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et répète les tentatives de déploiement en haut, à droite et à gauche. </p> <p>Lorsque la variable est définie sur <span class="codeph"> ajusté latéral</span>, le composant utilise une logique similaire. Cependant, il déplace d’abord la base vers la droite, en essayant vers la droite, vers le bas et vers le haut, puis déplace la base vers la gauche, en essayant vers la gauche, vers le bas et vers le haut, vers le haut, vers le haut. </p> </td> 
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
