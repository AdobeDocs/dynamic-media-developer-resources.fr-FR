---
title: SocialShare.bearing
description: SocialShare.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026b5921-53ae-436f-bf82-dee2e699405f
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-latéral </span> </p> </td> 
   <td colname="col2"> <p> Indique la direction de l’animation des diapositives pour le conteneur de boutons. </p> <p> Lorsqu'il est défini sur <span class="codeph"> up </span>, <span class="codeph"> down </span>, <span class="codeph"> left </span> ou <span class="codeph"> right </span>, le panneau se déploie dans une direction spécifiée sans vérification des limites supplémentaires. Ce comportement peut entraîner un écrêtage du panneau par un conteneur externe. </p> <p>Lorsqu’il est défini sur <span class="codeph"> ajusté vertical </span>, le composant déplace d’abord la position du panneau de base vers le bas de SocialShare et tente de déployer le panneau depuis le bas, la droite ou la gauche, à partir de cet emplacement de base. À chaque tentative, le composant vérifie si le panneau est tronqué par un conteneur externe. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et répète les tentatives de déploiement depuis le haut, la droite et la gauche. </p> <p>Lorsqu’il est défini sur <span class="codeph"> ajustable </span>, le composant utilise une logique similaire à celle appliquée à la verticale. Cependant, il déplace la base vers la droite en commençant par la droite, vers le bas et vers le haut en déployant des directions, puis la déplace vers la gauche, en essayant vers la gauche, vers le bas et vers le haut en déployant des directions. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-8e843b967237426e9a8b3cd0f27b9820}

Facultatif.

## Par défaut {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## Exemple {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
