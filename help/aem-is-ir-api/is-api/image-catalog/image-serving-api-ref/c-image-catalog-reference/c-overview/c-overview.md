---
description: Les catalogues d’images sont utilisés pour fournir au serveur des informations sur les images et les données prises en charge (telles que les polices et les profils ICC).
seo-description: Les catalogues d’images sont utilisés pour fournir au serveur des informations sur les images et les données prises en charge (telles que les polices et les profils ICC).
seo-title: présentation
solution: Experience Manager
title: présentation
uuid: e8c0401b-9161-4624-babb-6c7afb443e65
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---


# Aperçu{#overview}

Les catalogues d’images sont utilisés pour fournir au serveur des informations sur les images et les données prises en charge (telles que les polices et les profils ICC).

Les catalogues d’images sont utilisés pour fournir au serveur des informations sur les images et les données prises en charge (telles que les polices et les profils ICC).

Chaque catalogue d’images se compose d’un fichier d’attributs de catalogue requis et d’un ensemble de fichiers de données de catalogue facultatifs :

* Le fichier de données image, qui répertorie les images et les modèles et leurs métadonnées associées.
* Le fichier de données SVG, qui répertorie les fichiers SVG et leurs métadonnées associées.
* Fichier de définitions de macro qui fournit des définitions pour les macros de demande.
* Fichier de mappage des polices, qui conserve le suivi des polices de texte.
* Le fichier de mappage de profil, qui répertorie les profils de couleur ICC.
* Fichier de jeu de règles qui définit les règles de prétraitement des requêtes HTTP.

Les fichiers de données de catalogue sont associés aux catalogues d’images par référence de fichier dans le fichier d’attribut de catalogue. Le même fichier de données de catalogue peut être partagé par plusieurs catalogues d’images.

Les fichiers d’attribut de catalogue doivent avoir un suffixe de fichier [!DNL .ini] et être situés dans le dossier de catalogue de Platform Server ( `PlatformServer::catalog.rootPath`). Les fichiers de données de catalogue peuvent se trouver dans le même dossier ou dans tout autre dossier accessible au serveur de plateformes.

Ce document décrit le format de fichier du catalogue d’images pour le système de diffusion d’images Dynamic Media. L’audience souhaitée est destinée aux développeurs chevronnés et de sites Web qui souhaitent exploiter Dynamic Media Image Serving pour une application Web ou personnalisée.

On suppose que le lecteur est généralement familier avec le système de diffusion d’images de Dynamic Media, les normes et conventions de protocole HTTP générales et la terminologie de base de l’imagerie.
