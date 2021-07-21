---
description: Utilisez ces paramètres de serveur pour le service de catalogue d’images.
solution: Experience Manager
title: Service de catalogue d’images
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# Service de catalogue d’images{#image-catalog-service}

Utilisez ces paramètres de serveur pour le service de catalogue d’images.

## CS::catalog.rootPath - Dossier de catalogue d’images {#section-02d107f157384b18835f884f24fea3aa}

Emplacement du dossier du catalogue d’images (où tous les fichiers [!DNL catalog.ini] doivent être localisés). Il peut s’agir d’un chemin d’accès absolu au fichier ou d’un chemin d’accès relatif à *[!DNL install_folder]*. Le serveur surveille en permanence ce dossier et charge ou recharge les catalogues lorsqu’un nouveau fichier de catalogue principal (portant le suffixe [!DNL .ini]) est détecté ou lorsque l’heure de dernière modification d’un fichier de catalogue principal existant a changé.

## CS::catalog.cacheRoot - Dossier de cache du catalogue {#section-73e499c3a5974f1aa4251e70272ff503}

Dossier racine du cache du système de catalogue. Peut être défini sur la même valeur que l’un des dossiers de `PS::cache.rootPaths`. Le dossier doit être créé manuellement avant que ce paramètre ne soit modifié.

## CS::catalog.modificationWaitTime - Délai d’analyse des fichiers du catalogue {#section-7348065bcc124cb68ea947bf1b9b0845}

Temps, en msec, pendant lequel le service de catalogue attend après la modification d’un fichier [!DNL catalog.ini] jusqu’au chargement des fichiers de catalogue secondaires. Ce délai permet de s’assurer que tous les fichiers de catalogue secondaires sont à jour avant que le service de catalogue ne tente de les charger. Valeur entière en msec.

## CS::catalog.refreshInterval - Fréquence de vérification des fichiers du catalogue {#section-517fefc1d8784777a1026abec8630d58}

Fréquence à laquelle le service de catalogue recherche les modifications apportées aux catalogues d’images. Valeur entière en msec.
