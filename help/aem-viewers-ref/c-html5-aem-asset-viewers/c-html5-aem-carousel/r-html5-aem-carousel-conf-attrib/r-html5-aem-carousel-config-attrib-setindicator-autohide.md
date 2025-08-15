---
title: SetIndicator.autohide
description: SetIndicator.autohide
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 75521239-a0be-4aa0-b65d-9a1f7d902cf2
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`limite`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[,<span class="varname"> limite</span>]</span> </p> </td> 
   <td colname="col2"> <p> Configure le comportement de masquage automatique en fonction du nombre de pages et de la taille du composant d’exécution. </p> <p> <span class="codeph"></span> 0 désactive le masquage automatique. </p> <p> <span class="codeph"></span> 1 active le masquage automatique. Le composant masque ses points si au moins une des conditions suivantes s’avère vraie : </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">la rangée avec des points devient plus large que la largeur du composant de l’exécution, ou </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">Le nombre de pages défini pour ce composant dépasse la limite configurée par le <span class="codeph"><span class="varname"> paramètre limite</span></span> . </li> 
     </ul> </p> <p> Si vous définissez la limite<span class="codeph"><span class="varname"> sur </span></span> -1<span class="codeph">, la seconde </span> condition de masquage automatique est désactivée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`1,10`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
