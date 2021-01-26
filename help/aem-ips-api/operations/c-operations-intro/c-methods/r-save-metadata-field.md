---
description: Créez ou modifiez un champ de métadonnées. Omettez la poignée de champ facultative pour créer un champ de métadonnées.
seo-description: Créez ou modifiez un champ de métadonnées. Omettez la poignée de champ facultative pour créer un champ de métadonnées.
seo-title: saveMetadataField
solution: Experience Manager
title: saveMetadataField
topic: Dynamic Media Image Production System API
uuid: ccd84366-732a-4caf-914d-3bc5fe499e7a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 15%

---


# saveMetadataField{#savemetadatafield}

Créez ou modifiez un champ de métadonnées. Omettez la poignée de champ facultative pour créer un champ de métadonnées.

>[!NOTE]
>
>Cette méthode est désapprouvée.

## Types d’utilisateur autorisés {#section-0c1cbde0863346f8a31b32fd06ab2926}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-ec6827d485a143f4a059a92b18e40f4e}

**Entrée (saveMetadataFieldParam)**

<table id="table_C944A44352F2475A89CE86F3DB1B648A"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> La poignée de la société. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Poignée de champ. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Choix des types de fichier à partir desquels enregistrer les métadonnées. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Nom du champ. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Choix des types de champs de métadonnées. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Valeur par défaut des champs pour tous les fichiers. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Masquer ou exposer les métadonnées spécifiques au système IPS. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnded</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Indicateur booléen qui indique si le champ de métadonnées est appliqué (validé) lorsque la valeur est définie. </p> <p>Si la valeur est définie sur true, une erreur est générée si une valeur non autorisée est définie dans <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (saveMetadataFieldReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`fieldHandle`*` | `xsd:string` | Oui | Gestion du nouveau champ de métadonnées. |

## Exemples {#section-4441c26d1f41466ba972b43dd5189e89}

Cet exemple de code crée un nouveau champ de métadonnées limité par les constantes de chaîne Type de fichier et Types de champ de métadonnées. Si l’élément `fieldHandle` possède une valeur d’identificateur de champ valide, il modifie les valeurs de métadonnées et obtient le même nom d’identificateur de champ que celui spécifié dans la requête.

**Request**

```java
<ns1:saveMetadataFieldParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
   <ns1:name>Resolution</ns1:name>
   <ns1:fieldType>String</ns1:fieldType>
   <ns1:defaultValue>120</ns1:defaultValue>
</ns1:saveMetadataFieldParam>
```

**Réponse**

```java
<saveMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldHandle>47|ALL|Resolution</fieldHandle>
</saveMetadataFieldReturn>
```

