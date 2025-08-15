---
description: Utilisez ces paramètres du serveur pour définir les limites de taille des images.
solution: Experience Manager
title: Limites de taille des images
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 75ec58ee-8c98-46cb-96b2-79d1c32e576f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 1%

---

# Limites de taille des images{#image-size-limits}

Utilisez ces paramètres du serveur pour définir les limites de taille des images.

## IS::MaxMessageSize - Limite de taille de réponse {#section-bd942385d4d144cd904003695d72c85e}

Limite la taille des données que le serveur d’images est autorisé à envoyer au [!DNL Platform Server]. En effet, cela limite la taille de l’image de réponse codée/compressée que la diffusion d’images peut renvoyer au client au moyen du protocole HTTP (Mo).

## IS::MaxRenderRgnPixels - Limite de taille d’image en sortie {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Limite la taille des images que le serveur d’images peut produire (à l’exclusion des images enregistrées dans un fichier). Valeur entière supérieure à 0 en millions de pixels. Une erreur est renvoyée si une opération de rendu dépasse la limite de taille. Par défaut : 16.

## IS::MaxSavePixels - Limite de taille pour l’enregistrement dans les fichiers {#section-d1547c4afa88467080ab08356f775e06}

Limite la taille des images que le serveur d’images écrit dans les fichiers avec la commande `req=saveToFile`. Valeur entière supérieure à 0 en millions de pixels. Une erreur est renvoyée si l’opération d’enregistrement du fichier dépasse cette limite. La valeur par défaut est de 100 millions de pixels.

## IS::MaxNonDsfSize - Limite de taille pour les images d’entrée non PTIFF {#section-50de28a7158a436393cce5da0d1e4d46}

Taille maximale (en Mpixels) des images qui ne sont pas des PTIFF que le serveur d’images est autorisé à ouvrir. La diffusion d’images renvoie une erreur lorsqu’une tentative d’accès à une image non PTIFF supérieure à cette limite est effectuée.

>[!NOTE]
>
>Si vous définissez une valeur trop élevée, le serveur d’images risque de manquer de mémoire et d’entraîner des échecs, notamment des blocages.
