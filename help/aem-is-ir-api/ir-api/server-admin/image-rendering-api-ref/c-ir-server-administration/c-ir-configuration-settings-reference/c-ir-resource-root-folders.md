---
description: La liste des chemins, délimités par des points-virgules, sert de racines à tous les fichiers de données avec des chemins de fichier relatifs.
seo-description: La liste des chemins, délimités par des points-virgules, sert de racines à tous les fichiers de données avec des chemins de fichier relatifs.
seo-title: Dossiers racine de ressources (ir.resourceRootPaths)
solution: Experience Manager
title: Dossiers racine de ressources (ir.resourceRootPaths)
topic: Scene7 Image Serving - Image Rendering API
uuid: a2a8ecd1-ddfe-46c5-bb70-4640e0992de8
translation-type: tm+mt
source-git-commit: 2bc6fe0369808990642cf7afdccff647c48260d9
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---


# Dossiers racine de ressources (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

La liste des chemins, délimités par des points-virgules, sert de racines à tous les fichiers de données avec des chemins de fichier relatifs.

Il peut s’agir de chemins absolus ou de chemins relatifs à *[!DNL install_folder]*. Lorsque plusieurs chemins sont spécifiés, le serveur tente chaque racine dans l&#39;ordre indiqué jusqu&#39;à ce que le fichier soit trouvé. La valeur par défaut est [!DNL ./resources], pour un chemin racine par défaut de [!DNL install_folder/resources].
