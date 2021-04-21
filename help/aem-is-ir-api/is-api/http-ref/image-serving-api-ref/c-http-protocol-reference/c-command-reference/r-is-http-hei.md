---
description: Hauteur de la vue. Indique la hauteur de l’image de réponse (image de vue) lorsque la taille n’est pas présente dans la requête.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 2%

---


# hei{#hei}

Hauteur de la vue. Indique la hauteur de l’image de réponse (image de vue) lorsque la taille n’est pas présente dans la requête.

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Hauteur de l’image en pixels (int supérieur à 0). </p> </td> 
 </tr> 
</table>

Si `wid=` et `scl=` sont tous deux spécifiés, l’image composite peut être recadrée selon l’attribut `align=`. Lorsque `fit=` est présent, `hei=` indique la hauteur exacte, la hauteur minimale ou maximale de l&#39;image de réponse ; pour plus d&#39;informations, reportez-vous à la description de ` [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)`.

Si `scl=` n’est pas spécifié, l’image composite est mise à l’échelle pour s’ajuster. Si `wid=` et `hei=` sont spécifiés tous les deux, et `scl=` n&#39;est pas spécifié, l&#39;image est mise à l&#39;échelle pour s&#39;ajuster entièrement au rectangle large/hei, laissant une zone d&#39;arrière-plan aussi petite que possible exposée ; dans ce cas, l’image est positionnée dans le rectangle de la vue selon l’attribut `align=`. La zone d&#39;arrière-plan est remplie avec `bgc=` ou, si elle n&#39;est pas spécifiée avec `attribute::BkgColor`.

>[!NOTE]
>
>Une erreur est renvoyée si la taille de l&#39;image de réponse calculée est supérieure à `attribute::MaxPix`.

## Propriétés {#section-534923644a1e464496eeba83dedcbd3c}

Attribut de vue. S’applique quel que soit le paramètre de calque actif.

## Par défaut {#section-76544d34806d4124a8b173e229cba71f}

Si aucun élément `wid=`, `hei=` ou `scl=` n’est spécifié, l’image de réponse a la taille de l’image composite ou `attribute::DefaultPix`, selon la valeur la plus petite.

## Exemples {#section-eb10df7cd67e4733984810aaffd0b9e2}

Demander une image pour l&#39;adapter à un rectangle de 200 x 200 ; dans le coin supérieur gauche, alignez l’image si elle n’est pas carrée. Toute zone d’arrière-plan est remplie avec `attribute::BkgColor`.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

Même image, diffusée à une hauteur fixe de 200 pixels, mais avec une largeur variable correspondant au format de l’image. Dans ce cas, l’image renvoyée n’a jamais de zone de remplissage d’arrière-plan. Notez que, dans ce cas, `align=` n&#39;aurait aucun effet.

`http://server/myRootId/myImageId?hei=200`

## Voir aussi {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), bgc=, rgn=, attribut ::DefaultPix, attribut ::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)[
