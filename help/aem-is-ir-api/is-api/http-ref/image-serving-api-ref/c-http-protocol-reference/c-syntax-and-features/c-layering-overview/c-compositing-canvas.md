---
description: Les calques sont composés dans l’ordre spécifié par la commande layer=, où les calques à numéro supérieur masquent les calques à numéro inférieur.
solution: Experience Manager
title: La trame de composition
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# Canevas de composition {#the-compositing-canvas}

Les calques sont composés dans l’ordre spécifié par la commande layer=, où les calques à numéro supérieur masquent les calques à numéro inférieur.

La couche 0 constitue la couche d’arrière-plan, qui est toujours requise et qui définit la taille de l’image composite. Tous les types de calque sont autorisés pour le calque 0. La taille du calque 0 doit être définie, soit explicitement à l’aide de `size=`, soit implicitement, en fonction de l’image ou du texte du contenu. Les zones d’autres calques situées en dehors de la zone du calque 0 ne seront pas incluses dans l’image de sortie.

>[!NOTE]
>
>Une fois tous les calques aplatis, l’image composite est convertie en image de réponse finale, comme indiqué dans les commandes et attributs [de vue ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).

