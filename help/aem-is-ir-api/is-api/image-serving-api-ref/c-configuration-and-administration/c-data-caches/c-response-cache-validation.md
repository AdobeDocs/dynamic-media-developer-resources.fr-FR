---
description: Les entrées de cache sont actualisées automatiquement à l’aide de la validation du cache basée sur un catalogue ou sur l’expiration, comme sélectionné avec l’attribut CacheValidationPolicy (dans default.ini ou le fichier .ini d’un catalogue d’images spécifique).
solution: Experience Manager
title: Validation du cache de réponse
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# Validation du cache de réponse{#response-cache-validation}

Les entrées de cache sont actualisées automatiquement à l’aide de la validation du cache basée sur un catalogue ou sur l’expiration, comme sélectionné avec l’attribut::CacheValidationPolicy (dans default.ini ou le fichier .ini d’un catalogue d’images spécifique).

Avec la validation basée sur un catalogue, une entrée de cache existante est considérée comme obsolète si `catalog::LastModified` (ou `attribute::LastModified`, ou l’heure de modification du fichier [!DNL catalog.ini]) est plus récente que l’heure de création de l’entrée de cache.

Avec la validation basée sur l’expiration, une entrée de cache devient obsolète après 5 minutes depuis la validation la plus récente. Dans les deux cas, le serveur valide les entrées de cache obsolètes en vérifiant les dates des fichiers de tous les fichiers image impliqués dans la création de la requête. Si les dates du fichier ne sont pas modifiées, l’horodatage de l’entrée du cache est mis à jour et la date mise en cache est considérée comme valide.

Pour les applications standard qui impliquent principalement des images enregistrées dans des catalogues d’images, la validation basée sur un catalogue offre un avantage en termes de performances. Les applications qui n’impliquent pas de catalogues d’images doivent utiliser la validation du cache basée sur l’expiration. Pour ce faire, définissez `attribute::cacheValidationPolicy=0` dans [!DNL default.ini] et `1` dans tous les fichiers de catalogue d’images spécifiques.

Les entrées de cache deviennent non valides et peuvent être regénérées lorsqu’une entrée de catalogue impliquée dans la requête change d’une manière qui provoquerait probablement un changement de l’image de réponse. Par exemple, le contenu de `catalog::Modifier` change.

>[!NOTE]
>
>Les images PTIFF (Dynamic Media pyramid TIFF) conservent la date du fichier en interne dans l’en-tête du fichier à des fins de validation. L’heure de modification des fichiers conservée par le système de fichiers est utilisée pour vérifier si un fichier non PTIFF a changé.

Seuls les fichiers image participent au processus de validation du cache. Les modifications apportées aux fichiers de police ou de profil ICC ne provoquent pas l’invalidation automatique des entrées de cache.
