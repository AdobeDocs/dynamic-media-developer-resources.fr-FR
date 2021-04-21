---
description: Récupère les champs de métadonnées définis par l’utilisateur associés à un fichier.
solution: Experience Manager
title: getMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 14%

---


# getMetadataFields{#getmetadatafields}

Récupère les champs de métadonnées définis par l’utilisateur associés à un fichier.

Syntaxe

## Types d’utilisateur autorisés {#section-e32e481a02674b729bfc5454a6c9ff65}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-bac949e59c0546429c5786fe422d750d}

**Entrée (getMetadataFieldsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de société. |
| `*`assetType`*` | `xsd:string` | Oui | Types de ressources à partir desquels obtenir des métadonnées. |

**Output (getMetadataFieldsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`Expression de code`*` | `Code Phrase` |  |  |

## Exemples {#section-dbfde1483d614b5aac2b491cb32115d7}

Cet exemple de code renvoie des fichiers de métadonnées pour le type et la société spécifiés. La réponse contient un tableau de champs de métadonnées dans un tableau de champs. Tous les fichiers ne possèdent pas les mêmes métadonnées. L’utilisateur IPS définit le champ de métadonnées du fichier.

**Request**

```java
<ns1:getMetadataFieldsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
</ns1:getMetadataFieldsParam>
```

**Réponse**

```java
<getMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldArray>
      <items>
         <fieldHandle>47|ALL|Resolution</fieldHandle>
         <name>Resolution</name>
         <type>String</type>
         <defaultValue>120</defaultValue>
         <isRequired>false</isRequired>
         <isUserDefined>true</isUserDefined>
      </items>
   </fieldArray>
</getMetadataFieldsReturn>
```

