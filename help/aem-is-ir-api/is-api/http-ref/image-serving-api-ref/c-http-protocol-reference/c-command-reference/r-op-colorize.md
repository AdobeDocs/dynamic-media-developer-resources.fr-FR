---
title: op_colorize
description: Colorier l’image. Colore les données d’image tout en conservant les tons clairs et foncés.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1abbde32-867a-4596-a46b-12ec50d59170
TQID: 'https://experienceleague.adobe.com/vvDUoUKtzbNV64wfOq3gzJ1KnDb49-kDYUzDwF5A4Q0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 315
ht-degree: 3%

---

# op_colorize{#op-colorize}

Colorier l’image. Colore les données d’image tout en conservant les tons clairs et foncés.

` op_colorize= *`color`*[,off|norm[, *`contraste`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> de couleur <span class="varname"> </p> </td> 
  <td class="stentry"> <p>Couleur RGB de remplacement. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> de </span> </p> </td> 
  <td class="stentry"> <p>Désactivez la compensation automatique de la luminosité. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> de norme <span class="codeph"> </p> </td> 
  <td class="stentry"> <p>Activer la compensation automatique de la luminosité (par défaut). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> de contraste <span class="varname"> </p> </td> 
  <td class="stentry"> <p>Plage de contraste (0..100 réel) ; régler sur 0 pour conserver le contraste d’entrée. </p> </td> 
 </tr> 
</table>

Le deuxième argument spécifie si la luminosité de l’image source doit être ajustée avant la coloration. Spécifiez `off` pour désactiver la compensation automatique de la luminosité ou `norm` pour ajuster automatiquement la luminosité afin que la valeur médiane soit à 50 % d’intensité.

Définissez la valeur du *`contrast`* sur 0 pour conserver la plage de contraste de l’image d’entrée, ou spécifiez une plage de contraste souhaitée avec une valeur supérieure à 0. Une valeur égale à 100 produit le contraste maximum. Les valeurs standard peuvent être comprises entre 30 et 70.

En plus des réglages de luminosité et de contraste intégrés, `op_brightness=` et `op_contrast=` peuvent être utilisés pour affiner davantage l&#39;effet de coloration.

>[!NOTE]
>
>L’algorithme de coloration utilise uniquement les informations de luminance dans les données d’image. Cette conversion en niveaux de gris est simple et n’est pas gérée par les couleurs. `op_colorize` génère toujours des données RGB, même si l’entrée est en niveaux de gris ou en CMJN.

## Propriétés {#section-c0f8bd424b864153a1108f384939f55b}

Commande Calque. S’applique au calque actif ou à l’image composite, le cas `layer=comp`. Ignoré par les calques d’effet.

*`color`* doit être une valeur RGB ; les valeurs *`color`* gris ou CMJN ne sont pas prises en charge.

La valeur *`contrast`* est ignorée si la compensation de luminosité est désactivée.

*`color`* est supposé exister dans l’espace colorimétrique de travail correspondant au type de pixel du *`color`*. *`color`* est converti avec précision si l’image du calque a un type de pixel différent au moment de la fusion.

Les images CMJN sont converties en RGB avant l’application de l’opération .

## Par défaut {#section-0c3ea13efbac432c8970862d223e39b3}

`None`, pour aucune colorisation. Les deuxième et troisième arguments prennent par défaut la valeur `norm,0` pour une compensation automatique de la luminosité et aucune modification du contraste.

## Exemple {#section-4c418d7b5e97409d9a448b8f08a1eab3}

Réglez la luminosité et le contraste de manière dynamique avant de colorer un calque d’image :

... `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`...

Utilisez plutôt le réglage automatique de la luminosité et du contraste :

... `&op_colorize=a0b0c0,norm,50&`...

## Voir aussi {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a), [op_contraste=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), [Gestion des couleurs](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
