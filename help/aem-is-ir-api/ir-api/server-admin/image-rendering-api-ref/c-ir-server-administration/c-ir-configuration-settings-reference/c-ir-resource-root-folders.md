---
description: La liste des chemins, délimités par des points-virgules, sert de racines à tous les fichiers de données avec des chemins d’accès aux fichiers relatifs.
solution: Experience Manager
title: Dossiers de la racine de la ressource (ir.resourceRootPaths)
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---

# Dossiers de la racine de la ressource (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

La liste des chemins, délimités par des points-virgules, sert de racines à tous les fichiers de données avec des chemins d’accès aux fichiers relatifs.

Il peut s’agir de chemins absolus ou de chemins relatifs à *[!DNL install_folder]*. Lorsque plusieurs chemins sont spécifiés, le serveur tente chaque racine dans l’ordre indiqué jusqu’à ce que le fichier soit trouvé. La valeur par défaut est [!DNL ./resources], pour un chemin racine par défaut de [!DNL install_folder/resources].
