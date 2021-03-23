---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
uuid: c1eef3d1-471e-41ef-b899-008d45b616d0
feature: Dynamic Media Classic, Visionneuses, SDK/API, Visionneuses à 360°
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage des actions de rotation des clics/clics doublons. La définition de <span class="codeph"> none </span> désactive la rotation doublon-clic/clic. Si la valeur est définie sur <span class="codeph"> zoom </span> et que vous cliquez sur la rotation de l’image en une seule étape de rotation ; CTRL+clic permet de filtrer une étape de rotation. Si vous définissez <span class="codeph"> reset </span>, un seul clic sur l’image réinitialise la rotation au niveau de rotation initial. Pour <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de rotation actuel est égal ou supérieur à la limite spécifiée, sinon la réinitialisation est appliquée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-924163cb2f6542499f49894becef7fb5}

Facultatif.

## Par défaut {#section-7a2128fd488941948aff18421f533ccf}

`reset` sur les ordinateurs de bureau ;  `zoomReset` sur les périphériques tactiles.

## Exemple {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
