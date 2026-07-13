---
description: Dans ce type, le champ pageReset est significatif pour les types de ressources d’image RenderSet et Catalog
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 4c598afb-a80c-4fac-997f-ef1c7175430c
TQID: 'https://experienceleague.adobe.com/c9-ANQJjBlcpQYnSmrD8nQQ08Vllqt3ZcpW6IBJ9-4I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 4%

---

# [!DNL ImageSetMemberUpdate]{#imagesetmemberupdate}

Dans ce type, le champ pageReset est significatif pour les types de ressources d’image RenderSet et Catalog :

* Par `RenderSet`, `pageReset` indique le début d’un nouveau groupe d’échantillons ou d’une nouvelle vue de rendu.

* Pour Catalogue , `pageReset` indique le début d’une nouvelle page vue. En règle générale, il y a 2 images de page par page vue, mais vous pouvez en avoir plus ou moins.

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
   <td colname="col3"> Gestion des ressources dans le tableau des membres de la visionneuse d’images. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Réinitialise la page. <p>Le paramètre est ignoré et la valeur est forcée à true pour <span class="codeph"> ImageSet</span> et <span class="codeph"> SpinSet</span>. </p></td> 
  </tr> 
 </tbody> 
</table>

