---
description: Type de miniature. Décrit comment générer une miniature pour cette image.
solution: Experience Manager
title: ThumbType
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---


# ThumbType{#thumbtype}

Type de miniature. Décrit comment générer une miniature pour cette image.

Les types de miniatures suivants sont pris en charge :

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Recadrage (1) </p></td> 
  <td class="stentry"> <p>Recadrez l’image selon les proportions de la miniature. A moins que les proportions du rectangle de miniature et de l’image ne soient exactement identiques, une partie de l’image est recadrée pour s’assurer que l’ensemble du rectangle de miniature est rempli de données d’image. Le rectangle de recadrage est positionné dans l'image à l'aide des attributs <span class="codeph">::ThumbHorizAlign</span> et <span class="codeph">::ThumbVertAlign</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Ajuster (2) </p></td> 
  <td class="stentry"> <p>Ajustez l’image entière au rectangle de la miniature. L'image est positionnée dans le rectangle de la miniature à l'aide des attributs <span class="codeph">::ThumbHorizAlign</span> et <span class="codeph">::ThumbVertAlign</span>, et tout espace supplémentaire est rempli avec l'attribut <span class="codeph">::ThumbBkgColor</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Texture (3) </p></td> 
  <td class="stentry"> <p>Recadrez l’image en fonction de la résolution. L'image est mise à l'échelle par rapport à <span class="codeph"> catalog::ThumbRes</span> par <span class="codeph"> catalog::Resolution</span>. Si l’image obtenue est plus grande que la miniature, elle est rognée pour s’ajuster, si l’image mise à l’échelle est plus petite que la miniature, la zone restante est remplie avec l’attribut <span class="codeph">::ThumbBkgColor</span>. <span class="codeph"> attribut::</span> ThumbHorizAlignand  <span class="codeph"> attribut::</span> ThumbVertAlignare permet de déterminer la position du rectangle de recadrage dans une image plus grande ou la position d'une image plus petite dans la miniature. </p></td> 
 </tr> 
</table>

Les clients demandent des miniatures d’image avec des demandes `req=tmb`.

## Propriétés {#section-c58a8e67c2134ca3a0edd21b20dd3052}

Valeur Enum. Les valeurs valides sont 1, 2 ou 3, ce qui correspond aux types Recadrage, Ajuster et Texture, respectivement.

## Par défaut {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` est utilisée si le champ n’est pas présent, si la valeur est 0 ou si le champ est vide.

## Voir aussi {#section-fc1a79d3e6274b4381a17da159649a07}

[attribut ::ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) ,  [attribut ::ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e),  [attribut ::ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691),  [attribut ::ThumbVertAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f), catalogue  ::ThumbRes, cataloguededede : Mise à l’échelle à ongles](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)[](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)[](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)[](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)[
