---
description: SpinView.lockdirection
solution: Experience Manager
title: SpinView.lockdirection
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses à 360°
role: Developer,User
exl-id: e29ba926-9e0e-4ddd-9f76-408f8ab3b4ca
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Indique s’il faut autoriser ou non un changement de direction de rotation dans le cas d’une visionneuse à 360° 2D. </p> <p>Lorsqu’il est défini sur <span class="codeph"> 1 </span>, le composant identifie la Principale direction de glissement ou de glissement (horizontal par rapport à vertical) au début du mouvement. Ensuite, il maintient cette direction jusqu'à ce que le geste se termine. Par exemple, si l’utilisateur commence une rotation horizontale, puis décide de continuer son mouvement de glisser dans une direction verticale, le composant n’effectue pas de rotation verticale ; il ne prend en compte que le mouvement horizontal de la souris ou le glissement. </p> <p>Une valeur <span class="codeph"> 0 </span> permet à l’utilisateur de modifier la direction de rotation à tout moment pendant la progression du mouvement. Le paramètre n’a aucun effet si la visionneuse à 360° est 1D. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
