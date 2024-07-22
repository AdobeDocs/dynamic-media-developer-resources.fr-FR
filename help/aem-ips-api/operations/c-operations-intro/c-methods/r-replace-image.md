---
description: Remplace les données image d’une ressource image.
solution: Experience Manager
title: replaceImage
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: bf8c1f5c-7829-4750-b5b7-b8b20d115d17
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 14%

---

# replaceImage{#replaceimage}

Remplace les données image d’une ressource image.

Syntaxe

## Types d’utilisateurs autorisés {#section-e2aad71fb2a54612badc7b16f82ed544}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-0d0ab668fa6d4310a93fb7ef8d8dd1e0}

**Entrée (replaceImageParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyName | `xsd:string` | Oui | Gestionnaire de l’entreprise avec l’image que vous souhaitez remplacer. |
| assetHandle | `xsd:string` | Oui | Gestionnaire de la ressource à remplacer. |
| urlModifier | `xsd:string` | Oui | Commandes du serveur d’images qui génèrent de nouvelles données d’image. |

**Sortie (replaceImageReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| assetHandle | `xsd:string` | Oui | Traitement de la nouvelle ressource. |

## Exemples {#section-cebb93576bde4cb98cb27356ca66783b}

Cet exemple de code remplace une image et applique une commande `urlModifier` qui spécifie que le serveur d’images ne prend aucune action lors du remplacement.

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
