---
description: 'null'
seo-description: 'null'
seo-title: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
topic: Dynamic media
uuid: 8e78d91e-e4c6-40f1-9421-8da8bc404ee0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage des -clic/clic sur le pour les actions de rotation. La valeur <span class="codeph"> Aucun </span> désactive la rotation /clic sur le. Si cette option est définie pour <span class="codeph"> effectuer un zoom </span> en cliquant sur l’image qui tourne en une seule étape de rotation ; CTRL+clic permet d’effectuer une rotation. Si vous <span class="codeph"> </span> réinitialisez l’image, un seul clic sur l’image réinitialise la rotation au niveau de rotation initial. Dans le cas de <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de rotation actuel est au-delà de la limite spécifiée, sinon la rotation est appliquée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` sur les ordinateurs de bureau; `zoomReset` sur les périphériques tactiles.

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
