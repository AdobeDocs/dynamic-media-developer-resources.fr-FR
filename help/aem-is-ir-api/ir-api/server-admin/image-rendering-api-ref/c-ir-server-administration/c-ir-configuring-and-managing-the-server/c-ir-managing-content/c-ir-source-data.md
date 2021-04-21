---
description: Les fichiers de données source de rendu d’image comprennent les fichiers de vignettes, les fichiers de matériaux (images pour les textures et les décalcomanies répétables, ainsi que les fichiers de style d’armoire et de fenêtre) et les profils ICC.
solution: Experience Manager
title: Données source
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---


# Données source{#source-data}

Les fichiers de données source de rendu d’image comprennent les fichiers de vignettes, les fichiers de matériaux (images pour les textures et les décalcomanies répétables, ainsi que les fichiers de style d’armoire et de fenêtre) et les profils ICC.

Tous les fichiers de données source doivent être accessibles au composant de code natif de Image Rendering (colocalisé avec Image Server).

Si un catalogue de matières est impliqué, le fichier spécifié dans le catalogue de matières (avec `vignette::Path`, `catalog::Path` ou `icc::ProfilePath`) est recherché par le serveur de rendu comme suit :

* Si le chemin est absolu, il est utilisé en l’état.
* Si le chemin d’accès est relatif, il est précédé de `catalog::RootPath` (provenant d’un catalogue de matières nommé).
* Si le chemin est absolu, il est utilisé ; sinon, il est précédé de `default::RootPath` (à partir du catalogue par défaut).
* Si le chemin est absolu, il est utilisé ; sinon, le serveur la combine avec le chemin spécifié dans [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2).
* Si le chemin d’accès est maintenant absolu, il est utilisé ; sinon, il est supposé être relatif à [ ! DNL *[!DNL install_folder]*].

Si aucun catalogue d’images n’est impliqué, le chemin d’accès est combiné avec `default::RootPath`, puis traité comme ci-dessus.

L’emplacement physique des fichiers de données source est généralement spécifié avec [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). Plusieurs valeurs peuvent être spécifiées pour permettre la distribution des fichiers de données source sur plusieurs systèmes de fichiers. Le serveur de rendu teste chaque chemin d’accès dans l’ordre spécifié jusqu’à ce que le fichier de données soit trouvé.

De nouveaux fichiers de données de toute sorte peuvent être ajoutés à tout moment sans arrêter le serveur.
