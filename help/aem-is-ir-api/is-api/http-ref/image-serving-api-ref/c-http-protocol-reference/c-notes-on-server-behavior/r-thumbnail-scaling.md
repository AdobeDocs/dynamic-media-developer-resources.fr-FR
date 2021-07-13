---
description: L’étape 2 des transformations de couche d’image est modifiée comme suit pour les miniatures (c’est-à-dire si req=tmb).
solution: Experience Manager
title: Mise à l’échelle des miniatures
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# Mise à l’échelle des miniatures{#thumbnail-scaling}

L’étape 2 des transformations de couche d’image est modifiée comme suit pour les miniatures (c’est-à-dire si req=tmb).

* `2.` Si  `size=` est spécifié, ajustez l’image (recadrée) dans la  `size=` recette à l’aide des règles de miniature. Si `size=` n’est pas spécifié, mettez à l’échelle en fonction de `res=` ou, si `res=` n’est pas spécifié, ajustez l’image (recadrée) dans la zone de travail recto à l’aide des règles de miniature décrites ci-dessous.
