---
description: Activez les en-têtes de réponse modifiés en dernier. Active ou désactive l’inclusion de l’en-tête Dernière modification dans les réponses HTTP en mémoire cache émises par la diffusion d’images.
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 1%

---


# UseLastModified{#uselastmodified}

Activez les en-têtes de réponse modifiés en dernier. Active ou désactive l’inclusion de l’en-tête Dernière modification dans les réponses HTTP en mémoire cache émises par la diffusion d’images.

Le serveur utilise la valeur `catalog::TimeStamp` la plus récente de tous les catalogues/enregistrements de catalogue impliqués dans une réponse comme valeur d&#39;en-tête Dernière modification.

Ne doit être activé que si un réseau de mise en cache distribué ou un autre système de mise en cache est utilisé qui ne prend pas en charge les en-têtes d&#39;balises.

>[!NOTE]
>
>Soyez prudent lorsque vous utilisez des en-têtes Dernière modification dans un environnement à charge équilibrée impliquant plusieurs hôtes de diffusion d’images. La mise en cache du client peut être annulée et la charge du serveur augmenter si, pour une raison quelconque, les serveurs disposent de tampons temporels différents pour les mêmes entrées de catalogue. Cette situation peut se présenter comme suit :
>
>* Ni `catalog::TimeStamp` ni `attribute::TimeStamp`, de sorte que l’heure de modification du fichier [!DNL catalog.ini] soit utilisée comme valeur par défaut pour `catalog::TimeStamp`.
   >
   >
* Au lieu de partager les fichiers de catalogue d’images via un montage réseau, chaque serveur dispose de sa propre instance des fichiers de catalogue sur un système de fichiers local.
>* Deux instances ou plus d&#39;un même fichier [!DNL catalog.ini] ont des dates de modification de fichier différentes, peut-être en raison d&#39;une copie incorrecte des fichiers.

>



## Propriétés {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Indicateur. 0 pour désactiver, 1 pour activer les en-têtes HTTP Dernière modification.

## Par défaut {#section-4eb47aadab8b41609bef296a4115f9f4}

Hérité de `default::UseLastModified` si elle n&#39;est pas définie ou si elle est vide.

## Voir aussi {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalogue ::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
