---
description: Mode d’image par défaut. Sélectionne le mode d’application de l’image par défaut lorsque les images spécifiées dans la requête sont introuvables.
solution: Experience Manager
title: DefaultImageMode
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b30ce72f-7c74-407c-bd4a-042b84c469e9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 2%

---

# DefaultImageMode{#defaultimagemode}

Mode d’image par défaut. Sélectionne le mode d’application de l’image par défaut lorsque les images spécifiées dans la requête sont introuvables.

## Propriétés {#section-7fa8acb63540490d9f5186231b5e77c3}

Énumération. &#39;0&#39; pour remplacer l&#39;image composite entière, même si l&#39;image manquante n&#39;est qu&#39;un calque parmi plusieurs ; &#39;1&#39; pour remplacer chaque image source de calque manquante par l&#39;image par défaut et renvoyer l&#39;image composite comme d&#39;habitude.

## Restrictions {#section-04cb0d50e8914564a8d226d0d4663c8b}

La diffusion d’images revient à la `DefaultImageMode=0` lorsque le rendu d’images imbriquées, le FXG ou les requêtes `req=set` échouent.

## Par défaut {#section-9e318524a2a5496386901286748c7ee7}

Hérité de `default::DefaultImage` si non défini ou si vide.

## Voir aussi {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) , [attribute::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
