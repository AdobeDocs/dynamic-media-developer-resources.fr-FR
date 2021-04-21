---
description: Région d’intérêt. Indique une zone d’intérêt rectangulaire (RSI) dans l’image composite, exprimée en pixels.
solution: Experience Manager
title: rg
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 3%

---


# rgn{#rgn}

Région d’intérêt. Indique une zone d’intérêt rectangulaire (RSI) dans l’image composite, exprimée en pixels.

rgn= *`coord`*, *`size`*

<table id="simpletable_3A430F9078B04C2E90F4D1A130AFA20C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Décalage des pixels du coin supérieur gauche de l’image composite vers le coin supérieur gauche du RSI (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> taille</span> </p></td> 
  <td class="stentry"> <p>Taille du RSI en pixels (int, int). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>`rgn=` définit uniquement un RSI sans recadrer l’image. Lorsque des dimensions `wid=` et/ou `hei=` supérieures à la taille sont également appliquées, des données supplémentaires de l&#39;image composite peuvent être visibles dans l&#39;image de réponse finale.

## Propriétés {#section-53edb35f4e364d7ca13fd0886e8b0c86}

Attribut de vue. S’applique quel que soit le paramètre de calque actif.

Toutes les zones du RSI s’étendant en dehors de l’image composite sont complétées par `bgc=`.

`rgn=` est appliquée avant la mise à l’échelle finale et l’ajustement avec  `scl=`,  `wid=`,  `hei=`,  `fit=`,  `rect=` ou  `align=`.

## Par défaut {#section-6a3df8f670084def900ffef9dab7e94a}

Image composite complète ( `rgn=0,0,width,height`).

## Voir aussi {#section-07883760f25c4d17aedbee36b7883891}

[recadrage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), hei= [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), scl=, align=, =fit, rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)[
