---
description: Les fichiers de données de source de contenu statique sont accessibles uniquement par le  [!DNL Platform Server].
solution: Experience Manager
title: Données de source de contenu statique
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
TQID: 'https://experienceleague.adobe.com/XFhKuqGPsarkFZcYcBo7XuyCEsiJINf-o6koIZQKAXU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 0%

---

# Données de source de contenu statique{#static-content-source-data}

Les fichiers de données de source de contenu statique ne sont accessibles que par le [!DNL Platform Server] .

Le chemin d’accès aux fichiers de données de contenu statique est résolu comme suit :

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

Le serveur combine les segments de chemin d’accès de droite à gauche jusqu’à ce qu’un chemin d’accès absolu soit établi.

Tous les segments ` *[!DNL rootPath]*` peuvent être des segments de chemin d’accès vides, relatifs ou absolus.

` *[!DNL catalogPath]*` est un chemin/nom de fichier absolu ou relatif. *[!DNL requestPath]* doit être un chemin/nom de fichier relatif.

Plusieurs valeurs de `PS::staticContent.rootPaths` peuvent être définies dans [!DNL PlatformServer.conf]. Cela permet de distribuer les fichiers de données sources sur plusieurs systèmes de fichiers. Le [!DNL Platform Server] tente d’accéder à d’autres chemins dans l’ordre spécifié jusqu’à ce que le fichier de données soit trouvé.
