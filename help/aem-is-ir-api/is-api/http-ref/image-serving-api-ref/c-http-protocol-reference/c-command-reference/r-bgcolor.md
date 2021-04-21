---
description: Couleur d’arrière-plan du calque. Indique la couleur d’arrière-plan et l’opacité du calque actif.
solution: Experience Manager
title: bgColor
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 4%

---


# bgColor{#bgcolor}

Couleur d’arrière-plan du calque. Indique la couleur d’arrière-plan et l’opacité du calque actif.

`bgColor= *`color`*`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> color</span></span> </p> </td> 
  <td class="stentry"> <p>Gris, RVB ou CMJN, avec ou sans alpha. </p></td> 
 </tr> 
</table>

Les zones transparentes et semi-opaques du rectangle de délimitation du calque sont remplies avec la couleur spécifiée* après* `opac=`, `rotate=` et `extend=` sont appliquées.

## Propriétés {#section-19dfc13e997f4a33889a1df1e4ad50b9}

Attribut de couche. S&#39;applique au calque actif ou au calque 0 si `layer=comp`. Ignoré par les calques d’effet.

*`color`* est supposé exister dans l’espace colorimétrique de travail correspondant au type de pixel de  *`color`*. *`color`* est convertie avec précision si l’image du calque final a un type de pixel différent.

## Par défaut {#section-30cd43f922c04ed9b75875ff7f20c88f}

0,0,0,0 (entièrement transparent).

## Exemple {#section-6e14fcf1d31e432dbdb56b9320904453}

Voir [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423).

## Voir aussi {#section-64b3f153c6d94ab58f46e77324697818}

[couleur](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93),  [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423),  [blendMode=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172),  [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5), extended=, rotate=, bgc=, Gestion des couleurs de l’](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)[
