---
description: Supprime un format d’image. Obtenez la poignée du format d’image à partir de saveImageFormat.
solution: Experience Manager
title: deleteImageFormat
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: bd717c08-6da4-47f1-8614-e4ba79d8176c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 11%

---

# deleteImageFormat{#deleteimageformat}

Supprime un format d’image. Obtenez la poignée du format d’image à partir de saveImageFormat.

Syntaxe

## Types d’utilisateurs autorisés {#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-462c05d9aad746ee8d2be0656041b693}

**Entrée (deleteImageFormatParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Gestionnaire de l’entreprise qui contient le format d’image que vous souhaitez supprimer. |
| `*`imageFormatHandle`*` | `xsd:string` | Oui | Gestion du format d’image que vous souhaitez supprimer. |

**Sortie (deleteImageFormatParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

Cet exemple de code supprime un format d’image d’une société. Récupérez la gestion du format d’image à partir d’une autre opération.

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
