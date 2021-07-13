---
description: Utilisez ces paramètres de serveur pour déboguer la journalisation de trace.
solution: Experience Manager
title: Journalisation Debug_trace
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Journalisation Debug_trace{#debug-trace-logging}

Utilisez ces paramètres de serveur pour déboguer la journalisation de trace.

>[!NOTE]
>
>Il est recommandé de configurer tous les fichiers journaux à écrire dans le même dossier que `TC::directory`. Cela garantit que tous les fichiers journaux de diffusion d’images participent à la rotation automatique des fichiers journaux configurée avec `TC::maxDays`, ce qui empêchera toute instabilité potentielle du serveur en raison de conditions d’espace disque indisponibles.

## SV::log - Chemin du fichier journal de suivi du superviseur du serveur {#section-3697bc480ff646e79cacc2812c55ef26}

Nom du dossier et du fichier de base pour les fichiers journaux du responsable du serveur. Le chemin peut être absolu ou relatif à *[!DNL install_folder]*. Le responsable du serveur ajoute un trait d’union et la date courante ( *[!DNL -yyyy-mm-dd]*) au nom du fichier (avant le suffixe du fichier, le cas échéant). Il est recommandé d’envoyer tous les fichiers journaux dans le même dossier que les fichiers journaux de Platform Server ( `PS::LogFolder`) pour utiliser la gestion des fichiers journaux implémentée par Platform Server ( `PS::LogDays`). La valeur par défaut est [!DNL logs/Supervisor.log].

>[!NOTE]
>
>Le nouveau dossier doit être créé avant de modifier ce paramètre. Assurez-vous que les autorisations d’accès sont définies de sorte que le responsable du serveur dispose des privilèges de création, de lecture et d’écriture nécessaires.

## SV::tracelevel - Niveau de journal de suivi du superviseur de serveur {#section-36f8634741da4c618d67aa628b5fe474}

Le niveau de journalisation peut être 1, 2, 3 ou 4. Valeur par défaut : 2.

## IS::Log - Chemin du fichier journal du débogage du serveur d’images {#section-73a3f09b77f2446c9f82207b7d8aec39}

Nom du dossier et du fichier de base pour les fichiers journaux de suivi du serveur d’images. Le chemin peut être absolu ou relatif à *[!DNL install_folder]*. ImageServer ajoute un trait d’union et la date courante ( *[!DNL -yyyy-mm-dd]*) au nom du fichier (avant le suffixe du fichier, le cas échéant). Il est recommandé d’envoyer les fichiers journaux du serveur d’images dans le même dossier que les fichiers journaux de Platform Server ( `PS::LogFolder`) pour utiliser la gestion des fichiers journaux implémentée par Platform Server (voir `PS::LogDays`).

>[!NOTE]
>
>Le nouveau dossier doit être créé avant de modifier ce paramètre. Assurez-vous que les autorisations d’accès sont définies de sorte que le serveur d’images dispose des droits de création, de lecture et d’écriture nécessaires.

## IS:TraceClient - Image Server Debug Log Level {#section-3851f1f68e404430985c629ac80534db}

Le niveau de journalisation peut être 1, 2, 3 ou 4 (la valeur par défaut est 2).

Le niveau 1 consigne les événements liés aux connexions au démarrage, à l’arrêt et au serveur Platform.

Le niveau 2 consigne également la connexion et la déconnexion des images sources.

Le niveau 3 ajoute la journalisation des requêtes de données de pixel et la diffusion de ces données sur le serveur Platform.

Le niveau 4 enregistre tous les messages reçus du serveur Platform.

Les niveaux 3 et 4 ne doivent être utilisés qu’à des fins de débogage, car les fichiers journaux peuvent devenir très volumineux.

## IS::TraceStatsInterval - Intervalle du journal des statistiques du serveur d’images {#section-1d8df96d61044e33a5b2b2b0309c2d59}

Le serveur d’images écrit des statistiques de mémoire dans son fichier journal de suivi à l’intervalle spécifié par ce paramètre. La période valide est comprise entre 5 et 86 400 secondes.
