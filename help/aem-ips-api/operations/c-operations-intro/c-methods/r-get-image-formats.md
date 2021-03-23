---
description: Renvoie des formats d’image, tels que PDF, EPS, SWF, etc.
seo-description: Renvoie des formats d’image, tels que PDF, EPS, SWF, etc.
seo-title: getImageFormats
solution: Experience Manager
title: getImageFormats
uuid: 0adf989d-9c72-4337-99c0-de6931943e78
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 16%

---


# getImageFormats{#getimageformats}

Renvoie des formats d’image, tels que PDF, EPS, SWF, etc.

Syntaxe

## Types d’utilisateur autorisés {#section-6a386ad8641b4aa1a281600fc94fd3f6}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-eefa36a70b74498f8727ef61d98cfb63}

**Entrée (getImageFormatsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée vers la société avec les formats d’image que vous souhaitez obtenir. |

**Output (getImageFormatsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`imageFormatArray`*` | `types:ImageFormatArray` | Oui | Tableau de format d’image. |

## Exemples {#section-73881e12839b4904bf3299b0920bdd0c}

Cet exemple de code renvoie tous les formats d’image pour la société spécifiée.

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

