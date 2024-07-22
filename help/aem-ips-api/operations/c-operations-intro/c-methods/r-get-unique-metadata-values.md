---
description: Obtient des valeurs de champ de métadonnées uniques.
solution: Experience Manager
title: getUniqueMetadataValues
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: ac5f5667-6c94-425c-bc01-f9df48d16e00
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 24%

---

# getUniqueMetadataValues{#getuniquemetadatavalues}

Obtient des valeurs de champ de métadonnées uniques.

Syntaxe

## Types d’utilisateurs autorisés {#section-6a6b67e10a4c4e7bb18306115713380e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-b9d1413811c24566b6d095701f0f66db}

**Input (getUniqueMetadataValuesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Traitez la société. |
| fieldHandle | `xsd:string` | Non | Traitement du champ de métadonnées. |

**Sortie (getUniqueMetadataValuesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| valeurs | `type:StringArray` |  |  |

## Exemples {#section-440f3bc3e5be436cb6ec26117d05f476}

Cet exemple de code utilise une poignée de champ pour renvoyer des valeurs de métadonnées spécifiques.

**Requête**

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
