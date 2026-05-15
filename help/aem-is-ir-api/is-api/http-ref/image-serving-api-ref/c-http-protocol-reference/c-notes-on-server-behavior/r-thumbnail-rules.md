---
description: Tenez compte de ces règles de miniature.
solution: Experience Manager
title: Règles de miniature
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
TQID: 'https://experienceleague.adobe.com/2HjWzEcMFnTFzwDWz-Ld7wZ6FsFcq3gwaUFcSWgxPko'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 0%

---

# Règles de miniature{#thumbnail-rules}

Tenez compte de ces règles de miniature.

1. Si elle est `catalog::ThumbType=Crop`, l’image (recadrée) est mise à l’échelle à la plus petite taille possible tout en couvrant la totalité de la cible rect. Si `catalog::ThumbType=Fit`, l’image (recadrée) est mise à l’échelle à la plus grande taille possible tout en ajustant l’image entière dans le rectangle cible. Si `catalog::ThumbType=Texture`, l’image (recadrée) est mise à l’échelle dans le rapport `catalog::ThumbRes`/`catalog::Resolution`.
1. Alignez l’image à l’échelle sur le rectangle cible en fonction de la `attribute::ThumbHorizAlign` et de la `attribute::ThumbVertAlign`.
1. Recadrez le résultat dans le rectangle cible.
