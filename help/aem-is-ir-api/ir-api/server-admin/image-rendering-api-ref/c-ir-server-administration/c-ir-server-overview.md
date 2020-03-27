---
description: Cette documentation explique comment administrer le serveur de rendu d’image Scene7.
seo-description: Cette documentation explique comment administrer le serveur de rendu d’image Scene7.
seo-title: Présentation de l’administration du serveur
solution: Experience Manager
title: Présentation de l’administration du serveur
topic: Scene7 Image Serving - Image Rendering API
uuid: 83aa83b7-bb7a-4bbd-923c-dd69763fe9c9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Présentation de l’administration du serveur{#server-administration-overview}

Cette documentation explique comment administrer le serveur de rendu d’image Scene7.

Le rendu d’image se compose de deux composants principaux :

* Un package Java est déployé avec le serveur de plate-forme Image Serving et gère la connexion client, la mise en cache et les catalogues de matériaux.
* Un module de code natif est déployé en tant que bibliothèque d’extensions pour le serveur d’images et met en oeuvre les fonctionnalités de rendu d’image de base.

Les deux composants sont collectivement appelés *Render Server*.

Image Rendering partage de nombreuses fonctionnalités de serveur avec Image Serving, et toutes les options sont configurées en modifiant un fichier de configuration. D’autres attributs de configuration sont fournis par le catalogue par défaut ( [!DNL default.ini]) ou des catalogues de matières spécifiques. Voir Catalogues de matières pour plus d’informations.

Le dossier d’installation du rendu d’image ( *[!DNL install_folder]*) est [!DNL *[!DNL install_root]*/ImageRendering]. Sous Windows, la valeur par défaut *[!DNL install_root]* est [!DNL C:\Program Files\Scene7]. Un dossier différent peut être spécifié lors de l’installation. Sous Linux, *[!DNL install_root]* doit toujours être [!DNL /usr/local/scene7]. Des liens symboliques peuvent être utilisés.

Tous les chemins d’accès aux fichiers sont sensibles à la casse sous UNIX et non à la casse sous Windows.
