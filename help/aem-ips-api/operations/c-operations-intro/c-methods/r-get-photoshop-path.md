---
description: Renvoie les coordonnées du quadrilatère entourant le chemin Photoshop nommé.
solution: Experience Manager
title: getPhotoshopPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 46d88547-bb60-4370-9c79-bd281b40ba28
TQID: 'https://experienceleague.adobe.com/oYuZ7LC10b-3r3VvI-Kg4tlD7rMtshcswi3hctp6aUM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 17%

---

# getPhotoshopPath{#getphotoshoppath}

Renvoie les coordonnées du quadrilatère entourant le chemin Photoshop nommé.

Syntaxe

## Types d’utilisateurs autorisés {#section-c417a287612847cb98dd0aa9c67fd78a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* «

## Paramètres {#section-ebffe496284c4ced9f329f78127be199}

**Input (getPhotoshopPathParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gérer vers la société avec l’image que vous souhaitez utiliser. |
| assetHandle | `xsd:string` | Oui | Gérer vers la ressource image. |
| pathName | `xsd:string` | Oui | Nom du chemin d’accès Photoshop à renvoyer. |

**Output (getPhotoshopPathReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| perspectiveQuad | `types:PerspectiveQuad` | Oui | Renvoie les coordonnées de l’image en fonction du chemin d’accès. Voir [PerspectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204). |

## Exemples {#section-1f0461cbdc184c8d8925336d5279db47}

**Requête**

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
>* [PerspectiveQuad ](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204)

