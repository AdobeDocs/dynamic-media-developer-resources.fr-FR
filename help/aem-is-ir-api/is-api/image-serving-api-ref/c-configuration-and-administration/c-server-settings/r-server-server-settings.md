---
description: Utilisez ces paramètres de serveur pour configurer votre serveur.
solution: Experience Manager
title: Serveur
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---


# Serveur{#server}

Utilisez ces paramètres de serveur pour configurer votre serveur.

## SV::ImageServerMode - Mode Image Server {#section-991b287f2dde4f77a24fc69d5b32cabd}

Les versions 32 et 64 bits d’Image Server sont disponibles pour Linux. Spécifiez ImageServer64 lorsqu’il est installé sur des serveurs Linux 64 bits ou ImageServer32 (par défaut) lorsqu’il est installé sur des serveurs 32 bits.

>[!NOTE]
>
>La version 64 bits d’Image Server ne prend pas en charge les fichiers source FlashPix.

>[!NOTE]
>
>Le mode 64 bits n’est pas pris en charge sous Windows. Seul `ImageServer32` peut être spécifié. Sinon, la diffusion d’images ne sera pas début.

## SV::PsHeapSize - Platform Server Heap Size {#section-fd83715948764aeda58d6b3a9f9f8be9}

Taille du tas Java pour le serveur de plateformes. Valeur par défaut : &quot; `512m`&quot; (512 Mo).

## IS::TcpPort, PS::isConnection.port - Port d’écoute Image Server {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Spécifie le port utilisé pour la communication entre le serveur de plateformes et le serveur d’images. Veillez à spécifier un numéro de port qui n&#39;est pas utilisé autrement sur le système hôte.

>[!NOTE]
>
>Pour que la diffusion d’images fonctionne correctement, la même valeur doit être définie pour `IS::TcpPort` et `PS::isConnection.port`.

## IS::PhysicalMemory - Image Server Memory Limit {#section-85e37aa2ac6e456eb698da716dd3247d}

Limite approximative des données d’image en mémoire, exprimée en pourcentage de la mémoire physique. La plage valide est comprise entre 10 % et 90 %. Si possible, le serveur d’images tente de limiter son utilisation de la mémoire d’image à la quantité spécifiée. La limite peut être dépassée temporairement pendant l&#39;activité de traitement intensif.

## IS::WorkerThreads - Nombre de threads Image Server Worker {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Nombre maximal de threads que le serveur d’images utilise pour traiter les données image. La valeur par défaut est 0, ce qui permet au serveur d’images d’optimiser automatiquement le nombre de threads.

Certains systèmes d&#39;exploitation ont des modèles de thread avec une charge de commutation de contexte élevée. Dans ce cas, les performances globales du serveur peuvent s&#39;améliorer lorsqu&#39;un nombre de threads spécifique est sélectionné (par exemple un thread par processeur). Certaines expérimentations peuvent être nécessaires pour trouver le paramètre optimal. Pour plus d’informations, reportez-vous aux Notes de mise à jour d’Image Serving et à la documentation du système d’exploitation.

## IS::NumberOfTextServers - Nombre d’instances de serveur de texte {#section-971e20a90c1a473598fba738ed95671a}

Nombre maximal de rendus de texte à principal simultanément. 0 (par défaut) équivaut à 1,5 fois le nombre de coeurs de processeur disponibles.

## IS::TextServerTcpPortRange - Ports de communication du serveur de texte {#section-a13465de88ed4df09931e5ba840c1942}

Ports à utiliser pour les communications de serveur de texte. Spécifiez le premier et le dernier numéro de port, séparés par &quot;-&quot;.
