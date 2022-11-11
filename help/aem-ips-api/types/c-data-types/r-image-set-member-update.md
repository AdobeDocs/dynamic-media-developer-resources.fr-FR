---
description: Dans ce type, le champ pageReset est significatif pour les types de ressources d’image RenderSet et Catalog.
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 4c598afb-a80c-4fac-997f-ef1c7175430c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 7%

---

# [!DNL ImageSetMemberUpdate]{#imagesetmemberupdate}

Dans ce type, le champ pageReset est significatif pour les types de ressources d’image RenderSet et Catalog :

* Pour `RenderSet`, `pageReset` indique le début d’une nouvelle vue de rendu/groupe d’échantillons.

* Pour le catalogue, `pageReset` indique le début d’une nouvelle page vue. En règle générale, il existe deux images de page par page vue, mais vous pouvez en avoir plus ou moins.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Poignée de ressource dans le tableau des membres de la visionneuse d’images. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Réinitialise la page. <p>La définition de est ignorée et la valeur est forcée à true pour <span class="codeph"> ImageSet</span> et <span class="codeph"> SpinSet</span>. </p></td> 
  </tr> 
 </tbody> 
</table>
