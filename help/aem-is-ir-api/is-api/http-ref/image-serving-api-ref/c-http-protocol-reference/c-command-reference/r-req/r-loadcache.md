---
description: Précharger le cache du serveur. Exécute la requête comme req=img, mais au lieu de renvoyer l’image, le serveur renvoie la longueur de l’image de réponse (image.length), formatée en tant que données de texte avec le type MIME text/plain.
solution: Experience Manager
title: loadcache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 653842e9-bed1-462a-bb1f-39ac1ac9512c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# loadcache{#loadcache}

Précharger le cache du serveur. Exécute la requête comme req=img, mais au lieu de renvoyer l’image, le serveur renvoie la longueur de l’image de réponse (image.length), formatée en tant que données de texte avec le type MIME text/plain.

`req=loadcache`

La réponse HTTP ne peut pas être mise en cache.

D’autres commandes de la requête s’appliquent comme documentées.
