---
description: Utilisez ces paramètres de serveur pour définir les limites de taille d’image.
solution: Experience Manager
title: Limitations de taille d’image
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---


# Limites de taille d’image{#image-size-limits}

Utilisez ces paramètres de serveur pour définir les limites de taille d’image.

## IS::MaxMessageSize - Limite de taille de réponse {#section-bd942385d4d144cd904003695d72c85e}

Limite la taille des données que le serveur Image Server est autorisé à envoyer au serveur de plateformes. En effet, cela limite la taille de l’image de réponse codée/compressée que la diffusion d’images peut renvoyer au client via HTTP (Mbytes).

## IS::MaxRenderRgnPixels - Limite de la taille de l’image de sortie {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Limite la taille des images que le serveur Image Server peut produire (à l’exclusion des images enregistrées dans le fichier). Valeur entière supérieure à 0 en millions de pixels. Une erreur est renvoyée si une opération de rendu dépasse la limite de taille. Valeur par défaut : 16.

## IS::MaxSavePixels - Limite de taille pour l&#39;enregistrement dans des fichiers {#section-d1547c4afa88467080ab08356f775e06}

Limite la taille des images que le serveur d’images écrira dans les fichiers à l’aide de la commande `req=saveToFile`. Valeur entière supérieure à 0 en millions de pixels. Une erreur est renvoyée si l&#39;opération d&#39;enregistrement de fichier dépasse cette limite. La valeur par défaut est de 100 millions de pixels.

## IS::MaxNonDsfSize - Taille Limite Pour Les Images D’Entrée Non PTIFF {#section-50de28a7158a436393cce5da0d1e4d46}

Taille maximale (en pixels) des images qui ne sont pas des fichiers PTIFF que le serveur d’images est autorisé à ouvrir. La diffusion d’images renvoie une erreur lorsqu’une tentative d’accès à une image non-PTIFF est plus importante que cette limite.

>[!NOTE]
>
>Si cette valeur est trop élevée, le serveur d’images risque d’être saturé de mémoire et de provoquer des échecs, notamment des blocages.

