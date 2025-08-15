---
title: Mise à l’échelle des miniatures
description: L’étape 2 des transformations de calque d’image est modifiée comme suit pour les miniatures (c’est-à-dire si req=tmb).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# Mise à l’échelle des miniatures{#thumbnail-scaling}

L’étape 2 des transformations de calque d’image est modifiée comme suit pour les miniatures (c’est-à-dire si req=tmb).

* `2.` Si `size=` est spécifié, ajustez l’image (recadrée) dans le rectangle de `size=` à l’aide de règles de miniature. Si `size=` n’est pas spécifié, définissez une échelle basée sur `res=` ou, si `res=` n’est pas spécifié, ajustez l’image (recadrée) dans le rectangle de la zone de travail à l’aide des règles de miniature décrites ci-dessous.
