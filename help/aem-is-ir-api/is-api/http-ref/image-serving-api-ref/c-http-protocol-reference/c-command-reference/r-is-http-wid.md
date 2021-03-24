---
description: Largeur de la vue. Indique la largeur de l’image de réponse (image de vue) lorsque fit= n’est pas présent dans la requête.
solution: Experience Manager
title: wid
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 3%

---


# wid{#wid}

Largeur de la vue. Indique la largeur de l’image de réponse (image de vue) lorsque fit= n’est pas présent dans la requête.

` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Largeur de l’image en pixels (int supérieur à 0). </p> </td> 
 </tr> 
</table>

Si `hei=` et `scl=` sont tous deux spécifiés, l’image composite peut être recadrée selon l’attribut `align=`. Lorsque `fit=` est présent, `wid=` indique la largeur exacte, la largeur minimale ou maximale de l’image de réponse ; pour plus d&#39;informations, reportez-vous à la description de `fit=`.

Si `scl=` n’est pas spécifié, l’image composite est mise à l’échelle pour s’ajuster. Si `wid=` et `hei=` sont spécifiés tous les deux, et `scl=` n&#39;est pas spécifié, l&#39;image est mise à l&#39;échelle pour s&#39;ajuster entièrement au rectangle large/hei, laissant une zone d&#39;arrière-plan aussi petite que possible exposée. Dans ce cas, l’image est positionnée dans le rectangle de la vue selon l’attribut `align=`.

>[!NOTE]
>
>Une erreur est renvoyée si la taille de l&#39;image de réponse calculée ou par défaut est supérieure à `attribute::MaxPix`.

## Par défaut {#section-976d4c8554a34c899f85d172f6ac6f58}

Si aucun élément `wid=`, `hei=` ou `scl=` n&#39;est spécifié, l&#39;image de réponse aura la taille de l&#39;image composite ou `attribute::DefaultPix`, selon la valeur la plus petite.

## Propriétés {#section-c93b7ce1b0d2475f80b06264b45d1285}

Attribut de vue. S’applique quel que soit le paramètre de calque actif.

## Exemple {#section-82bc98b7c15a451bbe9b915d414c0470}

Demander une image pour l&#39;adapter à un rectangle de 200 x 200 ; dans le coin supérieur droit, alignez l’image si elle n’est pas carrée. Toute zone d’arrière-plan est remplie avec `attribute::BkgColor`.

` http:// *`server`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

Même image, diffusée à une largeur fixe de 200 pixels, mais avec une hauteur variable pour conserver les proportions de l’image. Dans ce cas, l’image renvoyée n’a jamais de zone de remplissage d’arrière-plan. Notez que, dans ce cas, align= n’aurait aucun effet.

` http:// *`server`*/myRootId/myImageId?wid=200`

## Voir aussi {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) ,  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), attribute::DefaultPix, attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)[
