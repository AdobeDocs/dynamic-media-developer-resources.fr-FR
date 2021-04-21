---
description: Les entrées de cache sont automatiquement actualisées à l’aide de la validation du cache basée sur un catalogue ou basée sur l’expiration, telle que sélectionnée avec l’attribut CacheValidationPolicy (dans default.ini ou le fichier .ini d’un catalogue d’images spécifique).
solution: Experience Manager
title: Validation du cache de réponse
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---


# Validation du cache de réponse{#response-cache-validation}

Les entrées de cache sont automatiquement actualisées à l’aide de la validation du cache basée sur le catalogue ou sur l’expiration, telle que sélectionnée avec attribut::CacheValidationPolicy (dans default.ini ou le fichier .ini d’un catalogue d’images spécifique).

Avec la validation basée sur un catalogue, une entrée de cache existante est considérée comme obsolète si `catalog::LastModified` (ou `attribute::LastModified`, ou l&#39;heure de modification du fichier [!DNL catalog.ini]) est plus récente que la date de création de l&#39;entrée de cache.

Avec la validation basée sur l’expiration, une entrée de cache devient obsolète après 5 minutes depuis la validation la plus récente. Dans les deux cas, le serveur valide les entrées de cache obsolètes en vérifiant les dates des fichiers de toutes les images impliquées dans la création de la demande. Si les dates du fichier n’ont pas changé, l’horodatage de l’entrée de cache est mis à jour et la date mise en cache est considérée comme valide.

Pour les applications courantes qui impliquent principalement des images enregistrées dans des catalogues d’images, la validation basée sur un catalogue offre un avantage en termes de performances. Les applications qui n’impliquent pas les catalogues d’images doivent utiliser la validation du cache basée sur l’expiration. Pour ce faire, il est possible de définir `attribute::cacheValidationPolicy=0` dans [!DNL default.ini] et `1` dans tous les fichiers de catalogue d’images spécifiques.

Les entrées de cache deviennent non valides et peuvent être regénérées lorsqu’une entrée de catalogue impliquée dans la demande change d’une manière susceptible de provoquer un changement de l’image de réponse. Par exemple, le contenu de `catalog::Modifier` change.

>[!NOTE]
>
>Les images Dynamic Media pyramid TIFF (PTIFF) conservent la date du fichier en interne dans l’en-tête du fichier à des fins de validation. Le temps de modification des fichiers conservé par le système de fichiers permet de vérifier si un fichier non PTIFF a changé.

Seuls les fichiers image participent au processus de validation du cache. Les modifications apportées aux fichiers de police ou aux fichiers de profil ICC ne provoquent pas l’invalidation automatique des entrées de cache.
