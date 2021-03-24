---
description: 'Dans ce type, le champ pageReset est significatif pour les types de fichier d’image RenderSet et Catalog. '
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media Classic, SDK/API, visionneuses d’images
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 7%

---


# ImageSetMemberUpdate{#imagesetmemberupdate}

Dans ce type, le champ pageReset est significatif pour les types de fichier d’image RenderSet et Catalog :

* Pour `RenderSet`, `pageReset` indique l&#39;début d&#39;un nouveau groupe de vues/échantillons de rendu.

* Pour le catalogue, `pageReset` indique le début d’une nouvelle vue de page. En règle générale, il existe deux images de page par vue de page, mais vous pouvez en avoir plus ou moins.

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
   <td colname="col3"> Handle de ressource dans le tableau des membres de la visionneuse d’images. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Réinitialise la page. <p>Le paramètre est ignoré et la valeur est forcée à true pour <span class="codeph"> ImageSet</span> et <span class="codeph"> SpinSet</span>. </p></td> 
  </tr> 
 </tbody> 
</table>

