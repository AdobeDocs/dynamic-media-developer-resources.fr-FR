---
description: Utilisez ces paramètres de serveur pour configurer votre serveur.
solution: Experience Manager
title: Serveur
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 0%

---

# Serveur{#server}

Utilisez ces paramètres de serveur pour configurer votre serveur.

## SV ::ImageServerMode - Mode Serveur d’images {#section-991b287f2dde4f77a24fc69d5b32cabd}

Une version 32 bits et une version 64 bits d’Image Server sont disponibles pour Linux. Spécifiez ImageServer64 lorsqu’il est installé sur des serveurs Linux 64 bits ou ImageServer32 (par défaut) lorsqu’il est installé sur des serveurs 32 bits.

>[!NOTE]
>
>La version 64 bits d’Image Server ne prend pas en charge les fichiers sources FlashPix.

>[!NOTE]
>
>Le mode 64 bits n’est pas pris en charge sous Windows. Seule `ImageServer32` peut être spécifiée. Sinon, la diffusion d’images ne démarre pas.

## SV ::P sHeapSize – [!DNL Platform Server] Taille du tas {#section-fd83715948764aeda58d6b3a9f9f8be9}

Taille du tas Java pour le [!DNL Platform Server]fichier . La valeur par défaut est &quot; `512m`&quot; (512 Mo).

## IS ::TcpPort, PS ::isConnection.port - Port d’écoute du serveur d’images {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Spécifie le port utilisé pour la communication entre le serveur et [!DNL Platform Server] le serveur d’images. Veillez à spécifier un numéro de port qui n’est pas utilisé autrement sur le système hôte.

>[!NOTE]
>
>Pour que la diffusion d’images fonctionne correctement, la même valeur doit être définie pour `IS::TcpPort` et `PS::isConnection.port`.

## IS ::P hysicalMemory – Mémoire limite de mémoire du serveur d’images {#section-85e37aa2ac6e456eb698da716dd3247d}

Limite approximative pour les données d’image en mémoire, exprimée en pourcentage de la mémoire physique. La plage valide s’étend de 10 % à 90 %. Le serveur d’images tente de limiter son utilisation de la mémoire d’image à la quantité spécifiée si possible. La limite peut être dépassée temporairement lors d’une activité de traitement intensive.

## IS ::WorkerThreads - Nombre de threads de travail du serveur d’images {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Nombre maximal de threads que le serveur d’images utilise pour le traitement des données image. La valeur par défaut est 0, ce qui permet au serveur d’images d’optimiser automatiquement le nombre de threads.

Certains systèmes d’exploitation ont des modèles de threading avec une surcharge de commutation contextuelle élevée. Dans un tel cas, les performances globales du serveur peuvent s’améliorer lorsqu’un nombre de threads spécifique est sélectionné (par exemple, un thread par CPU). Des expériences peuvent être nécessaires pour trouver le réglage optimal. Reportez-vous aux notes de version de Image Serving et à la documentation du système d’exploitation pour plus d’informations.

## IS ::NumberOfTextServers - Nombre d’instances de serveur de texte {#section-971e20a90c1a473598fba738ed95671a}

nombre maximum de moteurs de rendu de texte à activer simultanément. 0 (valeur par défaut) équivaut à 1,5 fois le nombre de cœurs de processeur.

## IS ::TextServerTcpPortRange - Ports de communication de serveur de texte {#section-a13465de88ed4df09931e5ba840c1942}

Ports à utiliser pour les communications de serveur de texte. Spécifiez le premier et le dernier numéro de port, séparés par &#39;-&#39;.
