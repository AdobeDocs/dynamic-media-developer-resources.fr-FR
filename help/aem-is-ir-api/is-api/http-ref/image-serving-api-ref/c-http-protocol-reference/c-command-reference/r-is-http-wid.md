---
title: éolien
description: Largeur de la vue. Indique la largeur de l’image de réponse (afficher l’image) lorsque fit= n’est pas présent dans la requête.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ba22c79b-da59-4993-aa1c-2c990a0c4be5
TQID: 'https://experienceleague.adobe.com/n6U4pPJuxOo3rX2nU7EYsnevrCPBzoYq5SiQvrr5t20'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 274
ht-degree: 1%

---

# éolien{#wid}

Largeur de la vue. Indique la largeur de l’image de réponse (afficher l’image) lorsque fit= n’est pas présent dans la requête.

`wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Largeur de l’image en pixels (nombre entier supérieur à 0). </p> </td> 
 </tr> 
</table>

Si les paramètres `hei=` et `scl=` sont spécifiés, l’image composite peut être recadrée en fonction de l’attribut `align=`. Lorsqu’`fit=` est présent, `wid=` spécifie la largeur exacte, minimale ou maximale de l’image de réponse. Pour plus d’informations, consultez la description des `fit=` .

Si `scl=` n’est pas spécifié, l’image composite est mise à l’échelle pour s’adapter. Si les options `wid=` et `hei=` sont spécifiées, mais que `scl=` n’est pas spécifié, l’image est mise à l’échelle afin de s’adapter entièrement au rectangle wid/hei, en laissant le moins de zone d’arrière-plan exposée possible. Dans ce cas, l&#39;image est positionnée dans le rectangle de vue en fonction de l&#39;attribut `align=`.

>[!NOTE]
>
>Une erreur est renvoyée si la taille de l’image de réponse calculée ou par défaut est supérieure à `attribute::MaxPix`.

## Par défaut {#section-976d4c8554a34c899f85d172f6ac6f58}

Si ni `wid=`, `hei=` ou `scl=` n’est spécifié, l’image de réponse a la taille de l’image composite ou de la `attribute::DefaultPix`, la plus petite des deux.

## Propriétés {#section-c93b7ce1b0d2475f80b06264b45d1285}

Attribut d’affichage. Il s’applique quel que soit le paramètre de calque actif.

## Exemple {#section-82bc98b7c15a451bbe9b915d414c0470}

Demandez une image afin qu’elle s’adapte à un rectangle de 200 x 200 ; alignez l’image en haut à droite si elle n’est pas carrée. Toute zone d’arrière-plan est remplie de `attribute::BkgColor`.

` http:// *`Serveur`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

La même image, délivrée à une largeur fixe de 200 pixels, mais avec une hauteur variable pour conserver les proportions de l’image. Dans ce cas, l’image renvoyée n’a jamais de zones de remplissage d’arrière-plan. Dans ce cas, `align=` n&#39;aurait aucun effet.

` http:// *`Serveur`*/myRootId/myImageId?wid=200`

## Voir aussi {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
