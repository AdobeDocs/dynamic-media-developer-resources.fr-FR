---
description: Mode de rééchantillonnage. Sélectionne l’algorithme de rééchantillonnage et/ou d’interpolation à utiliser pour mettre à l’échelle l’image rendue à la taille spécifiée par wid=, hei= ou scl=.
seo-description: Mode de rééchantillonnage. Sélectionne l’algorithme de rééchantillonnage et/ou d’interpolation à utiliser pour mettre à l’échelle l’image rendue à la taille spécifiée par wid=, hei= ou scl=.
seo-title: resMode
solution: Experience Manager
title: resMode
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 106da74a-d7da-4998-a719-c4c69ae36f6b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 7%

---


# resMode{#resmode}

Mode de rééchantillonnage. Sélectionne l’algorithme de rééchantillonnage et/ou d’interpolation à utiliser pour mettre à l’échelle l’image rendue à la taille spécifiée par wid=, hei= ou scl=.

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> biline  </span> </p> </td> 
   <td colname="col2"> <p>Sélectionne l’interpolation bilinéaire standard. Il s’agit de la méthode de ré-échantillonnage la plus rapide ; certains artefacts de crénelage peuvent être visibles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub  </span> </p> </td> 
   <td colname="col2"> <p>Sélectionne l’interpolation bicubique. Plus intensif en UC que l’interpolation bilinéaire, mais produira des images plus nettes avec des artefacts de crénelage moins visibles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2  </span> </p> </td> 
   <td colname="col2"> <p>Sélectionne une fonction Lanczos Window modifiée comme algorithme d'interpolation. Peut produire des résultats légèrement plus nets que bicubiques à un coût CPU plus élevé. </p> <p> <span class="codeph"> sharp  </span> a été remplacé par  <span class="codeph"> sharp2  </span>, qui a une probabilité moindre de causer des artefacts de crénelage, également appelés Moiré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> évêque  </span> </p> </td> 
   <td colname="col2"> <p>Sélectionne le rééchantillonneur par défaut <span class="keyword"> Adobe Photoshop </span> pour réduire la taille de l’image, appelé "netteté bicubique" dans <span class="keyword"> Adobe Photoshop </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-ea7029f37e094d9cb85646b85fbac0ce}

Peut se produire n’importe où dans la demande. Ignoré si aucune mise à l’échelle finale de l’image n’est appliquée.

## Par défaut {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## Voir aussi {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attribut ::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) ,  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
