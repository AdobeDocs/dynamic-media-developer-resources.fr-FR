---
title: qlt
description: Qualité JPEG. Indique les attributs de codage JPEG pour contrôler le niveau de compression. Cela fait varier la taille du fichier (quantité de données de réponse) et, indirectement, la qualité visuelle de l’image résultante.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a611a8-f331-4e01-a262-34340ce67b21
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 6%

---

# qlt{#qlt}

Qualité JPEG. Indique les attributs de codage JPEG pour contrôler le niveau de compression. Cela fait varier la taille du fichier (quantité de données de réponse) et, indirectement, la qualité visuelle de l’image résultante.

` qlt= *`Chrominance de qualité`*[, *` `*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> qualité </span> </p> </td> 
  <td class="stentry"> <p>Qualité d’encodage JPEG (1... 100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Chroma </span> </p> </td> 
  <td class="stentry"> <p>Sous-échantillonnage de la chromaticité JPEG (0 = normal, 1 = désactivé) ; facultatif, la valeur par défaut est 0. </p> </td> 
 </tr> 
</table>

Des valeurs plus élevées *`quality`* augmentent la taille et la qualité des fichiers, les valeurs inférieures diminuent la taille des fichiers et réduisent la qualité d’image perçue. Des valeurs supérieures à 90 génèrent des images impossibles à différencier d’une image non compressée.

Définissez l’indicateur *`chroma`* pour désactiver le sous-échantillonnage de chromaticité RVB utilisé par les codeurs JPEG classiques. Cela peut augmenter la netteté perçue des bords d’une image lorsque le bord est défini par un changement de teinte plutôt que de luminosité. La définition de cet indicateur peut entraîner une légère augmentation de la taille du fichier. Testez ce paramètre si le texte semble légèrement flou.

## Propriétés {#section-925a44cbdc9042db8d4eb149cd073d21}

Attribut de requête. S’applique quel que soit le paramètre de calque actuel. Ignoré si le format de fichier image de sortie ne prend pas en charge le codage JPEG. Reportez-vous à la description de pour plus d’informations `fmt=` sur les formats d’image de sortie pris en charge `qlt=`.

*`chroma`* est ignoré si le type de pixel de sortie est CMJN ou gris.

## Par défaut {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## Exemple {#section-d7d33871d401433aa51d028823eae7a9}

Réduisez la qualité pour une transmission plus rapide sur une connexion à faible bande passante :

`http://server/myRoodId/myImageId?qlt=60&wid=300`

Améliorez la qualité des connexions à large bande passante :

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## Voir aussi {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribute ::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
