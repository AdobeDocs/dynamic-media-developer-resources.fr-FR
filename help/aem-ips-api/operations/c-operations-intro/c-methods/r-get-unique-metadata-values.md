---
description: Obtient des valeurs de champ de métadonnées uniques.
seo-description: Obtient des valeurs de champ de métadonnées uniques.
seo-title: getUniqueMetadataValues
solution: Experience Manager
title: getUniqueMetadataValues
topic: Scene7 Image Production System API
uuid: 5b2f95a7-cc0b-4938-99b9-2aefa0ffe693
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 25%

---


# getUniqueMetadataValues{#getuniquemetadatavalues}

Obtient des valeurs de champ de métadonnées uniques.

Syntaxe

## Types d’utilisateur autorisés {#section-6a6b67e10a4c4e7bb18306115713380e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-b9d1413811c24566b6d095701f0f66db}

**Entrée (getUniqueMetadataValuesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Pose la société. |
| ` *`fieldHandle`*` | `xsd:string` | Non | Gérer en fonction du champ de métadonnées. |

**Output (getUniqueMetadataValuesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`valeurs`*` | `type:StringArray` |  |  |

## Exemples {#section-440f3bc3e5be436cb6ec26117d05f476}

Cet exemple de code utilise une poignée de champ pour renvoyer des valeurs de métadonnées spécifiques.

**Request**

```java
<ns1:getUniqueMetadataValuesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
</ns1:getUniqueMetadataValuesParam>
```

**Réponse**

```java
<getUniqueMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <values>
      <items>320</items>
   </values>
</getUniqueMetadataValuesReturn>
```

