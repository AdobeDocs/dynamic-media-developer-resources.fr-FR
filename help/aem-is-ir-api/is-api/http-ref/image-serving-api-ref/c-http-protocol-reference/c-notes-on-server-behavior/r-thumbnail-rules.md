---
description: Tenez compte de ces règles de miniature.
solution: Experience Manager
title: Règles de miniature
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# Règles de miniature{#thumbnail-rules}

Tenez compte de ces règles de miniature.

1. Si elle est `catalog::ThumbType=Crop`, l’image (recadrée) est mise à l’échelle à la plus petite taille possible tout en couvrant la totalité de la cible rect. Si `catalog::ThumbType=Fit`, l’image (recadrée) est mise à l’échelle à la plus grande taille possible tout en ajustant l’image entière dans le rectangle cible. Si `catalog::ThumbType=Texture`, l’image (recadrée) est mise à l’échelle dans le rapport `catalog::ThumbRes`/`catalog::Resolution`.
1. Alignez l’image à l’échelle sur le rectangle cible en fonction de la `attribute::ThumbHorizAlign` et de la `attribute::ThumbVertAlign`.
1. Recadrez le résultat dans le rectangle cible.
