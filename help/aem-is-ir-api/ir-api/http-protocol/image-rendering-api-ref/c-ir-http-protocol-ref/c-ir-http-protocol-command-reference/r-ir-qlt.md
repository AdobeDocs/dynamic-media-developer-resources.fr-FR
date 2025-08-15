---
title: qlt
description: Qualité Jpeg. Indique les attributs de codage JPEG pour contrôler le niveau de compression.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 49af2620-081f-4bcc-8245-5aa6bab89a05
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 7%

---

# qlt{#qlt}

Qualité Jpeg. Indique les attributs de codage JPEG pour contrôler le niveau de compression.

` qlt= *`Chrominance de qualité`*[. *``*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> qualité </span> </p> </td> 
  <td class="stentry"> <p>Qualité d’encodage JPEG (1... 100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Chroma </span> </p> </td> 
  <td class="stentry"> <p>Sous-échantillonnage de la chromaticité JPEG (0 = normal, 1 = désactivé) ; facultatif, la valeur par défaut est 0. </p> </td> 
 </tr> 
</table>

Indique les attributs de codage JPEG pour contrôler le niveau de compression. À son tour, cela fait varier la taille du fichier (quantité de données de réponse) et, indirectement, la qualité visuelle de l’image résultante.

Des valeurs plus élevées *`quality`* augmentent la taille et la qualité des fichiers, les valeurs inférieures diminuent la taille des fichiers et réduisent la qualité d’image perçue. Des valeurs supérieures à 90 génèrent des images impossibles à différencier d’une image non compressée.

Définissez l’indicateur *`chroma`* pour désactiver le sous-échantillonnage chromatique utilisé par les codeurs JPEG classiques. Ce paramètre peut augmenter la netteté perçue des bords d’une image lorsque le bord est défini par un changement de teinte plutôt que de luminosité. La définition de cet indicateur peut entraîner une légère augmentation de la taille du fichier. Testez ce paramètre si le texte semble légèrement flou.

## Propriétés {#section-897b61c786dd4230a2c5807f2f40e722}

Peut apparaître n’importe où dans la demande.

Ignoré si le format de l’image de sortie ne prend pas en charge la compression JPEG. Reportez-vous à la description de `fmt=` pour obtenir la liste des formats d’image de sortie prenant en charge la compression JPEG.

## Par défaut {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## Voir aussi {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attribute ::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
