---
title: op_grewMask
description: Dilater/éroder l’image. Applique une dilatation morphologique (rayon > 0) ou une érosion (rayon < 0) aux données du masque.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 322d97af-bb1b-44bb-90f1-cda9984b78b5
TQID: 'https://experienceleague.adobe.com/-MDsQlyw5ts3RL59hw4-EeF146qdxZqc3fOfzL8BUOA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 2%

---

# op_grewMask{#op-growmask}

Dilater/éroder l’image. Applique une dilatation morphologique (rayon > 0) ou une érosion (rayon &lt; 0) aux données du masque.

`op_growMask= *`radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> rayon </span> </p> </td> 
  <td class="stentry"> <p>Dilate/érode le rayon en pixels où le rayon est supposé s’appliquer au masque de résolution complète et est donc réduit pour les masques sous-échantillonnés (int -100..100). </p></td> 
 </tr> 
</table>

Principalement utilisé pour agrandir ou rétrécir légèrement un masque afin d’éviter les artefacts sur le bord du masque.

## Propriétés {#section-b1c66d65168d4ea695e8662ea690bd4e}

S’applique au calque actif ou au `0` de calque, le cas `layer=comp`.

## Par défaut {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`, pas de changement.

## Voir aussi {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Effets de calque](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grew](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_grewMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)
