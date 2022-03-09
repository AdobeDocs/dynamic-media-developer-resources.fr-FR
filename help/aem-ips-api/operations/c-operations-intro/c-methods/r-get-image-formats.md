---
description: Renvoie les formats d’image (PDF, EPS, SWF, etc.).
solution: Experience Manager
title: getImageFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c2fa4cdd-fb4f-4e6a-8197-8f64c986c3a0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 20%

---

# getImageFormats{#getimageformats}

Renvoie les formats d’image (PDF, EPS, SWF, etc.).

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

**Entrée (getImageFormatsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gestion de l’entreprise avec les formats d’image que vous souhaitez obtenir. |

**Sortie (getImageFormatsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| imageFormatArray | `types:ImageFormatArray` | Oui | Tableau du format d’image. |

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
