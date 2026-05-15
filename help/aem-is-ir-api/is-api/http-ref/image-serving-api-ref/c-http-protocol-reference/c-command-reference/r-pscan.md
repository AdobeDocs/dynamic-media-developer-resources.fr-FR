---
title: pscan
description: Analyse JPEG progressive. Le JPEG progressif affiche une image de telle sorte qu’elle présente initialement une photo floue/de faible qualité dans son intégralité.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1afd3a60-e0b6-47d1-b7e4-98a3145782a2
TQID: 'https://experienceleague.adobe.com/NhxrMkCLJuVcoakGVk7akMWm6Po9a-CSSegTqHLXMbo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 2%

---

# pscan{#pscan}

Analyse JPEG progressive. Le JPEG progressif affiche une image de telle sorte qu’elle présente initialement une photo floue/de faible qualité dans son intégralité. Au fur et à mesure que l’analyse se poursuit, les données de l’image sont de plus en plus téléchargées. Ce paramètre permet de définir le nombre d’analyses nécessaires (3, 4 ou 5) pour que l’image entière s’affiche.

`pscan=auto|3|4|5`

La vitesse réelle de chaque balayage dépend de la vitesse de transmission du système de l&#39;utilisateur et de l&#39;ordinateur qui reçoit et décompresse les données.

`Auto` utilise les paramètres d’analyse qui sont calculés par la bibliothèque JPEG indépendante et dépend du modèle de couleur. Les valeurs de `3`, `4` `5` correspondent au paramètre Analyse défini dans Adobe Photoshop lorsque vous enregistrez un fichier JPEG au format pjpeg (JPEG progressif).

Si `pscan` n’est pas défini, la valeur par défaut est `auto`.

## Propriétés {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Attribut de requête. S’applique quel que soit le paramètre de calque actif. Ignoré si le format de sortie n’est pas le JPEG progressif.

## Par défaut {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## Exemple {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## Voir aussi {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
