---
description: 'Dans ce type, le champ pageReset est significatif pour les types de fichier d’image RenderSet et Catalog. '
seo-description: 'Dans ce type, le champ pageReset est significatif pour les types de fichier d’image RenderSet et Catalog. '
seo-title: ImageSetMemberUpdate
solution: Experience Manager
title: ImageSetMemberUpdate
topic: Scene7 Image Production System API
uuid: b0226d21-87ba-4e07-9819-79c9df3df13c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ImageSetMemberUpdate{#imagesetmemberupdate}

Dans ce type, le champ pageReset est significatif pour les types de fichier d’image RenderSet et Catalog :

* Pour `RenderSet`, `pageReset` indique le  d’un nouveau groupe d’/échantillons de rendu.

* Dans le cas d’un catalogue, `pageReset` indique le  d’un nouvel  de page. En règle générale, il existe deux images de page par  de page, mais vous pouvez en avoir plus ou moins.

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Handle de ressource dans le tableau des membres de la visionneuse d’images. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Réinitialise la page. <p>Ce paramètre est ignoré et la valeur est obligatoirement définie sur true pour <span class="codeph"> la visionneuse</span> d’images <span class="codeph"> et la</span>visionneuse à 360°. </p></td> 
  </tr> 
 </tbody> 
</table>

