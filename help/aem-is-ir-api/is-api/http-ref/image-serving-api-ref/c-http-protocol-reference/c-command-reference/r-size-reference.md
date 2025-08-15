---
title: taille
description: Taille de calque. Spécifie la taille ou la taille maximale du calque d’un calque avant d’appliquer au calque rotate=, perspective= et extend=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55feeb32-b69d-4b95-80fb-c77f2612d255
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 1%

---

# taille{#size}

Taille de calque. Spécifie la taille ou la taille maximale du calque d’un calque avant d’appliquer au calque rotate=, perspective= et extend=.

` size= *``*, *`width height`*`

` sizeN= *`widthN`*, *`heightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> </span>width , <span class="varname"> height </span> </span> </p> </td> 
  <td class="stentry"> <p>Contrainte de taille de calque en pixels (entier, int, 0 ou plus). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> widthN</span>, <span class="varname"> heightN </span> </span> </p> </td> 
  <td class="stentry"> <p>Contrainte de taille de calque normalisée par rapport à la taille du calque 0 (réel, réel, 0,0... 1.0). </p> </td> 
 </tr> 
</table>

Lorsqu’il est spécifié pour un calque d’image, size= contraint la largeur, la hauteur ou les deux de l’image calque. L’image est mise à l’échelle de manière à ne pas dépasser `size=`la taille . Si une taille normalisée est spécifiée, elle est relative à la taille du calque 0. Si les deux *`width`* et *`height`* sont spécifiés, l’image source est mise à l’échelle (après `crop=` est appliqué) de sorte qu’aucune dimension ne dépasse la taille spécifiée. Le rapport L/H du rectangle source est conservé dans tous les cas. L’une ou l’autre *`width`* *`height`* peut être définie sur 0 ; dans ce cas, la valeur est calculée par le serveur en fonction du rapport L/H de l’image.

Lorsqu’elle est spécifiée pour un calque de texte, `size=` elle indique la taille de la zone de texte. *`width`* est requis ; *`height`* peut être définie sur 0, auquel cas la hauteur du texte mis en page est utilisée comme hauteur de calque. Par défaut, les moteurs de mise en page de texte insèrent des sauts de ligne pour s’assurer que le texte tient toujours horizontalement dans l’espace disponible. Si *`height`* est spécifié, les lignes qui ne rentrent pas dans l’espace disponible sont tronquées ( `text=`) ou omises ( `textPs=`). `text=` prend en charge des modes d’ajustement supplémentaires ; Reportez-vous à `textAttr=` la section pour plus de détails.

Lorsqu’il est spécifié pour un calque de couleur unie, `size=` définit la taille exacte du calque ; les deux valeurs doivent être spécifiées (sauf si un masque est fourni). Si `mask=` est également spécifié, l’image de masque est dimensionnée de la même manière que les images sont mises à l’échelle `size=` dans les calques d’image.

## Propriétés {#section-5f254b66fcba49bcb63f9c9ea40b230c}

Attribut de calque. S’applique au calque 0 si `layer=comp`. `sizeN=` n’est pas autorisé pour `layer=0` ou `layer=comp`. `sizeN=` est autorisée uniquement `layer=0` `layer=comp` dans les notices de catalogue qui définissent des images de filigrane. Dans ce cas, `sizeN` définit la mise à l’échelle de l’image de filigrane par rapport à l’image composite à laquelle le filigrane est appliqué. if `size=` est spécifié `res=` et `scale=` sont ignorés pour ce calque. Ignoré par les calques d’effets.

## Par défaut {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`, la taille du calque n’est pas limitée. Pour les calques d’image, la taille du calque est ensuite déterminée en fonction de la taille de l’image du calque après l’application des opérations `crop=``scale=` ou des `res=`modifications. Pour les calques de texte, si `size=` n’est pas spécifié, le calque est automatiquement dimensionné pour s’adapter au texte rendu.

Les calques de couleur unie nécessitent une propriété entièrement spécifiée `size=`, un ou `mask=`une `clipPath=`.

## Exemple {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

Voir [l’exemple A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) dans [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Voir aussi {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) , [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [Calques de texte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
