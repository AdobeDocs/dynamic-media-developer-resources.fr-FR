---
description: Si req=img, la taille du canevas de composition est entièrement déterminée par la taille du calque 0.
seo-description: Si req=img, la taille du canevas de composition est entièrement déterminée par la taille du calque 0.
seo-title: La toile de composition
solution: Experience Manager
title: La toile de composition
topic: Scene7 Image Serving - Image Rendering API
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# La toile de composition{#the-compositing-canvas}

Si req=img, la taille du canevas de composition est entièrement déterminée par la taille du calque 0.

Si le `size=` pour le calque 0 n’est pas spécifié explicitement, les transformations de calque sont utilisées pour calculer la taille de la zone de travail de composition (voir ci-dessous).

Si `req=tmb`la taille du canevas de composition est déterminée par la `size=` valeur spécifiée pour le calque 0 ou si la taille n’est pas spécifiée, la taille du canevas de composition est définie sur la  rect du (voir ci-dessous).
