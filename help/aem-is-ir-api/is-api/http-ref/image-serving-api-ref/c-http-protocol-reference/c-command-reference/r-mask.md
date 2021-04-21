---
description: Masque d’image. Indique une image de masque distincte à utiliser comme masque non associé.
solution: Experience Manager
title: masque
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 1%

---


# mask{#mask}

Masque d’image. Indique une image de masque distincte à utiliser comme masque non associé.

`mask= *``*|{[is|ir]'{' *`objectnestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> objet</span> </p></td> 
  <td class="stentry"> <p>Objet image à utiliser comme image ou masque de calque. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>Diffusion d’images imbriquée, rendu d’images ou requête externe. </p></td> 
 </tr> 
</table>

*`object`* peut être une entrée de catalogue ou un fichier image/SVG. Peut être spécifié pour les calques d’image et les calques de couleur unie.

Si *`object`* correspond à une entrée de catalogue d’images, `catalog::MaskPath` est utilisé ou, si `catalog::MaskPath` n’est pas défini, `catalog::Path` est utilisé. Si *`object`* ne correspond pas à une entrée de catalogue, il est interprété comme un chemin d’accès au fichier.

Dans tous les cas, si l’image source possède un canal alpha, elle est utilisée. Sinon, l’image est convertie en niveaux de gris, si nécessaire, avant de l’utiliser comme masque de calque.

Si un masque est attaché à un calque de couleur unie, il peut être recadré et mis à l’échelle à l’aide des mêmes règles que celles utilisées pour les images dans les calques d’image. `size=`,  `scale=`ou  `res=` peut être utilisé pour mettre le masque à l’échelle.

Les masques de couche peuvent également être spécifiés sous la forme d&#39;un *`nestedRequest`*. Les requêtes imbriquées ou incorporées sont entourées d’accolades. Préfixe une requête de diffusion d’images incorporée avec `is` et une requête de rendu d’image incorporée avec `ir`. Une requête envoyée à un serveur étranger est supposée si aucun préfixe n’est spécifié. Pour plus d’informations, voir [Demande d’imbrication et d’incorporation](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b).

## Propriétés {#section-a093043dc249423b8ae322cefb0d545d}

Attribut d’image ou de calque. S’applique au calque 0 si `layer=comp`. Ignoré par les calques d’effet.

*`object`* ne doit pas être résolu en un enregistrement de catalogue qui inclut une  `src=` commande ou une  `mask=` commande dans  `catalog::Modifier`.

Les préfixes `is` et `ir` ne sont pas sensibles à la casse.

## Par défaut {#section-10cf793c665f49deb1b248faa3b618a9}

Si `mask=` n’est pas spécifié explicitement et si l’image du calque est associée à une entrée de catalogue, `catalog::MaskPath` est utilisé. Sinon, le canal alpha de l’image de calque est utilisé, s’il existe. S’il n’y a pas de canal alpha, le calque n’a pas de masque et le rectangle du calque est rendu entièrement opaque.

## Exemple {#section-1bbe623f7c744bdf97b596458d8e7ea3}

Utilisez plusieurs masques distincts pour coloriser différentes zones d’une image. Les zones colorées masquées sont superposées à l’image originale non modifiée :

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## Voir aussi {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) ,  [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),  [objet](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) , Imbrication de  [requêtes et incorporation](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
