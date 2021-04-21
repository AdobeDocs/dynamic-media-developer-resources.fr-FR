---
description: Coloriser l’image. Colorise les données d’image tout en préservant les ombres et les tons clairs.
solution: Experience Manager
title: op_colorize
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 4%

---


# op_colorize{#op-colorize}

Coloriser l’image. Colorise les données d’image tout en préservant les ombres et les tons clairs.

` op_colorize= *``*[,off|norm[, *`contraste de couleur`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> color </span> </p> </td> 
  <td class="stentry"> <p>Couleur RVB de remplacement. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> désactivé </span> </p> </td> 
  <td class="stentry"> <p>Désactivez la compensation automatique de la luminosité. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> norme  </span> </p> </td> 
  <td class="stentry"> <p>Activez la compensation automatique de la luminosité (par défaut). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> contraster </span> </p> </td> 
  <td class="stentry"> <p>Plage de contraste (réel 0,100); défini sur 0 pour conserver le contraste d’entrée. </p> </td> 
 </tr> 
</table>

Le second argument indique si la luminosité de l’image source doit être ajustée avant la coloration. Spécifiez `off` pour désactiver la compensation automatique de la luminosité ou `norm` pour ajuster automatiquement la luminosité de sorte que la valeur médiane soit de 50 % d&#39;intensité.

Définissez la valeur *`contrast`* sur 0 pour conserver la plage de contraste de l’image d’entrée ou spécifiez une plage de contraste avec une valeur supérieure à 0. Une valeur égale à 100 produit le contraste maximum. Les valeurs types peuvent être comprises entre 30 et 70.

Outre les réglages de luminosité et de contraste intégrés, `op_brightness=` et `op_contrast=` peuvent être utilisés pour affiner davantage l&#39;effet de coloration.

>[!NOTE]
>
>L’algorithme de coloration utilise uniquement les informations de luminance dans les données image. Cette conversion en niveaux de gris est simple et non pas gérée par les couleurs. `op_colorize` génère toujours des données RVB, même si l’entrée est en niveaux de gris ou CMJN.

## Propriétés {#section-c0f8bd424b864153a1108f384939f55b}

Calque, commande. S’applique au calque actif ou à l’image composite si `layer=comp`. Ignoré par les calques d’effet.

*`color`* doit être une valeur RVB ; les  *`color`* valeurs grises ou CMJN ne sont pas prises en charge.

La valeur *`contrast`* est ignorée si la compensation de luminosité est désactivée.

*`color`* est supposé exister dans l’espace colorimétrique de travail correspondant au type de pixel de  *`color`*. *`color`* est convertie avec précision si l’image de calque a un type de pixel différent au moment de la fusion.

Les images CMJN sont converties en RVB avant l’application de l’opération.

## Par défaut {#section-0c3ea13efbac432c8970862d223e39b3}

`None`, sans colorisation. Les deuxième et troisième arguments sont définis par défaut sur `norm,0`, pour la compensation automatique de la luminosité et aucun changement de contraste.

## Exemple {#section-4c418d7b5e97409d9a448b8f08a1eab3}

Réglez dynamiquement la luminosité et le contraste avant de coloriser un calque d’image :

... `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`...

Utilisez plutôt la luminosité automatique et l’ajustement du contraste :

... `&op_colorize=a0b0c0,norm,50&`...

## Voir aussi {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a),  [op_contraste=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), Gestion des  [couleurs](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
