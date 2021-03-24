---
description: Utilisez ces paramètres de serveur pour les caches de serveur.
solution: Experience Manager
title: Cache serveur
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---


# Caches serveur{#server-caches}

Utilisez ces paramètres de serveur pour les caches de serveur.

## PS::cache.rootPaths - Cache Data Folders {#section-f0aa808304d74ecdb0c3644f11906c53}

Dossier(s) racine(s) du cache disque de Platform Server. Un ou plusieurs chemins d’accès ou chemins de fichier absolus relatifs à *[!DNL install_folder]*, séparés par des points-virgules (;). Les données du cache de réponse HTTP seront distribuées de manière uniforme dans tous les dossiers spécifiés. Les caches des caches auxiliaires (catalogues d’images compilés et données d’images étrangères) seront situés dans le dossier de cache Principal (le premier dossier de la liste).

## PS::cache.maxSize - Taille du cache des données de réponse {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

Taille maximale du cache de réponse HTTP en octets. Ce paramètre limite la quantité réelle de données à mettre en cache ; il ne tient pas compte des frais généraux du système de fichiers. (Voir [Cache de données de réponse](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca).) Si plusieurs dossiers de données de cache sont spécifiés, les données de cache sont réparties de manière uniforme sur tous les dossiers. La valeur de `cache.maxSize` dans [!DNL PlatformServer.conf] est en octets.

## PS::cache.maxEntries - Entrées maximales du cache de données de réponse {#section-5603e327e90542a5b50aeeb27b080410}

Nombre d’entrées allouées pour l’index du cache de réponse HTTP en mémoire.

>[!NOTE]
>
>Sous Linux, assurez-vous que suffisamment de i-noeuds sont alloués à la partition de cache pour éviter de manquer de i-noeuds.

## IS::TempDirectory - Dossier Fichiers temporaires du serveur d’images {#section-42ea1e7a68c444878f7245c5bbcb1672}

Le serveur d’images doit parfois enregistrer des données intermédiaires sur le disque. Le chemin peut être absolu ou relatif à *[!DNL install_folder]*.

>[!NOTE]
>
>Le nouveau dossier doit être créé avant de modifier ce paramètre. Assurez-vous que les autorisations d’accès sont définies de manière à ce que le serveur Image Server dispose d’un contrôle total sur le dossier.

## SV::temp - Dossier Fichiers temporaires du superviseur de serveur {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

Le contrôleur de serveur doit parfois enregistrer des données intermédiaires sur le disque. Le chemin peut être absolu ou relatif à *[!DNL install_folder]*. Par défaut : [ !DNL *[!DNL install_folder]*/temp].

>[!NOTE]
>
>Le nouveau dossier doit être créé avant de modifier ce paramètre. Assurez-vous que les autorisations d&#39;accès sont définies de sorte que le contrôleur de serveur dispose d&#39;un contrôle total sur le dossier.

