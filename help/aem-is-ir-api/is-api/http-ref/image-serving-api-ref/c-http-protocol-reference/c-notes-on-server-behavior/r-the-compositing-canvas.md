---
description: Si req=img, la taille du canevas de composition est déterminée entièrement par la taille du calque 0.
solution: Experience Manager
title: La zone de travail du compositeur
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---

# La zone de travail du compositeur{#the-compositing-canvas}

Si req=img, la taille du canevas de composition est déterminée entièrement par la taille du calque 0.

Si la valeur `size=` du calque 0 n’est pas spécifiée explicitement, les transformations de calque sont utilisées pour calculer la taille de la zone de travail du compositeur (voir ci-dessous).

Si la valeur est `req=tmb`, la taille de la zone de travail de composition est déterminée par la valeur `size=` spécifiée pour le calque 0 ou, si la taille n’est pas spécifiée, la taille de la zone de travail de composition est définie sur la vue rect (voir ci-dessous).
