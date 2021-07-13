---
description: Largeur de l’image de réponse. Indique la mise à l’échelle de l’image rendue de sorte que l’image de réponse ne soit pas plus grande que la valeur spécifiée, tout en conservant les proportions de l’image.
solution: Experience Manager
title: wid
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: a77b71c3-8600-4d7a-ba52-e158cf9668eb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---

# wid{#wid}

Largeur de l’image de réponse. Indique la mise à l’échelle de l’image rendue de sorte que l’image de réponse ne soit pas plus grande que la valeur spécifiée, tout en conservant les proportions de l’image.

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Largeur de l’image en pixels (int supérieur à 0). </p></td> 
 </tr> 
</table>

L’image n’est pas complétée si `wid=` et `hei=` sont spécifiés et si `wid`/ `hei` est différent du rapport L/H de l’image.

`wid=` et  `hei=` travaillez ensemble pour définir la taille de l’image renvoyée par le serveur. Si `scl=` se trouve après `wid=` ou `hei=` dans l’URL, il annule ces commandes et `scl=` définit la taille de l’image renvoyée par le serveur.

Cependant, si `wid=` ou `hei=` se trouve après `scl=` dans l’URL, ils annulent `scl=` et `wid=`/ `hei=` définissent la taille de l’image renvoyée par le serveur.

>[!NOTE]
>
>Une erreur est renvoyée si la taille de l’image de réponse calculée ou par défaut est supérieure à `attribute::MaxPix`.

## Propriétés {#section-2d067c6d371748e19cb157684700a49d}

Peut se produire n’importe où dans la requête. Le redimensionnement de l’image avec `wid=`, `hei=` ou `scl=` ne modifie pas la valeur de résolution d’impression incorporée dans l’image de réponse. Ignoré si `scl=` se produit après `wid=` ou `hei=` dans la séquence de commandes.

## Par défaut {#section-c7c6efa03d864592a3398b6f1de5a0b0}

Si aucun `wid=`, `hei=` ou `scl=` n’est spécifié, l’image de réponse est mise à l’échelle de façon à s’adapter à la taille définie par `attribute::DefaultPix`. Si `attribute::DefaultPix` est vide, l’image de réponse aura la même taille que l’image d’affichage de la vignette.

## Voir aussi {#section-450dfc12b1d440e2a3172a69d91db51f}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [attribut::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
