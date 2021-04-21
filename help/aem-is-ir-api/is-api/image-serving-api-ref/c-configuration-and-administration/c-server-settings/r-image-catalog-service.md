---
description: Utilisez ces paramètres de serveur pour le service de catalogue d’images.
solution: Experience Manager
title: Service de catalogue d’images
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# Service de catalogue d’images{#image-catalog-service}

Utilisez ces paramètres de serveur pour le service de catalogue d’images.

## CS::catalog.rootPath - Dossier du catalogue d’images {#section-02d107f157384b18835f884f24fea3aa}

Emplacement du dossier du catalogue d’images (où tous les fichiers [!DNL catalog.ini] doivent être localisés). Il peut s’agir d’un chemin d’accès absolu au fichier ou d’un chemin d’accès relatif à *[!DNL install_folder]*. Le serveur surveille en permanence ce dossier et charge ou recharge les catalogues lorsqu&#39;un nouveau fichier catalogue principal (avec le suffixe [!DNL .ini]) est détecté ou lorsque l&#39;heure de la dernière modification d&#39;un fichier catalogue principal existant a changé.

## CS::catalog.cacheRoot - Dossier du cache du catalogue {#section-73e499c3a5974f1aa4251e70272ff503}

Dossier racine du cache du système de catalogue. Peut être défini de la même manière que l&#39;un des dossiers de `PS::cache.rootPaths`. Le dossier doit être créé manuellement avant que ce paramètre ne soit modifié.

## CS::catalog.modificationWaitTime - Délai d&#39;analyse des fichiers du catalogue {#section-7348065bcc124cb68ea947bf1b9b0845}

Temps, en msec, pendant lequel le service de catalogue attend qu&#39;un fichier [!DNL catalog.ini] soit modifié jusqu&#39;à ce qu&#39;il charge les fichiers de catalogue secondaires. Ce délai permet de s’assurer que tous les fichiers de catalogue secondaires sont à jour avant que le service de catalogue ne tente de les charger. Valeur entière en msec.

## CS::catalog.refreshInterval - Fréquence de vérification des fichiers du catalogue {#section-517fefc1d8784777a1026abec8630d58}

Fréquence à laquelle le service de catalogue recherche les modifications apportées aux catalogues d’images. Valeur entière en msec.
