---
title: Convertisseur de vignettes
description: Le convertisseur de vignettes (vntc) est un utilitaire de ligne de commande utilisé pour préparer le contenu créé avec Image Authoring en vue d’un déploiement avec Image Rendering.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# Convertisseur de vignettes{#vignette-converter}

Le convertisseur de vignettes (vntc) est un utilitaire de ligne de commande utilisé pour préparer le contenu créé avec Image Authoring en vue d’un déploiement avec Image Rendering.

[!DNL vntc] est dans [ ! DNL *[!DNL install_root]*\ImageServing\bin]. Il possède les fonctionnalités suivantes :

* Convertit les vignettes principales en vignettes de production à résolution unique, multirésolution ou pyramidale (voir Mise à [l’échelle](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585) des vignettes).
* Produit des fichiers de style d’armoires de production et de garnitures de fenêtre (voir `-resolution` et `-jpegquality`).

* Produisez différentes versions de vignettes, d’armoires et de garnitures de fenêtre à utiliser avec les anciennes versions d’Image Rendering.
* Extrait les images de la vue des vignettes, en pleine résolution ou des miniatures (voir `-thumbwidth` et `-image`).
* Extrait les propriétés appropriées du fichier source (voir `-info`) et les envoie à `stdout` ou à un fichier journal facultatif (voir `-log`).

Bien que l’utilisation de [!DNL vntc] soit facultative, Adobe recommande son utilisation pour obtenir les meilleures performances de serveur. Le convertisseur de vignettes met également en œuvre une vérification approfondie des erreurs et peut éviter les problèmes de serveur graves, y compris les pannes, lorsqu’il est utilisé avec diligence.

Lors de la génération de vignettes de production, la largeur en pixels de la vignette de sortie (ou 0 si les vignettes pyramidales ou multirésolution) est ajoutée au nom du fichier de vignette de sortie généré. Lors du traitement de fichiers de style d’armoire, la résolution de sortie est ajoutée au nom du fichier de sortie. Tous les fichiers de sortie, y compris les fichiers de miniature, d’image et de journal facultatifs, ainsi que la vignette de production ou le fichier de style de meuble, sont placés dans le même répertoire que celui où *[!DNL sourceFile]* se trouve (sauf indication `-destPath` contraire).

Le convertisseur de vignettes se limite par défaut à au maximum 3 Go de mémoire. Lorsque vntc atteint cette limite, il arrête le traitement et génère une erreur. Cette limite peut être modifiée à l’aide du `-maxmem`fichier .

>[!NOTE]
>
>L’outil de mise à jour des vignettes dans Image Authoring peut également être utilisé pour préparer des vignettes destinées à l’utilisation Image Rendering. De même, l’outil de création de contenu peut générer des fichiers de style de meuble à utiliser avec Image Rendering. Utilisez cette [!DNL vntc] action si le traitement doit être automatisé. Les outils de création d’images incluent une interface utilisateur graphique, et sont donc généralement plus faciles à utiliser de manière interactive.

## Voir aussi {#section-3c756bf17b634543904fdd928adeafb2}

Documentation de création d’images
