---
title: SocialShare.bearing
description: Attribut de configuration de la visionneuse de vidéos interactives.
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

Attribut de configuration de la visionneuse de vidéos interactives.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-latéral</span> </p> </td> 
   <td colname="col2"> <p> Indique la direction de l’animation des diapositives pour le conteneur de boutons. Lorsqu’il est défini sur <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span> ou <span class="codeph"> right</span>, le panneau se déploie dans la direction spécifiée sans vérification des limites supplémentaire, ce qui peut entraîner le rognage du panneau par un conteneur externe. </p> <p>Lorsqu’il est défini sur <span class="codeph"> ajusté vertical </span>, le composant déplace d’abord la position du panneau de base vers le bas de SocialShare. Ensuite, il tente de déployer le panneau dans l’une des directions suivantes à partir d’un emplacement de base de ce type : bas, droite, gauche. À chaque tentative, le composant vérifie si le panneau est tronqué par un conteneur externe. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et répète les tentatives de déploiement depuis le haut, la droite et la gauche. </p> <p>Lorsqu’il est défini sur <span class="codeph"> rationnel </span>, le composant utilise une logique similaire, mais déplace d’abord la base vers la droite, en essayant de suivre les instructions de déploiement vers le bas, vers le bas et vers le haut. Ensuite, il déplace la base vers la gauche, en essayant de suivre les directions vers la gauche, vers le bas et vers le haut. </p> </td> 
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
