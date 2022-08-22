---
title: UseLastModified
description: Activez les en-têtes de réponse de dernière modification. Active ou désactive l’inclusion de l’en-tête Last-Modified dans les réponses HTTP pouvant être mises en cache émises par le rendu d’image.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

Activez les en-têtes de réponse de dernière modification. Active ou désactive l’inclusion de l’en-tête Last-Modified dans les réponses HTTP pouvant être mises en cache émises par le rendu d’image.

Le serveur utilise le plus récent `vignette::TimeStamp` et `catalog::TimeStamp` valeur de tous les catalogues/catalogues de vignettes et de matériaux impliqués dans une réponse en tant que valeur d’en-tête Last-Modified.

Doit être activé uniquement si un réseau de mise en cache distribué, tel qu’Akamai, est utilisé et ne prend pas en charge les en-têtes d’etag.

>[!NOTE]
>
>Il faut être prudent lors de l’utilisation d’en-têtes Last-Modified dans un environnement à répartition de charge impliquant plusieurs hôtes de diffusion/rendu d’images. La mise en cache du client peut être abandonnée et la charge du serveur augmenter si, pour une raison quelconque, les serveurs disposent de différents horodatages pour les mêmes entrées de catalogue. Une telle situation peut se produire comme suit :

* `catalog::TimeStamp`, `vignette::TimeStamp`ou `attribute::TimeStamp` n’est pas défini, de sorte que l’heure de modification de la variable [!DNL catalog.ini] est utilisé comme fichier par défaut pour `catalog::TimeStamp`.

* Au lieu de partager les fichiers de catalogue de matériaux via un montage réseau, chaque serveur possède sa propre instance des fichiers de catalogue sur un système de fichiers local.
* Deux instances ou plus de la même [!DNL catalog.ini] ont des dates de modification de fichier différentes, peut-être en raison d’une copie incorrecte des fichiers.

## Propriétés {#section-453952244193452caccfaf7f601007c1}

Indicateur. 0 pour désactiver, 1 pour activer les en-têtes HTTP Dernière modification.

## Par défaut {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Hérité de `default::UseLastModified` s’il n’est pas défini ou s’il est vide.

## Voir aussi {#section-1536715169da48b0aecc4ab7326c86db}

[catalogue ::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignette ::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
