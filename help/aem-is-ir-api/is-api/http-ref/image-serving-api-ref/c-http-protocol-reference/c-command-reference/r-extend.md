---
description: Étendre le calque. Ajoute des marges à un calque ou recadre le rectangle du calque.
solution: Experience Manager
title: étend
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 03db6555-6851-49d4-b0de-5570bf56ad76
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---

# étend{#extend}

Étendre le calque. Ajoute des marges à un calque ou recadre le rectangle du calque.

`extend= *``*, *``*, *``*, *`lefttoprightbottom`*`

`extendN= *``*, *``*, *``*, *`leftNtopNrightNbottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> left,top,bottom,right</span></span> </p></td> 
  <td class="stentry"> <p>Nombre de pixels à ajouter (ou à supprimer de, si la valeur est négative) sur les bords gauche, supérieur, droit et inférieur du rect de calque (int, int, int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>Quantité d’espace à ajouter (ou à supprimer de, si la valeur est négative) au bord gauche, supérieur, droit et inférieur de l’arrière de calque, exprimée en quantités normalisées par rapport à la taille de l’arrière de calque d’origine (réel, réel, réel, réel). </p></td> 
 </tr> 
</table>

`extend=` est appliquée au calque  ** après le recadrage de l’image (  `crop=`) et toutes les transformations de calque, y compris  `rotate=`, ont été appliquées.

La zone étendue est remplie avec la valeur `bgColor=` ou, si elle n’est pas spécifiée, reste transparente.

Les valeurs d’argument de `extendN=` sont normalisées par rapport à la taille de la recette de calque après les transformations de calque, y compris `rotate=` ont été appliquées.

## Propriétés {#section-8fc94de871f841f3bf5e1df135972ca9}

Attribut de calque. S’applique au calque 0 si `layer=comp`. Ignoré par les calques d’effet.

## Par défaut {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`, pour aucune modification du rectangle du calque.

## Exemples {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**Recadrez une image, puis ajoutez une bordure rouge de 5 pixels de large :**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**Mettez à l’échelle une image sur une largeur de 200 pixels et ajoutez le texte du titre dans une marge de 30 pixels au-dessus de l’image.**

Notez que la hauteur de l’image composite varie en fonction des proportions de l’image.

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## Voir aussi {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b),  [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138),  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
