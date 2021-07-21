---
description: Les fichiers de données source de contenu statique sont accessibles uniquement par le serveur Platform.
solution: Experience Manager
title: Données de source de contenu statique
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# Données de source de contenu statique{#static-content-source-data}

Les fichiers de données source de contenu statique sont accessibles uniquement par le serveur Platform.

Le chemin d’accès des fichiers de données de contenu statique est résolu comme suit :

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

Le serveur combine les segments de chemin d’accès de droite à gauche jusqu’à ce qu’un chemin d’accès absolu au fichier soit établi.

Tous les ` *[!DNL rootPath]*` segments peuvent être vides, relatifs ou absolus.

` *[!DNL catalogPath]*` est un chemin/nom de fichier absolu ou relatif. *[!DNL requestPath]* doit être un chemin/nom de fichier relatif.

Plusieurs `PS::staticContent.rootPaths` valeurs peuvent être définies dans [!DNL PlatformServer.conf]. Cela permet de répartir les fichiers de données sources sur plusieurs systèmes de fichiers. Le serveur Platform essaiera d’autres chemins d’accès dans l’ordre spécifié jusqu’à ce que le fichier de données soit trouvé.
