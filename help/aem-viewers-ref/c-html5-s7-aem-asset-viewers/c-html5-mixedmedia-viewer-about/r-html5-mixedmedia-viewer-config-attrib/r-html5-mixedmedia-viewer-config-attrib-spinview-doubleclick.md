---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage des actions de double-clic/appui sur la rotation. La définition sur <span class="codeph"> aucun </span> désactive la rotation par double-clic/appui. Si le paramètre est défini sur <span class="codeph"> </span> de zoom, un clic sur l’image produit une rotation au cours d’une étape ; CTRL+Clic produit une rotation au cours d’une étape. Si vous définissez sur <span class="codeph"> réinitialisation </span>, un seul clic sur l’image réinitialise la rotation au niveau de rotation initial. Pour <span class="codeph"> paramètre zoomReset </span>, la réinitialisation est appliquée si le facteur de rotation actuel est égal ou supérieur à la limite spécifiée, sinon la rotation est appliquée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` Sur les ordinateurs de bureau ; `zoomReset` sur les appareils tactiles.

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
