---
description: Utilisez ces paramètres de serveur pour définir les limites de taille d’image.
solution: Experience Manager
title: Limites de taille d’image
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 75ec58ee-8c98-46cb-96b2-79d1c32e576f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# Limites de taille d’image{#image-size-limits}

Utilisez ces paramètres de serveur pour définir les limites de taille d’image.

## IS::MaxMessageSize - Limite de taille de la réponse {#section-bd942385d4d144cd904003695d72c85e}

Limite la taille des données que le serveur d’images est autorisé à envoyer au serveur Platform. En fait, cela limite la taille de l’image de réponse codée/compressée que le serveur d’images peut renvoyer au client via HTTP (mégaoctets).

## IS::MaxRenderRgnPixels - Limite de taille de l’image de sortie {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Limite la taille des images que le serveur d’images peut produire (à l’exception des images enregistrées dans le fichier). Valeur entière supérieure à 0 en millions de pixels. Une erreur est renvoyée si une opération de rendu dépasse la limite de taille. Valeur par défaut : 16.

## IS::MaxSavePixels - Limite de taille pour l’enregistrement dans les fichiers {#section-d1547c4afa88467080ab08356f775e06}

Limite la taille des images que le serveur d’images écrira dans les fichiers avec la commande `req=saveToFile`. Valeur entière supérieure à 0 en millions de pixels. Une erreur est renvoyée si l’opération d’enregistrement de fichier dépasse cette limite. La valeur par défaut est de 100 millions de pixels.

## IS::MaxNonDsfSize - Taille Limite Pour Les Images D’Entrée Non PTIFF {#section-50de28a7158a436393cce5da0d1e4d46}

Taille maximale (en pixels) des images qui ne sont pas des fichiers PTIFF que le serveur d’images est autorisé à ouvrir. La diffusion d’images renvoie une erreur lorsqu’une tentative d’accès à une image non PTIFF est supérieure à cette limite.

>[!NOTE]
>
>Si vous définissez cette valeur sur une valeur trop élevée, le serveur d’images risque de manquer de mémoire et d’entraîner des échecs, notamment des blocages.
