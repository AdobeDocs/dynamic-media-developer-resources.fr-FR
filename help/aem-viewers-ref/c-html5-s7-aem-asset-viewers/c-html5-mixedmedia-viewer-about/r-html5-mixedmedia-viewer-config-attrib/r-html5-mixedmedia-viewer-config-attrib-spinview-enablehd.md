---
description: SpinView.enableHD
solution: Experience Manager
title: SpinView.enableHD
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,User
exl-id: 0a2abdc6-eae5-4dda-b749-599cd8a07a98
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 6%

---

# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`nombre`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Activez, limitez ou désactivez l’optimisation pour les appareils pour lesquels la valeur <span class="codeph"> devicePixelRatio</span> est supérieure à <span class="codeph"> 1</span>, c’est-à-dire les appareils avec un affichage haute densité comme l’iPhone4 et les appareils similaires. Si principal, le composant limite la taille de la demande d’image IS comme si l’appareil avait uniquement un rapport de pixels de <span class="codeph"> 1</span> et réduisait donc la bande passante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> nombre</span></span> </p> </td> 
   <td colname="col2"> <p> Si vous utilisez le paramètre <span class="codeph"> limit</span> , le composant n’active la haute densité en pixels que jusqu’à la limite spécifiée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
