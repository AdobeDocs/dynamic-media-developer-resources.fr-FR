---
description: Le convertisseur de vignettes (vntc) est un utilitaire de ligne de commande utilisé pour préparer le contenu créé avec la création d’images en vue d’un déploiement avec le rendu d’image.
solution: Experience Manager
title: Convertisseur de vignettes
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# Convertisseur de vignettes{#vignette-converter}

Le convertisseur de vignettes (vntc) est un utilitaire de ligne de commande utilisé pour préparer le contenu créé avec la création d’images en vue d’un déploiement avec le rendu d’image.

[!DNL vntc] se trouve dans [!DNL  *[!DNL install_root]*\ImageServing\bin]. Il dispose des fonctionnalités suivantes :

* Convertit les Principales vignettes en vignettes de production à résolution unique, multirésolution ou pyramidale (voir [Mise à l’échelle de la vignette](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Génère des fichiers de style de vitrine et d’armoire de production (voir `-resolution` et `-jpegquality`).

* Peut produire différentes versions de fichiers de vignettes, d’armoires et de recharges de fenêtre pour les fichiers de style à utiliser avec les anciennes versions du rendu d’image.
* Extrait les images des vignettes, en résolution complète ou sous forme de miniatures (voir `-thumbwidth` et `-image`).
* Extrait les propriétés appropriées du fichier source (voir `-info`) et les envoie à `stdout` ou à un fichier journal facultatif (voir `-log`).

Bien que l’utilisation de [!DNL vntc] soit facultative, elle est vivement recommandée pour de meilleures performances serveur. [!DNL vntc] met également en oeuvre une vérification approfondie des erreurs et peut empêcher les problèmes graves du serveur, y compris les blocages, lorsqu’ils sont utilisés avec diligence.

Lors de la génération de vignettes de production, la largeur en pixels de la vignette de sortie (ou 0 en cas de vignettes pyramidales ou multi-résolution) est ajoutée au nom du fichier de vignette de sortie généré. Lors du traitement des fichiers de style Cabinet, la résolution de sortie est ajoutée au nom du fichier de sortie. Tous les fichiers de sortie, y compris les fichiers de miniature, d’image et de journal facultatifs, ainsi que le fichier de style de vignette ou d’armoire de production, sont placés dans le même répertoire où se trouve *[!DNL sourceFile]* (sauf si `-destPath` est spécifié).

[!DNL vntc] se limite par défaut à 3 Go de mémoire maximum. Lorsque Vntc atteint cette limite, le traitement s’arrête et une erreur est générée. Cette limite peut être modifiée à l’aide de `-maxmem`.

>[!NOTE]
>
>L’outil de mise à jour des vignettes de la création d’images peut également être utilisé pour préparer les vignettes en vue de l’utilisation du rendu d’image. De même, l’outil de création de contenu est capable de générer des fichiers de style Cabinet à utiliser avec le rendu d’image. Utilisez [!DNL vntc] si le traitement doit être automatisé. Les outils de la création d’images incluent une interface utilisateur graphique, qui est généralement plus facile à utiliser de manière interactive.

## Voir aussi {#section-3c756bf17b634543904fdd928adeafb2}

Documentation sur la création d’images
