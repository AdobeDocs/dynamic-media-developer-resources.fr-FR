---
description: Utilisez ces paramètres de serveur pour le service de catalogue d’images.
seo-description: Utilisez ces paramètres de serveur pour le service de catalogue d’images.
seo-title: Service de catalogue d’images
solution: Experience Manager
title: Service de catalogue d’images
topic: Scene7 Image Serving - Image Rendering API
uuid: 601b1c30-7d51-448b-97b5-5ad9cb383975
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Service de catalogue d’images{#image-catalog-service}

Utilisez ces paramètres de serveur pour le service de catalogue d’images.

## CS::catalog.rootPath - Dossier du catalogue d’images {#section-02d107f157384b18835f884f24fea3aa}

Emplacement du dossier du catalogue d’images (où tous les [!DNL catalog.ini] fichiers doivent être situés). Il peut s’agir d’un chemin d’accès absolu au fichier ou d’un chemin d’accès relatif au fichier *[!DNL install_folder]*. Le serveur surveille en permanence ce dossier et charge ou recharge les catalogues lorsqu’un nouveau fichier catalogue principal (avec le suffixe [!DNL .ini] du fichier) est détecté ou lorsque l’heure de la dernière modification d’un fichier catalogue principal existant a changé.

## CS::catalog.cacheRoot - Dossier du cache du catalogue {#section-73e499c3a5974f1aa4251e70272ff503}

Dossier racine du cache du système de catalogue. Peut être défini sur la même valeur que l’un des dossiers dans `PS::cache.rootPaths`. Le dossier doit être créé manuellement avant que ce paramètre ne soit modifié.

## CS::catalog.modificationWaitTime - Délai d’analyse du fichier catalogue {#section-7348065bcc124cb68ea947bf1b9b0845}

En msec, le service de catalogue attend qu’un [!DNL catalog.ini] fichier soit modifié jusqu’à ce qu’il charge les fichiers de catalogue secondaires. Ce délai permet de s’assurer que tous les fichiers de catalogue secondaires sont à jour avant que le service de catalogue ne tente de les charger. Valeur entière en msec.

## CS::catalog.refreshInterval - Fréquence de vérification des fichiers du catalogue {#section-517fefc1d8784777a1026abec8630d58}

Fréquence à laquelle le service de catalogue vérifie les modifications apportées aux catalogues d’images. Valeur entière en msec.
