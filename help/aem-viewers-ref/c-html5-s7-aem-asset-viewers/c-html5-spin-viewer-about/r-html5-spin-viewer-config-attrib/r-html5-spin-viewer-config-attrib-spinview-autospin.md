---
title: SpinView.autospin
description: SpinView.autospin
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 16276e07-5494-4fd9-bd77-e77a46c57fd1
TQID: 'https://experienceleague.adobe.com/ZQj4mwz-MZWHf8MeY-hrrESZLucBeqXpGQV6tnD-U9w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 5%

---

# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *`duration`*][, *`direction`*][, *`spin_number`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Active ou désactive l'animation de rotation automatique. Pour obtenir une expérience de rotation automatique optimale, il est recommandé de précharger toutes les images en définissant <span class="codeph"> maxloadradius</span> sur <span class="codeph"> -1</span>. Notez toutefois que ce paramètre augmente le temps de chargement et l’utilisation de la bande passante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> durée</span></span> </p> </td> 
   <td colname="col2"> <p> Nombre de secondes par rotation complète. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> direction </span></span> </p> </td> 
   <td colname="col2"> <p> Direction de rotation qui est <span class="codeph"> 0</span> pour la rotation vers l’est et <span class="codeph"> 1</span> pour la rotation vers l’ouest. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> spin_number</span></span> </p> </td> 
   <td colname="col2"> <p> Nombre de rotations complètes effectuées avant l’arrêt de la rotation automatique. Le nombre est un nombre à virgule flottante. Définissez-le sur <span class="codeph"> -1</span> pour une rotation automatique infinie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-924163cb2f6542499f49894becef7fb5}

Facultatif.

## Par défaut {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## Exemple {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
