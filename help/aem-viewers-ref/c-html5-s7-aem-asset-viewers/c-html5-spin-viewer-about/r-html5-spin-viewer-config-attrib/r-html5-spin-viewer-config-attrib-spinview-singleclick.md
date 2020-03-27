---
description: 'null'
seo-description: 'null'
seo-title: SpinView.singleclick
solution: Experience Manager
title: SpinView.singleclick
topic: Dynamic media
uuid: b360db52-f705-4966-b77b-009bed729c25
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage des actions de zoom d’un simple clic/clic. La valeur <span class="codeph"> Aucune </span> désactive le zoom par clic/clic. Si cette option est définie pour <span class="codeph"> faire pivoter </span> un clic sur l’image, le zoom est effectué à une étape de zoom ; CTRL+clic permet d’effectuer un zoom arrière sur une étape de zoom. Si vous <span class="codeph"> réinitialisez </span> , un seul clic sur l’image réinitialise le zoom au niveau de rotation initial. Dans le cas de <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de zoom actuel est supérieur ou égal à la limite spécifiée, sinon un zoom est appliqué. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-924163cb2f6542499f49894becef7fb5}

Facultatif.

## Par défaut {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` sur les ordinateurs de bureau; `none` sur les périphériques tactiles.

## Exemple {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
