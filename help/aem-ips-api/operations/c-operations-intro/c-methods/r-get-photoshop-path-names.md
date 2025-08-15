---
description: Renvoie un tableau de noms de chemins d’Photoshop pour l’image donnée.
solution: Experience Manager
title: getPhotoshopPathNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 11d4c0d0-a3a3-4324-a4a6-1dd7b7e673da
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 18%

---

# getPhotoshopPathNames{#getphotoshoppathnames}

Renvoie un tableau de noms de chemins d’Photoshop pour l’image donnée.

Syntaxe

## Types d’utilisateurs autorisés {#section-baa0fd4b92bc4ad89809efd659b3a629}

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
| CompanyHandle | `xsd:string` | Oui | Gérez l’entreprise qui contient l’image avec laquelle vous souhaitez travailler. |
| AssetHandle | `xsd:string` | Oui | Poignée de la ressource image. |

**Output (getPhotoshopPathNamesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Tableau pathNameArray | `types:StringArray` | Oui | Tableau de noms de Photoshop chemins d’accès d’une image. |

## Exemples {#section-6d316f14b4184d42af4ca3f717b042dd}

**Demander**

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
