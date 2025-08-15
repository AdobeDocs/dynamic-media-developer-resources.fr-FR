---
description: Les fichiers de données source Image Rendering comprennent les fichiers de vignettes, les fichiers de matériaux (images pour les textures et les décalcomanies reproductibles ainsi que les fichiers de style de meuble et de garnitures de fenêtre) et les profils ICC.
solution: Experience Manager
title: Données sources
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Données sources{#source-data}

Les fichiers de données source Image Rendering comprennent les fichiers de vignettes, les fichiers de matériaux (images pour les textures et les décalcomanies reproductibles ainsi que les fichiers de style de meuble et de garnitures de fenêtre) et les profils ICC.

Tous les fichiers de données source doivent être accessibles au composant de code natif d’Image Rendering (colocalisé avec Image Server).

Si un catalogue de matériaux est impliqué, le fichier spécifié dans le catalogue de matériaux (avec `vignette::Path`, `catalog::Path`ou `icc::ProfilePath`) est recherché par le serveur de rendu comme suit :

* Si le chemin est absolu, il est utilisé tel quel.
* Si le chemin est relatif, il est précédé du préfixe ( `catalog::RootPath` d’un catalogue de matériaux nommé).
* Si le chemin est absolu, il est utilisé ; Sinon, il est précédé du préfixe ( `default::RootPath` du catalogue par défaut).
* Si le chemin est absolu, il est utilisé ; sinon, le serveur la combine avec le chemin indiqué dans [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2).
* Si le chemin est maintenant absolu, il est utilisé ; sinon, elle est supposée relative à [ ! DNL  *[!DNL install_folder]*].

Si aucun catalogue d’images n’est impliqué, le chemin est combiné, `default::RootPath` puis traité comme ci-dessus.

L’emplacement physique des fichiers de données sources est généralement spécifié avec [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). Plusieurs valeurs peuvent être spécifiées pour permettre la distribution des fichiers de données sources sur plusieurs systèmes de fichiers. Le serveur de rendu essaie chaque chemin dans l’ordre spécifié jusqu’à ce que le fichier de données soit trouvé.

De nouveaux fichiers de données de toute nature peuvent être ajoutés à tout moment sans arrêter le serveur.
