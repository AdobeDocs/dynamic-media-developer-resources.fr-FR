---
description: Qualité Jpeg. Spécifie les attributs de codage JPEG pour contrôler le niveau de compression.
seo-description: Qualité Jpeg. Spécifie les attributs de codage JPEG pour contrôler le niveau de compression.
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Scene7 Image Serving - Image Rendering API
uuid: 46f5b0da-7fe7-4daf-947b-bb5f5f5f5e6d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# qlt{#qlt}

Qualité Jpeg. Spécifie les attributs de codage JPEG pour contrôler le niveau de compression.

` qlt= *``*[. *`qualitychroma`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> qualité </span> </p> </td> 
  <td class="stentry"> <p>Qualité de codage JPEG (1...100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> chroma </span> </p> </td> 
  <td class="stentry"> <p>Prélèvement chromatique JPEG (0=normal, 1=disable); facultatif, la valeur par défaut est 0. </p> </td> 
 </tr> 
</table>

Spécifie les attributs de codage JPEG pour contrôler le niveau de compression. Cela modifie à son tour la taille du fichier (quantité des données de réponse) et, indirectement, la qualité visuelle de l’image résultante.

Higher *`quality`* values increase file size and quality, lower values decrease file sizes and reduce perceived image quality. Des valeurs supérieures à 90 génèrent des images impossibles à différencier d’une image non compressée.

Définissez l’ *`chroma`* indicateur pour désactiver le sous-échantillonnage chromatique utilisé par les encodeurs JPEG standard. Cela peut augmenter la perception de la netteté des bords dans une image lorsque le bord est défini par un changement de teinte plutôt que de luminosité. La définition de cet indicateur peut entraîner une légère augmentation de la taille du fichier. Essayez ce paramètre si le texte semble légèrement flou.

## Propriétés {#section-897b61c786dd4230a2c5807f2f40e722}

Peut se produire n’importe où dans la requête.

Ignoré si le format d’image de sortie ne prend pas en charge la compression JPEG. Reportez-vous à la description de `fmt=` pour un de formats d’image de sortie prenant en charge la compression JPEG.

## Par défaut {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## Voir aussi {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attribut::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
