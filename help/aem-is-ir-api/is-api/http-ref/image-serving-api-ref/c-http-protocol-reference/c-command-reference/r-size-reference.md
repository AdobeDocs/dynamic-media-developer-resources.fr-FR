---
title: taille
description: Taille de calque. Indique la taille ou la taille maximale du calque, avant l’application des paramètres rotate=, perspective= et extended= au calque.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55feeb32-b69d-4b95-80fb-c77f2612d255
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 1%

---

# taille{#size}

Taille de calque. Indique la taille ou la taille maximale du calque, avant l’application des paramètres rotate=, perspective= et extended= au calque.

` size= *`width`*, *`height`*`

` sizeN= *`widthN`*, *`heightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span>, <span class="varname"> height </span> </span> </p> </td> 
  <td class="stentry"> <p>Contrainte de taille de calque en pixels (int, int, 0 ou plus). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN </span>, <span class="varname"> heightN </span> </span> </p> </td> 
  <td class="stentry"> <p>Contrainte de taille de calque normalisée par rapport à la taille de calque 0 (réel, réel, 0,0...1.0). </p> </td> 
 </tr> 
</table>

Lorsqu’il est spécifié pour un calque d’image, size= limite la largeur, la hauteur ou les deux de l’image de calque. L’image n’est pas plus grande que `size=`. Si une taille normalisée est spécifiée, elle est relative à la taille du calque 0. Si les deux *`width`* et *`height`* sont spécifiées, l’image source est mise à l’échelle (après `crop=` est appliquée) de sorte qu’aucune dimension ne dépasse la taille spécifiée. Les proportions du rectangle source sont conservées dans tous les cas. Soit *`width`* ou *`height`* peut être défini sur 0 ; dans ce cas, la valeur est calculée par le serveur en fonction des proportions de l’image.

Lorsque spécifié pour un calque de texte, `size=` indique la taille de la zone de texte. *`width`* est requis ; *`height`* peut être défini sur 0, auquel cas la hauteur du texte disposé est utilisée comme hauteur du calque. Par défaut, les moteurs de mise en page de texte insèrent des sauts de ligne pour s’assurer que le texte s’insère toujours horizontalement dans l’espace disponible. If *`height`* est spécifié, les lignes qui ne correspondent pas à l’espace disponible sont tronquées ( `text=`) ou omis ( `textPs=`). `text=` prend en charge les modes d’ajustement supplémentaires ; voir `textAttr=` pour plus d’informations.

Lorsqu’elle est spécifiée pour une couche de couleur unie, `size=` définit la taille exacte du calque ; les deux valeurs doivent être spécifiées (sauf si un masque est fourni). If `mask=` est également spécifié, la taille de l’image de masque est adaptée. `size=` de la même manière que les images sont mises à l’échelle dans les calques d’image.

## Propriétés {#section-5f254b66fcba49bcb63f9c9ea40b230c}

Attribut de calque. S’applique au calque 0 si `layer=comp`. `sizeN=` n’est pas autorisé pour `layer=0` ou `layer=comp`. `sizeN=` est autorisé pour `layer=0` et `layer=comp` uniquement dans les enregistrements de catalogue qui définissent les images de filigrane. Dans ce cas, `sizeN` définit la mise à l’échelle de l’image du filigrane par rapport à l’image composite à laquelle le filigrane est appliqué. If `size=` est spécifié, `res=` et `scale=` sont ignorées pour ce calque. Ignoré par les calques d’effet.

## Par défaut {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`, la taille du calque n’est pas contrainte. Pour les calques d’image, la taille du calque est déterminée en fonction de la taille de l’image du calque, après toute `crop=`, `scale=`, ou `res=` ont été appliquées. Pour les calques de texte, si `size=` n’est pas spécifié, le calque est dimensionné automatiquement pour s’adapter au texte rendu.

Les calques de couleur unie nécessitent une spécification complète. `size=`, un `mask=`, ou `clipPath=`.

## Exemple {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

Voir [Exemple A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Voir aussi {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) , [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [Calques de texte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
