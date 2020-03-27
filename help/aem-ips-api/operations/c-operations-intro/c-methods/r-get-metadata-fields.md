---
description: Obtient les champs de métadonnées définis par l’utilisateur associés à un fichier.
seo-description: Obtient les champs de métadonnées définis par l’utilisateur associés à un fichier.
seo-title: getMetadataFields
solution: Experience Manager
title: getMetadataFields
topic: Scene7 Image Production System API
uuid: bf891bae-53c8-4e3d-90df-caca9a7e022b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getMetadataFields{#getmetadatafields}

Obtient les champs de métadonnées définis par l’utilisateur associés à un fichier.

Syntaxe

## Types d’utilisateurs autorisés {#section-e32e481a02674b729bfc5454a6c9ff65}

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
| ` *`companyHandle`*` | `xsd:string` | Oui |  poignée. |
| ` *`assetType`*` | `xsd:string` | Oui | Types de ressources à partir desquels obtenir des métadonnées. |

**Output (getMetadataFieldsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`Expression de code`*` | `Code Phrase` |  |  |

## Exemples {#section-dbfde1483d614b5aac2b491cb32115d7}

Cet exemple de code renvoie des fichiers de métadonnées pour le type et le  spécifiés. La réponse contient un tableau de champs de métadonnées dans un tableau de champs. Tous les fichiers n’ont pas les mêmes métadonnées. L’utilisateur IPS définit le champ de métadonnées du fichier.

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

