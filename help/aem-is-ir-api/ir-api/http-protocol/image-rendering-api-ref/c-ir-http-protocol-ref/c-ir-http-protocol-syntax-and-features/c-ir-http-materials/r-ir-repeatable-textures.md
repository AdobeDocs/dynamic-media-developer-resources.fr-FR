---
description: Les textures répétables comprennent les matériaux intérieurs et extérieurs, tels que les tissus (aussi bien pour les vêtements que pour les tissus), les dessus-de-sol, les papiers peints, les contreforts, les textures de grains de bois, les revêtements et les revêtements, ainsi que toute autre texture générique.
solution: Experience Manager
title: Textures répétables
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 3693498b-994a-460a-8b2e-780a1482d37a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 3%

---

# Textures répétables{#repeatable-textures}

Les textures répétables comprennent les matériaux intérieurs et extérieurs, tels que les tissus (aussi bien pour les vêtements que pour les tissus), les dessus-de-sol, les papiers peints, les contreforts, les textures de grains de bois, les revêtements et les revêtements, ainsi que toute autre texture générique.

Les textures répétables peuvent être appliquées à des objets plats, à contours, à esquisse, à plan, à mur et à armoire. Lorsqu’il est appliqué à un objet non texturable, l’objet est peint avec `color=` (ou `bgc=` si `color=` n’est pas spécifié).

Un matériau est considéré comme une texture s’il inclut un attribut `src=` spécifiant une image et s’il apparaît dans un MSS autre que la bordure oculaire ou mur.

Lors du rendu, la texture est alignée avec l’objet en faisant correspondre le point `anchor=` du matériau de texture avec le point d’origine de la texture de l’objet (tel qu’il a été créé dans la vignette).

<table id="table_992A6E93E4274B598A236F8F728F017A"> 
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
   <td colname="col2"> <p>Image textuelle répétable ; required </p> </td> 
   <td colname="col3"> <p>Aucune </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Résolution de la texture </p> </td> 
   <td colname="col3"> <span class="codeph"> attribute::Resolution  </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Point d'alignement de la texture </p> </td> 
   <td colname="col3"> <p>Coin supérieur gauche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Mode Répétition </p> </td> 
   <td colname="col3"> <p>0 (répétition droite). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Accentuation </p> </td> 
   <td colname="col3"> <p>0 (aucune accentuation). </p> </td> 
  </tr> 
 </tbody> 
</table>

Outre ces attributs de base, les textures répétables prennent en charge les attributs spéciaux suivants pour les applications avancées :

<table id="table_A97365804CB143DEB31F26A65DA3CE04"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
   <th colname="col3" class="entry"> <p>Par défaut </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> grout=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Couleur et épaisseur du sol; utile pour les matériaux en céramique/pierre </p> </td> 
   <td colname="col3"> <p>Gris déjà présent dans l’image </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph"> align=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Mode d’alignement (entre les objets) ; utilisé pour les applications de nettoyage </p> </td> 
   <td colname="col3"> <p>Correspondance centrale </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> rotate= </span> </a> </p> </td> 
   <td colname="col2"> <p>l’angle de rotation de la texture; non pris en charge par les objets de mur </p> </td> 
   <td colname="col3"> <p>0 (aucune rotation) </p> </td> 
  </tr> 
 </tbody> 
</table>
