---
description: Utilisez ces paramètres de serveur pour le service de catalogue d’images.
solution: Experience Manager
title: Service de catalogue d’images
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
TQID: 'https://experienceleague.adobe.com/Fs2xGD3Dpd8pe5jtto4kPMF0BrJiLNRvdBn8RSPiQjw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 197
ht-degree: 0%

---

# Service de catalogue d’images{#image-catalog-service}

Utilisez ces paramètres de serveur pour le service de catalogue d’images.

## CS::catalog.rootPath - Dossier de catalogue d’images {#section-02d107f157384b18835f884f24fea3aa}

Emplacement du dossier du catalogue d’images (où tous les fichiers [!DNL catalog.ini] doivent se trouver). Il peut s’agir d’un chemin d’accès absolu au fichier ou d’un chemin relatif au *[!DNL install_folder]*. Le serveur surveille en permanence ce dossier et charge ou recharge les catalogues lorsqu’un nouveau fichier catalogue principal (avec [!DNL .ini] suffixe de fichier) est détecté ou lorsque l’heure de dernière modification d’un fichier catalogue principal existant a changé.

## CS::catalog.cacheRoot - Dossier du cache de catalogue {#section-73e499c3a5974f1aa4251e70272ff503}

Dossier racine du cache du système de catalogue. Peut être défini sur le même que l’un des dossiers dans `PS::cache.rootPaths`. Le dossier doit être créé manuellement avant la modification de ce paramètre.

## CS::catalog.modificationWaitTime - Délai d’analyse du fichier catalogue {#section-7348065bcc124cb68ea947bf1b9b0845}

Durée en ms pendant laquelle le service de catalogue attend qu’un fichier [!DNL catalog.ini] soit modifié avant de charger les fichiers de catalogue secondaires. Ce délai permet de s’assurer que tous les fichiers de catalogue secondaires sont à jour avant que le service de catalogue ne tente de les charger. Valeur entière en ms.

## CS::catalog.refreshInterval - Fréquence de vérification des fichiers de catalogue {#section-517fefc1d8784777a1026abec8630d58}

Fréquence à laquelle le service de catalogue vérifie les modifications apportées aux catalogues d’images. Valeur entière en ms.
