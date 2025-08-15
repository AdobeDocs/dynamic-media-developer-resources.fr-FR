---
description: Cette documentation explique comment administrer le serveur Dynamic Media Image Rendering.
solution: Experience Manager
title: Présentation de l’administration du serveur
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Présentation de l’administration du serveur{#server-administration-overview}

Cette documentation explique comment administrer le serveur Dynamic Media Image Rendering.

Le rendu d’image se compose de deux composants principaux :

* Un package Java est déployé avec Image Serving [!DNL Platform Server] et gère la connexion cliente, la mise en cache et les catalogues de matériaux.
* Un module de code natif est déployé en tant que bibliothèque d’extension pour Image Server et implémente les fonctionnalités de base de rendu d’image.

Les deux composants sont collectivement appelés serveur de *rendu*.

Image Rendering partage de nombreuses installations serveur avec Image Server, et toutes les options sont configurées en modifiant un fichier de configuration. Des attributs de configuration supplémentaires sont fournis par le catalogue par défaut ( [!DNL default.ini]) ou des catalogues de matériaux spécifiques. Voir Catalogues de matériaux pour plus de détails.

Le dossier d’installation d’Image Rendering ( *[!DNL install_folder]*) est [!DNL *[!DNL install_root]*/ImageRendering]. Sous Windows, la valeur par défaut *[!DNL install_root]* est `C:\Program Files\Scene7`. Un autre dossier peut être spécifié pendant l’installation. Sous Linux, *[!DNL install_root]* doit toujours être [!DNL /usr/local/scene7]. Des liens symboliques peuvent être utilisés.

Tous les chemins d’accès aux fichiers sont sensibles à la casse sous UNIX et à la casse sous Windows.
