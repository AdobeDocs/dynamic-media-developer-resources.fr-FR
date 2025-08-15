---
title: SpinView.enableHD
description: SpinView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0a2abdc6-eae5-4dda-b749-599cd8a07a98
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`nombre`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> toujours|jamais|limite</span> </p> </td> 
   <td colname="col2"> <p> Activez, limitez ou désactivez l’optimisation pour les appareils sur lesquels <span class="codeph"> devicePixelRatio</span> est supérieur à <span class="codeph"> 1</span>, c’est-à-dire les appareils dotés d’un écran haute densité comme l’iPhone4 et les appareils similaires. S’il est actif, le composant limite la taille de la demande d’image IS comme si le périphérique n’avait qu’un rapport de pixels de <span class="codeph"> 1</span> et réduit donc la bande passante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> nombre</span></span> </p> </td> 
   <td colname="col2"> <p> Si vous utilisez le <span class="codeph"> paramètre de limite</span> , le composant permet une densité de pixels élevée uniquement jusqu’à la limite spécifiée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
