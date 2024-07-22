---
title: SpinView.singleclick
description: SpinView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 18c5c21d-af31-4b1c-ab8b-c04d08650123
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_0824E332DF1340A2ABC40A3EB428F2D0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage des actions de zoom d’un simple clic/d’un simple clic. La définition de sur <span class="codeph"> none </span> désactive le zoom par clic/pression. Si vous définissez sur <span class="codeph"> zoom </span>, cliquez sur l’image pour effectuer un zoom avant sur une étape de zoom ; Ctrl+Clic fait un zoom arrière sur une étape de zoom. La définition de la valeur <span class="codeph"> reset </span> entraîne un seul clic sur l’image pour réinitialiser le zoom au niveau de rotation initial. Pour <span class="codeph"> zoomReset </span>, la réinitialisation est appliquée si le facteur de zoom actuel est à ou au-delà de la limite spécifiée, sinon un zoom est appliqué. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` Sur ordinateurs de bureau ; `none` sur appareils tactiles.

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
