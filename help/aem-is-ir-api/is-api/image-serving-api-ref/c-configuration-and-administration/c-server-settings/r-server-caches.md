---
description: Utilisez ces paramètres de serveur pour les caches de serveur.
solution: Experience Manager
title: Caches du serveur
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6a8d44d3-ecac-4fe0-9f81-28b1cd55e7e1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Caches du serveur{#server-caches}

Utilisez ces paramètres de serveur pour les caches de serveur.

## PS::cache.rootPaths - Dossiers de données du cache {#section-f0aa808304d74ecdb0c3644f11906c53}

Dossier(s) racine(s) du cache disque du [!DNL Platform Server]. Un ou plusieurs chemins d’accès absolus aux fichiers ou chemins d’accès relatifs à *[!DNL install_folder]*, séparés par des points-virgules (;). Les données du cache de réponse HTTP sont réparties uniformément dans tous les dossiers spécifiés. Les caches des caches auxiliaires (catalogues d’images compilés et données d’images étrangères) se trouvent dans le dossier de cache principal (premier dossier de la liste).

## PS::cache.maxSize - Taille du cache des données de réponse {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

Taille maximale du cache de réponse HTTP en octets. Ce paramètre limite la quantité de données réelles à mettre en cache ; il ne prend pas en compte la surcharge du système de fichiers. (Voir [Cache des données de réponse](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca).) Si plusieurs dossiers de données de cache sont spécifiés, les données de cache sont réparties uniformément sur tous les dossiers. La valeur de `cache.maxSize` en [!DNL PlatformServer.conf] est exprimée en octets.

## PS::cache.maxEntries - Entrées max. du cache de données de réponse {#section-5603e327e90542a5b50aeeb27b080410}

Nombre d’entrées allouées pour l’index de cache de réponse HTTP en mémoire.

>[!NOTE]
>
>Sous Linux, assurez-vous qu’un nombre suffisant de nœuds i sont alloués à la partition de cache pour éviter de manquer de nœuds i.

## IS::TempDirectory - Dossier de fichiers temporaires du serveur d’images {#section-42ea1e7a68c444878f7245c5bbcb1672}

Le serveur d’images doit parfois enregistrer des données intermédiaires sur le disque. Le chemin d’accès peut être absolu ou relatif à *[!DNL install_folder]*.

>[!NOTE]
>
>Le nouveau dossier doit être créé avant de modifier ce paramètre. Assurez-vous que les autorisations d’accès sont définies de sorte que le serveur d’images puisse contrôler entièrement le dossier.

## SV::temp - Dossier de fichiers temporaires du superviseur de serveur {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

Le Superviseur du serveur doit parfois enregistrer des données intermédiaires sur le disque. Le chemin d’accès peut être absolu ou relatif à *[!DNL install_folder]*. La valeur par défaut est [!DNL *[!DNL install_folder]*/temp].

>[!NOTE]
>
>Le nouveau dossier doit être créé avant de modifier ce paramètre. Assurez-vous que les autorisations d’accès sont définies de sorte que le superviseur du serveur dispose d’un contrôle total sur le dossier.
