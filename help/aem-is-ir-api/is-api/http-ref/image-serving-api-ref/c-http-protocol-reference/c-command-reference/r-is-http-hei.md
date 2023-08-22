---
title: hei
description: Hauteur de l’affichage. Indique la hauteur de l’image de réponse (image d’affichage) lorsque l’ajustement n’est pas présent dans la requête.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c812c7f0-4ac1-42cb-be47-7baebd8caf60
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 2%

---

# hei{#hei}

Hauteur de l’affichage. Indique la hauteur de l’image de réponse (image d’affichage) lorsque l’ajustement n’est pas présent dans la requête.

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Hauteur de l’image en pixels (int supérieur à 0). </p> </td> 
 </tr> 
</table>

Si les deux `wid=` et `scl=` sont spécifiés, l’image composite peut être recadrée selon les `align=`attribut. When `fit=` est présent, `hei=` spécifie la hauteur exacte, minimale ou maximale de l’image de réponse ; voir la description de [fit=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md) pour plus d’informations.

If `scl=` n’est pas spécifié, l’image composite est mise à l’échelle de manière à s’adapter. Si les deux `wid=` et `hei=` sont spécifiés, et `scl=` n’est pas spécifié, l’image est mise à l’échelle de manière à s’adapter entièrement au rectangle large/hauteur, en laissant le moins de zone d’arrière-plan exposée possible ; dans ce cas, l’image est positionnée dans le rectangle de l’affichage en fonction de la variable `align=` attribut. La zone d’arrière-plan est remplie de `bgc=`, ou, si elle n’est pas spécifiée avec `attribute::BkgColor`.

>[!NOTE]
>
>Une erreur est renvoyée si la taille de l’image de réponse calculée est supérieure à `attribute::MaxPix`.

## Propriétés {#section-534923644a1e464496eeba83dedcbd3c}

Attribut d’affichage. S’applique quel que soit le paramètre de calque actif.

## Par défaut {#section-76544d34806d4124a8b173e229cba71f}

Si aucun `wid=`, `hei=`, ou `scl=` sont spécifiées, l’image de réponse a la taille de l’image composite ou `attribute::DefaultPix`, le plus petit.

## Exemples {#section-eb10df7cd67e4733984810aaffd0b9e2}

Demandez une image pour l’adapter à un rectangle de 200 x 200 ; alignez l’image en haut à gauche si elle n’est pas carrée. N’importe quelle zone d’arrière-plan est remplie de `attribute::BkgColor`.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

Même image, diffusée à une hauteur fixe de 200 pixels, mais avec une largeur variable pour correspondre aux proportions de l’image. Dans ce cas, l’image renvoyée ne comporte aucune zone de fond. Notez que dans ce cas `align=` n&#39;aurait aucun effet.

`http://server/myRootId/myImageId?hei=200`

## Voir aussi {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
