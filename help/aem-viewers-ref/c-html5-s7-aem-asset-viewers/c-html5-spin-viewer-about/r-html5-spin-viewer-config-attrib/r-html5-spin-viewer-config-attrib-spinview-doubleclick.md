---
description: 'null'
seo-description: 'null'
seo-title: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
topic: Dynamic media
uuid: c1eef3d1-471e-41ef-b899-008d45b616d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage des -clic/clic sur le pour les actions de rotation. La valeur <span class="codeph"> Aucun </span> désactive la rotation /clic sur le. Si cette option est définie pour <span class="codeph"> effectuer un zoom </span> en cliquant sur l’image qui tourne en une seule étape de rotation ; CTRL+clic permet d’effectuer une rotation. Si vous <span class="codeph"> </span> réinitialisez l’image, un seul clic sur l’image réinitialise la rotation au niveau de rotation initial. Dans le cas de <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de rotation actuel est au-delà de la limite spécifiée, sinon la rotation est appliquée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-924163cb2f6542499f49894becef7fb5}

Facultatif.

## Par défaut {#section-7a2128fd488941948aff18421f533ccf}

`reset` sur les ordinateurs de bureau; `zoomReset` sur les périphériques tactiles.

## Exemple {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
