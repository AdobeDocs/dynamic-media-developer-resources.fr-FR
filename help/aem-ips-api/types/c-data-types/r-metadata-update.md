---
description: Définit les valeurs de métadonnées pour un fichier spécifique utilisé avec setAssetMetadata. Décrit les modifications que vous souhaitez apporter aux métadonnées.
seo-description: Définit les valeurs de métadonnées pour un fichier spécifique utilisé avec setAssetMetadata. Décrit les modifications que vous souhaitez apporter aux métadonnées.
seo-title: MetadataUpdate
solution: Experience Manager
title: MetadataUpdate
topic: Dynamic Media Image Production System API
uuid: 09d3940b-117d-4d83-8b12-e86520c9da34
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 5%

---


# MetadataUpdate{#metadataupdate}

Définit les valeurs de métadonnées pour un fichier spécifique utilisé avec setAssetMetadata. Décrit les modifications que vous souhaitez apporter aux métadonnées.

>[!NOTE]
>
>Si le champ de valeur unique est transmis, la valeur de balise de la ressource est réinitialisée à la valeur de balise spécifiée.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Poignée de champ de métadonnées. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Valeur de mise à jour des métadonnées. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> boolVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Valeur de métadonnées booléenne (pour les champs de type booléen uniquement). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> longVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> Valeur de métadonnées longue (uniquement pour les champs à saisie). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:doublon</span> </td> 
   <td colname="col3"> Valeur des métadonnées de doublon (pour les champs à virgule flottante uniquement). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dateVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Valeur de métadonnées de date (pour les champs de type date uniquement). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> addTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> <p>Ajoute à la liste de valeur de balise existante pour la ressource. 
     <ul id="ul_08DE6C490B614560A6118E7AC59720E3"> 
      <li id="li_358A3BDC0EC94CCF8178CD789F09F804">Les champs de balise à valeur unique stockent uniquement la dernière valeur. </li> 
      <li id="li_3F47D3A3C63A4752BF9A45F7B00A6E70">Un champ de balise de dictionnaire fixe renvoie une erreur si la valeur ne figure pas dans le dictionnaire. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3">Remplace la liste de valeur de balise existante pour la ressource. 
    <ul id="ul_941C915C69E84CF2AC5938378837EB92"> 
     <li id="li_6E85019335034B2EB1302696AE690ED5">Les champs de balise à valeur unique stockent uniquement la dernière valeur. </li> 
     <li id="li_0DC56717EBB642D29FB7A3D043CEDED1">Un champ de balise de dictionnaire fixe renvoie une erreur si la valeur ne figure pas dans le dictionnaire. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> deleteTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Supprime les valeurs spécifiées de la liste de valeur de balise de la ressource, le cas échéant. </td> 
  </tr> 
 </tbody> 
</table>

