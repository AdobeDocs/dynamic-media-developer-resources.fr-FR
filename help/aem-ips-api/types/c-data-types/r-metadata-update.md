---
description: Définit les valeurs de métadonnées d’une ressource spécifique utilisée avec setAssetMetadata. Décrit les modifications que vous souhaitez apporter aux métadonnées.
solution: Experience Manager
title: MetadataUpdate
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 99dc1f0c-c4c4-433e-9b91-fa39ef6f84d7
TQID: 'https://experienceleague.adobe.com/55c5TnWcOF5S5XNlWQ1unTzNRKSXH2Fs-JTpvBdXyfo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 198
ht-degree: 2%

---

# [!DNL MetadataUpdate]{#metadataupdate}

Définit les valeurs de métadonnées d’une ressource spécifique utilisée avec setAssetMetadata. Décrit les modifications que vous souhaitez apporter aux métadonnées.

>[!NOTE]
>
>Si le champ à valeur unique est transmis, la valeur de balise de la ressource est réinitialisée à la valeur de balise spécifiée.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Descripteur de champ de métadonnées. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> valeur <span class="varname"> </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Valeur de mise à jour des métadonnées. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> boolVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Valeur de métadonnées booléennes (pour les champs de type booléen uniquement). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> longVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> Valeur de métadonnées longue (pour les champs entrés uniquement). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> Valeur de métadonnées double (pour les champs de type flottant uniquement). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dateVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Valeur de métadonnées de date (pour les champs de type date uniquement). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> addTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> <p>S’ajoute à la liste des valeurs de balise existante pour la ressource. 
     <ul id="ul_08DE6C490B614560A6118E7AC59720E3"> 
      <li id="li_358A3BDC0EC94CCF8178CD789F09F804">Les champs de balise à valeur unique stockent uniquement la dernière valeur. </li> 
      <li id="li_3F47D3A3C63A4752BF9A45F7B00A6E70">Un champ de balise de dictionnaire fixe renvoie une erreur si la valeur ne figure pas dans le dictionnaire. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3">Remplace la liste des valeurs de balise existante pour la ressource. 
    <ul id="ul_941C915C69E84CF2AC5938378837EB92"> 
     <li id="li_6E85019335034B2EB1302696AE690ED5">Les champs de balise à valeur unique stockent uniquement la dernière valeur. </li> 
     <li id="li_0DC56717EBB642D29FB7A3D043CEDED1">Un champ de balise de dictionnaire fixe renvoie une erreur si la valeur ne figure pas dans le dictionnaire. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> deleteTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Supprime les valeurs spécifiées de la liste de valeurs de balise de la ressource, le cas échéant. </td> 
  </tr> 
 </tbody> 
</table>
