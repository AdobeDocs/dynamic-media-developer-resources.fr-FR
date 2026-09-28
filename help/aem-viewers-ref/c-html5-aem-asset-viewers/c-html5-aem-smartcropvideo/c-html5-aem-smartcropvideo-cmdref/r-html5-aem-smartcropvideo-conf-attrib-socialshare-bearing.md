---
title: SocialShare.bear
description: Attribut de configuration de la visionneuse de vidéos avec recadrage intelligent.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: ef45ba40-661c-4898-a4df-6293ad799a79
TQID: 'https://experienceleague.adobe.com/5b7-Ofn9ZcJTxG-RSwXCbW0pb5EgItA15pG9i2iXUU0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 1%
---
# SocialShare.bear{#socialshare-bearing}

Attribut de configuration de la visionneuse de vidéos avec recadrage intelligent.

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
