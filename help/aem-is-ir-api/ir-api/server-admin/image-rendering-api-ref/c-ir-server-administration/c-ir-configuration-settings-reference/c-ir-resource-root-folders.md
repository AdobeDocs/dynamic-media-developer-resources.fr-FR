---
title: Dossiers de la racine de la ressource (ir.resourceRootPaths)
description: Une liste de chemins, délimités par des points-virgules, sert de racines à tous les fichiers de données avec des chemins d’accès aux fichiers relatifs.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# Dossiers de la racine de la ressource (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Une liste de chemins, délimités par des points-virgules, sert de racines à tous les fichiers de données avec des chemins d’accès aux fichiers relatifs.

Il peut s’agir de chemins absolus ou de chemins relatifs à *[!DNL install_folder]*. Lorsque plusieurs chemins sont spécifiés, le serveur tente chaque racine dans l’ordre indiqué jusqu’à ce que le fichier soit trouvé. La valeur par défaut est [!DNL ./resources], pour le chemin d’accès racine par défaut de [!DNL install_folder/resources].
