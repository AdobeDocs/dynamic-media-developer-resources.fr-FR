---
description: ZoomView.enableHD
solution: Experience Manager
title: ZoomView.enableHD
feature: Dynamic Media Classic, Visionneuses, SDK/API, Images interactives
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 6%

---


# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`nombre`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|jamais|limit</span> </p> </td> 
   <td colname="col2"> <p> Activez, limitez ou désactivez l’optimisation pour les périphériques pour lesquels <span class="codeph"> devicePixelRatio</span> est supérieur à <span class="codeph"> 1</span>. Affecte les périphériques à haute densité d’affichage tels que l’iPhone4 et les périphériques similaires. Si principal, le composant limite la taille de la demande d’image IS comme si le périphérique avait un rapport de pixels <span class="codeph"> 1</span>, réduisant ainsi la bande passante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> nombre</span></span> </p> </td> 
   <td colname="col2"> <p> Si vous utilisez le paramètre de limite, le composant n’active la densité de pixels élevée que jusqu’à la limite spécifiée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
