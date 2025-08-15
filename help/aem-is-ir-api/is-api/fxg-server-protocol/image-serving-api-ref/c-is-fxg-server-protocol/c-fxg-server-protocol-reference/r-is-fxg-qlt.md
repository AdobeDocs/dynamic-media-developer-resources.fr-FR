---
title: qlt
description: Qualité Jpeg. Indique les attributs de codage JPEG pour contrôler le niveau de compression. Cela fait varier la taille du fichier (quantité de données de réponse) et, indirectement, la qualité visuelle de l’image résultante.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 15%

---

# qlt{#qlt}

Qualité Jpeg. Indique les attributs de codage JPEG pour contrôler le niveau de compression. Cela fait varier la taille du fichier (quantité de données de réponse) et, indirectement, la qualité visuelle de l’image résultante.

` qlt= *`Chrominance de qualité`*[, *``*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> qualité </span> </span> </p> </td> 
  <td class="stentry"> <p>Qualité d’encodage JPEG (1... 100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> Chroma </span> </span> </p> </td> 
  <td class="stentry"> <p>Sous-échantillonnage de la chromaticité JPEG (0 = normal, 1 = désactivé) ; facultatif, la valeur par défaut est 0. </p> </td> 
 </tr> 
</table>

Utilisé uniquement si `fmt=jpg`. Ignoré autrement

Des valeurs supérieures de qualité augmentent la taille du fichier et sa qualité, tandis que des valeurs inférieures diminuent les tailles de fichier et réduisent la qualité de l’image perçue. Des valeurs supérieures à 90 génèrent des images impossibles à différencier d’une image non compressée.

Définissez l’indicateur `chroma` pour désactiver le sous-échantillonnage de chromaticité RVB utilisé par les codeurs JPEG classiques. Cela peut augmenter la netteté perçue des bords d’une image lorsque le bord est défini par un changement de teinte plutôt que de luminosité. La définition de cet indicateur peut entraîner une légère augmentation de la taille du fichier. Testez ce paramètre si le texte semble légèrement flou.

L’option `chroma` est ignorée si le type de pixel de sortie est CMJN ou gris.

## Exemple {#section-a6c263f15c29424a86ef267c96a6630a}

`http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80`
