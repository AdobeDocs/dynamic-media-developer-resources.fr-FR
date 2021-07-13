---
description: Les catalogues d’images sont utilisés pour fournir au serveur des informations sur les images et les données de prise en charge (polices et profils ICC, par exemple).
solution: Experience Manager
title: présentation
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# présentation{#overview}

Les catalogues d’images sont utilisés pour fournir au serveur des informations sur les images et les données de prise en charge (polices et profils ICC, par exemple).

Les catalogues d’images sont utilisés pour fournir au serveur des informations sur les images et les données de prise en charge (polices et profils ICC, par exemple).

Chaque catalogue d’images se compose d’un fichier d’attributs de catalogue requis et d’un ensemble de fichiers de données de catalogue facultatifs :

* Le fichier de données image, qui énumère les images, les modèles et leurs métadonnées associées.
* Le fichier de données SVG, qui énumère les fichiers SVG et leurs métadonnées associées.
* Le fichier de définitions de macro qui fournit des définitions pour les macros de requête.
* Le fichier de mappage des polices, qui effectue le suivi des polices de texte.
* Le fichier de mappage de profil, qui énumère les profils de couleurs ICC.
* Fichier d’ensemble de règles qui définit les règles de prétraitement des requêtes HTTP.

Les fichiers de données de catalogue sont associés aux catalogues d’images par référence de fichier dans le fichier d’attributs de catalogue. Le même fichier de données de catalogue peut être partagé par plusieurs catalogues d’images.

Les fichiers d’attributs du catalogue doivent comporter un suffixe de fichier [!DNL .ini] et se trouver dans le dossier de catalogue du serveur de plateformes ( `PlatformServer::catalog.rootPath`). Les fichiers de données du catalogue peuvent se trouver dans le même dossier ou tout autre dossier accessible au serveur Platform.

Ce document décrit le format de fichier du catalogue d’images pour le système de diffusion d’images Dynamic Media. L’audience prévue est composée de programmeurs chevronnés et de développeurs de sites web qui souhaitent exploiter le service Dynamic Media Image Serving pour une application web ou personnalisée.

On suppose que le lecteur est généralement familiarisé avec le système de diffusion d’images Dynamic Media, les normes et conventions générales du protocole HTTP, ainsi qu’avec la terminologie de base de l’imagerie.
