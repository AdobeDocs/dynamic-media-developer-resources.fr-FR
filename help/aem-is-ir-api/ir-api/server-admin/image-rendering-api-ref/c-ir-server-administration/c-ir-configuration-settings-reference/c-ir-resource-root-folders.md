---
title: Dossiers racine des ressources (ir.resourceRootPaths)
description: Une liste de chemins d’accès, délimités par des points-virgules, sert de racines à tous les fichiers de données ayant des chemins d’accès aux fichiers relatifs.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
TQID: 'https://experienceleague.adobe.com/5mKCVHonfG4riWoIenUyFHtMnSg3cmL-Lm-YTGN34fA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 84
ht-degree: 0%

---

# Dossiers racine des ressources (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Une liste de chemins d’accès, délimités par des points-virgules, sert de racines à tous les fichiers de données ayant des chemins d’accès aux fichiers relatifs.

Il peut s’agir de chemins absolus ou de chemins relatifs à *[!DNL install_folder]*. Lorsque plusieurs chemins d’accès sont spécifiés, le serveur tente d’accéder à chaque racine dans l’ordre indiqué jusqu’à ce que le fichier soit trouvé. La valeur par défaut est [!DNL ./resources], pour un chemin racine par défaut de [!DNL install_folder/resources].

