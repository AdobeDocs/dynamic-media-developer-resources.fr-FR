---
description: Dilate/érode l’image. Applique un dilate morphologique (rayon > 0) ou une érode (rayon < 0) aux données du masque.
solution: Experience Manager
title: op_grewMaskR
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 7abfbccf-8bcf-44d4-b50a-eca7a3f11360
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---

# op_grewMaskR{#op-growmaskr}

Dilate/érode l’image. Applique un dilate morphologique (rayon > 0) ou une érode (rayon &lt; 0) aux données du masque.

`op_growMaskR= *`radiusR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p> </td> 
  <td class="stentry"> <p>Dilate/érode radius en pixels où <span class="codeph"><span class="varname"> radiusR</span></span> est appliqué tel quel, que le masque soit sous-échantillonné ou non (int -100..100). </p></td> 
 </tr> 
</table>

Utilisé principalement pour faire légèrement pousser ou rétrécir un masque afin d’éviter les artefacts autour du bord du masque.

## Propriétés {#section-b1c66d65168d4ea695e8662ea690bd4e}

S’applique au calque actif ou au calque `0` si `layer=comp`.

## Par défaut {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`, pour aucune modification.

## Voir aussi {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Effets de calque](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grew](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_grewMask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)
