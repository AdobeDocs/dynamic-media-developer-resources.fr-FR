---
title: Convertisseur De Vignette
description: Vignette Converter (vntc) est un utilitaire de ligne de commande utilisé pour préparer le contenu créé avec la création d’images en vue d’un déploiement avec le rendu d’image.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
TQID: 'https://experienceleague.adobe.com/NZsbUGCd25rHyvrmt-Rh3XN0p3pHqEtGZrXLp-7JBsc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 337
ht-degree: 0%

---

# Convertisseur De Vignette{#vignette-converter}

Vignette Converter (vntc) est un utilitaire de ligne de commande utilisé pour préparer le contenu créé avec la création d’images en vue d’un déploiement avec le rendu d’image.

[!DNL vntc] se trouve dans [!DNL *[!DNL install_root]*\ImageServing\bin]. Il dispose des fonctionnalités suivantes :

* Convertit les vignettes principales en vignettes de production à résolution unique, multi-résolutions ou pyramidales (voir [Mise à l’échelle des vignettes](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Produit des fichiers de style d&#39;armoire de production et de couverture de fenêtre (voir `-resolution` et `-jpegquality`).

* Produisez différentes versions de fichiers de style de vignettes, d&#39;armoires et de couvre-fenêtres à utiliser avec les anciennes versions du rendu d&#39;image.
* Extrait les images d’affichage des vignettes, qu’elles soient en pleine résolution ou miniatures (voir `-thumbwidth` et `-image`).
* Extrait les propriétés pertinentes du fichier source (voir `-info`) et les envoie vers `stdout` ou un fichier journal facultatif (voir `-log`).

Bien que l’utilisation de [!DNL vntc] soit facultative, Adobe recommande son utilisation pour des performances optimales du serveur. Lorsqu&#39;il est utilisé avec diligence, le convertisseur Vignette met également en œuvre une vérification d&#39;erreur complète et peut prévenir les problèmes graves de serveur, y compris les pannes.

Lors de la génération de vignettes de production, la largeur en pixels de la vignette de sortie (ou 0 si elle est pyramidale ou multi-résolution) est ajoutée au nom du fichier de vignette de sortie généré. Lors du traitement des fichiers de style armoire, la résolution de sortie est ajoutée au nom du fichier de sortie. Tous les fichiers de sortie, y compris les fichiers facultatifs de miniature, d’image et de journal, ainsi que la vignette de production ou le fichier de style armoire, sont placés dans le même répertoire que celui où se trouve *[!DNL sourceFile]* (sauf si `-destPath` est spécifié).

Le convertisseur Vignette se limite par défaut à 3 Go de mémoire maximum. Lorsque vntc atteint cette limite, il arrête le traitement et génère une erreur. Cette limite peut être modifiée à l’aide de `-maxmem`.

>[!NOTE]
>
>L’outil Mise à jour de vignette dans la création d’images peut également être utilisé pour préparer des vignettes pour le rendu d’images. De même, l’outil de création de contenu peut générer des fichiers de style armoire à utiliser avec le rendu d’image. Utilisez [!DNL vntc] pour automatiser le traitement. Les outils de création d’images comprennent une interface utilisateur graphique, qui est généralement plus facile à utiliser de manière interactive.

## Voir aussi {#section-3c756bf17b634543904fdd928adeafb2}

Documentation de création d’images
