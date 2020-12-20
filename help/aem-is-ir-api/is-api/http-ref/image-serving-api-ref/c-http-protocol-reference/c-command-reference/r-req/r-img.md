---
description: Image (par défaut). Demande les données d’image standard.
seo-description: Image (par défaut). Demande les données d’image standard.
seo-title: img
solution: Experience Manager
title: img
topic: Scene7 Image Serving - Image Rendering API
uuid: 4809f916-0ccf-4a24-a93b-c51ed6203061
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 16%

---


# img{#img}

Image (par défaut). Demande les données d’image standard.

`req=img`

Le format des données de réponse et le type MIME de réponse sont déterminés par `fmt=`. `req=img` est le type de requête par défaut et ne doit pas être spécifié explicitement. La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::Expiration`.

D’autres commandes de requête sont appliquées comme documentées.
