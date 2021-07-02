---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,Business Practitioner
exl-id: 03a04bba-85ae-4c30-91fa-dfc6b732a9ac
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 5%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *``*[, *``*][, *`durationcountfade`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> durée</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le nombre de secondes pendant lesquelles le texte de l’info-bulle s’affiche avant qu’il ne se masque. Lorsqu’il est défini sur <span class="codeph"> -1</span>, le message s’affiche toujours, même si l’utilisateur active la fenêtre déroulante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> nombre</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le nombre d’affichages du texte lors de l’affichage de nouvelles images dans la visionneuse. Une valeur <span class="codeph"> -1</span> signifie que le texte est toujours affiché lors de l’affichage d’une image de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> Indique la durée d’une animation de fondu qui se produit lorsque le texte apparaît ou disparaît. Une valeur <span class="codeph"> 0</span> indique qu’aucune transition de fondu n’est effectuée. </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
