---
description: Tenez compte de ces règles de miniature.
seo-description: Tenez compte de ces règles de miniature.
seo-title: Règles de miniature
solution: Experience Manager
title: Règles de miniature
topic: Scene7 Image Serving - Image Rendering API
uuid: 7d04b923-e062-4764-9e48-99a7bba72d3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Règles de miniature{#thumbnail-rules}

Tenez compte de ces règles de miniature.

1. Si `catalog::ThumbType=Crop`cela se produit, l’image (recadrée) est redimensionnée à la taille la plus petite possible tout en couvrant l’ensemble du  rect. Si `catalog::ThumbType=Fit`cela se produit, l’image (recadrée) est redimensionnée à la taille la plus grande possible tout en ajustant l’image entière dans le  rectangle du. Si `catalog::ThumbType=Texture`cela se produit, l’image (recadrée) est mise à l’échelle selon le rapport `catalog::ThumbRes` / `catalog::Resolution`.
1. Alignez l’image mise à l’échelle avec le  rect du en fonction `attribute::ThumbHorizAlign` et `attribute::ThumbVertAlign`.
1. Recadrez le résultat au  rect du.

