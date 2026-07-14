---
title: taille
description: Taille de la vignette. Spécifie la taille d'un matériau de vignette.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 756d8b9f-076a-48d6-95c9-e0d6caeed3dd
TQID: 'https://experienceleague.adobe.com/Dlc-HhO8gjpNds-8-cv3vCxILlTePVblpu1D1MP8eN0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 220
ht-degree: 2%

---

# taille{#size}

Taille de la vignette. Spécifie la taille d&#39;un matériau de vignette.

` size= *`largeur,hauteur`*[ *`,épaisseur`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> largeur, hauteur </span> </p> </td> 
  <td class="stentry"> <p>Taille de l'objet de la vignette en unités de coordonnées de la scène (généralement pouces) (réel, réel). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> d'épaisseur <span class="varname"> </p> </td> 
  <td class="stentry"> <p>Épaisseur de l'objet décalque en unités de coordonnées de la scène (généralement pouces) (réelle). </p> </td> 
 </tr> 
</table>

Si ni la largeur ni la hauteur ne sont égales à 0, l’image est mise à l’échelle selon les dimensions exactes spécifiées et les proportions de l’image ne sont pas conservées. La définition de l’une des valeurs sur 0 conserve les proportions de l’image.

Si *`thickness`* est spécifié, une ombre portée est rendue si l’objet vignette définit un vecteur de lumière approprié. Définissez *`thickness`* sur 0 pour désactiver le rendu des ombres portées.

## Propriétés {#section-818e01e91fed4015951189c818ef28d8}

Attribut Material. Uniquement utilisé par les autocollants ; ignoré par tous les autres matériaux. `res=` est ignoré si la largeur ou la hauteur est supérieure à 0. Les valeurs ne doivent pas être négatives.

## Par défaut {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` si la matière de la vignette est basée sur une entrée de catalogue, sinon `size=0,0,0`. La taille de la vignette est calculée à partir de `res=` si *`wid`* et *`hei`* ne sont pas spécifiés ou sont définis sur 0. Aucune ombre portée n’est rendue si *`thickness`* n’est pas spécifié ou défini sur 0.

## Exemple {#section-04fdc2b60b9e4071b672bf6a913738ad}

MSS d’une décalcomanie, dimensionnée en fonction de la résolution, tournée de 20 degrés dans le sens des aiguilles d’une montre et d’une épaisseur de 2,5 pouces, pour un effet d’ombre portée approprié :

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## Voir aussi {#section-1b116ecd60214732a1757ee1f0cf21c2}

[Coordonnées Scene](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1), [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04), [attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)

