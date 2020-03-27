---
description: Renvoie des formats d’image, tels que PDF, EPS, SWF, etc.
seo-description: Renvoie des formats d’image, tels que PDF, EPS, SWF, etc.
seo-title: getImageFormats
solution: Experience Manager
title: getImageFormats
topic: Scene7 Image Production System API
uuid: 0adf989d-9c72-4337-99c0-de6931943e78
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getImageFormats{#getimageformats}

Renvoie des formats d’image, tels que PDF, EPS, SWF, etc.

Syntaxe

## Types d’utilisateurs autorisés {#section-6a386ad8641b4aa1a281600fc94fd3f6}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-eefa36a70b74498f8727ef61d98cfb63}

**Input (getImageFormatsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Poignée vers le avec les formats d’image que vous souhaitez obtenir. |

**Output (getImageFormatsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`imageFormatArray`*` | `types:ImageFormatArray` | Oui | Tableau de format d’image. |

## Exemples {#section-73881e12839b4904bf3299b0920bdd0c}

Cet exemple de code renvoie tous les formats d’image pour le  de spécifié.

**Request**

```java
<ns1:getImageFormatsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getImageFormatsParam>
```

**Réponse**

```java
<getImageFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <imageFormatArray></imageFormatArray>
</getImageFormatsReturn>
```

