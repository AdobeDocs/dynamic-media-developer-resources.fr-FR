---
description: Les calques sont composés dans l’ordre spécifié par la commande layer=, où les calques à numéro supérieur masquent les calques à numéro inférieur.
solution: Experience Manager
title: La zone de travail du compositeur
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# La zone de travail du compositeur{#the-compositing-canvas}

Les calques sont composés dans l’ordre spécifié par la commande layer=, où les calques à numéro supérieur masquent les calques à numéro inférieur.

Le calque 0 constitue la couche d’arrière-plan, qui est toujours requise et qui définit la taille de l’image composite. Tous les types de calques sont autorisés pour le calque 0. La taille du calque 0 doit être définie, explicitement à l’aide de `size=` ou implicitement, en fonction de l’image ou du texte du contenu. Les zones des autres calques qui se trouvent en dehors de la zone du calque 0 ne sont pas incluses dans l’image de sortie.

>[!NOTE]
>
>Une fois tous les calques aplatis, l’image composite est convertie en image de réponse finale, comme spécifié avec les [commandes d’affichage et attributs](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).
