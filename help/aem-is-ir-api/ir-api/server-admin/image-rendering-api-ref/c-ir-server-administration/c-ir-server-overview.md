---
description: Cette documentation explique comment administrer le serveur de rendu d’image Dynamic Media.
solution: Experience Manager
title: Présentation de l’administration des serveurs
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# Présentation de l’administration des serveurs{#server-administration-overview}

Cette documentation explique comment administrer le serveur de rendu d’image Dynamic Media.

Le rendu d’image se compose de deux composants principaux :

* Un package Java est déployé avec le serveur de la plateforme de diffusion d’images et gère la connexion du client, la mise en cache et les catalogues de matériaux.
* Un module de code natif est déployé en tant que bibliothèque d’extension pour le serveur d’images et met en oeuvre les principales fonctionnalités de rendu d’image.

Les deux composants sont appelés collectivement *Render Server*.

Le rendu d’image partage de nombreuses fonctionnalités de serveur avec le serveur d’images, et toutes les options sont configurées en modifiant un fichier de configuration. Des attributs de configuration supplémentaires sont fournis par le catalogue par défaut ( [!DNL default.ini]) ou des catalogues de matériaux spécifiques. Pour plus d’informations, voir Catalogues de matières .

Le dossier d’installation Image Rendering ( *[!DNL install_folder]*) est [!DNL *[!DNL install_root]*/ImageRendering]. Sous Windows, la valeur par défaut *[!DNL install_root]* est `C:\Program Files\Scene7`. Un autre dossier peut être spécifié lors de l’installation. Sous Linux, *[!DNL install_root]* doit toujours être [!DNL /usr/local/scene7]. Des liens symboliques peuvent être utilisés.

Tous les chemins d’accès aux fichiers sont sensibles à la casse sous UNIX et non à la casse sous Windows.
