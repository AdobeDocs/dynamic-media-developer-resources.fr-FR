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

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`Durée`*[, *`: nombre`*][, *`de fondus`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> durée</span> </span> </p> </td> 
   <td colname="col2"> <p>Spécifie le nombre de secondes pendant lesquelles le texte du conseil s’affiche avant d’être masqué. Lorsque la valeur <span class="codeph"> est -1</span>, le message s’affiche toujours, même si l’utilisateur active la fenêtre déroulante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> compter</span> </span> </p> </td> 
   <td colname="col2"> <p>Spécifie le nombre de fois que le texte est affiché lors de l’affichage de nouvelles images dans la visionneuse. La valeur -1<span class="codeph"> signifie que le texte est toujours affiché lors de </span> l’affichage d’une image de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> se faner</span> </span> </p> </td> 
   <td colname="col2"> <p>Spécifie la durée d’une animation de fondu qui se produit lorsque le texte apparaît ou disparaît. Une valeur égale à 0<span class="codeph"> signifie qu’il </span> n’y a pas de transition en fondu. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facultatif.

## Par défaut {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,1,0.3`

## Exemple {#section-3a188ab955c445bcb2efa3c49722c10d}

`tip=1,-1,0`
