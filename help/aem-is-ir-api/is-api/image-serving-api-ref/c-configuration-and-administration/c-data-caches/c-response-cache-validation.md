---
description: Les entrées de cache sont automatiquement actualisées à l’aide de la validation du cache basée sur le catalogue ou sur l’expiration, comme cela est sélectionné avec l’attribut CacheValidationPolicy (dans default.ini ou le fichier .ini d’un catalogue d’images spécifique).
seo-description: Les entrées de cache sont automatiquement actualisées à l’aide de la validation du cache basée sur le catalogue ou sur l’expiration, comme cela est sélectionné avec l’attribut CacheValidationPolicy (dans default.ini ou le fichier .ini d’un catalogue d’images spécifique).
seo-title: Validation du cache de réponse
solution: Experience Manager
title: Validation du cache de réponse
topic: Scene7 Image Serving - Image Rendering API
uuid: d1aad5ae-f0fa-489b-a48b-b0ac8c8f43bb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Validation du cache de réponse{#response-cache-validation}

Les entrées de cache sont automatiquement actualisées à l’aide de la validation du cache basée sur le catalogue ou sur l’expiration, comme sélectionné avec l’attribut::CacheValidationPolicy (dans default.ini ou le fichier .ini d’un catalogue d’images spécifique).

Avec la validation basée sur un catalogue, une entrée de cache existante est considérée comme obsolète si `catalog::LastModified` (ou `attribute::LastModified`, ou l’heure de modification du fichier du [!DNL catalog.ini] fichier) est plus récente que le moment de création de l’entrée de cache.

Avec la validation basée sur l’expiration, une entrée de cache devient obsolète après 5 minutes depuis la validation la plus récente. Dans les deux cas, le serveur valide les entrées obsolètes du cache en vérifiant les dates des fichiers de toutes les images impliquées dans la création de la requête. Si les dates du fichier n’ont pas changé, l’horodatage de l’entrée du cache est mis à jour et la date mise en cache est considérée comme valide.

Pour les applications standard qui impliquent principalement des images enregistrées dans des catalogues d’images, la validation basée sur un catalogue offre un avantage en termes de performances. Les applications qui n’impliquent pas de catalogues d’images doivent utiliser la validation du cache basée sur l’expiration. Pour ce faire, vous pouvez définir `attribute::cacheValidationPolicy=0` dans [!DNL default.ini]et `1` dans tous les fichiers de catalogue d’images spécifiques.

Les entrées du cache ne sont plus valides et sont sujettes à une nouvelle génération lorsqu’une entrée de catalogue impliquée dans la requête change d’une manière susceptible de provoquer un changement de l’image de réponse. Par exemple, le contenu des `catalog::Modifier` modifications.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Les images PTIFF (Scene7 pyramid TIFF) conservent la date du fichier en interne dans l’en-tête du fichier à des fins de validation. Le temps de modification du fichier conservé par le système de fichiers permet de vérifier si un fichier non PTIFF a changé.

Seuls les fichiers image participent au processus de validation du cache. Les modifications apportées aux fichiers de police ou aux fichiers de ICC ne provoquent pas l’invalidation automatique des entrées de cache.
