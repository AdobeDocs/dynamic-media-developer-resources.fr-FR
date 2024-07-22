---
title: Sources d’image étrangères
description: La diffusion d’images prend en charge l’accès aux images source sur les serveurs HTTP et FTP étrangers.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# Sources d’image étrangères{#foreign-image-sources}

La diffusion d’images prend en charge l’accès aux images source sur les serveurs HTTP et FTP étrangers.

Pour spécifier une URL étrangère pour une commande `src=` ou `mask=`, délimitez simplement l’URL entière incorporée par des accolades :

` …&src={ *[!DNL foreignUrl]*}&…`

Les URL absolues complètes (si `attribute::AllowDirectUrls` est défini) et les URL relatives à `attribute::RootUrl` sont autorisées. Une erreur se produit si une URL absolue est incorporée et l’attribut : `AllowDirectUrls` est 0 ou si une URL relative est spécifiée et `attribute::RootUrl` est vide.

Les images étrangères sont mises en cache par le serveur en fonction des en-têtes de mise en cache inclus dans la réponse HTTP.
