---
title: SocialShare.bearing
description: Attribut de configuration pour la visionneuse Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: f00b2539-3159-487a-b0fa-9589b694c2e6
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

Attribut de configuration pour la visionneuse Video360.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vers le haut|bas|gauche|droite|fit-vertical|fit-latéral</span> </p> </td> 
   <td colname="col2"> <p> Indique la direction de l’animation des diapositives pour le conteneur Boutons. </p> <p> Lorsqu’il est configuré pour <span class="codeph"> vers le haut</span> <span class="codeph"> le bas</span> <span class="codeph"> la gauche</span> ou <span class="codeph"> la droite</span> le panneau se déploie dans une direction spécifiée sans vérification des limites supplémentaires, ce qui peut entraîner l’écrêtage du panneau par un conteneur externe. </p> <p>Lorsqu'il est défini sur <span class="codeph"> ajustement vertical</span> le composant déplace d'abord la position du panneau de base vers le bas de SocialShare et tente de déployer le panneau à partir du bas, de la droite ou de la gauche de cet emplacement de base. À chaque tentative, le composant vérifie si le panneau est tronqué par un conteneur externe. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et de répéter les tentatives de déploiement dans les directions supérieure, droite et gauche. </p> <p>Lorsqu’il est défini sur <span class="codeph"> ajustement latéral</span> le composant utilise une logique similaire. Toutefois, il déplace d’abord la base vers la droite, en essayant vers la droite, vers le bas et vers le haut, puis déplace la base vers la gauche, en essayant vers la gauche, vers le bas et vers le haut. </p> </td> 
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
