---
description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-title: SocialPartager.aring
solution: Experience Manager
title: SocialPartager.aring
topic: Dynamic media
uuid: b3978280-7826-44c0-bd25-357e145121f8
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# SocialPartager.aring{#socialshare-bearing}

Attribut de configuration pour la visionneuse de vidéos interactive.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Haut|Bas|Gauche|Droite|Ajuster-vertical|Ajuster-latéral</span> </p> </td> 
   <td colname="col2"> <p> Indique la direction de l’animation des diapositives pour les  de boutons. Lorsqu’il est défini sur <span class="codeph"> Haut</span>, <span class="codeph"> Bas</span>, <span class="codeph"></span><span class="codeph"> gaucheou droite, le panneau se déploie dans la direction spécifiée sans vérification supplémentaire des limites, ce qui peut entraîner l’écrêtage du panneau par un  externe.</span> </p> <p>Lorsqu’il est <span class="codeph"> ajusté à la verticale</span>, le composant déplace d’abord la position du panneau de base vers le bas de SocialShare et tente de déployer le panneau dans l’une des directions suivantes à partir d’un emplacement de base : en bas, à droite, à gauche. A chaque tentative, le composant vérifie si le panneau est coupé par un  externe. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et répète les tentatives de déploiement depuis le haut, la droite et la gauche. </p> <p>Lorsqu’il est <span class="codeph"> ajusté latéralement</span>, le composant utilise une logique similaire, mais déplace d’abord la base vers la droite, en essayant de suivre les directions de droite, de bas et de déploiement vers le haut. Ensuite, il déplace la base vers la gauche, en essayant de suivre les directions vers la gauche, vers le bas et vers le haut. </p> </td> 
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

