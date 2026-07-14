---
title: resMode
description: Mode de rééchantillonnage. Sélectionne l’algorithme de rééchantillonnage et/ou d’interpolation à utiliser pour mettre à l’échelle l’image rendue à la taille spécifiée par wid=, hei= ou scl=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0926dcfe-881c-4b52-b08d-c56afa0ba04d
TQID: 'https://experienceleague.adobe.com/VLg7JU1aiA7tRGG6vmoHciv-hDIZftbYtU4hAE5N0DY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 172
ht-degree: 6%

---

# resMode{#resmode}

Mode de rééchantillonnage. Sélectionne l’algorithme de rééchantillonnage et/ou d’interpolation à utiliser pour mettre à l’échelle l’image rendue à la taille spécifiée par `wid=`, `hei=` ou `scl=`.

` `resMode=bilin|bicub|sharp2|bisharp«

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bilin </span> </p> </td> 
   <td colname="col2"> <p>Sélectionne l'interpolation bilinéaire standard. Il s’agit de la méthode de ré-échantillonnage la plus rapide ; certains artefacts de crénelage peuvent être visibles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="+ topic/ph pr-d/codeph codeph"> bicub </p> </td> 
   <td colname="col2"> <p>Sélectionne l’interpolation bicubique. Plus gourmande en CPU qu’une interpolation bilinéaire, mais offre des images plus nettes avec des artefacts d’alias moins visibles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>Sélectionne une fonction Lanczos Window modifiée comme algorithme d'interpolation. Peut produire des résultats légèrement plus nets que bicubique à un coût CPU plus élevé. </p> <p> <span class="codeph"> flou </span> a été remplacé par <span class="codeph"> flou2 </span>, qui a moins de chances de causer des artefacts de faux-fuyants, également connus sous le nom de Moiré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp </span> </p> </td> 
   <td colname="col2"> <p>Sélectionne le rééchantillonnage par défaut <span class="keyword"> Adobe Photoshop </span> pour réduire la taille de l’image, appelé « accentuateur bicubique » dans <span class="keyword">’</span> Adobe Photoshop. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-ea7029f37e094d9cb85646b85fbac0ce}

Peut se produire n’importe où dans la requête. Ignoré si aucune mise à l’échelle finale de l’image n’est appliquée.

## Par défaut {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## Voir aussi {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attribute::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)

