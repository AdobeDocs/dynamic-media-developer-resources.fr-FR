---
description: Supprime un format d’image. Récupérez la poignée de format d'image à partir de saveImageFormat.
seo-description: Supprime un format d’image. Récupérez la poignée de format d'image à partir de saveImageFormat.
seo-title: deleteImageFormat
solution: Experience Manager
title: deleteImageFormat
topic: Dynamic Media Image Production System API
uuid: 70dddde9-830b-4267-8ef5-df5241f549e3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 10%

---


# deleteImageFormat{#deleteimageformat}

Supprime un format d’image. Récupérez la poignée de format d&#39;image à partir de saveImageFormat.

Syntaxe

## Types d’utilisateur autorisés {#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-462c05d9aad746ee8d2be0656041b693}

**Entrée (deleteImageFormatParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société contenant le format d’image à supprimer. |
| `*`imageFormatHandle`*` | `xsd:string` | Oui | Poignée du format d’image à supprimer. |

**Output (deleteImageFormatParam)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

Cet exemple de code supprime un format d’image d’une société. Récupérez la poignée de format d’image à partir d’une autre opération.

**Request**

```java
<deleteImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageFormatHandle>47|301</imageFormatHandle>
</deleteImageFormatParam>
```

**Réponse**

Aucune

**Rubrique connexe :**

[saveImageFormat](../../../operations/c-operations-intro/c-methods/r-save-image-format.md#reference-d15c27f533ef41e38b54a539a304bd1d)
