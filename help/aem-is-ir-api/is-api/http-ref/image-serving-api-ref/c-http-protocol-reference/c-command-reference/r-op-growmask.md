---
description: Dilate/érode l’image. Applique un dilate morphologique (rayon > 0) ou une érode (rayon < 0) aux données du masque.
seo-description: Dilate/érode l’image. Applique un dilate morphologique (rayon > 0) ou une érode (rayon < 0) aux données du masque.
seo-title: op_grewMask
solution: Experience Manager
title: op_grewMask
topic: Scene7 Image Serving - Image Rendering API
uuid: 016501e8-33c5-4c9e-8d26-120b1e929c55
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_grewMask{#op-growmask}

Dilate/érode l’image. Applique un dilate morphologique (rayon > 0) ou une érode (rayon &lt; 0) aux données du masque.

`op_growMask= *`radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radius</span> </p> </td> 
  <td class="stentry"> <p>Dilate/érode le rayon en pixels où le rayon est supposé s’appliquer au masque à résolution entière et est donc réduit pour les masques sous-échantillonnés (int -100..100). </p></td> 
 </tr> 
</table>

Utilisé principalement pour développer ou rétrécir légèrement un masque afin d’éviter les artefacts autour du bord du masque.

## Propriétés {#section-b1c66d65168d4ea695e8662ea690bd4e}

S’applique au calque actif ou au calque `0` si `layer=comp`.

## Par défaut {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`, sans changement.

## Voir aussi {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Effets de calque](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grew](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_grewMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)
