---
description: Le convertisseur de vignettes (vntc) est un utilitaire de ligne de commande utilisé pour préparer le contenu créé avec la création d’images en vue d’un déploiement avec le rendu d’images.
seo-description: Le convertisseur de vignettes (vntc) est un utilitaire de ligne de commande utilisé pour préparer le contenu créé avec la création d’images en vue d’un déploiement avec le rendu d’images.
seo-title: Vignette Converter
solution: Experience Manager
title: Vignette Converter
topic: Scene7 Image Serving - Image Rendering API
uuid: b32a30d6-ae4a-406f-88a9-e8b0eec394c9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Vignette Converter{#vignette-converter}

Le convertisseur de vignettes (vntc) est un utilitaire de ligne de commande utilisé pour préparer le contenu créé avec la création d’images en vue d’un déploiement avec le rendu d’images.

[!DNL vntc] se trouve dans [!DNL *[!DNL install_root]*\ImageServing\bin]. Il possède les fonctionnalités suivantes :

* Convertit les vignettes originales en vignettes de production à résolution unique, multirésolution ou pyramidale (voir Mise à l’échelle [des vignettes](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Génère des fichiers de style d’armoire de production et de garniture de fenêtre (voir `-resolution` et `-jpegquality`).

* Peut produire différentes versions de fichiers de vignettes, d’armoires et de fichiers de style de garnitures de fenêtre à utiliser avec des versions plus anciennes du rendu d’image.
* Extrait  images des vignettes, en résolution totale ou sous forme de vignettes (voir `-thumbwidth` et `-image`).
* Extrait les propriétés appropriées du fichier source (voir `-info`) et les envoie vers `stdout` ou un fichier journal facultatif (voir `-log`).

Bien que l’utilisation de [!DNL vntc] soit facultative, elle est vivement recommandée pour optimiser les performances du serveur. [!DNL vntc] met également en oeuvre une vérification approfondie des erreurs et peut prévenir les problèmes graves du serveur, y compris les blocages, lorsqu’ils sont utilisés avec diligence.

Lors de la génération de vignettes de production, la largeur en pixels de la vignette de sortie (ou 0 en cas de vignettes pyramidales ou multirésolutions) est ajoutée au nom du fichier de vignette de sortie généré. Lors du traitement des fichiers de style d’armoire, la résolution de sortie est ajoutée au nom du fichier de sortie. Tous les fichiers de sortie, y compris les fichiers de miniature, d’image et de journal facultatifs, ainsi que le fichier de vignette de production ou de style d’armoire, sont placés dans le même répertoire que celui où *[!DNL sourceFile]* se trouve (sauf `-destPath` indication contraire).

[!DNL vntc] se limite par défaut à 3 Go de mémoire maximum. Lorsque Vntc atteint cette limite, il arrête le traitement et génère une erreur. Vous pouvez modifier cette limite à l’aide de `-maxmem`.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>L’outil de mise à jour des vignettes de la création d’images peut également être utilisé pour préparer des vignettes en vue d’une utilisation du rendu d’image. De même, l’outil de création de contenu est capable de générer des fichiers de style d’armoire à utiliser avec le rendu d’image. Utilisez [!DNL vntc] si le traitement doit être automatisé. Les outils de création d’images incluent une interface utilisateur graphique, qui est généralement plus facile à utiliser de manière interactive.

## Voir aussi {#section-3c756bf17b634543904fdd928adeafb2}

Documentation sur la création d’images
