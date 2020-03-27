---
description: Les fichiers de données source de contenu statique sont accessibles uniquement par le serveur de plateformes.
seo-description: Les fichiers de données source de contenu statique sont accessibles uniquement par le serveur de plateformes.
seo-title: Données de source de contenu statique
solution: Experience Manager
title: Données de source de contenu statique
topic: Scene7 Image Serving - Image Rendering API
uuid: a3280ce7-20d7-4f4b-bf3e-e77cc7aca35f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Données de source de contenu statique{#static-content-source-data}

Les fichiers de données source de contenu statique sont accessibles uniquement par le serveur de plateformes.

Le chemin d’accès des fichiers de données de contenu statique est résolu comme suit :

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

Le serveur combine les segments de chemin de droite à gauche jusqu’à ce qu’un chemin de fichier absolu soit établi.

Tous les ` *[!DNL rootPath]*` segments peuvent être des segments de chemin vides, relatifs ou absolus.

` *[!DNL catalogPath]*` est un chemin/nom de fichier absolu ou relatif. *[!DNL requestPath]* doit être un chemin/nom de fichier relatif.

Plusieurs `PS::staticContent.rootPaths` valeurs peuvent être définies dans [!DNL PlatformServer.conf]. Cela permet de répartir les fichiers de données source sur plusieurs systèmes de fichiers. Le serveur de plateformes tentera d’utiliser d’autres chemins dans l’ordre spécifié jusqu’à ce que le fichier de données soit trouvé.
