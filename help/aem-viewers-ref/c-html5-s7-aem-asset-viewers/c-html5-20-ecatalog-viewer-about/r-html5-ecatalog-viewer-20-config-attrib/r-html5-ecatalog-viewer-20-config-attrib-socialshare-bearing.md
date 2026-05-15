---
title: SocialShare.bear
description: SocialShare.bear
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026b5921-53ae-436f-bf82-dee2e699405f
TQID: 'https://experienceleague.adobe.com/sWilQyllf5wtlr-tP1kKtK4L0taRA6HWQW2Yh0MSefQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 184
ht-degree: 1%

---

# SocialShare.bear{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vers le haut|vers le bas|gauche|droite|fit-vertical|fit-latéral </span> </p> </td> 
   <td colname="col2"> <p> Indique la direction de l’animation des diapositives pour le conteneur Boutons. </p> <p> Lorsqu’il est configuré pour <span class="codeph"> </span> vers le haut, <span class="codeph"> vers le bas </span>, <span class="codeph"> </span> gauche ou <span class="codeph"> </span> droite, le panneau se déploie dans une direction spécifiée sans vérification des limites supplémentaires. Ce comportement peut entraîner l’écrêtage du panneau par un conteneur externe. </p> <p>Lorsqu'il est défini sur <span class="codeph">'</span> vertical ajusté, le composant déplace d'abord la position du panneau de base vers le bas de SocialShare et tente de déployer le panneau depuis le bas, la droite ou la gauche, à partir de cet emplacement de base. À chaque tentative, le composant vérifie si le panneau est tronqué par un conteneur externe. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et de répéter les tentatives de déploiement dans les directions supérieure, droite et gauche. </p> <p>Lorsqu’il est défini sur <span class="codeph"> des </span> d’ajustement latéraux, le composant utilise une logique similaire à celle de l’ajustement vertical. Toutefois, il déplace la base vers la droite en commençant par la direction de déploiement vers la droite, vers le bas et vers le haut, puis déplace la base vers la gauche en essayant vers la gauche, vers le bas et vers le haut. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-8e843b967237426e9a8b3cd0f27b9820}

Facultatif.

## Par défaut {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## Exemple {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
