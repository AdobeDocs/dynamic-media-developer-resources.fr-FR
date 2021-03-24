---
description: Qualité Jpeg. Spécifie les attributs de codage JPEG pour contrôler le niveau de compression. Cela modifie à son tour la taille du fichier (quantité des données de réponse) et, indirectement, la qualité visuelle de l’image résultante.
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 15%

---


# qlt{#qlt}

Qualité Jpeg. Spécifie les attributs de codage JPEG pour contrôler le niveau de compression. Cela modifie à son tour la taille du fichier (quantité des données de réponse) et, indirectement, la qualité visuelle de l’image résultante.

` qlt= *``*[, *`qualité chroma`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> qualité  </span> </span> </p> </td> 
  <td class="stentry"> <p>Qualité de codage JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> chroma  </span> </span> </p> </td> 
  <td class="stentry"> <p>échantillonnage de chromaticité JPEG (0=normal, 1=disable); facultatif, la valeur par défaut est 0. </p> </td> 
 </tr> 
</table>

Utilisé uniquement si `fmt=jpg`. Ignoré autrement

Des valeurs supérieures de qualité augmentent la taille du fichier et sa qualité, tandis que des valeurs inférieures diminuent les tailles de fichier et réduisent la qualité de l’image perçue. Des valeurs supérieures à 90 génèrent des images impossibles à différencier d’une image non compressée.

Définissez l’indicateur `chroma` pour désactiver le sous-échantillonnage chromatique RVB utilisé par les encodeurs JPEG standard. Cela peut augmenter la netteté perçue des bords dans une image lorsque le bord est défini par un changement de teinte plutôt que de luminosité. La définition de cet indicateur peut entraîner une légère augmentation de la taille du fichier. Testez ce paramètre si le texte semble légèrement flou.

`chroma` est ignorée si le type de pixel de sortie est CMJN ou gris.

## Exemple {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]
