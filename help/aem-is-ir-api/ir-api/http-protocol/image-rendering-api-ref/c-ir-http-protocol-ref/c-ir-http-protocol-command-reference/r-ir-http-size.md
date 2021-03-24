---
description: Taille de la poule. Indique la taille d’un matériau de décrochage.
solution: Experience Manager
title: taille
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 3%

---


# taille{#size}

Taille de la poule. Indique la taille d’un matériau de décrochage.

` size= *`largeur,hauteur`*[ *`,épaisseur`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> largeur, hauteur  </span> </p> </td> 
  <td class="stentry"> <p>Taille de l’objet decal en unités de coordonnées de scène (généralement en pouces) (réel, réel). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> épaisseur  </span> </p> </td> 
  <td class="stentry"> <p>Epaisseur de l’objet de la colonne dans les unités de coordonnées de scène (généralement en pouces) (réel). </p> </td> 
 </tr> 
</table>

Si la largeur et la hauteur ne sont pas égales à 0, l’image est mise à l’échelle selon les dimensions spécifiées et les proportions de l’image ne sont pas conservées. La définition de l’une ou l’autre valeur sur 0 préserve les proportions de l’image.

Si *`thickness`* est spécifié, une ombre portée est générée si l’objet de vignette définit un vecteur de lumière approprié. Définissez *`thickness`* sur 0 pour désactiver le rendu des ombres portées.

## Propriétés {#section-818e01e91fed4015951189c818ef28d8}

Attribut de matériau. Uniquement utilisé par les poubelles ; ignoré par tous les autres documents. `res=` est ignorée si la largeur ou la hauteur est supérieure à 0. Les valeurs ne doivent pas être négatives.

## Par défaut {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` si le matériel de la vignette est basé sur une entrée de catalogue ; sinon  `size=0,0,0`. La taille de la valeur décimale est calculée à partir de `res=` si *`wid`* et *`hei`* ne sont pas spécifiés ou sont définis sur 0. Aucune ombre portée n’est générée si *`thickness`* n’est pas spécifié ou défini sur 0.

## Exemple {#section-04fdc2b60b9e4071b672bf6a913738ad}

MSS d’une décimale, dimensionnée en fonction de la résolution, pivotée de 20° dans le sens des aiguilles d’une montre et d’une épaisseur de 2,5 pouces, pour un effet d’ombre portée approprié :

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## Voir aussi {#section-1b116ecd60214732a1757ee1f0cf21c2}

[Coordonnées](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1) de scène,  [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04),  [attribut::Résolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
