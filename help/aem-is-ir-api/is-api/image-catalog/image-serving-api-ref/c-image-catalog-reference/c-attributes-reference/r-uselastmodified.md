---
description: Activez les en-têtes de réponse modifiés en date de la dernière modification. Active ou désactive l’inclusion de l’en-tête Dernière modification dans les réponses HTTP pouvant être mises en cache émises par le serveur d’images.
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

Activez les en-têtes de réponse modifiés en date de la dernière modification. Active ou désactive l’inclusion de l’en-tête Dernière modification dans les réponses HTTP pouvant être mises en cache émises par le serveur d’images.

Le serveur utilise la valeur la plus récente `catalog::TimeStamp` de tous les catalogues/enregistrements de catalogue impliqués dans une réponse comme valeur d’en-tête Dernière modification.

Ne doit être activé que si un réseau de mise en cache distribué ou un autre système de mise en cache qui ne prend pas en charge les en-têtes etag est utilisé.

>[!NOTE]
>
>Des précautions doivent être prises lors de l’utilisation d’en-têtes Dernière modification dans un environnement à charge équilibrée impliquant plusieurs hôtes Image Server. La mise en cache du client peut être annulée et la charge du serveur peut augmenter si, pour une raison quelconque, les serveurs ont des horodatages différents pour les mêmes entrées de catalogue. Une telle situation peut se produire comme suit :
>
>* Ni `catalog::TimeStamp` ni , `attribute::TimeStamp`de sorte que l’heure [!DNL catalog.ini] de modification du fichier soit utilisée par défaut pour `catalog::TimeStamp`.
>
>* Au lieu de partager les fichiers de catalogue d’images via un montage réseau, chaque serveur dispose de sa propre instance des fichiers de catalogue sur un système de fichiers local.
>* Deux instances ou plus du même [!DNL catalog.ini] fichier ont des dates de modification de fichier différentes, peut-être causées par une copie incorrecte des fichiers.
>

## Propriétés {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Drapeau. 0 à désactiver, 1 à activer les en-têtes HTTP Last-Modified.

## Par défaut {#section-4eb47aadab8b41609bef296a4115f9f4}

Hérité de `default::UseLastModified` si non défini ou si vide.

## Voir aussi {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalog ::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
