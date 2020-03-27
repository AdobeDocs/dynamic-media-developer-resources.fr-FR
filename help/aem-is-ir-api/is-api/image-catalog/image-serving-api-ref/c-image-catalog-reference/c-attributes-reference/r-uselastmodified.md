---
description: Activez les en-têtes de réponse modifiés en dernier. Active ou désactive l’inclusion de l’en-tête Dernière modification dans les réponses HTTP mises en cache émises par la diffusion d’images.
seo-description: Activez les en-têtes de réponse modifiés en dernier. Active ou désactive l’inclusion de l’en-tête Dernière modification dans les réponses HTTP mises en cache émises par la diffusion d’images.
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: 9dae4f15-4323-4f68-917f-6d72ae52c753
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# UseLastModified{#uselastmodified}

Activez les en-têtes de réponse modifiés en dernier. Active ou désactive l’inclusion de l’en-tête Dernière modification dans les réponses HTTP mises en cache émises par la diffusion d’images.

Le serveur utilise la `catalog::TimeStamp` valeur la plus récente de tous les catalogues/enregistrements de catalogue impliqués dans une réponse comme valeur d’en-tête Dernière modification.

Doit être activé uniquement si un réseau de mise en cache distribué ou un autre système de mise en cache est utilisé, qui ne prend pas en charge les en-têtes d’étiquette.

>[!NOTE]
>
>Soyez vigilant lorsque vous utilisez des en-têtes Dernière modification dans un à équilibrage de charge  impliquant plusieurs hôtes de diffusion d’images. La mise en cache du client peut être annulée et la charge du serveur augmenter si, pour une raison quelconque, les serveurs disposent de tampons temporels différents pour les mêmes entrées de catalogue. Une telle situation peut se produire comme suit :
>
>* Ni `catalog::TimeStamp` ni `attribute::TimeStamp`, de sorte que l’heure de modification du [!DNL catalog.ini] fichier soit utilisée comme valeur par défaut `catalog::TimeStamp`.
   >
   >
* Au lieu de partager les fichiers de catalogue d’images via un montage réseau, chaque serveur dispose de sa propre instance des fichiers de catalogue sur un système de fichiers local.
>* Deux instances ou plus d’un même [!DNL catalog.ini] fichier ont des dates de modification différentes, peut-être en raison d’une copie incorrecte des fichiers.
>



## Propriétés {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Drapeau. 0 pour désactiver, 1 pour activer les en-têtes HTTP Dernière modification.

## Par défaut {#section-4eb47aadab8b41609bef296a4115f9f4}

Héritée de `default::UseLastModified` si non définie ou si vide.

## Voir aussi {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalogue::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
