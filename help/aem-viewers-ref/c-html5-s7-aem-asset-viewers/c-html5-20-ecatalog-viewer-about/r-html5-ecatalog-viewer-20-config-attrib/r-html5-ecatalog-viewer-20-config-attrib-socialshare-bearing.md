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
   <td colname="col1"> <p> <span class="codeph"> haut|bas|gauche|droite|ajuster-vertical|ajuster-latéral </span> </p> </td> 
   <td colname="col2"> <p> Indique la direction de l’animation de la diapositive pour le conteneur de boutons. </p> <p> Lorsqu’il est réglé sur <span class="codeph"> haut </span>, <span class="codeph"> bas </span>, <span class="codeph"> gauche </span>ou <span class="codeph"> droite </span>, le panneau se déploie dans une direction spécifiée sans vérification supplémentaire des limites. Ce comportement peut entraîner l’écrêtage du panneau par un conteneur extérieur. </p> <p>Lorsqu’il est défini sur <span class="codeph"> ajuster verticalement </span>, le composant déplace d’abord la position du panneau de base vers le bas de SocialShare et tente de déployer le panneau à partir du bas, de la droite ou de la gauche, à partir de cet emplacement de base. À chaque tentative, le composant vérifie si le panneau est écrêté par un conteneur extérieur. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et de répéter les tentatives de déploiement en haut, à droite et à gauche. </p> <p>Lorsqu’il est défini sur ajustement latéral, <span class="codeph">le composant utilise une logique similaire à celle de l’ajustement </span> vertical. Toutefois, il déplace la base vers la droite (première tentative vers la droite, vers le bas et vers le haut), puis déplace la base vers la gauche, en essayant les directions de déploiement vers la gauche, vers le bas et vers le haut. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-8e843b967237426e9a8b3cd0f27b9820}

Facultatif.

## Par défaut {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## Exemple {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
