---
description: Analyse JPEG progressive. Le format JPEG progressif affiche une image de telle sorte qu’elle affiche initialement une photo floue/de faible qualité dans son intégralité. Au fur et à mesure que la numérisation se poursuit, elle devient plus claire à mesure que les données de l’image sont téléchargées. Ce paramètre vous permet de définir le nombre d’analyses nécessaires (3, 4 ou 5) pour que l’image entière s’affiche.
solution: Experience Manager
title: pscan
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 2%

---


# pscan{#pscan}

Analyse JPEG progressive. Le format JPEG progressif affiche une image de telle sorte qu’elle affiche initialement une photo floue/de faible qualité dans son intégralité. Au fur et à mesure que la numérisation se poursuit, elle devient plus claire à mesure que les données de l’image sont téléchargées. Ce paramètre vous permet de définir le nombre d’analyses nécessaires (3, 4 ou 5) pour que l’image entière s’affiche.

`pscan=auto|3|4|5`

La vitesse réelle de chaque analyse dépend de la vitesse de transmission du système de l&#39;utilisateur et de l&#39;ordinateur qui reçoit et décompresse les données.

`Auto` utilise les paramètres d’analyse calculés par la bibliothèque JPEG indépendante et dépendent du modèle de couleur. Les valeurs de `3`, `4`, `5` correspondent au paramètre d’analyse détecté dans Adobe Photoshop lorsque vous enregistrez un fichier JPEG en tant que pjpeg (JPEG progressif).

Si `pscan` n&#39;est pas défini, il prend par défaut la valeur `auto`.

## Propriétés {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Attribut de requête. S’applique quel que soit le paramètre de calque actif. Ignoré si le format de sortie n’est pas JPEG progressif.

## Par défaut {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## Exemple {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## Voir aussi {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
