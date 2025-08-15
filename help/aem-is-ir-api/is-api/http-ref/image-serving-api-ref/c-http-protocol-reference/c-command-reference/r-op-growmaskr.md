---
title: op_growMaskR
description: Retarder/éroder l’image. Applique un dilat morphologique (rayon > 0) ou une érosion (rayon < 0) to the mask data.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7abfbccf-8bcf-44d4-b50a-eca7a3f11360
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 3%

---

# op_growMaskR{#op-growmaskr}

Retarder/éroder l’image. Applique un dilat morphologique (rayon > 0) ou une érosion (rayon &lt; 0) to the mask data.

`op_growMaskR= *`Rayon R`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Rayon R</span></span> </p> </td> 
  <td class="stentry"> <p>Diviser/éroder le rayon en pixels où <span class="codeph"><span class="varname"> le rayon R</span></span> est appliqué tel quel, que le masque soit sous-échantillonné ou non (int -100..100). </p></td> 
 </tr> 
</table>

Principalement utilisé pour agrandir ou rétrécir légèrement un masque afin d’éviter les artefacts autour du bord du masque.

## Propriétés {#section-b1c66d65168d4ea695e8662ea690bd4e}

S’applique au calque actif ou au calque `0` si `layer=comp`.

## Par défaut {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`, sans changement.

## Voir aussi {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Effets de calque](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)
