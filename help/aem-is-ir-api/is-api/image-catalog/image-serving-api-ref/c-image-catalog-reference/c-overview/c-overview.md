---
description: Les catalogues d’images sont utilisés pour fournir des informations sur les images et les données de prise en charge (telles que les polices et les  ICC) au serveur.
seo-description: Les catalogues d’images sont utilisés pour fournir des informations sur les images et les données de prise en charge (telles que les polices et les  ICC) au serveur.
seo-title: présentation
solution: Experience Manager
title: présentation
topic: Scene7 Image Serving - Image Rendering API
uuid: e8c0401b-9161-4624-babb-6c7afb443e65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Aperçu{#overview}

Les catalogues d’images sont utilisés pour fournir des informations sur les images et les données de prise en charge (telles que les polices et les  ICC) au serveur.

Les catalogues d’images sont utilisés pour fournir des informations sur les images et les données de prise en charge (telles que les polices et les  ICC) au serveur.

Chaque catalogue d’images se compose d’un fichier d’attribut de catalogue obligatoire et d’un ensemble de fichiers de données de catalogue facultatifs :

* Fichier de données image, qui répertorie les images et les modèles et leurs métadonnées associées.
* Fichier de données SVG, qui répertorie les fichiers SVG et leurs métadonnées associées.
* Fichier de définitions de macro, qui fournit des définitions pour les macros de demande.
* Fichier de mappage des polices, qui effectue le suivi des polices de texte.
* Le fichier de mappage , qui répertorie les de couleurs ICC .
* Fichier de jeu de règles, qui définit les règles de prétraitement des requêtes HTTP.

Les fichiers de données de catalogue sont associés aux catalogues d’images par référence de fichier dans le fichier d’attribut de catalogue. Le même fichier de données de catalogue peut être partagé par plusieurs catalogues d’images.

Les fichiers d’attribut de catalogue doivent avoir un suffixe de [!DNL .ini] fichier et se trouver dans le dossier de catalogue du serveur de plateformes ( `PlatformServer::catalog.rootPath`). Les fichiers de données de catalogue peuvent se trouver dans le même dossier ou dans tout autre dossier accessible au serveur de plateformes.

Ce décrit le format de fichier du catalogue d’images pour le système de diffusion d’images Scene7. Le  prévu est constitué de développeurs expérimentés et de développeurs de sites Web qui souhaitent exploiter Scene7 Image Serving pour une application Web ou personnalisée.

Le lecteur est généralement familiarisé avec le système Scene7 Image Serving, les normes et conventions de protocole HTTP générales et la terminologie de base de l’imagerie.
