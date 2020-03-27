---
description: Qualité JPEG. Spécifie les attributs de codage JPEG pour contrôler le niveau de compression. Cela modifie à son tour la taille du fichier (quantité des données de réponse) et, indirectement, la qualité visuelle de l’image résultante.
seo-description: Qualité JPEG. Spécifie les attributs de codage JPEG pour contrôler le niveau de compression. Cela modifie à son tour la taille du fichier (quantité des données de réponse) et, indirectement, la qualité visuelle de l’image résultante.
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f69845d-3b25-41a7-b6c0-83cf1d2bc450
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# qlt{#qlt}

Qualité JPEG. Spécifie les attributs de codage JPEG pour contrôler le niveau de compression. Cela modifie à son tour la taille du fichier (quantité des données de réponse) et, indirectement, la qualité visuelle de l’image résultante.

` qlt= *``*[, *`qualitychroma`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> qualité </span> </p> </td> 
  <td class="stentry"> <p>Qualité de codage JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> chroma </span> </p> </td> 
  <td class="stentry"> <p>Prélèvement chromatique JPEG (0=normal, 1=disable); facultatif, la valeur par défaut est 0. </p> </td> 
 </tr> 
</table>

Higher *`quality`* values increase file size and quality, lower values decrease file sizes and reduce perceived image quality. Des valeurs supérieures à 90 génèrent des images impossibles à différencier d’une image non compressée.

Définissez l’ *`chroma`* indicateur pour désactiver le sous-échantillonnage chromatique RVB utilisé par les encodeurs JPEG standard. Cela peut augmenter la perception de la netteté des bords dans une image lorsque le bord est défini par un changement de teinte plutôt que de luminosité. La définition de cet indicateur peut entraîner une légère augmentation de la taille du fichier. Essayez ce paramètre si le texte semble légèrement flou.

## Propriétés {#section-925a44cbdc9042db8d4eb149cd073d21}

Attribut de requête. S’applique indépendamment du paramètre de calque actif. Ignoré si le format du fichier image de sortie ne prend pas en charge le codage JPEG. Reportez-vous à la description de `fmt=` pour savoir quels formats d’image de sortie prennent en charge `qlt=`.

*`chroma`* est ignorée si le type de pixel de sortie est CMJN ou gris.

## Par défaut {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## Exemple {#section-d7d33871d401433aa51d028823eae7a9}

Réduisez la qualité pour une transmission plus rapide sur une connexion à faible bande passante :

`http://server/myRoodId/myImageId?qlt=60&wid=300`

Améliorer la qualité des connexions à large bande passante :

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## Voir aussi {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribut::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
