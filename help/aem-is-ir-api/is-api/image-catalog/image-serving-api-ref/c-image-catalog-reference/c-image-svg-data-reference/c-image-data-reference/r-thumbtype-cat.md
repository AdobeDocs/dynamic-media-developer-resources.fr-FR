---
description: Type de miniature. Décrit comment générer une miniature pour cette image.
solution: Experience Manager
title: ThumbType
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a90b587d-6893-44e4-8dce-7676bc7eebe3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 1%

---

# ThumbType{#thumbtype}

Type de miniature. Décrit comment générer une miniature pour cette image.

Les types de miniatures suivants sont pris en charge :

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Recadrer (1) </p></td> 
  <td class="stentry"> <p>Recadrez l’image selon les proportions de la miniature. À moins que les proportions du rectangle de miniature et de l’image ne soient exactement identiques, une partie de l’image est recadrée pour s’assurer que l’intégralité du rectangle de miniature est remplie de données d’image. Le rectangle de recadrage est positionné dans l’image à l’aide de l’attribut <span class="codeph"> ::ThumbHorizAlign</span> et de l’attribut <span class="codeph"> ::ThumbVertAlign</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Ajuster (2) </p></td> 
  <td class="stentry"> <p>Ajustez l’image entière dans le rectangle de la miniature. L’image est positionnée dans le rectangle de la miniature à l’aide de l’attribut <span class="codeph"> ::ThumbHorizAlign</span> et de l’attribut <span class="codeph"> ::ThumbVertAlign</span>, et tout espace supplémentaire est rempli avec l’attribut <span class="codeph">::ThumbBkgColor</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Texture (3) </p></td> 
  <td class="stentry"> <p>Recadrez l’image en fonction de sa résolution. L’image est mise à l’échelle par rapport au catalogue <span class="codeph"> ::ThumbRes</span> au catalogue <span class="codeph"> ::Resolution</span>. Si l’image obtenue est plus grande que la miniature, elle est recadrée pour s’adapter, si l’image mise à l’échelle est plus petite que la miniature, la zone restante est remplie avec l’attribut <span class="codeph">::ThumbBkgColor</span>. <span class="codeph"> attribute::ThumbHorizAlign</span> et <span class="codeph"> attribute::ThumbVertAlign</span> sont utilisés pour déterminer la position du rectangle de recadrage dans une image plus grande ou la position d’une image plus petite dans la miniature. </p></td> 
 </tr> 
</table>

Les clients demandent des miniatures d’image avec des demandes `req=tmb`.

## Propriétés {#section-c58a8e67c2134ca3a0edd21b20dd3052}

Valeur Enum. Les valeurs valides sont 1, 2 ou 3, ce qui correspond respectivement aux types Recadrage, Ajuster et Texture.

## Par défaut {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` est utilisé si le champ est absent, si la valeur est 0 ou si le champ est vide.

## Voir aussi {#section-fc1a79d3e6274b4381a17da159649a07}

[attribute::ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) , [attribute::ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e), [attribute::ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691), [attribute::ThumbVertAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f), [catalog::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69), [catalog:Resolution: 1}, [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Mise à l’échelle des miniatures](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)
