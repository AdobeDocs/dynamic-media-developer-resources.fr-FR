---
description: Qualité Jpeg. Spécifie les attributs de codage JPEG pour contrôler le niveau de compression.
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 7%

---


# qlt{#qlt}

Qualité Jpeg. Spécifie les attributs de codage JPEG pour contrôler le niveau de compression.

` qlt= *``*[. *`qualité chroma`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> qualité </span> </p> </td> 
  <td class="stentry"> <p>Qualité de codage JPEG (1...100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> chroma  </span> </p> </td> 
  <td class="stentry"> <p>échantillonnage de chromaticité JPEG (0=normal, 1=disable); facultatif, la valeur par défaut est 0. </p> </td> 
 </tr> 
</table>

Spécifie les attributs de codage JPEG pour contrôler le niveau de compression. Cela modifie à son tour la taille du fichier (quantité des données de réponse) et, indirectement, la qualité visuelle de l’image résultante.

Des valeurs *`quality`* supérieures augmentent la taille et la qualité du fichier, des valeurs inférieures diminuent la taille des fichiers et réduisent la qualité d’image perçue. Des valeurs supérieures à 90 génèrent des images impossibles à différencier d’une image non compressée.

Définissez l’indicateur *`chroma`* pour désactiver le sous-échantillonnage chromatique utilisé par les encodeurs JPEG standard. Cela peut augmenter la netteté perçue des bords dans une image lorsque le bord est défini par un changement de teinte plutôt que de luminosité. La définition de cet indicateur peut entraîner une légère augmentation de la taille du fichier. Testez ce paramètre si le texte semble légèrement flou.

## Propriétés {#section-897b61c786dd4230a2c5807f2f40e722}

Peut se produire n’importe où dans la demande.

Ignoré si le format d’image de sortie ne prend pas en charge la compression JPEG. Reportez-vous à la description de `fmt=` pour obtenir une liste des formats d’image de sortie qui prennent en charge la compression JPEG.

## Par défaut {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## Voir aussi {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [attribut::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
