---
description: Toutes les polices référencées dans la chaîne RTF doivent être disponibles dans le fichier de mappage des polices du catalogue par défaut ou du catalogue d’images actuel, sinon une erreur est renvoyée.
solution: Experience Manager
title: Gestion des polices
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 1%

---


# Gestion des polices{#font-handling}

Toutes les polices référencées dans la chaîne RTF doivent être disponibles dans le fichier de mappage des polices du catalogue par défaut ou du catalogue d’images actuel, sinon une erreur est renvoyée.

L’enregistrement des fichiers de polices correspondants garantit une qualité optimale pour le texte en italique et en gras. S’il n’est pas disponible, le serveur peut synthétiser les faces de police en gras et/ou en italique à partir de la face standard. (voir ` [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)`.)

La face de police spécifiée avec `attribute::DefaultFont` est utilisée lorsque aucune n&#39;est spécifiée explicitement dans la chaîne RTF.

Image Serving prend en charge les polices TrueType, OpenType, Adobe Type 1 (Windows uniquement).

## Prise en charge des polices Photofont® {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` prend en charge les polices Photofont®, avec les restrictions suivantes :

* `\cf` est ignoré dans les plages de texte qui spécifient une police Photofont ; Les polices de caractères de la police Photofont ont des couleurs prédéfinies
* Les styles de police synthétisés ne sont pas pris en charge ; l&#39;utilisation de `\b` et `\i`nécessite des entrées de mappage de polices correspondantes, sinon une erreur est renvoyée.

* L’enchaînement vertical n’est pas pris en charge
* Les polices Photofont contenant des images 16 bits ne sont pas prises en charge
* Les polices Photofont avec plusieurs glyphes par image ne sont pas prises en charge
* La conversion des couleurs naïves est appliquée à moins que les images de glyphe Photofont incorporent des profils de couleur ; dans ce cas, l’intention de rendu colorimétrique relative et la compensation du point de blocage sont toujours appliquées.

Consultez ` [www.photofont.com](http://www.photofont.com)` pour plus d&#39;informations.

## Voir aussi {#section-6cb8a802aa044836bbe449d559093f3a}

[Référence](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d) de mappage des polices,  [attribut::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15),  [attribut::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107),  [ [!DNL www.photofont.com] ](http://www.photofont.com)
