---
description: Utilisez ces paramètres de serveur pour les caches de serveur.
seo-description: Utilisez ces paramètres de serveur pour les caches de serveur.
seo-title: Caches serveur
solution: Experience Manager
title: Caches serveur
topic: Scene7 Image Serving - Image Rendering API
uuid: 73745363-2011-453f-b7a0-96de4b44186d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Caches serveur{#server-caches}

Utilisez ces paramètres de serveur pour les caches de serveur.

## PS::cache.rootPaths - Dossiers de données du cache {#section-f0aa808304d74ecdb0c3644f11906c53}

Dossier(s) racine(s) du cache disque du serveur de plateformes. Un ou plusieurs chemins d’accès ou chemins de fichier absolus relatifs à *[!DNL install_folder]*, séparés par des points-virgules (;). Les données du cache de réponse HTTP seront réparties uniformément dans tous les dossiers spécifiés. Les caches des caches auxiliaires (catalogues d’images compilés et données d’images étrangères) se trouvent dans le dossier cache principal (le premier dossier du  du).

## PS::cache.maxSize - Taille du cache des données de réponse {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

taille maximale du cache de réponse HTTP en octets. Ce paramètre limite la quantité réelle de données à mettre en cache ; il ne tient pas compte des frais généraux du système de fichiers. (Voir Cache [des données de](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca)réponse.) Si plusieurs dossiers de données de cache sont spécifiés, les données de cache sont réparties uniformément sur tous les dossiers. La valeur de `cache.maxSize` in [!DNL PlatformServer.conf] est en octets.

## PS::cache.maxEntries - Entrées maximales du cache des données de réponse {#section-5603e327e90542a5b50aeeb27b080410}

Nombre d’entrées allouées pour l’index du cache de réponse HTTP en mémoire.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Sous Linux, assurez-vous que suffisamment de i-noeuds sont alloués pour la partition cache afin d’éviter de manquer de i-noeuds.

## IS::TempDirectory - Dossier des fichiers temporaires du serveur d’images {#section-42ea1e7a68c444878f7245c5bbcb1672}

Le serveur d’images doit parfois enregistrer des données intermédiaires sur le disque. Le chemin peut être absolu ou relatif à *[!DNL install_folder]*.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Le nouveau dossier doit être créé avant de modifier ce paramètre. Assurez-vous que les autorisations d’accès sont définies de sorte que le serveur Image Server dispose d’un contrôle total du dossier.

## SV::temp - Dossier des fichiers temporaires du contrôleur de serveur {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

Le contrôleur de serveur doit parfois enregistrer des données intermédiaires sur le disque. Le chemin peut être absolu ou relatif à *[!DNL install_folder]*. Valeur par défaut : [!DNL *[!DNL install_folder]*/temp].

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Le nouveau dossier doit être créé avant de modifier ce paramètre. Assurez-vous que les autorisations d’accès sont définies de manière à ce que le contrôleur de serveur dispose d’un contrôle total du dossier.

