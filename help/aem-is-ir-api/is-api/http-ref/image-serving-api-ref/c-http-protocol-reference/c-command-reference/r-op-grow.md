---
title: op_grow
description: Retarder/éroder l’image. Applique un dilat morphologique (rayon > 0) ou une érosion (rayon < 0) to the image data.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4c5bef4e-f80e-454d-8e93-30bf33d7ec9e
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 2%

---

# op_grow{#op-grow}

Retarder/éroder l’image. Applique un dilat morphologique (rayon > 0) ou une érosion (rayon &lt; 0) to the image data.

`op_grow= *`rayon`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> rayon</span></span> </p> </td> 
  <td class="stentry"> <p>Rayon de dilatation/érosion en pixels (int -100..100). </p></td> 
 </tr> 
</table>

`*`rayon`*` est exprimé en pixels par rapport à l’image composite. Si l’image est en couleur, chaque composant est traité indépendamment.

Principalement utilisé pour modifier la taille des effets de calque. Également utile pour obtenir des effets spéciaux sur les calques de texte ou les calques de couleur unie avec masques.

## Propriétés {#section-b1c66d65168d4ea695e8662ea690bd4e}

Attribut de calque. S’applique au calque actif ou à l’image composite si `layer=comp`.

## Par défaut {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`, sans changement.

## Voir aussi {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Effets de calque](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
