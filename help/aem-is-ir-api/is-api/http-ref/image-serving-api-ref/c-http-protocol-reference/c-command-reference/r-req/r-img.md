---
description: Image (par défaut). Demande les données d’image standard.
seo-description: Image (par défaut). Demande les données d’image standard.
seo-title: img
solution: Experience Manager
title: img
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 4809f916-0ccf-4a24-a93b-c51ed6203061
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 16%

---


# img{#img}

Image (par défaut). Demande les données d’image standard.

`req=img`

Le format des données de réponse et le type MIME de réponse sont déterminés par `fmt=`. `req=img` est le type de requête par défaut et ne doit pas être spécifié explicitement. La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::Expiration`.

D’autres commandes de requête sont appliquées comme documentées.
