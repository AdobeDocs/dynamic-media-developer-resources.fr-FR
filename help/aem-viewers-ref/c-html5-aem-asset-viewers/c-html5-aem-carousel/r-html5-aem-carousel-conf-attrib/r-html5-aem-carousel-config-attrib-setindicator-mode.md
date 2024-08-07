---
title: SetIndicator.mode
description: SetIndicator.mode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 4%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> numeric|dotted</span> </p> </td> 
   <td colname="col2"> <p> Configure le style de rendu de l’indicateur défini. </p> <p>Lorsqu’il est défini sur <span class="codeph"> pointillés </span>, le composant effectue le rendu des indicateurs identiques pour toutes les pages. </p> <p>Lorsqu’il est défini sur <span class="codeph"> numeric</span>, il place un numéro de page de base 1 dans chaque élément d’indicateur. </p> <p>Le mode d’opération <span class="codeph"> numérique</span> n’est pas pris en charge sur les périphériques dotés d’une entrée tactile. À la place, le composant utilise <span class="codeph"> pointillé</span> sur ces périphériques. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`dotted`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
