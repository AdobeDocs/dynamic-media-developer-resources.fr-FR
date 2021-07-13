---
description: Image (par défaut). Demande les données d’image standard.
solution: Experience Manager
title: img
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 5338358e-755b-41d6-a941-8754d0deb9aa
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 16%

---

# img{#img}

Image (par défaut). Demande les données d’image standard.

`req=img`

Le format des données de réponse et le type MIME de réponse sont déterminés par `fmt=`. `req=img` est le type de requête par défaut et ne doit pas être spécifié explicitement. La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::Expiration`.

D’autres commandes de requête sont appliquées comme documentées.
