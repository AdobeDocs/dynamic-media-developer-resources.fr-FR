---
description: Utilisez ces paramètres de serveur pour déboguer la journalisation du suivi.
seo-description: Utilisez ces paramètres de serveur pour déboguer la journalisation du suivi.
seo-title: Journalisation Debug_trace
solution: Experience Manager
title: Journalisation Debug_trace
topic: Scene7 Image Serving - Image Rendering API
uuid: 33f1d093-007d-453b-965a-9d701a845954
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Journalisation Debug_trace{#debug-trace-logging}

Utilisez ces paramètres de serveur pour déboguer la journalisation du suivi.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Il est recommandé de configurer tous les fichiers journaux pour qu’ils soient écrits dans le même dossier que `TC::directory`. Cela permet de s’assurer que tous les fichiers journaux de diffusion d’images participent à la rotation automatique des fichiers journaux configurée avec `TC::maxDays`, ce qui évite toute instabilité potentielle du serveur en raison de conditions d’espace disque insuffisant.

## SV::log - Chemin du fichier journal de suivi du superviseur du serveur {#section-3697bc480ff646e79cacc2812c55ef26}

Nom du dossier et du fichier de base pour les fichiers journaux du contrôleur de serveur. Le chemin peut être absolu ou relatif à *[!DNL install_folder]*. Le contrôleur du serveur ajoute un tiret et la date actuelle ( *[!DNL -yyyy-mm-dd]*) au nom du fichier (avant le suffixe du fichier, le cas échéant). Il est recommandé d’envoyer tous les fichiers journaux dans le même dossier que les fichiers journaux de Platform Server ( `PS::LogFolder`) afin d’exploiter la gestion des fichiers journaux implémentée par Platform Server ( `PS::LogDays`). Default is [!DNL logs/Supervisor.log].

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Le nouveau dossier doit être créé avant de modifier ce paramètre. Assurez-vous que les autorisations d&#39;accès sont définies de sorte que le contrôleur du serveur dispose des privilèges de création, de lecture et d&#39;écriture nécessaires.

## SV::traclevel - Niveau du journal de suivi du contrôleur de serveur {#section-36f8634741da4c618d67aa628b5fe474}

Le niveau de journal peut être 1, 2, 3 ou 4. Valeur par défaut : 2.

## IS::Log - Chemin du fichier journal de débogage du serveur d’images {#section-73a3f09b77f2446c9f82207b7d8aec39}

Nom du dossier et du fichier de base pour les fichiers journaux de suivi Image Server. Le chemin peut être absolu ou relatif à *[!DNL install_folder]*. ImageServer ajoute un trait d’union et la date courante ( *[!DNL -yyyy-mm-dd]*) au nom du fichier (avant le suffixe du fichier, le cas échéant). Il est recommandé d’envoyer les fichiers journaux du serveur Image Server dans le même dossier que les fichiers journaux du serveur de plateformes ( `PS::LogFolder`) afin d’exploiter la gestion des fichiers journaux implémentée par le serveur de plateformes (voir `PS::LogDays`).

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Le nouveau dossier doit être créé avant de modifier ce paramètre. Assurez-vous que les autorisations d’accès sont définies de manière à ce que la diffusion d’images dispose des droits de création, de lecture et d’écriture nécessaires.

## IS:TraceClient - Niveau du journal de débogage du serveur d’images {#section-3851f1f68e404430985c629ac80534db}

Le niveau de journal peut être 1, 2, 3 ou 4 (2 par défaut)

Le niveau 1 consigne les liés aux connexions au serveur de plateformes, au serveur de, à l’arrêt et au serveur de plateformes.

Le niveau 2 consigne également la connexion et la déconnexion des images source.

Le niveau 3 ajoute la journalisation des demandes de données de pixels et de  identiques au serveur de plateformes.

Le niveau 4 enregistre tous les messages reçus du serveur de plateformes.

Les niveaux 3 et 4 doivent être utilisés uniquement à des fins de débogage, car les fichiers journaux peuvent devenir très volumineux.

## IS::TraceStatsInterval - Intervalle du journal des statistiques du serveur d’images {#section-1d8df96d61044e33a5b2b2b0309c2d59}

Le serveur d’images écrit les statistiques de mémoire dans son fichier journal de suivi à l’intervalle spécifié par ce paramètre. La plage valide est comprise entre 5 et 86 400 secondes.
