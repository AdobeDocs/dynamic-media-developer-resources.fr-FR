---
description: Les calques sont composés dans l’ordre spécifié par la commande layer= , où les calques dont les numéros sont supérieurs masquent les calques dont les numéros sont inférieurs.
solution: Experience Manager
title: Zone de travail de composition
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
TQID: 'https://experienceleague.adobe.com/WNvq6dLRetz3iEbtP0ugmOPagUfTCaa5eXdB3lEzEaQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 136
ht-degree: 0%

---

# Zone de travail de composition{#the-compositing-canvas}

Les calques sont composés dans l’ordre spécifié par la commande layer= , où les calques dont les numéros sont supérieurs masquent les calques dont les numéros sont inférieurs.

La couche 0 constitue la couche de fond qui est toujours nécessaire et qui définit la taille de l&#39;image composite. Tous les types de calque sont autorisés pour le calque 0. La taille du calque 0 doit être définie, soit explicitement à l’aide de `size=`, soit implicitement, en fonction de l’image ou du texte du contenu. Les zones des autres calques qui se trouvent en dehors de la zone du calque 0 ne sont pas incluses dans l&#39;image de sortie.

>[!NOTE]
>
>Une fois tous les calques aplatis, l’image composite est convertie en image de réponse finale, comme indiqué avec les commandes et attributs [view](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).
