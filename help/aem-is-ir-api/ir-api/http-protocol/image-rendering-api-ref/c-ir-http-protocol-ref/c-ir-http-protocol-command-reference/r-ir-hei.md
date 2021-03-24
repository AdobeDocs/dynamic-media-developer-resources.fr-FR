---
description: Hauteur de l’image de réponse. Indique la mise à l’échelle de l’image rendue de sorte que la hauteur de l’image de réponse ne dépasse pas la valeur spécifiée, tout en conservant les proportions de l’image.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 2%

---


# hei{#hei}

Hauteur de l’image de réponse. Indique la mise à l’échelle de l’image rendue de sorte que la hauteur de l’image de réponse ne dépasse pas la valeur spécifiée, tout en conservant les proportions de l’image.

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Hauteur de l’image de réponse en pixels (entier supérieur à 0). </p></td> 
 </tr> 
</table>

L’image n’est pas complétée si `wid=` et `hei=` sont tous deux spécifiés et si la largeur/hauteur est différente du format de l’image.

`wid=` et  `hei=` travaillez ensemble pour définir la taille de l’image qui est renvoyée par le serveur. Si `scl=` vient après `wid=` ou `hei=` dans l’URL, il annule ces commandes et `scl=` définit la taille de l’image renvoyée par le serveur.

Cependant, si `wid=` ou `hei=` vient après `scl=` dans l’URL, ils annulent `scl=` et `wid=`/ `hei=` définissent la taille de l’image renvoyée par le serveur.

>[!NOTE]
>
>Une erreur est renvoyée si la taille de l&#39;image de réponse calculée ou par défaut est supérieure à `attribute::MaxPix`.

## Propriétés {#section-6cbc6acd37c847beab84c896ac25280c}

Peut se produire n’importe où dans la demande. Le redimensionnement de l’image avec `wid=`, `hei=` ou `scl=` ne modifie pas la valeur de résolution d’impression incorporée dans l’image de réponse. Ignoré si `scl=` survient après `wid=` et/ou `hei=` dans la séquence de commandes.

## Par défaut {#section-61043f6c1f5d450883ff9e5eafd95955}

Si aucun élément `wid=`, `hei=` ou `scl=` n’est spécifié, l’image de réponse est mise à l’échelle pour s’ajuster à la taille définie par `attribute::DefaultPix`. Si `attribute::DefaultPix` est vide, l’image de réponse a la même taille que l’image de vue de la vignette.

## Voir aussi {#section-7ba51379f1e2421c92d3592d20a37734}

[attribut ::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [attribut ::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)[
