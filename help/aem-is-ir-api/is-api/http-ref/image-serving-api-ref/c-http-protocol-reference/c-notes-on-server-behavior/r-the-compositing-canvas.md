---
description: Si req=img, la taille de la zone de travail de composition est entièrement déterminée par la taille du calque 0.
solution: Experience Manager
title: Canevas de composition
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# Canevas de composition{#the-compositing-canvas}

Si req=img, la taille de la zone de travail de composition est entièrement déterminée par la taille du calque 0.

Si le calque for 0 n’est `size=` pas spécifié explicitement, les transformations de calque sont utilisées pour calculer la taille du canevas de composition (voir ci-dessous).

Si `req=tmb`, la taille de la zone de travail de composition est déterminée par la valeur spécifiée pour le `size=` calque 0 ou, si la taille n’est pas spécifiée, la taille de la zone de travail de composition est définie sur la vue rect (voir ci-dessous).
