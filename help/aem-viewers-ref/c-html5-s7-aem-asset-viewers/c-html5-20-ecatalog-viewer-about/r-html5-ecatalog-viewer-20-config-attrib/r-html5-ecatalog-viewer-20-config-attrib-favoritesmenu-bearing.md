---
title: FavoritesMenu.bing
description: Indique la direction de l’animation des diapositives pour le conteneur Boutons.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: f08545fd-f039-41a1-ad0b-430ce7c1bdd1
TQID: 'https://experienceleague.adobe.com/zWVKT6TznkJpBNJ74-vkCnfNkgjBiGJ0dKRVsQnEwvs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 189
ht-degree: 1%

---

# FavoritesMenu.bing{#favoritesmenu-bearing}

Indique la direction de l’animation des diapositives pour le conteneur Boutons.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> vers le haut|bas|gauche|droite|fit-vertical|fit-latéral</span> </p> </td> 
   <td colname="col2"> <p> Lorsque vous définissez cette option sur <span class="codeph"> vers le haut</span> <span class="codeph"> vers le bas</span> <span class="codeph"> vers la gauche</span> ou <span class="codeph"> droite</span> le panneau se déploie dans une direction spécifiée sans vérification des limites supplémentaires, ce qui entraîne l’écrêtage du panneau par un conteneur externe. </p> <p>Lorsqu’il est défini sur <span class="codeph"> vertical</span> le composant déplace d’abord la position du panneau de base vers le bas du menu Favoris. Il tente de déployer le panneau dans l’une des directions suivantes à partir de cet emplacement de base : bas, droite, gauche. À chaque tentative, le composant vérifie si le panneau est tronqué par un conteneur externe. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et de répéter les tentatives de déploiement dans les directions supérieure, droite et gauche. </p> <p>Lorsqu’il est défini sur <span class="codeph"> ajustement latéral</span> le composant utilise une logique similaire. La base est d'abord décalée vers la droite, en essayant vers la droite, vers le bas et vers le haut. Ensuite, il déplace la base vers la gauche, essayant vers la gauche, vers le bas et vers le haut. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
