---
description: Largeur de l’affichage. Indique la largeur de l’image de réponse (image d’affichage) lorsque l’attribut fit= n’est pas présent dans la requête.
solution: Experience Manager
title: wid
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: ba22c79b-da59-4993-aa1c-2c990a0c4be5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 3%

---

# wid{#wid}

Largeur de l’affichage. Indique la largeur de l’image de réponse (image d’affichage) lorsque l’attribut fit= n’est pas présent dans la requête.

` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Largeur de l’image en pixels (int supérieur à 0). </p> </td> 
 </tr> 
</table>

Si `hei=` et `scl=` sont spécifiés, l’image composite peut être recadrée selon l’attribut `align=` . `fit=` est présent, `wid=` spécifie la largeur exacte, le minimum ou la largeur maximale de l’image de réponse ; pour plus d’informations, reportez-vous à la description de `fit=` .

Si `scl=` n’est pas spécifié, l’image composite est mise à l’échelle de manière adaptée. Si `wid=` et `hei=` sont spécifiés tous les deux et `scl=` n’est pas spécifié, l’image est mise à l’échelle de manière à s’adapter entièrement au rectangle large/hauteur, laissant une zone d’arrière-plan aussi petite que possible exposée. Dans ce cas, l’image est positionnée dans le rectangle de la vue en fonction de l’attribut `align=` .

>[!NOTE]
>
>Une erreur est renvoyée si la taille de l’image de réponse calculée ou par défaut est supérieure à `attribute::MaxPix`.

## Par défaut {#section-976d4c8554a34c899f85d172f6ac6f58}

Si aucun `wid=`, `hei=` ou `scl=` n’est spécifié, l’image de réponse aura la taille de l’image composite ou `attribute::DefaultPix`, selon la valeur la plus petite.

## Propriétés {#section-c93b7ce1b0d2475f80b06264b45d1285}

Attribut d’affichage. S’applique quel que soit le paramètre de calque actif.

## Exemple {#section-82bc98b7c15a451bbe9b915d414c0470}

Demandez une image pour l’adapter à un rectangle de 200 x 200 ; alignez l’image en haut à droite si elle n’est pas carrée. Toute zone d’arrière-plan est remplie avec `attribute::BkgColor`.

` http:// *`server`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

Même image, diffusée à une largeur fixe de 200 pixels, mais avec une hauteur variable pour conserver les proportions de l’image. Dans ce cas, l’image renvoyée ne comporte aucune zone de fond. Notez que dans ce cas, align= n’aurait aucun effet.

` http:// *`server`*/myRootId/myImageId?wid=200`

## Voir aussi {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) ,  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1),  [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
