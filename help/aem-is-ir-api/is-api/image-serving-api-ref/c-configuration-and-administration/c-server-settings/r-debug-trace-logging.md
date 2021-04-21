---
description: Utilisez ces paramètres de serveur pour déboguer la journalisation du suivi.
solution: Experience Manager
title: Journalisation Debug_trace
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---


# Journalisation Debug_trace{#debug-trace-logging}

Utilisez ces paramètres de serveur pour déboguer la journalisation du suivi.

>[!NOTE]
>
>Il est recommandé de configurer tous les fichiers journaux pour qu’ils soient écrits dans le même dossier que `TC::directory`. Cela permet de s’assurer que tous les fichiers journaux de diffusion d’images participent à la rotation automatique des fichiers journaux configurée avec `TC::maxDays`, ce qui évite toute instabilité potentielle du serveur en raison de conditions d’espace disque.

## SV::log - Chemin du fichier journal de suivi du superviseur de serveur {#section-3697bc480ff646e79cacc2812c55ef26}

Nom de dossier et de fichier de base pour les fichiers journaux du contrôleur de serveur. Le chemin peut être absolu ou relatif à *[!DNL install_folder]*. Le responsable du serveur ajoute un trait d&#39;union et la date actuelle ( *[!DNL -yyyy-mm-dd]*) au nom du fichier (avant le suffixe du fichier, le cas échéant). Il est recommandé d’envoyer tous les fichiers journaux dans le même dossier que les fichiers journaux de Platform Server ( `PS::LogFolder`) afin d’exploiter la gestion des fichiers journaux mise en oeuvre par Platform Server ( `PS::LogDays`). La valeur par défaut est [!DNL logs/Supervisor.log].

>[!NOTE]
>
>Le nouveau dossier doit être créé avant de modifier ce paramètre. Assurez-vous que les autorisations d&#39;accès sont définies de sorte que le contrôleur de serveur dispose des privilèges de création, de lecture et d&#39;écriture nécessaires.

## SV::tracheight - Niveau du journal de suivi du superviseur de serveur {#section-36f8634741da4c618d67aa628b5fe474}

Le niveau de journal peut être 1, 2, 3 ou 4. Valeur par défaut : 2.

## IS::Log - Chemin du fichier journal de débogage du serveur d’images {#section-73a3f09b77f2446c9f82207b7d8aec39}

Nom de dossier et de fichier de base pour les fichiers journaux de suivi Image Server. Le chemin peut être absolu ou relatif à *[!DNL install_folder]*. ImageServer ajoute un trait d’union et la date actuelle ( *[!DNL -yyyy-mm-dd]*) au nom du fichier (avant le suffixe du fichier, le cas échéant). Il est recommandé d’envoyer les fichiers journaux Image Server dans le même dossier que les fichiers journaux Platform Server ( `PS::LogFolder`) afin d’exploiter la gestion des fichiers journaux mise en oeuvre par Platform Server (voir `PS::LogDays`).

>[!NOTE]
>
>Le nouveau dossier doit être créé avant de modifier ce paramètre. Assurez-vous que les autorisations d’accès sont définies de sorte que Image Serving dispose des droits de création, de lecture et d’écriture nécessaires.

## IS:TraceClient - Niveau du journal de débogage du serveur d’images {#section-3851f1f68e404430985c629ac80534db}

Le niveau de journal peut être 1, 2, 3 ou 4 (par défaut, 2)

Le niveau 1 consigne les événements liés aux connexions au début-up, à l&#39;arrêt et au serveur de plateformes.

Le niveau 2 consigne également les connexions aux images source et leur déconnexion.

Le niveau 3 ajoute la journalisation des requêtes de données de pixels et la diffusion de celles-ci sur le serveur de plateformes.

Le niveau 4 enregistre tous les messages reçus de Platform Server.

Les niveaux 3 et 4 doivent être utilisés uniquement à des fins de débogage, car les fichiers journaux peuvent devenir très volumineux.

## IS::TraceStatsInterval - Intervalle du journal des statistiques du serveur d’images {#section-1d8df96d61044e33a5b2b2b0309c2d59}

Le serveur d’images écrit les statistiques de mémoire dans son fichier journal de suivi à l’intervalle spécifié par ce paramètre. La plage valide est comprise entre 5 et 86 400 secondes.
