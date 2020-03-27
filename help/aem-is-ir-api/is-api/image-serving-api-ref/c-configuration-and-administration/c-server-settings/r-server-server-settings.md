---
description: Utilisez ces paramètres de serveur pour configurer votre serveur.
seo-description: Utilisez ces paramètres de serveur pour configurer votre serveur.
seo-title: Serveur
solution: Experience Manager
title: Serveur
topic: Scene7 Image Serving - Image Rendering API
uuid: 50db98cc-8354-4884-9416-00808828061b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Serveur{#server}

Utilisez ces paramètres de serveur pour configurer votre serveur.

## SV::ImageServerMode - Mode Image Server {#section-991b287f2dde4f77a24fc69d5b32cabd}

Les versions 32 et 64 bits du serveur Image Server sont disponibles pour Linux. Spécifiez ImageServer64 lorsqu’il est installé sur des serveurs Linux 64 bits ou ImageServer32 (valeur par défaut) lorsqu’il est installé sur des serveurs 32 bits.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>La version 64 bits d’Image Server ne prend pas en charge les fichiers source FlashPix.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Le mode 64 bits n’est pas pris en charge sous Windows. Seul `ImageServer32` peut être spécifié. Dans le cas contraire, la diffusion d’images ne  pas.

## SV::PsHeapSize - Platform Server Heap Size {#section-fd83715948764aeda58d6b3a9f9f8be9}

Taille du tas Java pour le serveur de plateformes. La valeur par défaut est &quot; `512m`&quot; (512 Mo).

## IS::TcpPort, PS::isConnection.port - Port d’écoute Image Server {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Spécifie le port utilisé pour la communication entre le serveur de plateformes et le serveur d’images. Veillez à spécifier un numéro de port qui n’est pas utilisé autrement sur le système hôte.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Pour que la diffusion d’images fonctionne correctement, la même valeur doit être définie pour `IS::TcpPort` et `PS::isConnection.port`.

## IS::PhysicalMemory - Limite de mémoire du serveur d’images {#section-85e37aa2ac6e456eb698da716dd3247d}

Limite approximative des données d’image en mémoire, exprimée en pourcentage de la mémoire physique. La plage valide est comprise entre 10 % et 90 %. Le serveur d’images tente, si possible, de limiter son utilisation de la mémoire d’image à la quantité spécifiée. La limite peut être temporairement dépassée pendant  traitement intensif .

## IS::WorkerThreads - Nombre de threads de travail Image Server {#section-e2946063b13c4f728cdf5dba3d8b4de1}

nombre maximal de threads que le serveur Image Server utilise pour traiter les données image. La valeur par défaut est 0, ce qui permet au serveur Image Server d’optimiser automatiquement le nombre de threads.

Certains systèmes d’exploitation ont des modèles de thread avec une forte charge de commutation de contexte. Dans de telles circonstances, les performances globales du serveur peuvent s&#39;améliorer lorsqu&#39;un nombre de threads spécifique est sélectionné (par exemple, un thread par UC). Certaines expériences peuvent être nécessaires pour trouver le paramètre optimal. Pour plus d’informations, reportez-vous aux notes de mise à jour de la diffusion d’images et à la documentation du système d’exploitation.

## IS::NumberOfTextServers - Nombre d’instances du serveur de texte {#section-971e20a90c1a473598fba738ed95671a}

Nombre maximal de rendus de texte à activer simultanément. 0 (par défaut) équivaut à 1,5 fois le nombre de coeurs de processeur disponibles.

## IS::TextServerTcpPortRange - Ports de communication du serveur de texte {#section-a13465de88ed4df09931e5ba840c1942}

Ports à utiliser pour les communications du serveur de texte. Spécifiez le premier et le dernier numéro de port, séparés par &quot;-&quot;.
