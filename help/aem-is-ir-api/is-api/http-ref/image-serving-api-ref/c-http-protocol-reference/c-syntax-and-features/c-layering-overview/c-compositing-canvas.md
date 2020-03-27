---
description: Les calques sont composés dans l’ordre spécifié par la commande layer=, où les calques à numéro supérieur masquent les calques à numéro inférieur.
seo-description: Les calques sont composés dans l’ordre spécifié par la commande layer=, où les calques à numéro supérieur masquent les calques à numéro inférieur.
seo-title: La toile de composition
solution: Experience Manager
title: La toile de composition
topic: Scene7 Image Serving - Image Rendering API
uuid: 057b11cb-36f3-40f8-b095-9ad05da858a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# La toile de composition{#the-compositing-canvas}

Les calques sont composés dans l’ordre spécifié par la commande layer=, où les calques à numéro supérieur masquent les calques à numéro inférieur.

Le calque 0 constitue le calque d’arrière-plan, qui est toujours requis et qui définit la taille de l’image composite. Tous les types de calque sont autorisés pour le calque 0. La taille du calque 0 doit être définie, explicitement à l’aide `size=` ou implicitement, en fonction de l’image ou du texte du contenu. Les zones d’autres calques situées en dehors de la zone du calque 0 ne seront pas incluses dans l’image de sortie.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Une fois tous les calques aplatis, l’image composite est convertie en image de réponse finale, comme spécifié avec les commandes et les attributs [de ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).

