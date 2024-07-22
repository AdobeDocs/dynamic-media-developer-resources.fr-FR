---
title: Convertisseur de vignettes
description: Le convertisseur de vignettes (vntc) est un utilitaire de ligne de commande utilisé pour préparer le contenu créé avec la création d’images en vue d’un déploiement avec le rendu d’image.
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

Le convertisseur de vignettes (vntc) est un utilitaire de ligne de commande utilisé pour préparer le contenu créé avec la création d’images en vue d’un déploiement avec le rendu d’image.

[!DNL vntc] se trouve dans [!DNL *[!DNL install_root]*\ImageServing\bin]. Il dispose des fonctionnalités suivantes :

* Convertit les vignettes primaires en vignettes de production à résolution unique, à résolution multiple ou pyramidale (voir [Mise à l’échelle de vignette](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Génère des fichiers de style de vitrine et d&#39;armoire de production (voir `-resolution` et `-jpegquality`).

* Génère différentes versions de fichiers de vignettes, d’armoires et de fichiers de style de recouvrement des fenêtres à utiliser avec les anciennes versions du rendu d’image.
* Extrait les images des vignettes, en résolution complète ou sous forme de miniatures (voir `-thumbwidth` et `-image`).
* Extrait les propriétés appropriées du fichier source (voir `-info`) et les envoie à `stdout` ou à un fichier journal facultatif (voir `-log`).

Bien que l’utilisation de [!DNL vntc] soit facultative, Adobe recommande son utilisation pour optimiser les performances du serveur. Le convertisseur de vignettes met également en oeuvre une vérification approfondie des erreurs et peut prévenir de graves problèmes de serveur, y compris des blocages, lorsqu’il est utilisé avec diligence.

Lors de la génération de vignettes de production, la largeur en pixels de la vignette de sortie (ou 0 si des vignettes pyramidales ou multi-résolution) est ajoutée au nom du fichier de vignette de sortie généré. Lors du traitement des fichiers de style Cabinet, la résolution de sortie est ajoutée au nom du fichier de sortie. Tous les fichiers de sortie, y compris les fichiers de miniature, d’image et de journal facultatifs, ainsi que le fichier de style de vignette ou d’armoire de production, sont placés dans le même répertoire où se trouve *[!DNL sourceFile]* (sauf si `-destPath` est spécifié).

Le convertisseur de vignettes se limite par défaut à 3 Go de mémoire maximum. Lorsque vntc atteint cette limite, il arrête le traitement et génère une erreur. Cette limite peut être modifiée à l’aide de `-maxmem`.

>[!NOTE]
>
>L’outil de mise à jour des vignettes de la création d’images peut également être utilisé pour préparer les vignettes en vue de l’utilisation du rendu d’image. De la même manière, l’outil de création de contenu peut générer des fichiers de style Cabinet à utiliser avec le rendu d’image. Utilisez [!DNL vntc] si le traitement doit être automatisé. Les outils de la création d’images incluent une interface utilisateur graphique, qui est généralement plus facile à utiliser de manière interactive.

## Voir aussi {#section-3c756bf17b634543904fdd928adeafb2}

Documentation sur la création d’images
