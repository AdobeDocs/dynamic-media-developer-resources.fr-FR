---
title: Réflexions
description: Les vignettes peuvent être créées pour inclure des données de réflexion quasi 3D.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f67ede68-03c0-461f-a16d-a308f76fd24c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---

# Réflexions{#reflections}

Les vignettes peuvent être créées pour inclure des données de réflexion quasi 3D.

Si tel est le cas, les attributs de matériau suivants sont utilisés pour définir les propriétés de surface réfléchissante du matériau :

<table id="table_8769C726A17E412FB41F7CB87690B1FE"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Attribut </p> </th> 
   <th class="entry"> <p>Description </p> </th> 
   <th class="entry"> <p>Par défaut </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca" type="reference" format="dita" scope="local"> <span class="codeph"> gloss=</span> </a> </p> </td> 
   <td> <p>Brillance de surface </p> </td> 
   <td> <p>Depuis la vignette </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap= </span> </a> </p> </td> 
   <td> <p>Variation de brillance (image en niveaux de gris) </p> </td> 
   <td> <p>Aucun </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> brut= </span> </a> </p> </td> 
   <td> <p>Rugosité de surface </p> </td> 
   <td> <p>40 % </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span> </a> </p> </td> 
   <td> <p>Type de matériau </p> </td> 
   <td> <p>0 (inconnu) </p> </td> 
  </tr> 
 </tbody> 
</table>

Le moteur de rendu ajuste la plage de l’attribut `gloss=` et `rough=` en fonction des `type=`. Certains types de matériaux, comme le tissu, sont moins réfléchissants que d&#39;autres, comme la pierre ou le métal. De plus, une même quantité de brillance spécifiée pour l&#39;un entraîne souvent un effet de réflexion différent de l&#39;autre. La `gloss=` et la rugosité des attributs ont une gamme assez large si `type=` n’est pas spécifié ou est défini sur `0`.

`glossmap=` Permet de contrôler la brillance d’un matériau pixel par pixel.
