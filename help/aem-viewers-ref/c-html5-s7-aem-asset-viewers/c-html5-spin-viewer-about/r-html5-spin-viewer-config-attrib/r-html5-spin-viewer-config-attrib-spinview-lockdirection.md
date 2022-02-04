---
title: SpinView.lockdirection
description: SpinView.lockdirection
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: e29ba926-9e0e-4ddd-9f76-408f8ab3b4ca
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Indique s’il faut autoriser ou non une modification de la direction de rotation en cas de visionneuse à 360° 2D. </p> <p>Lorsque la variable est définie sur <span class="codeph"> 1 </span>, le composant identifie la direction du glissement ou du glissement Principal (horizontal par rapport à vertical) au début du mouvement. Ensuite, il maintient cette direction jusqu'à ce que le geste se termine. Par exemple, si l’utilisateur commence une rotation horizontale, puis décide de continuer son mouvement de glisser dans une direction verticale, le composant n’effectue pas de rotation verticale. Il ne prend en compte que le mouvement horizontal de la souris ou du glissement. </p> <p>Une valeur de <span class="codeph"> 0 </span> permet à l’utilisateur de modifier la direction de rotation à tout moment pendant la progression du mouvement. Le paramètre n’a aucun effet si la visionneuse à 360° est 1D. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
