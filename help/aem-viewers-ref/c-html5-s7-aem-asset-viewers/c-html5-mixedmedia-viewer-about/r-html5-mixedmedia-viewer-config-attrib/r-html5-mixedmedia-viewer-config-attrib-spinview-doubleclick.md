---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
TQID: 'https://experienceleague.adobe.com/U3RCx6F9hsywdWgtBZukWi6b-Yh5dWzba-2VvxaPMAU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
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
