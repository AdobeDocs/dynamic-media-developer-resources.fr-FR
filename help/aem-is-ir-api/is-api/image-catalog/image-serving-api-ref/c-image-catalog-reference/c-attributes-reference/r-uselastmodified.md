---
description: Activez les en-têtes de réponse de dernière modification. Active ou désactive l’inclusion de l’en-tête Last-Modified dans les réponses HTTP pouvant être mises en cache émises par le serveur d’images.
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

Activez les en-têtes de réponse de dernière modification. Active ou désactive l’inclusion de l’en-tête Last-Modified dans les réponses HTTP pouvant être mises en cache émises par le serveur d’images.

Le serveur utilise la valeur `catalog::TimeStamp` la plus récente de tous les catalogues/enregistrements de catalogue impliqués dans une réponse comme valeur d’en-tête Last-Modified.

Doit être activé uniquement si un réseau de mise en cache distribué ou un autre système de mise en cache est utilisé et ne prend pas en charge les en-têtes d’etag.

>[!NOTE]
>
>Soyez prudent lorsque vous utilisez des en-têtes Last-Modified dans un environnement à répartition de charge impliquant plusieurs hôtes de diffusion d’images. La mise en cache du client peut être abandonnée et la charge du serveur augmenter si, pour une raison quelconque, les serveurs disposent de différents horodatages pour les mêmes entrées de catalogue. Une telle situation peut se produire comme suit :
>
>* Ni `catalog::TimeStamp` ni `attribute::TimeStamp`, de sorte que l’heure de modification du fichier [!DNL catalog.ini] soit utilisée par défaut pour `catalog::TimeStamp`.
   >
   >
* Au lieu de partager les fichiers du catalogue d’images via un montage réseau, chaque serveur possède sa propre instance des fichiers de catalogue sur un système de fichiers local.
>* Deux instances ou plus du même fichier [!DNL catalog.ini] ont des dates de modification de fichier différentes, peut-être en raison d’une copie incorrecte des fichiers.

>



## Propriétés {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Indicateur. 0 pour désactiver, 1 pour activer les en-têtes HTTP Dernière modification.

## Par défaut {#section-4eb47aadab8b41609bef296a4115f9f4}

Hérité de `default::UseLastModified` si elle n’est pas définie ou si elle est vide.

## Voir aussi {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalogue ::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
