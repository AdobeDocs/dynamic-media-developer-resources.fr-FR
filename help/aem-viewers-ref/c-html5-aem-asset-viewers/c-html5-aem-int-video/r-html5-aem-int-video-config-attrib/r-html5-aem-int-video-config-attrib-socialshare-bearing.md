---
title: SocialShare.bearing
description: Attribut de configuration pour la visionneuse de vidéos interactives.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f34d6954-01c5-49e0-94d4-fd577c57956e
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

Attribut de configuration pour la visionneuse de vidéos interactives.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vers le haut|bas|gauche|droite|fit-vertical|fit-latéral</span> </p> </td> 
   <td colname="col2"> <p> Indique la direction de l’animation des diapositives pour le conteneur Boutons. Lorsqu’il est réglé pour <span class="codeph"> vers le haut</span> <span class="codeph"> vers le bas</span> <span class="codeph"> vers la gauche</span> ou <span class="codeph"> droite</span> le panneau se déploie dans la direction spécifiée sans vérification supplémentaire des limites, ce qui peut entraîner l’écrêtage du panneau par un conteneur externe. </p> <p>Lorsqu'il est défini sur <span class="codeph"> ajustement vertical</span> le composant déplace d'abord la position du panneau de base vers le bas de SocialShare. Ensuite, il tente de déployer le panneau dans l’une des directions suivantes à partir d’un tel emplacement de base : bas, droite, gauche. À chaque tentative, le composant vérifie si le panneau est tronqué par un conteneur externe. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et répète les tentatives de déploiement dans une direction supérieure, droite et gauche. </p> <p>Lorsqu’il est défini sur <span class="codeph"> d’ajustement latéral</span> le composant utilise une logique similaire, mais déplace d’abord la base vers la droite, en essayant vers la droite, vers le bas et vers le haut. Elle déplace ensuite la base vers la gauche, en essayant la direction de déploiement vers la gauche, vers le bas et vers le haut. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```
