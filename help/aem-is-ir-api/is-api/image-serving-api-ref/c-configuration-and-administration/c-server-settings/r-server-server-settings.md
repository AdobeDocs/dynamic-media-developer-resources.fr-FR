---
description: Utilisez ces paramètres de serveur pour configurer votre serveur.
solution: Experience Manager
title: Serveur
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
TQID: 'https://experienceleague.adobe.com/403CInOL4425Gv35Njb69WSo-QRyvTuDUZEBtNRsvj0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 357
ht-degree: 0%

---

# Serveur{#server}

Utilisez ces paramètres de serveur pour configurer votre serveur.

## SV::ImageServerMode - Mode Serveur d’images {#section-991b287f2dde4f77a24fc69d5b32cabd}

Une version 32 bits et une version 64 bits du serveur d’images sont disponibles pour Linux. Spécifiez ImageServer64 lors de l’installation sur des serveurs Linux 64 bits ou ImageServer32 (par défaut) lors de l’installation sur des serveurs 32 bits.

>[!NOTE]
>
>La version 64 bits du serveur d’images ne prend pas en charge les fichiers sources FlashPix.

>[!NOTE]
>
>Le mode 64 bits n’est pas pris en charge sous Windows. Seul `ImageServer32` peut être spécifié. Sinon, la diffusion d’images ne démarre pas.

## SV::PsHeapSize - Taille du tas [!DNL Platform Server] {#section-fd83715948764aeda58d6b3a9f9f8be9}

Taille du tas Java du [!DNL Platform Server]. La valeur par défaut est « `512m` » (512 Mo).

## IS::TcpPort, PS::isConnection.port - Port d’écoute du serveur d’images {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Indique le port utilisé pour la communication entre le [!DNL Platform Server] et le serveur d’images. Veillez à spécifier un numéro de port qui n&#39;est pas utilisé autrement sur le système hôte.

>[!NOTE]
>
>Pour que le service d’images fonctionne correctement, la même valeur doit être définie pour `IS::TcpPort` et `PS::isConnection.port`.

## IS::PhysicalMemory - Limite de mémoire du serveur d&#39;images {#section-85e37aa2ac6e456eb698da716dd3247d}

Limite approximative des données d’image en mémoire, exprimée en pourcentage de la mémoire physique. La plage valide est comprise entre 10 % et 90 %. Le serveur d’images tente, si possible, de limiter son utilisation de la mémoire d’image à la quantité spécifiée. La limite peut être dépassée temporairement pendant une activité de traitement intensive.

## IS::WorkerThreads - Nombre de Threads de traitement du serveur d’images {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Nombre maximal de threads que le serveur d’images utilise pour traiter les données d’image. La valeur par défaut est 0, ce qui permet au serveur d’images d’optimiser automatiquement le nombre de threads.

Certains systèmes d’exploitation disposent de modèles de thread avec une surcharge de commutation contextuelle élevée. Dans ce cas, les performances globales du serveur peuvent s’améliorer lorsqu’un nombre spécifique de threads est sélectionné (par exemple, un thread par CPU). Il peut être nécessaire de procéder à quelques expériences pour trouver le paramètre optimal. Reportez-vous aux notes de mise à jour du service d’images et à la documentation du système d’exploitation pour plus d’informations.

## IS::NumberOfTextServers - Nombre d&#39;instances de serveur de texte {#section-971e20a90c1a473598fba738ed95671a}

Nombre maximal de rendus de texte pouvant être actifs simultanément. 0 (par défaut) équivaut à 1,5 fois le nombre de cœurs CPU disponibles.

## IS::TextServerTcpPortRange - Ports de communication du serveur de texte {#section-a13465de88ed4df09931e5ba840c1942}

Ports à utiliser pour les communications du serveur de texte. Indiquez le premier et le dernier numéro de port, séparés par le caractère « - ».
