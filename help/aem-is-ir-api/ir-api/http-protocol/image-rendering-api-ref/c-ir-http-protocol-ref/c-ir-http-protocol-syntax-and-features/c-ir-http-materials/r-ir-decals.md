---
title: Décalcomanies
description: Les matériaux de décalcomanie comprennent les vêtements tels que les appliqués, les imprimés de t-shirts et les logos brodés ou imprimés. Il comprend également des objets plats non répétables utilisés dans des applications intérieures ou extérieures, tels que des tapis, des œuvres murales suspendues et des enseignes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 07190abd-9f6f-46b5-bf77-cd97c48fc9be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 1%

---

# Décalcomanies{#decals}

Les matériaux de décalcomanie comprennent les vêtements tels que les appliqués, les imprimés de t-shirts et les logos brodés ou imprimés. Il comprend également des objets plats non répétables utilisés dans des applications intérieures ou extérieures, tels que des tapis, des œuvres murales suspendues et des enseignes.

Un matériau est considéré comme un autocollant s’il est spécifié dans un autocollant MSS. Un décalcomanie est généralement une image RVBA, le canal alpha définissant la forme de l’autocollant.

Un autocollant peut être appliqué sur chaque objet plat, liaison, esquisse, plan ou mur (sauf si l’indicateur « Aucune texture » est défini). Les décalcomanies sont appliquées à l’objet en alignant les décalcomanies `anchor=` sur le point d’origine de l’objet vignette. La position peut encore être ajustée avec `pos=`.

Une ombre portée est rendue si le matériau de décalcomanie définit une épaisseur et l’objet vignette définit un vecteur lumière.

<table id="table_3F119BC9B7654FD092826A34F5827268"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
   <th colname="col3" class="entry"> <p>Par défaut </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"><span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Image (généralement avec alpha) ; Obligatoire. </p> </td> 
   <td colname="col3"> <p>Aucune </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"><span class="codeph"> taille= </span> </a> </p> </td> 
   <td colname="col2"> <p>Largeur, hauteur et épaisseur de décalcomanie (pour l’ombre portée). </p> </td> 
   <td colname="col3"> <p> <span class="varname"> imageWidth </span> x <span class="codeph"> res </span>, <span class="varname"> imageHeight </span> x <span class="codeph"> res, 0 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"><span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Résolution de texture (ignorée si taille= est spécifié). </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribut ::Résolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"><span class="codeph"> ancre= </span> </a> </p> </td> 
   <td colname="col2"> <p>Point d’alignement de décalcomanie. </p> </td> 
   <td colname="col3"> <p>Centre de l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"><span class="codeph"> pos= </span> </a> </p> </td> 
   <td colname="col2"> <p>Position relative de l’autocollant. </p> </td> 
   <td colname="col3"> <p>0, 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"><span class="codeph"> opac= </span> </a> </p> </td> 
   <td colname="col2"> <p>Opacité de décalcomanie. </p> </td> 
   <td colname="col3"> <p>100% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"><span class="codeph"> sharp= </span> </a> </td> 
   <td colname="col2"> <p>Affilage. </p> </td> 
   <td colname="col3"> <p>0 (pas d’accentuation) </p> </td> 
  </tr> 
 </tbody> 
</table>
