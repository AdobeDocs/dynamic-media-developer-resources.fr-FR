---
title: op_grew
description: Dilater/éroder l’image. Applique une dilatation morphologique (rayon > 0) ou une érosion (rayon < 0) aux données d'image.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4c5bef4e-f80e-454d-8e93-30bf33d7ec9e
TQID: 'https://experienceleague.adobe.com/vNFqqzcSqktgB5ohUZjqf0RtQNOD-t7fxITR2gZl-T4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 111
ht-degree: 2%

---

# op_grew{#op-grow}

Dilater/éroder l’image. Applique une dilatation morphologique (rayon > 0) ou une érosion (rayon &lt; 0) aux données d&#39;image.

`op_grow= *`radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> rayon </span></span> </p> </td> 
  <td class="stentry"> <p>Rayon de dilatation/érosion en pixels (int -100..100). </p></td> 
 </tr> 
</table>

Le `*`rayon`*` est exprimé en pixels par rapport à l’image composite. Si l’image est en couleur, chaque composant est traité indépendamment.

Principalement utilisé pour modifier la taille des effets de calque. Également utile pour obtenir des effets spéciaux sur les calques de texte ou les calques de couleur unie avec des masques.

## Propriétés {#section-b1c66d65168d4ea695e8662ea690bd4e}

Attribut de calque. S’applique au calque actif ou à l’image composite, le cas `layer=comp`.

## Par défaut {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`, pas de changement.

## Voir aussi {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Effets de calque](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
