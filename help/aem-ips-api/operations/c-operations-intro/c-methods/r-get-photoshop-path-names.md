---
description: Renvoie un tableau de noms de chemin Photoshop pour l’image donnée.
solution: Experience Manager
title: getPhotoshopPathNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 11d4c0d0-a3a3-4324-a4a6-1dd7b7e673da
TQID: 'https://experienceleague.adobe.com/BxFBNXpa9ilc4lXeXiuuvCQb9ChImZWt13-pJ3b3osk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 77
ht-degree: 18%

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

**Input (getPhotoshopPathNamesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gérer vers la société qui contient l’image que vous souhaitez utiliser. |
| assetHandle | `xsd:string` | Oui | Gérer vers la ressource image. |

**Output (getPhotoshopPathNamesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| pathNameArray | `types:StringArray` | Oui | Tableau de noms de chemin Photoshop dans une image. |

## Exemples {#section-6d316f14b4184d42af4ca3f717b042dd}

**Requête**

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

