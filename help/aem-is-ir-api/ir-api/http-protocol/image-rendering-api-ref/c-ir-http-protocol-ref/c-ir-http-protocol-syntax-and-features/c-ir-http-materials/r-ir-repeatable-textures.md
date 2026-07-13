---
title: Textures répétables
description: Les textures répétables comprennent les matériaux intérieurs et extérieurs, tels que les tissus (vêtements et tissus d'ameublement), les revêtements de sol mur à mur, les papiers peints, les matériaux de comptoir, les textures de grain de bois, les matériaux de toiture et de revêtement, et toute autre texture générique.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3693498b-994a-460a-8b2e-780a1482d37a
TQID: 'https://experienceleague.adobe.com/hWfVo7g-LL9l-G8FkN4HZ4B1X7uX85LlklZFjNBsjZI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 251
ht-degree: 3%

---

# Textures répétables{#repeatable-textures}

Les textures répétables comprennent les matériaux intérieurs et extérieurs, tels que les tissus (vêtements et tissus d&#39;ameublement), les revêtements de sol mur à mur, les papiers peints, les matériaux de comptoir, les textures de grain de bois, les matériaux de toiture et de revêtement, et toute autre texture générique.

Les textures répétables peuvent être appliquées à des objets plats, de ligne de flux, d&#39;esquisse, de plan, de mur ou d&#39;armoire. Lorsqu&#39;il est appliqué à un objet non texturable, l&#39;objet est peint avec `color=` (ou `bgc=` si `color=` n&#39;est pas spécifié).

Un matériau est considéré comme une texture s&#39;il inclut un attribut `src=` spécifiant une image et s&#39;il se produit dans un MSS autre qu&#39;une vignette ou une bordure de mur.

Lors du rendu, la texture est alignée avec l’objet en faisant correspondre le point de `anchor=` du matériau de texture avec le point d’origine de texture de l’objet (tel que créé dans la vignette).

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Image de texture reproductible ; obligatoire </p> </td> 
   <td colname="col3"> <p>Aucune </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Résolution de la texture </p> </td> 
   <td colname="col3"> <span class="codeph"> attribute::Resolution </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor= </span> </a> </p> </td> 
   <td colname="col2"> <p>Point d'alignement de la texture </p> </td> 
   <td colname="col3"> <p>Coin supérieur gauche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat= </span> </a> </p> </td> 
   <td colname="col2"> <p>Mode de répétition </p> </td> 
   <td colname="col3"> <p>0 (répétition droite). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>Accentuation </p> </td> 
   <td colname="col3"> <p>0 (aucun accentuation). </p> </td> 
  </tr> 
 </tbody> 
</table>

En plus de ces attributs de base, les textures répétables prennent en charge les attributs spécifiques suivants pour les applications avancées :

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> coulis= </span> </a> </p> </td> 
   <td colname="col2"> <p>Couleur et épaisseur du coulis ; utile pour les matériaux de carreaux de céramique/pierre </p> </td> 
   <td colname="col3"> <p>Le coulis est déjà présent dans l'image </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph"> align= </span> </a> </p> </td> 
   <td colname="col2"> <p>Mode d'alignement (entre objets); utilisé pour les applications de capitonnage </p> </td> 
   <td colname="col3"> <p>Centre-correspondant </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> rotation= </span> </a> </p> </td> 
   <td colname="col2"> <p>Angle de rotation de la texture ; non pris en charge par les objets de mur </p> </td> 
   <td colname="col3"> <p>0 (pas de rotation) </p> </td> 
  </tr> 
 </tbody> 
</table>

