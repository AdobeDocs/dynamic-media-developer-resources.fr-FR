---
description: Les fichiers de données de source de contenu statique sont accessibles uniquement par le  [!DNL Platform Server].
solution: Experience Manager
title: Données de source de contenu statique
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Données de source de contenu statique{#static-content-source-data}

Les fichiers de données de source de contenu statique sont accessibles uniquement par [!DNL Platform Server].

Le chemin d’accès des fichiers de données de contenu statique est résolu comme suit :

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

Le serveur combine les segments de chemin d’accès de droite à gauche jusqu’à ce qu’un chemin d’accès absolu au fichier soit établi.

Tous les segments ` *[!DNL rootPath]*` peuvent être vides, relatifs ou absolus.

` *[!DNL catalogPath]*` est un chemin/nom de fichier absolu ou relatif. *[!DNL requestPath]* doit être un chemin/nom de fichier relatif.

Plusieurs valeurs `PS::staticContent.rootPaths` peuvent être définies dans [!DNL PlatformServer.conf]. Cela permet de répartir les fichiers de données sources sur plusieurs systèmes de fichiers. [!DNL Platform Server] tente d’autres chemins d’accès dans l’ordre spécifié jusqu’à ce que le fichier de données soit trouvé.
