---
title: qlt
description: Qualité du JPEG. Indique les attributs de codage JPEG pour contrôler le niveau de compression. Cela modifie ensuite la taille du fichier (quantité des données de réponse) et, indirectement, la qualité visuelle de l’image créée.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a611a8-f331-4e01-a262-34340ce67b21
TQID: 'https://experienceleague.adobe.com/e7zzYHSi7X5tdPAy-0CWTK-Wqs5nfhEDLs2HYJ1D-f4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 242
ht-degree: 6%

---

# qlt{#qlt}

Qualité du JPEG. Indique les attributs de codage JPEG pour contrôler le niveau de compression. Cela modifie ensuite la taille du fichier (quantité des données de réponse) et, indirectement, la qualité visuelle de l’image créée.

` qlt= *`qualité`*[, *`chroma`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> de qualité <span class="varname"> </p> </td> 
  <td class="stentry"> <p>Qualité de l’encodage JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> chroma </span> </p> </td> 
  <td class="stentry"> <p>Sous-échantillonnage de la résolution chromatique de JPEG (0=normal, 1=désactiver) ; facultatif, la valeur par défaut est 0. </p> </td> 
 </tr> 
</table>

Des valeurs *`quality`* élevées augmentent la taille et la qualité du fichier, des valeurs faibles réduisent la taille du fichier et réduisent la qualité d’image perçue. Des valeurs supérieures à 90 génèrent des images impossibles à différencier d’une image non compressée.

Définissez l’indicateur *`chroma`* pour désactiver la réduction de la résolution chromatique de RGB utilisée par les encodeurs JPEG standard. Cela peut augmenter la netteté perçue des bords d’une image lorsque le bord est défini par une modification de la teinte plutôt que par la luminosité. La définition de cet indicateur peut entraîner une légère augmentation de la taille du fichier. Testez ce paramètre si le texte semble légèrement flou.

## Propriétés {#section-925a44cbdc9042db8d4eb149cd073d21}

Attribut de requête. S’applique quel que soit le paramètre de calque actuel. Ignoré si le format du fichier image de sortie ne prend pas en charge le codage JPEG. Reportez-vous à la description de `fmt=` pour savoir quels formats d’image de sortie prennent en charge les `qlt=`.

*`chroma`* est ignoré si le type de pixel de sortie est CMJN ou gris.

## Par défaut {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## Exemple {#section-d7d33871d401433aa51d028823eae7a9}

Réduisez la qualité pour une transmission plus rapide sur une connexion à faible bande passante :

`http://server/myRoodId/myImageId?qlt=60&wid=300`

Amélioration de la qualité des connexions à large bande passante :

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## Voir aussi {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribute::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
