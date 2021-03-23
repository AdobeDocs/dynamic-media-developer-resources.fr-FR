---
description: Remplace les données d’image d’un fichier d’image.
seo-description: Remplace les données d’image d’un fichier d’image.
seo-title: replaceImage
solution: Experience Manager
title: replaceImage
uuid: 46824e33-265c-4425-9ab1-8ad6b7ac154d
feature: Dynamic Media Classic, SDK/API, Gestion des ressources
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 14%

---


# replaceImage{#replaceimage}

Remplace les données d’image d’un fichier d’image.

Syntaxe

## Types d’utilisateur autorisés {#section-e2aad71fb2a54612badc7b16f82ed544}

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
| `*`companyName`*` | `xsd:string` | Oui | Poignée de la société contenant l&#39;image à remplacer. |
| `*`assetHandle`*` | `xsd:string` | Oui | Poignée de la ressource à remplacer. |
| `*`urlModificateur`*` | `xsd:string` | Oui | Commandes du serveur d’images qui génèrent de nouvelles données d’image. |

**Output (replaceImageReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Oui | Gérer vers la nouvelle ressource. |

## Exemples {#section-cebb93576bde4cb98cb27356ca66783b}

Cet exemple de code remplace une image et applique une commande `urlModifier` avec une commande qui spécifie que le serveur d’images n’agira pas lors du remplacement.

**Request**

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

