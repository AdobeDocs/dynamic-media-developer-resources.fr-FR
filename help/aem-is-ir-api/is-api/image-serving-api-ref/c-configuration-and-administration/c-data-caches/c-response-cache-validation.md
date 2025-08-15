---
description: Les entrées de cache sont actualisées automatiquement à l’aide de la validation du cache basée sur le catalogue ou sur l’expiration, comme sélectionné avec l’attribut CacheValidationPolicy (dans default.ini ou le fichier .ini d’un catalogue d’images spécifique).
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

Les entrées de cache sont actualisées automatiquement à l’aide de la validation du cache basée sur le catalogue ou sur l’expiration, comme sélectionné avec attribute ::CacheValidationPolicy (dans default.ini ou le fichier .ini d’un catalogue d’images spécifique).

Avec la validation basée sur un catalogue, une entrée de cache existante est considérée comme obsolète si `catalog::LastModified` (ou `attribute::LastModified`, ou l’heure de modification du fichier du fichier) est plus récente que l’heure de création de l’entrée de [!DNL catalog.ini] cache.

Avec la validation basée sur l’expiration, une entrée de cache devient obsolète après 5 minutes depuis la validation la plus récente. Dans les deux cas, le serveur valide les entrées de cache obsolètes en vérifiant les dates de fichier de tous les fichiers image impliqués dans la création de la demande. Si les dates du fichier n’ont pas changé, l’horodatage de l’entrée de cache est mis à jour et la date mise en cache est considérée comme valide.

Pour les applications typiques qui impliquent principalement des images enregistrées dans des catalogues d’images, la validation basée sur un catalogue offre un avantage en termes de performances. Les applications qui n’impliquent pas de catalogues d’images doivent utiliser la validation du cache basée sur l’expiration. Pour ce faire `attribute::cacheValidationPolicy=0` , définissez dans [!DNL default.ini]et dans tous les fichiers spécifiques du catalogue d’images `1` .

Les entrées de cache deviennent non valides et peuvent être régénérées lorsqu’une entrée de catalogue impliquée dans la demande change d’une manière susceptible d’entraîner une modification de l’image de réponse. par exemple, le contenu des `catalog::Modifier` modifications.

>[!NOTE]
>
>Dynamic Media images TIFF (PTIFF) pyramidales conservent la date du fichier en interne dans l’en-tête du fichier à des fins de validation. Le temps de modification du fichier conservé par le système de fichiers est utilisé pour vérifier si un fichier non-PTIFF a changé.

Seuls les fichiers image participent au processus de validation du cache. Les modifications apportées aux fichiers de polices ou aux fichiers de profil ICC n’entraînent pas l’invalidation automatique des entrées du cache.
