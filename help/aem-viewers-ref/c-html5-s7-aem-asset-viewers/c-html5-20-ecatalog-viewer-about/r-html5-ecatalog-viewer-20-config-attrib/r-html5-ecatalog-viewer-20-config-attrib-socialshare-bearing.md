---
description: 'null'
seo-description: 'null'
seo-title: SocialPartager.aring
solution: Experience Manager
title: SocialPartager.aring
topic: Dynamic media
uuid: e48b39bb-c23d-42ce-9dc6-6e8b0d9b04ea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SocialPartager.aring{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Haut|Bas|Gauche|Droite|Ajuster-vertical|Ajuster-latéral </span> </p> </td> 
   <td colname="col2"> <p> Indique la direction de l’animation des diapositives pour le de boutons. </p> <p> Lorsqu’il est défini sur <span class="codeph"> Haut </span>, <span class="codeph"> Bas </span>, <span class="codeph"> Gauche </span><span class="codeph"> ou  droite, le panneau se déploie dans une direction spécifiée sans vérification supplémentaire des limites. </span> Ce comportement peut entraîner l’écrêtage du panneau par un  externe. </p> <p>Lorsqu’il est <span class="codeph"> ajusté à la verticale </span>, le composant déplace d’abord la position du panneau de base vers le bas de SocialShare et tente de déployer le panneau depuis le bas, la droite ou la gauche de cet emplacement de base. A chaque tentative, le composant vérifie si le panneau est coupé par un  externe. Si toutes les tentatives échouent, le composant tente de déplacer la position du panneau de base vers le haut et de répéter les tentatives de déploiement depuis le haut, la droite et la gauche. </p> <p>Lorsqu’il est défini sur <span class="codeph"> latéral </span>, le composant utilise une logique similaire à celle de l’ajustement vertical, mais déplace la base vers la droite en essayant d’abord vers la droite, vers le bas et vers le haut en déroulant les directions, puis déplace la base vers la gauche, en essayant vers la gauche, vers le bas et vers le haut en déroulant les directions. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-8e843b967237426e9a8b3cd0f27b9820}

Facultatif.

## Par défaut {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## Exemple {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
