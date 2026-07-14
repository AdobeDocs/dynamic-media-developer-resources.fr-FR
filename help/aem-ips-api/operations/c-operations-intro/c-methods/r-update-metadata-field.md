---
description: Mettez à jour les métadonnées des champs.
solution: Experience Manager
title: updateMetadataField
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 67506e76-aa23-46a7-a900-03d89b4266fd
TQID: 'https://experienceleague.adobe.com/KWv2pWCAN3eKZ5FLG2e62qGKSLpMt0eH5QBbQpSOTNM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 12%

---

# updateMetadataField{#updatemetadatafield}

Mettez à jour les métadonnées des champs.

Syntaxe

## Types d’utilisateurs autorisés {#section-540e91823fee49a4920ca738f7bfeb99}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-69681ed1ddff437ca1c73f46fe835c96}

**Input (updateMetadataFieldParam)**

<table id="table_65D6EE6C402E4F01819822A855B6BB7F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom du paramètre </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Obligatoire </th> 
   <th colname="col4" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Identifiant de la société. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Descripteur de champ de métadonnées. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nom </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Nom du champ de métadonnées. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Valeur du champ de métadonnées. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Masquez ou exposez les métadonnées spécifiques au système IPS. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Indicateur booléen qui indique si le champ de métadonnées est appliqué (validé) lorsque la valeur est définie. </p> <p>Si la valeur est définie sur true, une erreur est générée si une valeur non autorisée est définie dans <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Permet de créer un ensemble de valeurs énumérées partagées vers lesquelles les balises sélectionnées peuvent pointer. </td> 
  </tr> 
 </tbody> 
</table>

**Output (updateMetadataFieldReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| fieldHandle | `xsd:string` | Oui | Descripteur de champ de métadonnées. |

## Exemples {#section-bb7d93ab6d914ddfa294e08983e589ee}

Cet exemple de mise à jour de code attribue un nouveau nom et une valeur par défaut à un champ de métadonnées. La réponse renvoie une poignée au champ mis à jour.

**Requête**

```java
<updateMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
   <name>updateMetadataField</name>
   <defaultValue>Default</defaultValue>
</updateMetadataFieldParam>
```

**Réponse**

```java
<updateMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|updateMetadataField</fieldHandle>
</updateMetadataFieldReturn>
```

