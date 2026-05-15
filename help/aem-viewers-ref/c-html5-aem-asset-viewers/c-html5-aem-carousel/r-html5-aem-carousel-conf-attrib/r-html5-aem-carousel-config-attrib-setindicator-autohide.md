---
title: SetIndicator.autohide
description: SetIndicator.autohide
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 75521239-a0be-4aa0-b65d-9a1f7d902cf2
TQID: 'https://experienceleague.adobe.com/3L6Dr9wnZCV-YCNkZ-kLmF-xZMn-sv1qCo7QeGT-CHU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 89
ht-degree: 3%

---

# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`limit`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[,<span class="varname"> limite</span>]</span> </p> </td> 
   <td colname="col2"> <p> Configure le comportement de masquage automatique en fonction du nombre de pages et de la taille du composant d’exécution. </p> <p> <span class="codeph"> 0</span> désactive le masquage automatique. </p> <p> <span class="codeph"> 1</span> active le masquage automatique. Le composant masque ses points si au moins l’une des conditions suivantes se vérifie : </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">la ligne avec des points devient plus large que la largeur du composant d’exécution, ou </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">le nombre de pages défini pour ce composant dépasse la limite configurée par le paramètre <span class="codeph"><span class="varname"> limit</span></span>. </li> 
     </ul> </p> <p> Définir <span class="codeph"><span class="varname"> limite </span></span> sur <span class="codeph"> -1</span> désactive la deuxième condition de masquage automatique. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`1,10`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
