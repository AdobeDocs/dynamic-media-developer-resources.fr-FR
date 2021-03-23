---
description: La diffusion d’images prend en charge l’accès aux images source sur les serveurs HTTP et FTP étrangers.
seo-description: La diffusion d’images prend en charge l’accès aux images source sur les serveurs HTTP et FTP étrangers.
seo-title: Sources d’images étrangères
solution: Experience Manager
title: Sources d’images étrangères
uuid: 28a17400-4807-4e14-937a-80309be53d55
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# Sources d’image étrangères{#foreign-image-sources}

La diffusion d’images prend en charge l’accès aux images source sur les serveurs HTTP et FTP étrangers.

Pour spécifier une URL étrangère pour une commande `src=` ou `mask=` ; délimitez simplement l’intégralité de l’URL incorporée par des accolades :

` …&src={ *[!DNL foreignUrl]*}&…`

Les URL absolues complètes (si `attribute::AllowDirectUrls` est défini) et les URL relatives à `attribute::RootUrl` sont autorisées. Une erreur se produit si une URL absolue est incorporée et que l’attribut : `AllowDirectUrls` est 0 ou si une URL relative est spécifiée et `attribute::RootUrl` est vide.

Les images étrangères sont mises en cache par le serveur en fonction des en-têtes de mise en cache inclus dans la réponse HTTP.
