---
title: ErrorImage
description: Image de réponse d’erreur. Le rendu d’image renvoie normalement un statut d’erreur avec un message texte lorsqu’une erreur se produit.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
TQID: 'https://experienceleague.adobe.com/RRWlVPBpoUXafivRlOtzZoe5vExwnRB409SCOwhSRJI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 1%

---

# ErrorImage {#errorimage}

Image de réponse d’erreur. Le rendu d’image renvoie normalement un statut d’erreur avec un message texte lorsqu’une erreur se produit. Le `attribute::ErrorImage` permet de renvoyer une image de configuration en cas d&#39;erreur.

Lorsqu’une erreur se produit, le serveur tente d’interpréter la valeur de `ImageRendering::attribute::ErrorImage`comme un simple chemin d’accès au fichier image. Si le fichier ne peut pas être ouvert, il envoie la valeur d’attribut et les détails de l’erreur au service d’images, qui effectue le traitement comme décrit dans la section `ImageServing::attribute::ErrorImage`. Si la diffusion d’images ne renvoie pas d’image de réponse valide, le statut d’erreur HTTP standard et le message texte sont envoyés au client.

Les images d’erreur sont renvoyées avec le statut HTTP 200.

## Propriétés {#section-4a4a7e37ed11483db0b9922dc68ea7db}

Chaîne de texte. S’il est spécifié, il doit s’agir d’une valeur **`ImageServing::catalog::id`**, d’un chemin relatif (vers **`ImageServing::attribute::RootPath`** ou **`ImageRendering::attribute::RootPath`**) ou d’un chemin absolu vers un fichier image accessible par le serveur d’images.

## Par défaut {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

Hérité de `default::ErrorImage` s’il n’est pas défini. S’il est défini mais vide, le comportement d’image d’erreur est désactivé, même si `default::ErrorImage` est défini et un statut d’erreur HTTP est renvoyé.

## Voir aussi {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3), [catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)

