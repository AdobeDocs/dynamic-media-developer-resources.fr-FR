---
title: qlt
description: Qualité Jpeg. Indique les attributs de codage JPEG pour contrôler le niveau de compression.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 49af2620-081f-4bcc-8245-5aa6bab89a05
TQID: 'https://experienceleague.adobe.com/T-e5oTA39GatOq7DkXIZPelLxnudZe3O1JYX0bOwlXk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 201
ht-degree: 6%

---

# qlt{#qlt}

Qualité Jpeg. Indique les attributs de codage JPEG pour contrôler le niveau de compression.

` qlt= *`qualité`*[. *`chroma`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> de qualité <span class="varname"> </p> </td> 
  <td class="stentry"> <p>Qualité de codage JPEG (1...100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> chroma </span> </p> </td> 
  <td class="stentry"> <p>Sous-échantillonnage de la résolution chromatique de JPEG (0=normal, 1=désactiver) ; facultatif, la valeur par défaut est 0. </p> </td> 
 </tr> 
</table>

Indique les attributs de codage JPEG pour contrôler le niveau de compression. Cela modifie ensuite la taille du fichier (quantité des données de réponse) et, indirectement, la qualité visuelle de l’image créée.

Des valeurs *`quality`* élevées augmentent la taille et la qualité du fichier, des valeurs faibles réduisent la taille du fichier et réduisent la qualité d’image perçue. Des valeurs supérieures à 90 génèrent des images impossibles à différencier d’une image non compressée.

Définissez l’indicateur *`chroma`* pour désactiver la réduction de résolution chromatique utilisée par les encodeurs JPEG standard. Ce paramètre peut augmenter la netteté perçue des bords d’une image lorsque le bord est défini par une modification de la teinte plutôt que par la luminosité. La définition de cet indicateur peut entraîner une légère augmentation de la taille du fichier. Testez ce paramètre si le texte semble légèrement flou.

## Propriétés {#section-897b61c786dd4230a2c5807f2f40e722}

Peut se produire n’importe où dans la requête.

Ignoré si le format de l’image de sortie ne prend pas en charge la compression JPEG. Reportez-vous à la description de `fmt=` pour obtenir une liste des formats d’image de sortie qui prennent en charge la compression JPEG.

## Par défaut {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## Voir aussi {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attribute::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)

