---
description: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fa094d84-927b-48f2-9c82-61f2a446158b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vers le haut|vers le bas|gauche|droite|fit-vertical|fit-latéral </span> </p> </td> 
   <td colname="col2"> <p> Indique la direction de l’animation des diapositives pour le conteneur Boutons. </p> <p> Lorsqu’il est configuré pour <span class="codeph"> des </span>, <span class="codeph"> vers le bas </span>, <span class="codeph"> </span> gauche ou <span class="codeph"> </span> droite, le panneau se déploie dans une direction spécifiée sans vérification supplémentaire des limites. Ce comportement peut entraîner l’écrêtage du panneau par un conteneur externe. </p> <p>Lorsqu'il est défini sur <span class="codeph">'</span> vertical ajusté, le composant déplace d'abord la position du panneau de base vers le bas de SocialShare et tente de déployer le panneau depuis le bas, la droite ou la gauche, à partir de cet emplacement de base. À chaque tentative, le composant vérifie si le panneau est tronqué par un conteneur externe. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et de répéter les tentatives de déploiement dans les directions supérieure, droite et gauche. </p> <p>Lorsqu’il est défini sur <span class="codeph"> les </span> d’ajustement latéraux, le composant utilise une logique similaire à celle de l’ajustement vertical, mais déplace plutôt la base vers la droite en essayant d’abord les directions de déploiement droite, vers le bas et vers le haut, puis déplace la base vers la gauche en essayant les directions de déploiement gauche, vers le bas et vers le haut. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-8e843b967237426e9a8b3cd0f27b9820}

Facultatif.

## Par défaut {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## Exemple {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
