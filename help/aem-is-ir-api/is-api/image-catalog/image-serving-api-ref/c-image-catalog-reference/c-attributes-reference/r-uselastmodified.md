---
description: Activez les en-têtes de réponse de dernière modification. Active ou désactive l’inclusion de l’en-tête Last-Modified dans les réponses HTTP pouvant être mises en cache émises par la diffusion d’images.
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
TQID: 'https://experienceleague.adobe.com/jmwz9jThBnFtTZBRoI0kbKwoxf1MU7rn1CpKrSU4f04'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

Activez les en-têtes de réponse de dernière modification. Active ou désactive l’inclusion de l’en-tête Last-Modified dans les réponses HTTP pouvant être mises en cache émises par la diffusion d’images.

Le serveur utilise la valeur de `catalog::TimeStamp` la plus récente de tous les catalogues/enregistrements de catalogue impliqués dans une réponse comme valeur d’en-tête Dernière modification .

Doit être activé uniquement si un réseau de mise en cache distribué ou un autre système de mise en cache utilisé ne prend pas en charge les en-têtes etag.

>[!NOTE]
>
>Des précautions doivent être prises lors de l’utilisation d’en-têtes Dernière modification dans un environnement avec équilibrage de charge impliquant plusieurs hôtes de diffusion d’images. La mise en cache client peut être annulée et la charge du serveur augmentée si, pour une raison quelconque, les serveurs ont des horodatages différents pour les mêmes entrées de catalogue. Une telle situation peut se produire comme suit :
>
>* Ni `catalog::TimeStamp` ni `attribute::TimeStamp`, de sorte que l’heure de modification du fichier [!DNL catalog.ini] est utilisée par défaut pour `catalog::TimeStamp`.
>
>* Au lieu de partager les fichiers de catalogue d’images par le biais d’un montage réseau, chaque serveur dispose de sa propre instance des fichiers de catalogue sur un système de fichiers local.
>* Plusieurs instances d’un même fichier [!DNL catalog.ini] ont des dates de modification de fichier différentes, probablement en raison d’une copie incorrecte des fichiers.
>

## Propriétés {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Drapeau. 0 pour désactiver, 1 pour activer les en-têtes HTTP de dernière modification.

## Par défaut {#section-4eb47aadab8b41609bef296a4115f9f4}

Hérité de `default::UseLastModified` si non défini ou si vide.

## Voir aussi {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
