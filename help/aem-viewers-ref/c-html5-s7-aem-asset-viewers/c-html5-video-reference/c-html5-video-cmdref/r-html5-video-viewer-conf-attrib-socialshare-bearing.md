---
title: SocialShare.bear
description: Attribut de configuration de la visionneuse de vidéos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 391efc4e-23f6-4159-8b03-ad1c9a887ec3
TQID: 'https://experienceleague.adobe.com/YhNrijfrkxHpLzZFMRr2AdjFARJ8E5xSaTfhANHbXGo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 185
ht-degree: 1%

---

# SocialShare.bear{#socialshare-bearing}

Attribut de configuration de la visionneuse de vidéos.

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
