---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: df73235b-547e-4d47-aa76-1d2bd4aead9b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`duration`*[, *`count`*][, *`fade`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration</span> </span> </p> </td> 
   <td colname="col2"> <p>Indique le nombre de secondes pendant lesquelles le texte de l’info-bulle s’affiche avant qu’il ne se masque. Lorsqu’il est défini sur <span class="codeph"> -1</span>, le message s’affiche toujours, même si l’utilisateur active la fenêtre déroulante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p>Indique le nombre d’affichages du texte lors de l’affichage de nouvelles images dans la visionneuse. Une valeur <span class="codeph"> -1</span> signifie que le texte est toujours affiché lors de l’affichage d’une image dans la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fondu</span> </span> </p> </td> 
   <td colname="col2"> <p>Indique la durée d’une animation de fondu qui se produit lorsque le texte apparaît ou disparaît. Une valeur <span class="codeph"> 0</span> signifie qu’aucune transition de fondu n’est définie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facultatif.

## Par défaut {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,1,0.3`

## Exemple {#section-3a188ab955c445bcb2efa3c49722c10d}

`tip=1,-1,0`
