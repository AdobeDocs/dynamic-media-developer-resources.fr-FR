---
description: Un matériau est considéré comme une bordure murale lorsqu'il est spécifié dans un MSS de bordure murale (introduit avec sub=3.5).
solution: Experience Manager
title: Bordures de mur
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 4%

---


# Bordures du mur{#wall-borders}

Un matériau est considéré comme une bordure murale lorsqu&#39;il est spécifié dans un MSS de bordure murale (introduit avec sub=3.5).

Les images de texture de la bordure du mur peuvent inclure un canal alpha pour définir la forme de la bordure. Les bordures de mur ne peuvent être appliquées qu’aux objets de mur.

<table id="table_906C5CC4CADF4024AA0E29544AF48080"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
   <th colname="col3" class="entry"> <p>Par défaut </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Image de texture répétable ; requis </p> </td> 
   <td colname="col3"> <p>Aucun </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Résolution de la texture </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribut::Résolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Alignement horizontal de la texture (la valeur y est ignorée) </p> </td> 
   <td colname="col3"> <p>0 (bord gauche de l’image) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Accentuation </p> </td> 
   <td colname="col3"> <p>0 (aucune accentuation) </p> </td> 
  </tr> 
 </tbody> 
</table>

