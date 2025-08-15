---
title: UseLastModified
description: Activez les en-têtes de réponse modifiés en date de la dernière modification. Active ou désactive l’inclusion de l’en-tête Dernière modification dans les réponses HTTP pouvant être mises en cache émises par Image Rendering.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

Activez les en-têtes de réponse modifiés en date de la dernière modification. Active ou désactive l’inclusion de l’en-tête Dernière modification dans les réponses HTTP pouvant être mises en cache émises par Image Rendering.

Le serveur utilise la valeur la plus récente et `vignette::TimeStamp` la plus précieuse `catalog::TimeStamp` de tous les catalogues de vignettes et de matériaux/enregistrements de catalogue impliqués dans une réponse comme valeur d’en-tête Dernière modification.

Ne doit être activé que si un réseau de mise en cache distribué, tel qu’Akamai, qui ne prend pas en charge les en-têtes etag, est utilisé.

>[!NOTE]
>
>Des précautions doivent être prises lors de l’utilisation d’en-têtes Dernière modification dans un environnement à charge équilibrée impliquant plusieurs hôtes de serveur d’images/rendu. La mise en cache du client peut être annulée et la charge du serveur peut augmenter si, pour une raison quelconque, les serveurs ont des horodatages différents pour les mêmes entrées de catalogue. Une telle situation peut se produire comme suit :

* `catalog::TimeStamp`, `vignette::TimeStamp`ou n’est pas définie, de `attribute::TimeStamp` sorte que l’heure [!DNL catalog.ini] de modification du fichier est utilisée par défaut pour `catalog::TimeStamp`.

* Au lieu de partager les fichiers de catalogue de matériaux via un montage réseau, chaque serveur dispose de sa propre instance des fichiers de catalogue sur un système de fichiers local.
* Deux instances ou plus du même [!DNL catalog.ini] fichier ont des dates de modification de fichier différentes, peut-être causées par une copie incorrecte des fichiers.

## Propriétés {#section-453952244193452caccfaf7f601007c1}

Drapeau. 0 à désactiver, 1 à activer les en-têtes HTTP Last-Modified.

## Par défaut {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Hérité de `default::UseLastModified` si non défini ou si vide.

## Voir aussi {#section-1536715169da48b0aecc4ab7326c86db}

[catalog ::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignette ::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
