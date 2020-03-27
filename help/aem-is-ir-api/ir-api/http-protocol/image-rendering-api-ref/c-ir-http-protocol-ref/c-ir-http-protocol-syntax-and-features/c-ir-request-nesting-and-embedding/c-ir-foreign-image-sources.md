---
description: Image Serving prend en charge l’accès aux images source sur les serveurs HTTP et FTP étrangers.
seo-description: Image Serving prend en charge l’accès aux images source sur les serveurs HTTP et FTP étrangers.
seo-title: Sources d’images étrangères
solution: Experience Manager
title: Sources d’images étrangères
topic: Scene7 Image Serving - Image Rendering API
uuid: 28a17400-4807-4e14-937a-80309be53d55
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Sources d’images étrangères{#foreign-image-sources}

Image Serving prend en charge l’accès aux images source sur les serveurs HTTP et FTP étrangers.

Pour spécifier une URL étrangère pour une `src=` commande ou une `mask=` commande ; délimitez simplement l’intégralité de l’URL incorporée par des accolades :

` …&src={ *[!DNL foreignUrl]*}&…`

Les URL absolues complètes (si `attribute::AllowDirectUrls` elles sont définies) et les URL relatives à `attribute::RootUrl` sont autorisées. Une erreur se produit si une URL absolue est incorporée et un attribut : `AllowDirectUrls` est 0 ou si une URL relative est spécifiée et `attribute::RootUrl` est vide.

Les images étrangères sont mises en cache par le serveur en fonction des en-têtes de mise en cache inclus dans la réponse HTTP.
