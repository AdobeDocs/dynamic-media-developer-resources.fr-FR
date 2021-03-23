---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
uuid: 8e78d91e-e4c6-40f1-9421-8da8bc404ee0
feature: Dynamic Media Classic, Visionneuses, SDK/API, Combiner des visionneuses de supports
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage des actions de rotation des clics/clics doublons. La définition de <span class="codeph"> none </span> désactive la rotation doublon-clic/clic. Si la valeur est définie sur <span class="codeph"> zoom </span> et que vous cliquez sur la rotation de l’image en une seule étape de rotation ; CTRL+clic permet de filtrer une étape de rotation. Si vous définissez <span class="codeph"> reset </span>, un seul clic sur l’image réinitialise la rotation au niveau de rotation initial. Pour <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de rotation actuel est égal ou supérieur à la limite spécifiée, sinon la réinitialisation est appliquée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` sur les ordinateurs de bureau ;  `zoomReset` sur les périphériques tactiles.

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
