---
title: op_colorize
description: Coloriez l’image. Colorise les données de l’image tout en préservant les ombres et les surbrillances.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1abbde32-867a-4596-a46b-12ec50d59170
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 4%

---

# op_colorize{#op-colorize}

Coloriez l’image. Colorise les données de l’image tout en préservant les ombres et les surbrillances.

` op_colorize= *`color`*[,off|norm[, *`contraste`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> color </span> </p> </td> 
  <td class="stentry"> <p>Couleur du RGB de remplacement. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> désactivé </span> </p> </td> 
  <td class="stentry"> <p>Désactivez la compensation automatique de la luminosité. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> standard </span> </p> </td> 
  <td class="stentry"> <p>Activez la compensation automatique de la luminosité (par défaut). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> contraster </span> </p> </td> 
  <td class="stentry"> <p>Plage de contraste (réel 0..100) ; définie sur 0 pour préserver le contraste d’entrée. </p> </td> 
 </tr> 
</table>

Le deuxième argument indique si la luminosité de l’image source doit être ajustée avant la coloration. Spécifier `off` pour désactiver la compensation automatique de la luminosité ou `norm` pour régler automatiquement la luminosité afin que la valeur médiane soit d’une intensité de 50 %.

Définissez la variable *`contrast`* sur 0 pour conserver la plage de contraste de l’image d’entrée ou spécifier une plage de contraste avec une valeur supérieure à 0. Une valeur égale à 100 produit le contraste maximum. Les valeurs types peuvent être comprises entre 30 et 70.

Outre les réglages de luminosité et de contraste intégrés, `op_brightness=` et `op_contrast=` peut être utilisé pour affiner davantage l’effet de coloration.

>[!NOTE]
>
>L’algorithme de coloration utilise uniquement les informations de luminance dans les données de l’image. Cette conversion en niveaux de gris est simple et n’est pas gérée par les couleurs. `op_colorize` génère toujours des données de RGB, même si l’entrée est en niveaux de gris ou CMJN.

## Propriétés {#section-c0f8bd424b864153a1108f384939f55b}

Couche, commande. S’applique au calque actif ou à l’image composite si `layer=comp`. Ignoré par les calques d’effet.

*`color`* doit être une valeur RGB ; grise ou CMJN *`color`* ne sont pas prises en charge.

La variable *`contrast`* est ignorée si la compensation de la luminosité est désactivée.

*`color`* est supposé exister dans l’espace colorimétrique de travail correspondant au type de pixel de *`color`*. *`color`* est converti avec précision si l’image de calque a un type de pixel différent au moment de la fusion.

Les images CMJN sont converties en RGB avant l’application de l’opération.

## Par défaut {#section-0c3ea13efbac432c8970862d223e39b3}

`None`, sans colorisation. Les deuxième et troisième arguments sont définis par défaut sur `norm,0`, pour une compensation automatique de la luminosité et aucun changement de contraste.

## Exemple {#section-4c418d7b5e97409d9a448b8f08a1eab3}

Ajustez dynamiquement la luminosité et le contraste avant de colorer un calque d’image :

… `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`…

Utilisez plutôt l’ajustement automatique de la luminosité et du contraste :

… `&op_colorize=a0b0c0,norm,50&`…

## Voir aussi {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a), [op_contraste=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), [Gestion des couleurs](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
