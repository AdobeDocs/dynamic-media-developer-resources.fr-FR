---
title: qlt
description: Qualité Jpeg. Indique les attributs de codage JPEG pour contrôler le niveau de compression. Cela modifie ensuite la taille du fichier (quantité des données de réponse) et, indirectement, la qualité visuelle de l’image créée.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
TQID: 'https://experienceleague.adobe.com/sf3ydtf3lGCG1BfJfc1vW5hXFBawbeWJwXNSJdUEei8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 15%

---

# qlt{#qlt}

Qualité Jpeg. Indique les attributs de codage JPEG pour contrôler le niveau de compression. Cela modifie ensuite la taille du fichier (quantité des données de réponse) et, indirectement, la qualité visuelle de l’image créée.

` qlt= *`Qualité`*[, *`chroma`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> qualité </span> </span> </p> </td> 
  <td class="stentry"> <p>Qualité de l’encodage JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> chroma </span> </span> </p> </td> 
  <td class="stentry"> <p>Sous-échantillonnage de la résolution chromatique de JPEG (0=normal, 1=désactiver) ; facultatif, la valeur par défaut est 0. </p> </td> 
 </tr> 
</table>

Utilisé uniquement si `fmt=jpg`. Ignoré dans le cas contraire

Des valeurs supérieures de qualité augmentent la taille du fichier et sa qualité, tandis que des valeurs inférieures diminuent les tailles de fichier et réduisent la qualité de l’image perçue. Des valeurs supérieures à 90 génèrent des images impossibles à différencier d’une image non compressée.

Définissez l’indicateur `chroma` pour désactiver la réduction de la résolution chromatique de RGB utilisée par les encodeurs JPEG standard. Cela peut augmenter la netteté perçue des bords d’une image lorsque le bord est défini par une modification de la teinte plutôt que par la luminosité. La définition de cet indicateur peut entraîner une légère augmentation de la taille du fichier. Testez ce paramètre si le texte semble légèrement flou.

Le `chroma` est ignoré si le type de pixel de sortie est CMJN ou gris.

## Exemple {#section-a6c263f15c29424a86ef267c96a6630a}

`http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80`
