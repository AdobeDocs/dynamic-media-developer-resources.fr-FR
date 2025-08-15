---
title: Dossiers racine des ressources (ir.resourceRootPaths)
description: Une liste de chemins d’accès, délimités par des points-virgules, sert de racines à tous les fichiers de données ayant des chemins d’accès aux fichiers relatifs.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# Dossiers racine des ressources (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Une liste de chemins d’accès, délimités par des points-virgules, sert de racines à tous les fichiers de données ayant des chemins d’accès aux fichiers relatifs.

Il peut s’agir de chemins absolus ou de chemins relatifs à *[!DNL install_folder]*. Lorsque plusieurs chemins d’accès sont spécifiés, le serveur tente d’accéder à chaque racine dans l’ordre indiqué jusqu’à ce que le fichier soit trouvé. La valeur par défaut est [!DNL ./resources], pour un chemin racine par défaut de [!DNL install_folder/resources].
