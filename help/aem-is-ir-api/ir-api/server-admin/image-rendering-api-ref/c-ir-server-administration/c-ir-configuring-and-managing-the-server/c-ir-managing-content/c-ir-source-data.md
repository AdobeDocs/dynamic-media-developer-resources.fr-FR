---
description: Les fichiers de données sources de rendu d’image comprennent les fichiers vignette, les fichiers de matériaux (images pour les textures et les décalcomanies répétables ainsi que les fichiers de style d’armoire et de recouvrement de fenêtre) et les profils ICC.
solution: Experience Manager
title: Données Source
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
TQID: 'https://experienceleague.adobe.com/lvrZxGOZbo6ORttqcBhCTuYPzbiD9xei5qkRwnapIh8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 258
ht-degree: 0%

---

# Données Source{#source-data}

Les fichiers de données sources de rendu d’image comprennent les fichiers vignette, les fichiers de matériaux (images pour les textures et les décalcomanies répétables ainsi que les fichiers de style d’armoire et de recouvrement de fenêtre) et les profils ICC.

Tous les fichiers de données sources doivent être accessibles au composant de code natif du rendu d’image (co-localisé avec le serveur d’images).

Si un catalogue de matières est impliqué, le fichier spécifié dans le catalogue de matières (avec `vignette::Path`, `catalog::Path` ou `icc::ProfilePath`) est recherché par le serveur de rendu comme suit :

* Si le chemin est absolu, il est utilisé tel quel.
* Si le chemin est relatif, il est précédé du préfixe `catalog::RootPath` (d&#39;un catalogue de matériaux nommé).
* Si le chemin est absolu, il est utilisé ; dans le cas contraire, il est précédé du préfixe `default::RootPath` (du catalogue par défaut).
* Si le chemin est absolu, il est utilisé ; dans le cas contraire, le serveur le combine avec le chemin spécifié dans [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2).
* Si le chemin est maintenant absolu, il est utilisé ; dans le cas contraire, il est supposé relatif à [!DNL *[!DNL install_folder]*].

Si aucun catalogue d’images n’est impliqué, le chemin d’accès est combiné avec `default::RootPath`, puis traité comme ci-dessus.

L’emplacement physique des fichiers de données sources est généralement spécifié avec [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). Plusieurs valeurs peuvent être spécifiées pour permettre la distribution des fichiers de données sources sur plusieurs systèmes de fichiers. Le serveur de rendu tente d’accéder à chaque chemin dans l’ordre spécifié jusqu’à ce que le fichier de données soit trouvé.

Il est possible d’ajouter de nouveaux fichiers de données de n’importe quel type à tout moment sans arrêter le serveur.

