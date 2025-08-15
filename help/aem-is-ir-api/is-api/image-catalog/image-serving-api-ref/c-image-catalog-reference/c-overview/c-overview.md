---
description: Les catalogues d’images sont utilisés pour fournir au serveur des informations sur les images et les données annexes (telles que les polices et les profils ICC).
solution: Experience Manager
title: présentation
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# présentation{#overview}

Les catalogues d’images sont utilisés pour fournir au serveur des informations sur les images et les données annexes (telles que les polices et les profils ICC).

Les catalogues d’images sont utilisés pour fournir au serveur des informations sur les images et les données annexes (telles que les polices et les profils ICC).

Chaque catalogue d’images se compose d’un fichier d’attributs de catalogue obligatoire et d’un ensemble de fichiers de données de catalogue facultatifs :

* Le fichier de données d’image, qui énumère les images et les modèles ainsi que leurs métadonnées associées.
* Le fichier de données SVG qui énumère les fichiers SVG et leurs métadonnées associées.
* Le fichier de définitions de macro, qui fournit des définitions pour les macros de requête.
* Le fichier de mappage des polices, qui effectue le suivi des polices de texte.
* Le fichier de mappage de profils qui énumère les profils de couleurs ICC.
* Le fichier d’ensemble de règles, qui définit les règles de prétraitement des requêtes HTTP.

Les fichiers de données de catalogue sont associés aux catalogues d’images par des références de fichier dans le fichier d’attributs de catalogue. Un même fichier de données de catalogue peut être partagé par plusieurs catalogues d’images.

Les fichiers d’attributs de catalogue doivent comporter un suffixe de fichier [!DNL .ini] et se trouver dans le dossier de catalogue de l’[!DNL Platform Server] ( `PlatformServer::catalog.rootPath`). Les fichiers de données du catalogue peuvent se trouver dans le même dossier ou dans tout autre dossier accessible au [!DNL Platform Server].

Ce document décrit le format de fichier du catalogue d’images pour le système de diffusion d’images Dynamic Media. L’audience ciblée est constituée de programmeurs et de développeurs de sites web expérimentés qui souhaitent utiliser la diffusion d’images Dynamic Media pour une application web ou personnalisée.

On suppose que le lecteur connaît généralement le système de diffusion d’images Dynamic Media, les normes et conventions générales du protocole HTTP et la terminologie de base de l’imagerie.
