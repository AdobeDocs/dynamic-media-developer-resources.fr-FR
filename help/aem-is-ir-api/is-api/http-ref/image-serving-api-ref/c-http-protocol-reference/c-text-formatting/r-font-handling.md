---
description: Toutes les polices référencées dans la chaîne RTF doivent être disponibles dans le fichier de mappage des polices du catalogue d’images par défaut ou du catalogue d’images actuel, faute de quoi une erreur est renvoyée.
seo-description: Toutes les polices référencées dans la chaîne RTF doivent être disponibles dans le fichier de mappage des polices du catalogue d’images par défaut ou du catalogue d’images actuel, faute de quoi une erreur est renvoyée.
seo-title: Gestion des polices
solution: Experience Manager
title: Gestion des polices
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a751973-5dae-472e-a908-bf24fa59d031
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Gestion des polices{#font-handling}

Toutes les polices référencées dans la chaîne RTF doivent être disponibles dans le fichier de mappage des polices du catalogue d’images par défaut ou du catalogue d’images actuel, faute de quoi une erreur est renvoyée.

La meilleure qualité pour le texte en italique et en gras est obtenue en enregistrant les fichiers de police correspondants. S’il n’est pas disponible, le serveur peut synthétiser les faces de police en gras et/ou en italique de la face standard. (voir ` [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)`.)

La face de police spécifiée par `attribute::DefaultFont` est utilisée lorsqu’aucune police n’est explicitement spécifiée dans la chaîne RTF.

Image Serving prend en charge les polices TrueType, OpenType et Adobe Type 1 (Windows uniquement).

## Prise en charge des polices Photofont® {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` prend en charge les polices Photofont®, avec les restrictions suivantes :

* `\cf` est ignorée dans les plages de texte qui spécifient une police Photofont ; Les polices de caractères des polices Photofont ont des couleurs prédéfinies
* Les styles de police synthétisés ne sont pas pris en charge ; utilisation des entrées de mappage de polices `\b` et `\i`nécessité d’effectuer cette opération ; dans le cas contraire, une erreur est renvoyée

* L’enchaînement de texte vertical n’est pas pris en charge
* Les polices Photofont avec des images 16 bits ne sont pas prises en charge
* Les polices Photofont avec plusieurs glyphes par image ne sont pas prises en charge
* La conversion des couleurs naïves est appliquée sauf si les images de glyphe Photofont incorporent des  de couleur ; dans ce cas, le mode de rendu colorimétrique relatif et la compensation du point noir sont toujours appliqués.

Pour plus ` [www.photofont.com](http://www.photofont.com)` d&#39;informations, reportez-vous à la section.

## Voir aussi {#section-6cb8a802aa044836bbe449d559093f3a}

[Référence](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)de mappage de polices, [attribut::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15), [attribut::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107), [ [!DNL www.photofont.com] ](http://www.photofont.com)
