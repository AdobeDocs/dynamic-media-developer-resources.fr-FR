---
description: ZoomView.zoomstep
solution: Experience Manager
title: ZoomView.zoomstep
feature: Dynamic Media Classic, Visionneuses, SDK/API, Combiner des visionneuses de supports
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 6%

---


# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *``*[, *`pas à pas`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> étape</span></span> </p> </td> 
   <td colname="col2"> <p> Configure le nombre d’actions de zoom avant et d’zoom arrière requises pour augmenter ou diminuer la résolution d’un facteur de deux. La modification de résolution pour chaque action de zoom est de 2^1 par étape. Définissez ce paramètre sur <span class="codeph"> 0</span> pour effectuer un zoom en résolution maximale avec une seule action de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> limiter</span></span> </p> </td> 
   <td colname="col2"> <p> Indique la résolution de zoom maximale par rapport à l’image de résolution complète. La valeur par défaut est <span class="codeph"> 1.0</span>, ce qui n’autorise pas le zoom au-delà de la résolution maximale. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomstep=2,3`
