---
description: SpinView.autospin
solution: Experience Manager
title: SpinView.autospin
feature: Dynamic Media Classic, Visionneuses, SDK/API, Visionneuses à 360°
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 6%

---


# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *``*][, *``*][, *`durationdirectionspin_number`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Active ou désactive l'animation à 360° automatique. Pour optimiser la rotation automatique, il est recommandé de précharger toutes les images en définissant <span class="codeph"> maxloadradius</span> sur <span class="codeph"> -1</span>. Notez toutefois que cela se traduit par une augmentation du temps de chargement et de l’utilisation de la bande passante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> durée</span></span> </p> </td> 
   <td colname="col2"> <p> Nombre de secondes par rotation complète. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> direction</span></span> </p> </td> 
   <td colname="col2"> <p> La direction de rotation qui est <span class="codeph"> 0</span> pour la rotation est et <span class="codeph"> 1</span> pour la rotation ouest. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> spin_number</span></span> </p> </td> 
   <td colname="col2"> <p> Nombre de rotations complètes effectuées avant l’arrêt de la rotation automatique. Le nombre est un nombre à virgule flottante. Définissez sur <span class="codeph"> -1</span> pour une rotation automatique infinie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-924163cb2f6542499f49894becef7fb5}

Facultatif.

## Par défaut {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## Exemple {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
