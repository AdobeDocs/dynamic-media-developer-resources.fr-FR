---
description: Renvoie un tableau de noms de chemin Photoshop pour l’image donnée.
seo-description: Renvoie un tableau de noms de chemin Photoshop pour l’image donnée.
seo-title: getPhotoshopPathNames
solution: Experience Manager
title: getPhotoshopPathNames
topic: Scene7 Image Production System API
uuid: d3f1dea5-393b-498e-963d-37a4e38068a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getPhotoshopPathNames{#getphotoshoppathnames}

Renvoie un tableau de noms de chemin Photoshop pour l’image donnée.

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
| ` *`companyHandle`*` | `xsd:string` | Oui | Pointez sur le  qui contient l’image à utiliser. |
| ` *`assetHandle`*` | `xsd:string` | Oui | Traitement du fichier d’image. |

**Output (getPhotoshopPathNamesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`pathNameArray`*` | `types:StringArray` | Oui | Tableau de noms de chemins Photoshop dans une image. |

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

