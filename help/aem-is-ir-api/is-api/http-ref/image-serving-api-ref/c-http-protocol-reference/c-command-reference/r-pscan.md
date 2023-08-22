---
title: pscan
description: Analyse JPEG progressive. Le JPEG progressif affiche une image de telle sorte qu’elle affiche initialement une photo floue/de mauvaise qualité dans son intégralité.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1afd3a60-e0b6-47d1-b7e4-98a3145782a2
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---

# pscan{#pscan}

Analyse JPEG progressive. Le JPEG progressif affiche une image de telle sorte qu’elle affiche initialement une photo floue/de mauvaise qualité dans son intégralité. Au fur et à mesure que la numérisation se poursuit, elle devient plus claire à mesure que les données de l’image sont téléchargées plus complètement. Ce paramètre permet de définir le nombre d’analyses nécessaires (3, 4 ou 5) pour que l’image entière s’affiche.

`pscan=auto|3|4|5`

La vitesse réelle de chaque analyse dépend de la vitesse de transmission du système de l’utilisateur et de l’ordinateur qui reçoit et décompresse les données.

`Auto` utilise les paramètres d’analyse calculés par la bibliothèque de JPEG indépendants et dépendent du modèle de couleur. Les valeurs de `3`, `4`, `5` correspondent au paramètre d’analyse d’Adobe Photoshop lorsque vous enregistrez un fichier de JPEG en tant que pjpeg (JPEG progressif).

If `pscan` n’est pas défini, sa valeur par défaut est `auto`.

## Propriétés {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Attribut de requête. S’applique quel que soit le paramètre de calque actif. Ignoré si le format de sortie n’est pas un JPEG progressif.

## Par défaut {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## Exemple {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## Voir aussi {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
