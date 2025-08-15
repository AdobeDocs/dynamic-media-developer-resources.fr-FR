---
description: Ajoute un terme à utiliser avec searchAssets.
solution: Experience Manager
title: Condition des métadonnées
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 9226fb81-b3ff-41e4-a3cd-d5a40f359be6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---

# [!DNL MetadataCondition]{#metadatacondition}

Ajoute un terme de recherche à utiliser avec searchAssets.

Syntaxe

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
   <td colname="col3"> Poignée de champ. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Choix des opérateurs de comparaison de chaînes. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> valeur</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne</span> </td> 
   <td colname="col3"> Valeur à tester. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> boolVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Valeur de comparaison booléenne (pour les champs de type booléen uniquement). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> longVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> Valeur de comparaison longue (pour les champs entrés uniquement). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> MinLong</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :long</span> </td> 
   <td colname="col3"> Valeur longue minimale dans la comparaison des plages (pour les champs int-typés uniquement). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> MaxLong</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> Valeur long maximale dans la comparaison des plages (pour les champs avec type int uniquement). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> Valeur de comparaison double (pour les champs de type flottant uniquement). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> minDouble</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :double</span> </td> 
   <td colname="col3"> Double valeur minimale dans la comparaison de plages (pour les champs de saisie flottante uniquement). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> maxDouble</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :double</span> </td> 
   <td colname="col3"> Double valeur maximale dans la comparaison de plages (pour les champs de saisie flottante uniquement). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dateVale </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Valeur de comparaison de dates (pour les champs de type date uniquement). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> minDate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Valeur de date minimale dans la comparaison de périodes (pour les champs de type date uniquement). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Date max.</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :dateTime</span> </td> 
   <td colname="col3"> Valeur de date maximale dans la comparaison de plages (pour les champs de date saisie uniquement). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Sensible à la</span> casse </span> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p> Définit le respect de la casse pour le serveur de métadonnées. Utilisé dans l’appel <span class="codeph"> searchAssetsByMetadata</span>. </p> <p>Voir <a href="../../operations/c-operations-intro/c-methods/r-search-assets-by-metadata.md#reference-609ec73944a34ce49b152389fbb40414" format="dita" scope="local"> searchAssetsByMetadata</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>
