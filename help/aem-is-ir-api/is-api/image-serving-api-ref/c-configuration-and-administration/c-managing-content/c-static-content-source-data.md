---
description: Les fichiers de données source de contenu statique sont accessibles uniquement par le serveur de plateformes.
seo-description: Les fichiers de données source de contenu statique sont accessibles uniquement par le serveur de plateformes.
seo-title: Données de la source de contenu statique
solution: Experience Manager
title: Données de la source de contenu statique
topic: Scene7 Image Serving - Image Rendering API
uuid: a3280ce7-20d7-4f4b-bf3e-e77cc7aca35f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# Données de la source de contenu statique{#static-content-source-data}

Les fichiers de données source de contenu statique sont accessibles uniquement par le serveur de plateformes.

Le chemin d’accès des fichiers de données de contenu statique est résolu comme suit :

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

Le serveur combine les segments de chemin d’accès de droite à gauche jusqu’à ce qu’un chemin d’accès absolu au fichier soit établi.

Tous les segments ` *[!DNL rootPath]*` peuvent être des segments de chemin vides, relatifs ou absolus.

` *[!DNL catalogPath]*` est un chemin/nom de fichier absolu ou relatif. *[!DNL requestPath]* doit être un chemin/nom de fichier relatif.

Plusieurs valeurs `PS::staticContent.rootPaths` peuvent être définies dans [!DNL PlatformServer.conf]. Cela permet de distribuer les fichiers de données source sur plusieurs systèmes de fichiers. Le serveur de plateformes tentera d&#39;autres chemins dans l&#39;ordre spécifié jusqu&#39;à ce que le fichier de données soit trouvé.
