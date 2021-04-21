---
description: Renvoie un tableau de noms de chemins d’accès Photoshop pour l’image donnée.
solution: Experience Manager
title: getPhotoshopPathNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 19%

---


# getPhotoshopPathNames{#getphotoshoppathnames}

Renvoie un tableau de noms de chemins d’accès Photoshop pour l’image donnée.

Syntaxe

## Types d’utilisateur autorisés {#section-baa0fd4b92bc4ad89809efd659b3a629}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-605a4aab23104489a21f7f7f5849801b}

**Entrée (getPhotoshopPathNamesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Pointez sur la société contenant l’image à utiliser. |
| `*`assetHandle`*` | `xsd:string` | Oui | Pointez sur le fichier d’image. |

**Output (getPhotoshopPathNamesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`pathNameArray`*` | `types:StringArray` | Oui | Tableau de noms de chemins d’accès Photoshop dans une image. |

## Exemples {#section-6d316f14b4184d42af4ca3f717b042dd}

**Request**

```java
<getPhotoshopPathNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
</getPhotoshopPathNamesParam>
```

**Réponse**

```java
<getPhotoshopPathNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <pathNameArray>
    <items>Background Path</items>
    <items>Face Path</items>
  </pathNameArray>
</getPhotoshopPathNamesReturn>
```

