---
description: Utilisez ces paramètres de serveur pour les dossiers de données de contenu.
seo-description: Utilisez ces paramètres de serveur pour les dossiers de données de contenu.
seo-title: Dossiers de données de contenu
solution: Experience Manager
title: Dossiers de données de contenu
topic: Scene7 Image Serving - Image Rendering API
uuid: 7c4d60ca-8a8b-453c-887d-a6a16eacc883
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---


# Dossiers de données de contenu{#content-data-folders}

Utilisez ces paramètres de serveur pour les dossiers de données de contenu.

## IS::RootPath - Dossiers racine des données image {#section-5c57569514bb4d00b19de31d2e137e3b}

Emplacement de toutes les données source, y compris les images, les polices et les profils ICC. Il peut s’agir d’un ou plusieurs chemins d’accès ou chemins de fichier absolus par rapport à *[!DNL install_folder]*, séparés par des points-virgules. S’il est vide, *[!DNL install_folder]* il s’agit de la racine par défaut. Plusieurs valeurs peuvent être spécifiées pour distribuer des données d’image sur plusieurs systèmes de fichiers. Le serveur d’images tentera les chemins d’accès racine dans l’ordre spécifié jusqu’à ce que le fichier demandé soit trouvé.

## PS::staticContent.rootPath - Dossiers racine de données de contenu statique {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

Emplacement des données de source de contenu statique destinées à être diffusées par le [!DNL /is/static] contexte. Il peut s’agir d’un ou plusieurs chemins d’accès ou chemins de fichier absolus par rapport à *[!DNL install_folder]*, séparés par des points-virgules. S’il est vide, *[!DNL install_folder]* il s’agit de la racine par défaut.

Plusieurs valeurs peuvent être spécifiées, séparées par des points-virgules, pour distribuer le contenu statique sur plusieurs systèmes de fichiers. En règle générale, définissez les mêmes valeurs que `IS::RootPath`.

Le serveur Platform tente les chemins d’accès racine dans l’ordre spécifié jusqu’à ce que le fichier demandé soit trouvé.

>[!NOTE]
>
>Par défaut, ce champ est délibérément défini sur un emplacement non existant ( [ !DNL *[!DNL install_folder]*/static]), ce qui désactive le service de contenu statique.

## IS::SaveDirectory - Fichier Enregistrer le dossier racine {#section-1c517f8d49ce4cb8b9013e520bf309c9}

Chemin d’accès racine pour `attribute::SavePath` (utilisé par `req=saveToFile`). Le serveur Image Server doit disposer des autorisations de création d’accès pour le sous-dossier dans lequel il va créer des fichiers image.
