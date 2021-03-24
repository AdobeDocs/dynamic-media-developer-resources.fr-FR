---
description: Activez les en-têtes de réponse modifiés en dernier. Active ou désactive l’inclusion de l’en-tête Dernière modification dans les réponses HTTP en mémoire cache émises par le rendu d’image.
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 1%

---


# UseLastModified{#uselastmodified}

Activez les en-têtes de réponse modifiés en dernier. Active ou désactive l’inclusion de l’en-tête Dernière modification dans les réponses HTTP en mémoire cache émises par le rendu d’image.

Le serveur utilise les valeurs `vignette::TimeStamp` et `catalog::TimeStamp` les plus récentes de tous les catalogues de vignettes et de matériaux/enregistrements de catalogue impliqués dans une réponse comme valeur d&#39;en-tête Dernière modification.

Ne doit être activé que si un réseau de mise en cache distribué, tel qu’Akamai, est utilisé, ce qui ne prend pas en charge les en-têtes d’balises.

>[!NOTE]
>
>Soyez prudent lorsque vous utilisez des en-têtes Dernière modification dans un environnement à charge équilibrée impliquant plusieurs hôtes de diffusion/rendu d’images. La mise en cache du client peut être annulée et la charge du serveur augmenter si, pour une raison quelconque, les serveurs disposent de tampons temporels différents pour les mêmes entrées de catalogue. Cette situation peut se présenter comme suit :

* Ni `catalog::TimeStamp`, `vignette::TimeStamp`, ni `attribute::TimeStamp` n&#39;est défini, de sorte que l&#39;heure de modification du fichier [!DNL catalog.ini] est utilisée comme valeur par défaut pour `catalog::TimeStamp`.

* Au lieu de partager les fichiers de catalogue de matériaux via un montage réseau, chaque serveur dispose de sa propre instance des fichiers de catalogue sur un système de fichiers local.
* Deux instances ou plus d&#39;un même fichier [!DNL catalog.ini] ont des dates de modification de fichier différentes, peut-être en raison d&#39;une copie incorrecte des fichiers.

## Propriétés {#section-453952244193452caccfaf7f601007c1}

Indicateur. 0 pour désactiver, 1 pour activer les en-têtes HTTP Dernière modification.

## Par défaut {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Hérité de `default::UseLastModified` si elle n&#39;est pas définie ou si elle est vide.

## Voir aussi {#section-1536715169da48b0aecc4ab7326c86db}

[catalogue ::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ,  [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
