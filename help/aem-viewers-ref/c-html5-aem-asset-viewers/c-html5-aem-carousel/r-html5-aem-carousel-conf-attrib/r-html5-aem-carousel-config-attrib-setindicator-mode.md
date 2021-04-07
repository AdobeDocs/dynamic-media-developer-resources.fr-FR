---
description: SetIndicator.mode
solution: Experience Manager
title: SetIndicator.mode
feature: Dynamic Media Classic, Visionneuses, SDK/API, Bannières de carrousel
role: Développeur, Professionnel
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 5%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> numérique|pointillé</span> </p> </td> 
   <td colname="col2"> <p> Configure le style de rendu de l’indicateur défini. </p> <p>Lorsqu’il est défini sur <span class="codeph"> pointillé</span>, le composant effectue le rendu des indicateurs identiques pour toutes les pages. </p> <p>Lorsqu’elle est définie sur <span class="codeph"> numeric</span>, elle place un numéro de page de base 1 à l’intérieur de chaque élément d’indicateur. </p> <p>Le mode de fonctionnement <span class="codeph"> numeric</span> n'est pas pris en charge sur les périphériques capables d'entrer des données tactiles. À la place, le composant utilise <span class="codeph"> pointillé</span> sur ces périphériques. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`dotted`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
