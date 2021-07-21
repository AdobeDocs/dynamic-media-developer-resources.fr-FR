---
description: Permet aux administrateurs de créer de nouveaux champs de métadonnées à coordonner avec les systèmes de gestion de contenu ou pour les opérations de modèle. Parmi les exemples de champs de métadonnées créés, citons les mots-clés, les informations sur l’auteur de l’image ou les informations sur le titulaire du copyright.
solution: Experience Manager
title: createMetadataField
feature: Dynamic Media Classic,SDK/API,Métadonnées
role: Developer,Admin
exl-id: eac7fa54-ebe2-4f42-a478-d9a6fb54d1b6
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 13%

---

# createMetadataField{#createmetadatafield}

Permet aux administrateurs de créer de nouveaux champs de métadonnées à coordonner avec les systèmes de gestion de contenu ou pour les opérations de modèle. Parmi les exemples de champs de métadonnées créés, citons les mots-clés, les informations sur l’auteur de l’image ou les informations sur le titulaire du copyright.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Nom de la société à laquelle le champ de métadonnées appartient. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Type de fichier. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Nom du champ de métadonnées que vous créez. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4">Type de champ de métadonnées. <p>La constante Types de champ de métadonnées définit les types disponibles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>La valeur par défaut du champ de métadonnées à créer (par exemple, <span class="codeph"> Scene 7</span>). </p> <p>Les valeurs par défaut ne sont pas prises en charge pour les types de champ de balise et doivent être omises. Si une valeur par défaut non vide est spécifiée pour un type de champ de balise, une erreur est renvoyée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Masquer ou exposer les métadonnées spécifiques au système IPS. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Indicateur boolean qui indique si le champ de métadonnées est appliqué (validé) lorsque la valeur est définie. </p> <p>Si la valeur est définie sur true, une erreur est générée si une valeur non autorisée est définie dans <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Permet de créer un ensemble de valeurs énumérées partagées auxquelles les balises sélectionnées peuvent pointer. </td> 
  </tr> 
 </tbody> 
</table>

**Sortie (createMetadataFieldReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`fieldHandle`*` | `xsd:string` | Oui | Gestion du nouveau champ de métadonnées. |

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
