---
description: Vignette Converter (vntc) est un utilitaire de ligne de commande utilisé pour préparer le contenu créé avec Image Authoring en vue d’un déploiement avec Image Rendering.
solution: Experience Manager
title: Convertisseur de vignettes
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---


# Convertisseur de vignette{#vignette-converter}

Vignette Converter (vntc) est un utilitaire de ligne de commande utilisé pour préparer le contenu créé avec Image Authoring en vue d’un déploiement avec Image Rendering.

[!DNL vntc] se trouve dans [ !DNL  *[!DNL install_root]*\ImageServing\bin]. Il possède les fonctionnalités suivantes :

* Convertit les vignettes Principales en vignettes de production à résolution unique, multirésolution ou pyramidale (voir [Mise à l’échelle des vignettes](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Génère des fichiers de style d&#39;armoire et de fenêtre de production (voir `-resolution` et `-jpegquality`).

* Peut produire différentes versions de fichiers de vignettes, d’armoires et de fichiers de style de garnitures de fenêtre à utiliser avec des versions plus anciennes du rendu d’image.
* Extrait les images de vue des vignettes, en résolution totale ou en miniatures (voir `-thumbwidth` et `-image`).
* Extrait les propriétés appropriées du fichier source (voir `-info`) et les envoie à `stdout` ou à un fichier journal facultatif (voir `-log`).

Bien que l&#39;utilisation de [!DNL vntc] soit facultative, elle est vivement recommandée pour de meilleures performances de serveur. [!DNL vntc] met également en oeuvre une vérification approfondie des erreurs et peut prévenir de graves problèmes de serveur, y compris des blocages, lorsqu&#39;ils sont utilisés avec diligence.

Lors de la génération de vignettes de production, la largeur en pixels de la vignette de sortie (ou 0 en cas de vignettes pyramidales ou multirésolution) est ajoutée au nom du fichier de vignette de sortie généré. Lors du traitement des fichiers de style d&#39;armoire, la résolution de sortie est ajoutée au nom du fichier de sortie. Tous les fichiers de sortie, y compris les fichiers de miniature, d&#39;image et de journal facultatifs, ainsi que le fichier de style de vignette ou d&#39;armoire de production, sont placés dans le même répertoire où se trouve *[!DNL sourceFile]* (sauf si `-destPath` est spécifié).

[!DNL vntc] se limite par défaut à 3 Go de mémoire maximum. Lorsque Vntc atteint cette limite, il arrête le traitement et génère une erreur. Vous pouvez modifier cette limite à l&#39;aide de `-maxmem`.

>[!NOTE]
>
>L’outil de mise à jour des vignettes de la création d’images peut également être utilisé pour préparer des vignettes en vue de leur utilisation dans le rendu des images. De même, l’outil de création de contenu permet de générer des fichiers de style d’armoire à utiliser avec le rendu d’image. Utilisez [!DNL vntc] si le traitement doit être automatisé. Les outils de création d’images incluent une interface utilisateur graphique, qui est généralement plus facile à utiliser de manière interactive.

## Voir aussi {#section-3c756bf17b634543904fdd928adeafb2}

Documentation sur la création d’images
