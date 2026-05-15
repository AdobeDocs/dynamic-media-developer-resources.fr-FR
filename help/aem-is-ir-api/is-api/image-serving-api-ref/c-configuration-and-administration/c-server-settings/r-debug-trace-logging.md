---
title: Journalisation de Debug_trace
description: Utilisez ces paramètres de serveur pour déboguer la journalisation de trace.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
TQID: 'https://experienceleague.adobe.com/vkvp3WTt-nSSAQPaHUgXvMCuEkD-vEno-ot3Nxn9ReE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 407
ht-degree: 0%

---

# Journalisation de Debug_trace{#debug-trace-logging}

Utilisez ces paramètres de serveur pour déboguer la journalisation de trace.

>[!NOTE]
>
>Adobe vous recommande de configurer tous les fichiers journaux à écrire dans le même dossier que `TC::directory`. Cela permet de s’assurer que tous les fichiers journaux de la diffusion d’images participent à la rotation automatique des fichiers journaux configurée avec `TC::maxDays`, ce qui empêche une instabilité potentielle du serveur en raison de conditions d’espace disque insuffisant.

## SV::log - Chemin du fichier journal de suivi du superviseur du serveur {#section-3697bc480ff646e79cacc2812c55ef26}

Nom du dossier et du fichier de base pour les fichiers journaux du Superviseur de serveur. Le chemin d’accès peut être absolu ou relatif à *[!DNL install_folder]*. Le Superviseur du serveur ajoute un trait d&#39;union et la date actuelle ( *[!DNL -yyyy-mm-dd]*) au nom de fichier (avant le suffixe de fichier, le cas échéant). Adobe vous recommande d’envoyer tous les fichiers journaux dans le même dossier que [!DNL Platform Server] fichiers journaux ( `PS::LogFolder`) afin d’utiliser la gestion des fichiers journaux implémentée par [!DNL Platform Server] (`PS::LogDays`). La valeur par défaut est [!DNL logs/Supervisor.log].

>[!NOTE]
>
>Le nouveau dossier doit être créé avant de modifier ce paramètre. Assurez-vous que les autorisations d’accès sont définies de sorte que le superviseur de serveur dispose des privilèges de création, de lecture et d’écriture nécessaires.

## SV::tracelevel - Niveau de journal de suivi du superviseur de serveur {#section-36f8634741da4c618d67aa628b5fe474}

Le niveau de journalisation peut être 1, 2, 3 ou 4. La valeur par défaut est 2.

## IS::Log - Chemin du fichier journal de débogage du serveur d’images {#section-73a3f09b77f2446c9f82207b7d8aec39}

Nom du dossier et du fichier de base pour les fichiers journaux de trace Image Server. Le chemin d’accès peut être absolu ou relatif à *[!DNL install_folder]*. ImageServer ajoute un trait d’union et la date actuelle ( *[!DNL -yyyy-mm-dd]*) au nom du fichier (avant le suffixe du fichier, le cas échéant). Adobe recommande d’envoyer les fichiers journaux du serveur d’images dans le même dossier que [!DNL Platform Server] fichiers journaux ( `PS::LogFolder`) afin d’utiliser la gestion des fichiers journaux implémentée par le [!DNL Platform Server] (voir `PS::LogDays`).

>[!NOTE]
>
>Le nouveau dossier doit être créé avant de modifier ce paramètre. Assurez-vous que les autorisations d’accès sont définies de sorte que la diffusion d’images dispose des privilèges de création, de lecture et d’écriture nécessaires.

## IS:TraceClient - Niveau du journal de débogage du serveur d’images {#section-3851f1f68e404430985c629ac80534db}

Le niveau de journalisation peut être 1, 2, 3 ou 4 (la valeur par défaut est 2)

Le niveau 1 enregistre les événements liés au démarrage, à l’arrêt et à la [!DNL Platform Server] des connexions.

Le niveau 2 enregistre également la connexion et la déconnexion des images sources.

Le niveau 3 ajoute la journalisation des demandes de données de pixels et leur diffusion au [!DNL Platform Server].

Le niveau 4 enregistre tous les messages reçus du [!DNL Platform Server].

Les niveaux 3 et 4 ne doivent être utilisés qu’à des fins de débogage, car les fichiers journaux peuvent devenir volumineux.

## IS::TraceStatsInterval - Intervalle du journal des statistiques du serveur d’images {#section-1d8df96d61044e33a5b2b2b0309c2d59}

Le serveur d’images écrit des statistiques de mémoire dans son fichier journal de suivi à l’intervalle spécifié par ce paramètre. La plage valide est comprise entre 5 et 86 400 secondes.
