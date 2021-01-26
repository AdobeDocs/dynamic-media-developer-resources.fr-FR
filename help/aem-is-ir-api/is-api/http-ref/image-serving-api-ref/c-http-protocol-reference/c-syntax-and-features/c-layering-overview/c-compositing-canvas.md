---
description: Les calques sont composés dans l’ordre spécifié par la commande layer=, où les calques à numéro supérieur masquent les calques à numéro inférieur.
seo-description: Les calques sont composés dans l’ordre spécifié par la commande layer=, où les calques à numéro supérieur masquent les calques à numéro inférieur.
seo-title: La trame de composition
solution: Experience Manager
title: La trame de composition
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 057b11cb-36f3-40f8-b095-9ad05da858a9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# Canevas de composition {#the-compositing-canvas}

Les calques sont composés dans l’ordre spécifié par la commande layer=, où les calques à numéro supérieur masquent les calques à numéro inférieur.

La couche 0 constitue la couche d’arrière-plan, qui est toujours requise et qui définit la taille de l’image composite. Tous les types de calque sont autorisés pour le calque 0. La taille du calque 0 doit être définie, soit explicitement à l’aide de `size=`, soit implicitement, en fonction de l’image ou du texte du contenu. Les zones d’autres calques situées en dehors de la zone du calque 0 ne seront pas incluses dans l’image de sortie.

>[!NOTE]
>
>Une fois tous les calques aplatis, l’image composite est convertie en image de réponse finale, comme indiqué dans les commandes et attributs [de vue ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).

