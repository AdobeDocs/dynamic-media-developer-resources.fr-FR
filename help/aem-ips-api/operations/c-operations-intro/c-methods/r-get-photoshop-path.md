---
description: Renvoie les coordonnées du quadrilatère englobant le chemin Photoshop nommé.
seo-description: Renvoie les coordonnées du quadrilatère englobant le chemin Photoshop nommé.
seo-title: getPhotoshopPath
solution: Experience Manager
title: getPhotoshopPath
topic: Scene7 Image Production System API
uuid: e3ed4888-18db-40bc-a1db-f44a342d0293
translation-type: tm+mt
source-git-commit: 22b447e66c223126f4e6b91f9a0102e86731c4a4
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 17%

---


# getPhotoshopPath{#getphotoshoppath}

Renvoie les coordonnées du quadrilatère englobant le chemin Photoshop nommé.

Syntaxe

## Types d’utilisateur autorisés {#section-c417a287612847cb98dd0aa9c67fd78a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* &quot;

## Paramètres {#section-ebffe496284c4ced9f329f78127be199}

**Entrée (getPhotoshopPathParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Pointez sur la société avec l’image que vous souhaitez utiliser. |
| ` *`assetHandle`*` | `xsd:string` | Oui | Pointez sur le fichier d’image. |
| ` *`pathName`*` | `xsd:string` | Oui | Nom du chemin Photoshop à renvoyer. |

**Output (getPhotoshopPathReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`perspectiveQuad`*` | `types:PerspectiveQuad` | Oui | Renvoie les coordonnées de l’image en fonction du chemin d’accès. Voir [PerspectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204). |

## Exemples {#section-1f0461cbdc184c8d8925336d5279db47}

**Request**

```java
<getPhotoshopPathParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
  <pathName>Face Path</pathName>
</getPhotoshopPathParam>
```

**Réponse**

```java
<getPhotoshopPathReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <perspectiveQuad>
    <x0>932.19</x0>
    <y0>296.592</y0>
    <x1>968.769</x1>
    <y1>320.16</y1>
    <x2>1119.56</x2>
    <y2>1200.0</y2>
    <x3>900.43</x3>
    <y3>1200.0</y3>
  </perspectiveQuad>
</getPhotoshopPathReturn>
```

>[!MORELIKETHIS]
>
>* [PerspectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204)

