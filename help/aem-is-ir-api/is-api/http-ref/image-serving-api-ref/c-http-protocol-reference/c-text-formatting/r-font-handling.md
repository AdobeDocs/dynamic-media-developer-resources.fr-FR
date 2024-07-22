---
title: Gestion des polices
description: Toutes les polices référencées dans la chaîne RTF doivent être disponibles dans le fichier de mappage des polices du catalogue par défaut ou du catalogue d’images actuel, faute de quoi une erreur est renvoyée.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: e8e3ce9850ab8059aed81e720574d0c93f867a22
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---

# Gestion des polices{#font-handling}

Toutes les polices référencées dans la chaîne RTF doivent être disponibles dans le fichier de mappage des polices du catalogue par défaut ou du catalogue d’images actuel, faute de quoi une erreur est renvoyée.

L’enregistrement des fichiers de police correspondants garantit une qualité optimale pour le texte en italique et en gras. S’il n’est pas disponible, le serveur peut synthétiser les polices gras et/ou italique des faces standard. (Voir [attribute::SynthesizeFontStyles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md).

La police spécifiée avec `attribute::DefaultFont` est utilisée lorsqu’aucune police n’est spécifiée explicitement dans la chaîne RTF.

La diffusion d’images prend en charge les polices TrueType, OpenType® et Adobe Type 1 (Windows uniquement).

<!-- THIS APPEARS TO BE VERY OLD OUTDATED INFORMATION; URL IS DEAD TOO ## Photofont&reg; font support {#section-74560ae898cf4708aba4c8b4093f5f00}

Photofont&reg; fonts support `textPs=`, with the following restrictions:

* `\cf` is ignored in text spans that specify a Photofont font; Photofont font faces have predefined colors 
* Synthesized font styles are not supported; use of `\b` and `\i`require corresponding font map entries, otherwise an error is returned 

* Vertical text flow is not supported 
* Photofont fonts with 16-bit images are not supported 
* Photofont fonts with multiple glyphs per image are not supported 
* Naïve color conversion is applied unless the Photofont glyph images embed color profiles; in this case, relative colorimetric render intent and blackpoint compensation are always applied

See [https://www.photofont.com](https://www.photofont.com) for additional information. -->

## Voir aussi {#section-6cb8a802aa044836bbe449d559093f3a}

[Référence de carte des polices](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d), [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15), [attribute::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107)
