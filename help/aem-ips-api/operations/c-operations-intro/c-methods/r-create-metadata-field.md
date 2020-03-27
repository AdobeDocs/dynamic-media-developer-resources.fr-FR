---
description: Permet aux administrateurs de créer de nouveaux champs de métadonnées afin de les coordonner avec les systèmes  ou pour les opérations de modèle. Les champs de métadonnées créés sont, par exemple, des mots-clés, des informations sur l’auteur de l’image ou des informations sur le détenteur du copyright.
seo-description: Permet aux administrateurs de créer de nouveaux champs de métadonnées afin de les coordonner avec les systèmes  ou pour les opérations de modèle. Les champs de métadonnées créés sont, par exemple, des mots-clés, des informations sur l’auteur de l’image ou des informations sur le détenteur du copyright.
seo-title: createMetadataField
solution: Experience Manager
title: createMetadataField
topic: Scene7 Image Production System API
uuid: 50ab61fa-df44-4305-ad9f-693c4aea1e69
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# createMetadataField{#createmetadatafield}

Permet aux administrateurs de créer de nouveaux champs de métadonnées afin de les coordonner avec les systèmes  ou pour les opérations de modèle. Les champs de métadonnées créés sont, par exemple, des mots-clés, des informations sur l’auteur de l’image ou des informations sur le détenteur du copyright.

Syntaxe

## Types d’utilisateurs autorisés {#section-2f61d79f8cac4692bfa53b95035ddd89}

* `IpsAdmin`

## Paramètres {#section-f8260bc8dd0a4570bc7f714f81ab975f}

**Entrée (createMetadataFieldParam)**

<table id="table_E5B249BBED3B4D2F9CEE2CCF27472D1B"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Nom du auquel le champ de métadonnées appartient. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Type de fichier. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nom</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Nom du champ de métadonnées que vous créez. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4">Type de champ de métadonnées. <p>La constante de types de champ de métadonnées définit les types disponibles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Valeur par défaut du champ de métadonnées à créer ( <span class="codeph"> Scene 7</span>, par exemple). </p> <p>Les valeurs par défaut ne sont pas prises en charge pour les types de champs de balise et doivent être omises. Si une valeur par défaut non vide est spécifiée pour un type de champ de balise, une erreur est renvoyée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> est Masqué</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Masquez ou affichez les métadonnées spécifiques au système IPS. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnered</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Indicateur booléen indiquant si le champ de métadonnées est appliqué (validé) lorsque la valeur est définie. </p> <p>Si la valeur est définie sur true, une erreur est générée si une valeur non autorisée est définie dans <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Permet de créer un ensemble de valeurs énumérées partagées auxquelles les balises sélectionnées peuvent pointer. </td> 
  </tr> 
 </tbody> 
</table>

**Output (createMetadataFieldReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`fieldHandle`*` | `xsd:string` | Oui | Poignée du nouveau champ de métadonnées. |

## Exemples {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

Cet exemple de code crée un champ de métadonnées de type chaîne appelé `createMetadataField`. La réponse renvoie la poignée au nouveau champ de métadonnées.

**Request**

```java
<createMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetType>Image</assetType>
   <name>createMetadataField</name>
   <fieldType>String</fieldType>
   <initialTagValue>Fall</initialTagValue>
   <defaultValue>Default</defaultValue>
</createMetadataFieldParam>
```

**Réponse**

```java
<createMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
</createMetadataFieldReturn>
```

