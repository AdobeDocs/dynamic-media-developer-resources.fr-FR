---
description: Tenez compte de ces règles de miniature.
seo-description: Tenez compte de ces règles de miniature.
seo-title: Règles de miniature
solution: Experience Manager
title: Règles de miniature
uuid: 7d04b923-e062-4764-9e48-99a7bba72d3f
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---


# Règles de miniature{#thumbnail-rules}

Tenez compte de ces règles de miniature.

1. Si `catalog::ThumbType=Crop`, l’image (recadrée) est mise à l’échelle à la taille la plus petite possible tout en recouvrant l’intégralité de la recette de la cible. Si `catalog::ThumbType=Fit`, l’image (recadrée) est redimensionnée à la taille la plus grande possible tout en ajustant l’ensemble de l’image dans la recette de la cible. Si `catalog::ThumbType=Texture`, l’image (recadrée) est mise à l’échelle selon le rapport `catalog::ThumbRes` à `catalog::Resolution`.
1. Alignez l’image mise à l’échelle avec la recette de la cible en fonction de `attribute::ThumbHorizAlign` et `attribute::ThumbVertAlign`.
1. Recadrez le résultat jusqu’à la recette de la cible.

