---
description: Supprime un format d’image. Récupérez la poignée de format d’image à partir de saveImageFormat.
solution: Experience Manager
title: deleteImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bd717c08-6da4-47f1-8614-e4ba79d8176c
TQID: 'https://experienceleague.adobe.com/BOhXqXdUG6BUA9VsI9faDIeRfdCwlqYsj6sqS-uQ330'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 102
ht-degree: 9%

---

# deleteImageFormat{#deleteimageformat}

Supprime un format d’image. Récupérez la poignée de format d’image à partir de saveImageFormat.

Syntaxe

## Types d’utilisateurs autorisés {#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-462c05d9aad746ee8d2be0656041b693}

**Input (deleteImageFormatParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Descripteur de la société qui contient le format d’image à supprimer. |
| imageFormatHandle | `xsd:string` | Oui | Poignée du format d’image à supprimer. |

**Output (deleteImageFormatParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

Cet exemple de code supprime un format d’image d’une société. Récupérez l’identificateur de format d’image à partir d’une autre opération.

**Requête**

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
