---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 122c6406-6fd7-4e45-bff2-11022a3f2cf7
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

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,1,0.3`

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

`tip=1,-1,0`
