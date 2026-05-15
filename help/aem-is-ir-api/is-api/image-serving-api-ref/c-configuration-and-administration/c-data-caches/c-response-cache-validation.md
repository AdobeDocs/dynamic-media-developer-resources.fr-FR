---
description: Les entrées du cache sont actualisées automatiquement à l’aide de la validation du cache basée sur le catalogue ou sur l’expiration, telle que sélectionnée avec l’attribut CacheValidationPolicy (dans default.ini ou le fichier .ini d’un catalogue d’images spécifique).
solution: Experience Manager
title: Validation du cache de réponse
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
TQID: 'https://experienceleague.adobe.com/VnvYNkc3yijayG8tnJKHsp94Qto8VZj9OkIgfIv1Kc0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 311
ht-degree: 0%

---

# Validation du cache de réponse{#response-cache-validation}

Les entrées du cache sont actualisées automatiquement à l’aide de la validation du cache basée sur le catalogue ou sur l’expiration, telle que sélectionnée avec l’attribut ::CacheValidationPolicy (dans default.ini ou le fichier .ini d’un catalogue d’images spécifique).

Avec la validation par catalogue, une entrée de cache existante est considérée comme obsolète si `catalog::LastModified` (ou `attribute::LastModified`, ou l’heure de modification du fichier [!DNL catalog.ini]) est plus récente que l’heure de création de l’entrée de cache.

Avec la validation basée sur l’expiration, une entrée de cache devient obsolète au bout de 5 minutes depuis la dernière validation. Dans les deux cas, le serveur valide les entrées de cache obsolètes en vérifiant les dates de tous les fichiers image impliqués dans la création de la requête. Si les dates du fichier n’ont pas changé, l’horodatage de l’entrée du cache est mis à jour et la date mise en cache est considérée comme valide.

Pour les applications classiques qui impliquent principalement des images enregistrées dans des catalogues d’images, la validation catalogue offre un avantage en termes de performances. Les applications qui n’impliquent pas de catalogues d’images doivent utiliser la validation de cache basée sur l’expiration. Pour ce faire, vous pouvez définir des `attribute::cacheValidationPolicy=0` dans [!DNL default.ini] et les `1` dans tous les fichiers de catalogue d’images spécifiques.

Les entrées du cache ne sont plus valides et sont susceptibles d’être générées à nouveau lorsqu’une entrée du catalogue impliquée dans la demande est modifiée d’une manière qui entraînerait probablement une modification de l’image de réponse. Par exemple, le contenu de `catalog::Modifier` change.

>[!NOTE]
>
>Les images TIFF pyramidales Dynamic Media (PTIFF) conservent la date du fichier en interne dans l’en-tête du fichier à des fins de validation. L’heure de modification du fichier gérée par le système de fichiers est utilisée pour vérifier si un fichier non PTIFF a été modifié.

Seuls les fichiers image participent au processus de validation du cache. Les modifications apportées aux fichiers de polices ou aux fichiers de profil ICC n’entraînent pas l’invalidation automatique des entrées du cache.
