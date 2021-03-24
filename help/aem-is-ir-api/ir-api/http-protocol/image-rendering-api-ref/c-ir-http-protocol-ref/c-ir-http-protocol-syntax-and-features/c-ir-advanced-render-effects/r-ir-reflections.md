---
description: Il est possible de créer des vignettes pour inclure des données de réflexion presque 3D.
solution: Experience Manager
title: Réflexions
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 3%

---


# Réflexions{#reflections}

Il est possible de créer des vignettes pour inclure des données de réflexion presque 3D.

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
   <td> <p>Lissage de surface </p> </td> 
   <td> <p>De la vignette </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap=  </span> </a> </p> </td> 
   <td> <p>Variation de brillance (image en niveaux de gris) </p> </td> 
   <td> <p>Aucun </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> rugueux=  </span> </a> </p> </td> 
   <td> <p>Rougeur de surface </p> </td> 
   <td> <p>40 % </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span> </a> </p> </td> 
   <td> <p>Type de matériau </p> </td> 
   <td> <p>0 (inconnu) </p> </td> 
  </tr> 
 </tbody> 
</table>

Le rendu ajuste la plage des attributs `gloss=` et `rough=` en fonction de `type=`. Certains types de matériaux tels que le tissu sont généralement moins réfléchissants que les types de matériaux tels que la pierre ou le métal, et la même quantité de brillance spécifiée pour l&#39;un entraîne un effet de reflet différent de l&#39;autre. `gloss=`et la rugosité ont une gamme assez large si  `type=` n’est pas spécifiée ou si elle est définie sur 0.

`glossmap=` peut être utilisé pour contrôler la brillance d&#39;un matériau pixel par pixel.
