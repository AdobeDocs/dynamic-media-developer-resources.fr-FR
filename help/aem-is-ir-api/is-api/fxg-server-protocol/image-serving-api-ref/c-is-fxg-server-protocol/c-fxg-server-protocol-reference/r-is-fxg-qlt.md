---
description: Qualité Jpeg. Spécifie les attributs de codage JPEG pour contrôler le niveau de compression. Cela varie à son tour la taille du fichier (quantité des données de réponse) et, indirectement, la qualité visuelle de l’image obtenue.
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 15%

---

# qlt{#qlt}

Qualité Jpeg. Spécifie les attributs de codage JPEG pour contrôler le niveau de compression. Cela varie à son tour la taille du fichier (quantité des données de réponse) et, indirectement, la qualité visuelle de l’image obtenue.

` qlt= *``*[, *`qualitychroma`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> qualité  </span> </span> </p> </td> 
  <td class="stentry"> <p>Qualité de codage JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> chroma  </span> </span> </p> </td> 
  <td class="stentry"> <p>sous-échantillonnage chromatique JPEG (0=normal, 1=désactivé); facultatif, la valeur par défaut est 0. </p> </td> 
 </tr> 
</table>

Utilisé uniquement si `fmt=jpg`. Ignoré dans le cas contraire

Des valeurs supérieures de qualité augmentent la taille du fichier et sa qualité, tandis que des valeurs inférieures diminuent les tailles de fichier et réduisent la qualité de l’image perçue. Des valeurs supérieures à 90 génèrent des images impossibles à différencier d’une image non compressée.

Définissez l’indicateur `chroma` pour désactiver le sous-échantillonnage chromatique RVB utilisé par les encodeurs JPEG standard. Cela peut augmenter la netteté perçue des bords d’une image lorsque le bord est défini par un changement de couleur plutôt que par la luminosité. La définition de cet indicateur peut entraîner une légère augmentation de la taille du fichier. Testez ce paramètre si le texte semble légèrement flou.

`chroma` est ignoré si le type de pixel de sortie est CMJN ou gris.

## Exemple {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]
