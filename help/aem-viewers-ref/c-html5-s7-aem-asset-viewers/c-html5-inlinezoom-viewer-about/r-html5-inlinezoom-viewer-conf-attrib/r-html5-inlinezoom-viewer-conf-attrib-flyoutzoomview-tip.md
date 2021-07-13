---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
feature: Dynamic Media Classic,Visionneuses,SDK/API,Zoom intégré
role: Developer,User
exl-id: df73235b-547e-4d47-aa76-1d2bd4aead9b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *``*[, *``*][, *`durationcountfade`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durée</span> </span> </p> </td> 
   <td colname="col2"> <p>Indique le nombre de secondes pendant lesquelles le texte de l’info-bulle s’affiche avant qu’il ne se masque. Lorsqu’il est défini sur <span class="codeph"> -1</span>, le message s’affiche toujours, même si l’utilisateur active la fenêtre déroulante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p>Indique le nombre d’affichages du texte lors de l’affichage de nouvelles images dans la visionneuse. Une valeur <span class="codeph"> -1</span> signifie que le texte est toujours affiché lors de l’affichage d’une image de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fade</span> </span> </p> </td> 
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
