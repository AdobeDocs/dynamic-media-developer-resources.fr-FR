---
description: Remplace les données d’image d’une ressource image.
solution: Experience Manager
title: replaceImage
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: bf8c1f5c-7829-4750-b5b7-b8b20d115d17
TQID: 'https://experienceleague.adobe.com/11bWPLId2s4gOVhiIFr93Ca4D-7SJ0PYHFmiSKtStjk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 14%

---

# replaceImage{#replaceimage}

Remplace les données d’image d’une ressource image.

Syntaxe

## Types d’utilisateurs autorisés {#section-e2aad71fb2a54612badc7b16f82ed544}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-0d0ab668fa6d4310a93fb7ef8d8dd1e0}

**Input (replaceImageParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyName | `xsd:string` | Oui | Poignée de la société contenant l’image à remplacer. |
| assetHandle | `xsd:string` | Oui | Poignée de la ressource à remplacer. |
| urlModifier | `xsd:string` | Oui | Commandes du serveur d’images qui génèrent de nouvelles données d’image. |

**Output (replaceImageReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| assetHandle | `xsd:string` | Oui | Gérer vers la nouvelle ressource. |

## Exemples {#section-cebb93576bde4cb98cb27356ca66783b}

Cet exemple de code remplace une image et applique une `urlModifier` avec une commande qui spécifie que le serveur d’images ne doit rien faire lors du remplacement.

**Requête**

```java
<replaceImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|140626|1|102524</assetHandle>
   <urlModifier>action=none</urlModifier>
</replaceImageParam>
```

**Réponse**

```java
<replaceImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|140626|1|102524</assetHandle>
</replaceImageReturn>
```

