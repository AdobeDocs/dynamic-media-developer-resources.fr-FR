---
title: Mise à l’échelle des miniatures
description: L’étape 2 des transformations de calque d’image est modifiée comme suit pour les miniatures (c’est-à-dire si req=tmb).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
TQID: 'https://experienceleague.adobe.com/He10BtjrEIOQW6SZcaUhcExDjP05BR-pc3BCj9TRawU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 79
ht-degree: 0%

---

# Mise à l’échelle des miniatures{#thumbnail-scaling}

L’étape 2 des transformations de calque d’image est modifiée comme suit pour les miniatures (c’est-à-dire si req=tmb).

* `2.` Si `size=` est spécifié, ajustez l’image (recadrée) dans le rectangle de `size=` à l’aide de règles de miniature. Si `size=` n’est pas spécifié, définissez une échelle basée sur `res=` ou, si `res=` n’est pas spécifié, ajustez l’image (recadrée) dans le rectangle de la zone de travail à l’aide des règles de miniature décrites ci-dessous.
