---
description: Taille de la poubelle. Indique la taille d’un matériau de décomposition.
seo-description: Taille de la poubelle. Indique la taille d’un matériau de décomposition.
seo-title: taille
solution: Experience Manager
title: taille
topic: Scene7 Image Serving - Image Rendering API
uuid: b82f3429-3d84-4707-8126-d390239df9a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# taille{#size}

Taille de la poubelle. Indique la taille d’un matériau de décomposition.

` size= *`largeur,hauteur`*[ *`,épaisseur`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> largeur, hauteur </span> </p> </td> 
  <td class="stentry"> <p>Taille de l’objet decal en unités de coordonnées de scène (généralement en pouces) (réel, réel). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> épaisseur </span> </p> </td> 
  <td class="stentry"> <p>Epaisseur de l’objet decal dans les unités de coordonnées de scène (généralement pouces) (réel). </p> </td> 
 </tr> 
</table>

Si aucune largeur ni hauteur n’est égale à 0, l’image est mise à l’échelle selon les dimensions spécifiées et les proportions de l’image ne sont pas conservées. La définition de l’une ou l’autre valeur sur 0 préserve les proportions de l’image.

Si *`thickness`* est spécifié, une ombre portée est générée si l’objet de vignette définit un vecteur lumineux approprié. Définissez *`thickness`* sur 0 pour désactiver le rendu de l’ombre portée.

## Propriétés {#section-818e01e91fed4015951189c818ef28d8}

Attribut de matière. Uniquement utilisé par les poubelles; ignoré par tous les autres matériaux. `res=` est ignorée si la largeur ou la hauteur est supérieure à 0. Les valeurs ne doivent pas être négatives.

## Par défaut {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` si le matériau de la poubelle est basé sur une entrée de catalogue; sinon `size=0,0,0`. La taille de la valeur décimale est calculée à partir de `res=` si *`wid`* et *`hei`* ne sont pas spécifiés ou si elle est définie sur 0. Aucune ombre portée n’est générée si elle *`thickness`* n’est pas spécifiée ou définie sur 0.

## Exemple {#section-04fdc2b60b9e4071b672bf6a913738ad}

MSS pour une décimale, dimensionnée en fonction de la résolution, pivotée de 20 degrés dans le sens des aiguilles d’une montre et d’une épaisseur de 2,5 pouces, pour un effet d’ombre portée approprié :

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## Voir aussi {#section-1b116ecd60214732a1757ee1f0cf21c2}

[Coordonnées](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1)de scène, [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04), [attribut::Résolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
