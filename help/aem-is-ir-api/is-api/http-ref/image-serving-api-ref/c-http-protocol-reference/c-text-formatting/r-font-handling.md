---
description: Toutes les polices référencées dans la chaîne RTF doivent être disponibles dans le fichier de mappage des polices du catalogue par défaut ou du catalogue d’images actuel, faute de quoi une erreur est renvoyée.
solution: Experience Manager
title: Gestion des polices
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---

# Gestion des polices{#font-handling}

Toutes les polices référencées dans la chaîne RTF doivent être disponibles dans le fichier de mappage des polices du catalogue par défaut ou du catalogue d’images actuel, faute de quoi une erreur est renvoyée.

L’enregistrement des fichiers de police correspondants garantit une qualité optimale pour le texte en italique et en gras. S’il n’est pas disponible, le serveur peut synthétiser les polices gras et/ou italique des faces standard. (voir ` [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)`.)

La police spécifiée avec `attribute::DefaultFont` est utilisée lorsqu’aucune police n’est spécifiée explicitement dans la chaîne RTF.

Image Serving prend en charge les polices TrueType, OpenType et Adobe Type 1 (Windows uniquement).

## Prise en charge des polices Photofont® {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` prend en charge les polices Photofont®, avec les restrictions suivantes :

* `\cf` est ignoré dans les zones de texte qui spécifient une police Photofont ; Les polices de caractères de la police photo possèdent des couleurs prédéfinies.
* Les styles de police synthétiqués ne sont pas pris en charge ; l’utilisation de `\b` et `\i`nécessite des entrées de mappage de polices correspondantes, sinon une erreur est renvoyée.

* Le flux de texte vertical n’est pas pris en charge
* Les polices Photofont avec des images 16 bits ne sont pas prises en charge.
* Les polices Photofont avec plusieurs glyphes par image ne sont pas prises en charge.
* La conversion naïve des couleurs est appliquée sauf si les images Photofont glyph incorporent des profils de couleurs ; dans ce cas, l’intention de rendu colorimétrique relative et la compensation du point noir sont toujours appliquées.

Voir ` [www.photofont.com](http://www.photofont.com)` pour plus d’informations.

## Voir aussi {#section-6cb8a802aa044836bbe449d559093f3a}

[Font Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d),  [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15),  [attribute::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107),  [ [!DNL www.photofont.com] ](http://www.photofont.com)
