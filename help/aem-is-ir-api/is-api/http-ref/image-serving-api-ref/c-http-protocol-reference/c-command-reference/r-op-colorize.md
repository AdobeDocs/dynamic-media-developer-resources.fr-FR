---
title: op_colorize
description: Coloriser l’image. Colorise les données d’image tout en préservant les ombres et les hautes lumières.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1abbde32-867a-4596-a46b-12ec50d59170
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 3%

---

# op_colorize{#op-colorize}

Coloriser l’image. Colorise les données d’image tout en préservant les ombres et les hautes lumières.

` op_colorize= *`Contraste des couleurs`*[,off|norm[, *` `*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Couleur </span> </p> </td> 
  <td class="stentry"> <p>Couleur RVB de remplacement. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> de </span> </p> </td> 
  <td class="stentry"> <p>Désactiver la compensation automatique de la luminosité. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> norme </span> </p> </td> 
  <td class="stentry"> <p>Activer la compensation automatique de la luminosité (par défaut). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> contraste </span> </p> </td> 
  <td class="stentry"> <p>Plage de contraste (réel 0..100) ; Définissez ce paramètre sur 0 pour conserver le contraste d’entrée. </p> </td> 
 </tr> 
</table>

Le deuxième argument spécifie si la luminosité de l’image source doit être ajustée avant la colorisation. Spécifiez `off` de désactiver la compensation automatique de luminosité ou `norm` de régler la luminosité automatiquement de sorte que la valeur médiane soit à 50 % d’intensité.

Définissez la *`contrast`* valeur sur 0 pour préserver la plage de contraste de l’image d’entrée ou spécifiez une plage de contraste souhaitée avec une valeur supérieure à 0. Une valeur égale à 100 produit le contraste maximum. Les valeurs habituelles peuvent se situer entre 30 et 70.

En plus des réglages intégrés de la luminosité et du contraste, `op_brightness=` et `op_contrast=` peut être utilisé pour affiner davantage l’effet colorisant.

>[!NOTE]
>
>L’algorithme de colorisation utilise uniquement les informations de luminance contenues dans les données d’image. Cette conversion en niveaux de gris est simple et ne dépend pas de la gestion des couleurs. `op_colorize` génère toujours des données RVB, même si l’entrée est en niveaux de gris ou CMJN.

## Propriétés {#section-c0f8bd424b864153a1108f384939f55b}

Calque, commande S’applique au calque actif ou à l’image composite si `layer=comp`. Ignoré par les calques d’effets.

*`color`* doit être une valeur RVB ; Les valeurs grises ou CMJN *`color`* ne sont pas prises en charge.

La *`contrast`* valeur est ignorée si la compensation de luminosité est désactivée.

*`color`* est supposé exister dans l’espace colorimétrique de travail correspondant au type de pixels de *`color`*. *`color`* est converti avec précision si l’image de calque possède un type de pixel différent au moment de la fusion.

Les images CMJN sont converties en RVB avant l’opération.

## Par défaut {#section-0c3ea13efbac432c8970862d223e39b3}

`None`, pour aucune colorisation. Les deuxième et troisième arguments sont définis par défaut sur , pour une compensation automatique de la luminosité et aucun changement de `norm,0`contraste.

## Exemple {#section-4c418d7b5e97409d9a448b8f08a1eab3}

Réglez dynamiquement la luminosité et le contraste avant de coloriser un calque d’image :

... `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`…

Utilisez à la place le réglage automatique de la luminosité et du contraste :

... `&op_colorize=a0b0c0,norm,50&`…

## Voir aussi {#section-5581eb0e03014fa795e8f078c60e6c8d}

[couleur](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a), [op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), [Gestion des couleurs](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
