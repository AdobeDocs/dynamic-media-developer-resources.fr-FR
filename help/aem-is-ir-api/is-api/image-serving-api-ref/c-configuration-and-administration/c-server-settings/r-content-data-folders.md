---
description: Utilisez ces paramètres de serveur pour les dossiers de données de contenu.
solution: Experience Manager
title: Dossiers de données de contenu
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Dossiers de données de contenu{#content-data-folders}

Utilisez ces paramètres de serveur pour les dossiers de données de contenu.

## IS ::RootPath - Dossiers racine de données image {#section-5c57569514bb4d00b19de31d2e137e3b}

L’emplacement de toutes les données sources, y compris les images, les polices et les profils ICC. Il peut s’agir d’un ou de plusieurs chemins absolus de fichier ou relatifs à *[!DNL install_folder]*, séparés par des points-virgules. Si elle est vide, *[!DNL install_folder]* est la racine par défaut. Plusieurs valeurs peuvent être spécifiées pour répartir les données image sur plusieurs systèmes de fichiers. Le serveur d’images essaie les chemins racines dans l’ordre spécifié jusqu’à ce que le fichier demandé soit trouvé.

## PS ::staticContent.rootPath - Contenu statique Dossiers racine de données {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

Emplacement des données de source de contenu statique destinées à être fournies par le [!DNL /is/static] biais du contexte. Il peut y avoir un ou plusieurs chemins absolus de fichier ou relatifs à *[!DNL install_folder]*, séparés par des points-virgules. Si elle est vide, *[!DNL install_folder]* est la racine par défaut.

Plusieurs valeurs peuvent être spécifiées, séparées par des points-virgules, pour répartir le contenu statique sur plusieurs systèmes de fichiers. Généralement définie sur les mêmes valeurs que `IS::RootPath`.

Le [!DNL Platform Server] teste les chemins racine dans l’ordre indiqué jusqu’à ce que le fichier demandé soit trouvé.

>[!NOTE]
>
>Par défaut, ce champ est intentionnellement défini sur un emplacement inexistant ( [!DNL *[!DNL install_folder]*/static]), désactivant efficacement le service de contenu statique.

## IS ::SaveDirectory - Enregistrement du fichier Dossier racine {#section-1c517f8d49ce4cb8b9013e520bf309c9}

Chemin d’accès racine pour `attribute::SavePath` (utilisé par `req=saveToFile`). Le serveur d’images doit disposer d’autorisations d’accès en création pour le sous-dossier dans lequel il crée des fichiers image.
