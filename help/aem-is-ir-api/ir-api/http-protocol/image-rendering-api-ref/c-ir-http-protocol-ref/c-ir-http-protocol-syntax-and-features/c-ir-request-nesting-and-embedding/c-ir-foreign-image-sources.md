---
description: La diffusion d’images prend en charge l’accès aux images source sur les serveurs HTTP et FTP étrangers.
solution: Experience Manager
title: Sources d’images étrangères
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# Sources d’image étrangères{#foreign-image-sources}

La diffusion d’images prend en charge l’accès aux images source sur les serveurs HTTP et FTP étrangers.

Pour spécifier une URL étrangère pour une commande `src=` ou `mask=` ; délimitez simplement l’intégralité de l’URL incorporée par des accolades :

` …&src={ *[!DNL foreignUrl]*}&…`

Les URL absolues complètes (si `attribute::AllowDirectUrls` est défini) et les URL relatives à `attribute::RootUrl` sont autorisées. Une erreur se produit si une URL absolue est incorporée et que l’attribut : `AllowDirectUrls` est 0 ou si une URL relative est spécifiée et `attribute::RootUrl` est vide.

Les images étrangères sont mises en cache par le serveur en fonction des en-têtes de mise en cache inclus dans la réponse HTTP.
