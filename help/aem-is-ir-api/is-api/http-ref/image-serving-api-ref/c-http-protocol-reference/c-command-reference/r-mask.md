---
title: masque
description: Masque d’image. Spécifie une image de masque distincte à utiliser comme masque non associé.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5785844b-945b-4dd0-ac59-efbf1360b7cd
TQID: 'https://experienceleague.adobe.com/QV2kCpSVhXdG59s5WjrQ7ENp-F5qkDuHCJeL-nkwuP4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 342
ht-degree: 1%

---

# masque{#mask}

Masque d’image. Spécifie une image de masque distincte à utiliser comme masque non associé.

`mask= *`object`*|{[is|ir]'{' *`nestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> objet </span> </p></td> 
  <td class="stentry"> <p>Objet image à utiliser comme image ou masque de calque. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>Diffusion d’images imbriquées, rendu d’images ou requête externe. </p></td> 
 </tr> 
</table>

*`object`* peut s’agir d’une entrée de catalogue ou d’un fichier image/SVG. Peut être spécifié pour les calques d’image et les calques de couleur unie.

Si *`object`* correspond à une entrée de catalogue d’images, `catalog::MaskPath` est utilisé ou, si `catalog::MaskPath` n’est pas défini, `catalog::Path` est utilisé. Si *`object`* n’est pas résolu sur une entrée de catalogue, il est interprété comme un chemin d’accès au fichier.

Dans tous les cas, si l’image source possède une couche alpha, elle est utilisée. Sinon, l’image est convertie en niveaux de gris, si nécessaire, avant de l’utiliser comme masque de calque.

Si un masque est attaché à un calque de couleur unie, il peut être recadré et mis à l’échelle en utilisant les mêmes règles que celles utilisées pour les images dans les calques d’image. `size=`, `scale=` ou `res=` peuvent être utilisés pour mettre le masque à l’échelle.

Les masques de calque peuvent également être spécifiés sous la forme d’un *`nestedRequest`*. Les requêtes imbriquées ou incorporées sont entourées d’accolades. Préfixez une requête de diffusion d’images incorporée avec `is` et une requête de rendu d’images incorporée avec `ir`. Une requête vers un serveur étranger est supposée si aucun préfixe n’est spécifié. Pour plus d’informations, voir [Demande d’imbrication et d’incorporation](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b).

## Propriétés {#section-a093043dc249423b8ae322cefb0d545d}

Attribut d’image ou de calque. S’applique au calque 0 si `layer=comp`. Ignoré par les calques d’effet.

*`object`* ne devez pas être résolu sur un enregistrement de catalogue qui inclut une commande `src=` ou `mask=` dans `catalog::Modifier`.

Les préfixes `is` et `ir` ne respectent pas la casse.

## Par défaut {#section-10cf793c665f49deb1b248faa3b618a9}

Si `mask=` n’est pas spécifié explicitement et si l’image de calque est associée à une entrée de catalogue, la `catalog::MaskPath` est utilisée. Sinon, la couche alpha de l’image de calque est utilisée, le cas échéant. S’il n’existe pas de couche alpha, le calque n’a pas de masque et le rectangle du calque est entièrement opaque.

## Exemple {#section-1bbe623f7c744bdf97b596458d8e7ea3}

Utilisez plusieurs masques distincts pour colorer différentes zones d’une image. Les zones colorées et masquées sont superposées sur l’image d’origine non modifiée :

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## Voir aussi {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md), [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) , [Request Nested and Embedding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
