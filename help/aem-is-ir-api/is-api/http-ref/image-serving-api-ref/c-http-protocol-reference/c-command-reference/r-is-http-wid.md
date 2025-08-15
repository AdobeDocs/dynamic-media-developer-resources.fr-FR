---
title: Wid
description: Largeur de la vue. Spécifie la largeur de l’image de réponse (voir l’image) lorsque fit= n’est pas présent dans la demande.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ba22c79b-da59-4993-aa1c-2c990a0c4be5
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 1%

---

# Wid{#wid}

Largeur de la vue. Spécifie la largeur de l’image de réponse (voir l’image) lorsque fit= n’est pas présent dans la demande.

`wid= *`Val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Val </span> </p> </td> 
  <td class="stentry"> <p>Largeur de l’image en pixels (nombre entier supérieur à 0). </p> </td> 
 </tr> 
</table>

Si les deux sont `hei=` `scl=` spécifiés, l’image composite peut être recadrée en fonction de l’attribut `align=` . Lorsque `fit=` est présent, `wid=` spécifie la largeur exacte, minimale ou maximale de l’image de réponse. Reportez-vous à la description de pour plus de `fit=` détails.

Si `scl=` cette valeur n’est pas spécifiée, l’image composite est redimensionnée en conséquence. Si les deux `wid=` et `hei=` sont spécifiés, et `scl=` n’est pas spécifié, l’image est mise à l’échelle pour tenir entièrement dans le rectangle wid/hei, laissant aussi peu de zone d’arrière-plan exposée que possible. Dans ce cas, l’image est positionnée dans le rectangle de vue en fonction de l’attribut `align=` .

>[!NOTE]
>
>Une erreur est renvoyée si la taille de l’image de réponse calculée ou par défaut est supérieure à `attribute::MaxPix`.

## Par défaut {#section-976d4c8554a34c899f85d172f6ac6f58}

Si ni `wid=`, `hei=`ni `scl=` ne sont spécifiés, l’image de réponse a la taille de l’image composite ou `attribute::DefaultPix`, selon la plus petite des deux.

## Propriétés {#section-c93b7ce1b0d2475f80b06264b45d1285}

Attribut View. Il s’applique quel que soit le paramètre de calque actuel.

## Exemple {#section-82bc98b7c15a451bbe9b915d414c0470}

Demandez une image afin qu’elle puisse tenir dans un rectangle 200x200 ; En haut à droite Aligne l’image si elle n’est pas carrée. Toute zone d’arrière-plan est remplie de `attribute::BkgColor`fichiers .

` http:// *`Serveur`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

La même image, livrée à une largeur fixe de 200 pixels, mais avec une hauteur variable pour conserver le format de l’image. Dans ce cas, l’image renvoyée n’a jamais de zone de fond définie. Dans ce cas, `align=` n’aurait aucun effet.

` http:// *`Serveur`*/myRootId/myImageId?wid=200`

## Voir aussi {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [attribute ::D efaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute ::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
