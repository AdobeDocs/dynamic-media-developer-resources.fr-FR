---
description: Mode d’image par défaut. Sélectionne le mode d’application de l’image par défaut lorsque les images spécifiées dans la requête sont introuvables.
seo-description: Mode d’image par défaut. Sélectionne le mode d’application de l’image par défaut lorsque les images spécifiées dans la requête sont introuvables.
seo-title: DefaultImageMode
solution: Experience Manager
title: DefaultImageMode
topic: Scene7 Image Serving - Image Rendering API
uuid: e5640f09-e1e3-473b-8fbc-84c6bfce2460
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DefaultImageMode{#defaultimagemode}

Mode d’image par défaut. Sélectionne le mode d’application de l’image par défaut lorsque les images spécifiées dans la requête sont introuvables.

## Propriétés {#section-7fa8acb63540490d9f5186231b5e77c3}

Enum. &quot;0&quot; pour remplacer l’image composite entière, même si l’image manquante n’est qu’un calque parmi plusieurs ; &quot;1&quot; pour remplacer chaque image source de calque manquante par l’image par défaut et renvoyer le composite comme d’habitude.

## Restrictions {#section-04cb0d50e8914564a8d226d0d4663c8b}

La diffusion d’images revient à `DefaultImageMode=0` lorsque le rendu d’image imbriqué, le fichier FXG ou les `req=set` demandes échouent.

## Par défaut {#section-9e318524a2a5496386901286748c7ee7}

Héritée de `default::DefaultImage` si non définie ou si vide.

## Voir aussi {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) , [attribut::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
