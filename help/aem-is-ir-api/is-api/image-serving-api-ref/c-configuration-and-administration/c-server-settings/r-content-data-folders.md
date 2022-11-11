---
description: Utilisez ces paramètres de serveur pour les dossiers de données de contenu.
solution: Experience Manager
title: Dossiers de données de contenu
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Dossiers de données de contenu{#content-data-folders}

Utilisez ces paramètres de serveur pour les dossiers de données de contenu.

## IS::RootPath - Dossiers racine des données d’image {#section-5c57569514bb4d00b19de31d2e137e3b}

L’emplacement de toutes les données source, y compris les images, les polices et les profils ICC. Il peut s’agir d’un ou plusieurs chemins ou chemins de fichier absolus par rapport à *[!DNL install_folder]*, séparés par des points-virgules. Si vide, *[!DNL install_folder]* est la racine par défaut. Plusieurs valeurs peuvent être spécifiées pour distribuer des données d’image sur plusieurs systèmes de fichiers. Le serveur d’images tente les chemins d’accès racine dans l’ordre spécifié jusqu’à ce que le fichier demandé soit trouvé.

## PS::staticContent.rootPath - Dossiers racine de données de contenu statique {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

L’emplacement des données de source de contenu statique destinées à être diffusées via le [!DNL /is/static] contexte. Peut contenir un ou plusieurs chemins ou chemins d’accès absolus relatifs à *[!DNL install_folder]*, séparés par des points-virgules. Si vide, *[!DNL install_folder]* est la racine par défaut.

Plusieurs valeurs peuvent être spécifiées, séparées par des points-virgules, afin de répartir le contenu statique sur plusieurs systèmes de fichiers. Généralement défini sur les mêmes valeurs que `IS::RootPath`.

Le [!DNL Platform Server] tente les chemins d’accès racine dans l’ordre spécifié jusqu’à ce que le fichier demandé soit trouvé.

>[!NOTE]
>
>Par défaut, ce champ est délibérément défini sur un emplacement non existant ( [!DNL] *[!DNL install_folder]*/static]), désactivant efficacement le service de contenu statique.

## IS::SaveDirectory - Fichier Enregistrer le dossier racine {#section-1c517f8d49ce4cb8b9013e520bf309c9}

Le chemin d’accès racine pour `attribute::SavePath` (utilisé par `req=saveToFile`). Le serveur d’images doit disposer des autorisations de création d’accès pour le sous-dossier dans lequel il va créer des fichiers image.
