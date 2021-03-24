---
description: La liste des chemins, délimités par des points-virgules, sert de racines à tous les fichiers de données avec des chemins de fichier relatifs.
solution: Experience Manager
title: Dossiers racine de ressources (ir.resourceRootPaths)
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# Dossiers racine de ressources (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

La liste des chemins, délimités par des points-virgules, sert de racines à tous les fichiers de données avec des chemins de fichier relatifs.

Peut être un chemin absolu ou un chemin relatif à *[!DNL install_folder]*. Lorsque plusieurs chemins sont spécifiés, le serveur tente chaque racine dans l&#39;ordre indiqué jusqu&#39;à ce que le fichier soit trouvé. La valeur par défaut est [!DNL ./resources], pour un chemin racine par défaut de [!DNL install_folder/resources].
