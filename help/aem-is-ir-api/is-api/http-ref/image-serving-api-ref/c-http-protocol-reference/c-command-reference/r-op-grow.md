---
description: Dilate/erode image. Applique un dilate morphologique (rayon > 0) ou une érode (rayon < 0) aux données image.
seo-description: Dilate/erode image. Applique un dilate morphologique (rayon > 0) ou une érode (rayon < 0) aux données image.
seo-title: op_grew
solution: Experience Manager
title: op_grew
topic: Dynamic Media Image Serving - Image Rendering API
uuid: bc9bf889-f7e1-4a65-b6d6-7e1257ef8c11
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# op_grew{#op-grow}

Dilate/erode image. Applique un dilate morphologique (rayon > 0) ou une érode (rayon &lt; 0) aux données image.

`op_grow= *`radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radius</span></span> </p> </td> 
  <td class="stentry"> <p>Rayon dilaté/érodé en pixels (int -100..100). </p></td> 
 </tr> 
</table>

`*``*` radium en pixels par rapport à l’image composite. Si l’image est de couleur, chaque composant est traité indépendamment.

Utilisé principalement pour modifier la taille des effets de calque. Également utile pour obtenir des effets spéciaux sur les calques de texte ou les calques de couleur unie avec des masques.

## Propriétés {#section-b1c66d65168d4ea695e8662ea690bd4e}

Attribut de couche. S’applique au calque actif ou à l’image composite si `layer=comp`.

## Par défaut {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`, sans changement.

## Voir aussi {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Effets de calque](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
