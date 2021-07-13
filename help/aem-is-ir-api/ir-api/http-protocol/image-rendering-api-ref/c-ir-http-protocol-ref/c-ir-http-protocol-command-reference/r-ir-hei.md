---
description: Hauteur de l’image de réponse. Indique la mise à l’échelle de l’image rendue de sorte que la hauteur de l’image de réponse ne soit pas supérieure à la valeur spécifiée, tout en conservant les proportions de l’image.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 8e93aa32-b38e-46e4-be52-abd81222cfc3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 2%

---

# hei{#hei}

Hauteur de l’image de réponse. Indique la mise à l’échelle de l’image rendue de sorte que la hauteur de l’image de réponse ne soit pas supérieure à la valeur spécifiée, tout en conservant les proportions de l’image.

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Hauteur de l’image de réponse en pixels (nombre entier supérieur à 0). </p></td> 
 </tr> 
</table>

L’image n’est pas complétée si `wid=` et `hei=` sont spécifiés et si la largeur/hauteur est différente du rapport L/H de l’image.

`wid=` et  `hei=` travaillez ensemble pour définir la taille de l’image renvoyée par le serveur. Si `scl=` se trouve après `wid=` ou `hei=` dans l’URL, il annule ces commandes et `scl=` définit la taille de l’image renvoyée par le serveur.

Cependant, si `wid=` ou `hei=` se trouve après `scl=` dans l’URL, ils annulent `scl=` et `wid=`/ `hei=` définissent la taille de l’image renvoyée par le serveur.

>[!NOTE]
>
>Une erreur est renvoyée si la taille de l’image de réponse calculée ou par défaut est supérieure à `attribute::MaxPix`.

## Propriétés {#section-6cbc6acd37c847beab84c896ac25280c}

Peut se produire n’importe où dans la requête. Le redimensionnement de l’image avec `wid=`, `hei=` ou `scl=` ne modifie pas la valeur de résolution d’impression incorporée dans l’image de réponse. Ignoré si `scl=` se produit après `wid=` et/ou `hei=` dans la séquence de commande.

## Par défaut {#section-61043f6c1f5d450883ff9e5eafd95955}

Si aucun `wid=`, `hei=` ou `scl=` n’est spécifié, l’image de réponse est mise à l’échelle de façon à s’adapter à la taille définie par `attribute::DefaultPix`. Si `attribute::DefaultPix` est vide, l’image de réponse a la même taille que l’image d’affichage de la vignette.

## Voir aussi {#section-7ba51379f1e2421c92d3592d20a37734}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
