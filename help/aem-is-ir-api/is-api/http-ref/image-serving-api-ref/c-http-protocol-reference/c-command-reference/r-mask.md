---
title: masque
description: Masque d’image. Spécifie une image de masque distincte à utiliser comme masque non associé.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5785844b-945b-4dd0-ac59-efbf1360b7cd
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 1%

---

# masque{#mask}

Masque d’image. Spécifie une image de masque distincte à utiliser comme masque non associé.

`mask= *`objet`*|{[is|ir]'{' *`nestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> objet</span> </p></td> 
  <td class="stentry"> <p>Objet d’image à utiliser comme masque d’image ou de calque. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Demande imbriquée</span> </p></td> 
  <td class="stentry"> <p>Serveur d’images imbriqué, rendu d’image ou requête externe. </p></td> 
 </tr> 
</table>

*`object`* Il peut s’agir d’une entrée de catalogue ou d’un fichier image/SVG. Peut être spécifié pour les calques d’image et les calques de couleur unie.

S’il *`object`* s’agit d’une entrée de catalogue d’images, `catalog::MaskPath` est utilisé ou, si `catalog::MaskPath` n’est pas défini, est `catalog::Path` utilisé. Si *`object`* elle ne se résout pas sur une entrée de catalogue, elle est interprétée comme un chemin de fichier.

Dans tous les cas, si l’image source possède un canal alpha, il est utilisé. Sinon, l’image est convertie en niveaux de gris, si nécessaire, avant de l’utiliser comme masque de calque.

Si un masque est attaché à un calque de couleur unie, il peut être recadré et mis à l’échelle à l’aide des mêmes règles que celles utilisées pour les images dans les calques d’image. `size=`, ou `scale=` `res=` peut être utilisé pour mettre le masque à l’échelle.

Les masques de calque peuvent également être spécifiés sous la forme d’un *`nestedRequest`* fichier . Les requêtes imbriquées ou incorporées sont entourées par des accolades. Préfixe une demande de diffusion d’images incorporée avec `is` et une demande de rendu d’image incorporée avec `ir`. Une demande à un serveur étranger est supposée si aucun préfixe n’est spécifié. Pour plus d’informations, reportez-vous à [la section Demande d’imbrication et d’intégration](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) .

## Propriétés {#section-a093043dc249423b8ae322cefb0d545d}

Attribut d’image ou de calque. S’applique au calque 0 si `layer=comp`. Ignoré par les calques d’effets.

*`object`* ne doit pas être résolue en un enregistrement de catalogue contenant une `src=` commande OR `mask=` dans `catalog::Modifier`.

Les préfixes et `is` `ir` ne sont pas sensibles à la casse.

## Par défaut {#section-10cf793c665f49deb1b248faa3b618a9}

Si `mask=` n’est pas spécifié explicitement et si l’image de calque est associée à une entrée de catalogue, est `catalog::MaskPath` utilisée. Sinon, le canal alpha de l’image de calque est utilisé, le cas échéant. S’il n’y a pas de couche alpha, le calque n’a pas de masque et le rectangle de calque est rendu entièrement opaque.

## Exemple {#section-1bbe623f7c744bdf97b596458d8e7ea3}

Utilisez plusieurs masques distincts pour coloriser différentes zones d’une image. Les zones colorisées et masquées sont superposées à l’image originale non modifiée :

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## Voir aussi {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) , [catalog ::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md), [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) , [Demande d’imbrication et d’incorporation](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
