---
title: Textures reproductibles
description: Les textures reproductibles comprennent les matériaux intérieurs et extérieurs, tels que les tissus (vêtements et tissus d’ameublement), les revêtements de sol mur à mur, les papiers peints, les matériaux de comptoir, les textures de grain de bois, les matériaux de toiture et de revêtement et toute autre texture générique.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3693498b-994a-460a-8b2e-780a1482d37a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 3%

---

# Textures reproductibles{#repeatable-textures}

Les textures reproductibles comprennent les matériaux intérieurs et extérieurs, tels que les tissus (vêtements et tissus d’ameublement), les revêtements de sol mur à mur, les papiers peints, les matériaux de comptoir, les textures de grain de bois, les matériaux de toiture et de revêtement et toute autre texture générique.

Les textures reproductibles peuvent être appliquées à des objets plats, en courbes de transfert, esquisses, plans, murs et armoires. Lorsqu’il est appliqué à un objet non texturable, l’objet est peint avec `color=` (ou `bgc=` si `color=` n’est pas spécifié).

Un matériau est considéré comme une texture s’il comprend un `src=` attribut spécifiant une image et s’il apparaît dans un MSS autre qu’une bordure de décalcomanie ou de mur.

Lors du rendu, la texture est alignée avec l’objet en faisant correspondre le `anchor=` point du matériau de texture avec le point d’origine de la texture de l’objet (tel que créé dans la vignette).

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"><span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Image de texture reproductible ; Obligatoire </p> </td> 
   <td colname="col3"> <p>Aucune </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"><span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Résolution de la texture </p> </td> 
   <td colname="col3"> <span class="codeph"> attribut ::Résolution </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"><span class="codeph"> ancre= </span> </a> </p> </td> 
   <td colname="col2"> <p>Point d’alignement de texture </p> </td> 
   <td colname="col3"> <p>Coin supérieur gauche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"><span class="codeph"> repeat= </span> </a> </p> </td> 
   <td colname="col2"> <p>Mode Répétition </p> </td> 
   <td colname="col3"> <p>0 (répétition directe). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"><span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>Accentuation </p> </td> 
   <td colname="col3"> <p>0 (aucun renforcement). </p> </td> 
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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"><span class="codeph"> coulis= </span> </a> </p> </td> 
   <td colname="col2"> <p>Couleur et épaisseur du coulis ; Utile pour les matériaux de carreaux de céramique / pierre </p> </td> 
   <td colname="col3"> <p>Coulis déjà présent dans l’image </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"><span class="codeph"> align= </span> </a> </p> </td> 
   <td colname="col2"> <p>Mode d’alignement (entre les objets) ; Utilisé pour les applications de rembourrage </p> </td> 
   <td colname="col3"> <p>Correspondance au centre </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> rotation= </span> </a> </p> </td> 
   <td colname="col2"> <p>Angle de rotation de la texture ; non pris en charge par les objets de mur </p> </td> 
   <td colname="col3"> <p>0 (pas de rotation) </p> </td> 
  </tr> 
 </tbody> 
</table>
