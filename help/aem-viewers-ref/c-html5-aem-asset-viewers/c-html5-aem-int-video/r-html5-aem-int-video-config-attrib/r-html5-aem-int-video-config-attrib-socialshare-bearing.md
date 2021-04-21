---
description: Attribut de configuration pour la visionneuse de vidéos interactive.
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: f34d6954-01c5-49e0-94d4-fd577c57956e
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

Attribut de configuration pour la visionneuse de vidéos interactive.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-latéral</span> </p> </td> 
   <td colname="col2"> <p> Indique la direction de l'animation des diapositives pour le conteneur des boutons. Lorsqu’il est défini sur <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span> ou <span class="codeph"> right</span>, le panneau se déploie dans la direction spécifiée sans vérification des limites supplémentaires, ce qui peut entraîner l’écrêtage du panneau par un conteneur externe. </p> <p>Lorsqu’il est défini sur <span class="codeph"> fit-vertical</span>, le composant déplace d’abord la position du panneau de base vers le bas de SocialShare et tente de déployer le panneau dans l’une des directions suivantes à partir d’un tel emplacement de base : en bas, à droite, à gauche. A chaque tentative, le composant vérifie si le panneau est coupé par un conteneur extérieur. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et répète les tentatives de déploiement depuis le haut, la droite et la gauche. </p> <p>Lorsqu'il est défini sur <span class="codeph"> raccord-latéral</span>, le composant utilise une logique similaire, mais déplace d'abord la base vers la droite, en essayant de suivre les directions de droite, de bas et de déploiement supérieur. Ensuite, il déplace la base vers la gauche, en essayant de suivre les directions de déploiement vers la gauche, vers le bas et vers le haut. </p> </td> 
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
