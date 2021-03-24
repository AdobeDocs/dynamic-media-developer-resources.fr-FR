---
description: Les matériaux décoratifs comprennent les vêtements, tels que les appliques, les t-shirts imprimés et les logos brodés ou imprimés, ainsi que les objets plats non répétables utilisés dans des applications intérieures ou extérieures, tels que les tapis de surface, les peintures murales, les panneaux, etc.
solution: Experience Manager
title: Décles
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 2%

---


# Decals{#decals}

Les matériaux décoratifs comprennent les vêtements, tels que les appliques, les t-shirts imprimés et les logos brodés ou imprimés, ainsi que les objets plats non répétables utilisés dans des applications intérieures ou extérieures, tels que les tapis de surface, les peintures murales, les panneaux, etc.

Un matériau est considéré comme une poubelle s&#39;il est spécifié dans un MSS décal. Une coquille est généralement une image RGBA, avec le canal alpha qui définit la forme de la coquille.

Une case peut être appliquée à chaque objet plat, à chaque trait de flux, à chaque esquisse, plan ou mur (à moins que l&#39;indicateur &quot;Aucune texture&quot; ne soit défini). Les décalcomanies sont appliquées à l’objet en alignant la valeur `anchor=` de l’indicateur avec le point d’origine de l’objet de la vignette. La position peut être ajustée avec `pos=`.

Une ombre portée est générée si le matériau de la vignette définit une épaisseur et que l’objet de la vignette définit un vecteur de lumière.

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Image (généralement avec alpha); obligatoire. </p> </td> 
   <td colname="col3"> <p>Aucune </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"> <span class="codeph"> size=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Largeur, hauteur et épaisseur de la poutre (pour l’ombre portée). </p> </td> 
   <td colname="col3"> <p> <span class="varname"> ImageWidth  </span> x  <span class="codeph"> res  </span>,  <span class="varname"> imageHeight  </span> x  <span class="codeph"> res, 0  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Résolution de la texture (ignorée si size= est spécifié). </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribut::Résolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Point d’alignement des décimales. </p> </td> 
   <td colname="col3"> <p>Centre d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"> <span class="codeph"> pos=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Position de la décimale relative. </p> </td> 
   <td colname="col3"> <p>0, 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"> <span class="codeph"> opac=  </span> </a> </p> </td> 
   <td colname="col2"> <p>L'opacité du démon. </p> </td> 
   <td colname="col3"> <p>100 % </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </td> 
   <td colname="col2"> <p>Accentuation. </p> </td> 
   <td colname="col3"> <p>0 (aucune accentuation) </p> </td> 
  </tr> 
 </tbody> 
</table>

