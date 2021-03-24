---
description: Cette documentation explique comment administrer le serveur de rendu d’image Dynamic Media.
solution: Experience Manager
title: Présentation de l’administration du serveur
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---


# Présentation de l&#39;administration du serveur{#server-administration-overview}

Cette documentation explique comment administrer le serveur de rendu d’image Dynamic Media.

Le rendu d’image se compose de deux composants principaux :

* Un package Java est déployé avec le serveur de plate-forme Image Serving et gère la connexion client, la mise en cache et les catalogues de matériaux.
* Un module de code natif est déployé en tant que bibliothèque d’extensions pour le serveur d’images et met en oeuvre les fonctionnalités de rendu d’image de base.

Les deux composants sont collectivement appelés *Render Server*.

Image Rendering partage de nombreuses fonctionnalités de serveur avec Image Serving et toutes les options sont configurées en modifiant un fichier de configuration. D&#39;autres attributs de configuration sont fournis par le catalogue par défaut ( [!DNL default.ini]) ou des catalogues de matières spécifiques. Voir Catalogues de matières pour plus d&#39;informations.

Le dossier d’installation du rendu d’image ( *[!DNL install_folder]*) est [ !DNL *[!DNL install_root]*/ImageRendering]. Sous Windows, la valeur par défaut *[!DNL install_root]* est `C:\Program Files\Scene7`. Un autre dossier peut être spécifié lors de l&#39;installation. Sous Linux, *[!DNL install_root]* doit toujours être [!DNL /usr/local/scene7]. Des liens symboliques peuvent être utilisés.

Tous les chemins d’accès aux fichiers sont sensibles à la casse sous UNIX et non à la casse sous Windows.
