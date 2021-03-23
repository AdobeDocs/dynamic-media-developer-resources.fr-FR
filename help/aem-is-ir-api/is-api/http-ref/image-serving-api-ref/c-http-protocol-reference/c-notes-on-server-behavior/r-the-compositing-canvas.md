---
description: Si req=img, la taille de la trame de composition est entièrement déterminée par la taille du calque 0.
seo-description: Si req=img, la taille de la trame de composition est entièrement déterminée par la taille du calque 0.
seo-title: La trame de composition
solution: Experience Manager
title: La trame de composition
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# Canevas de composition {#the-compositing-canvas}

Si req=img, la taille de la trame de composition est entièrement déterminée par la taille du calque 0.

Si `size=` pour le calque 0 n’est pas spécifié explicitement, les transformations de calque sont utilisées pour calculer la taille de la trame de composition (voir ci-dessous).

Si `req=tmb`, la taille du canevas de composition est déterminée par le `size=` spécifié pour le calque 0 ou, si la taille n&#39;est pas spécifiée, la taille du canevas de composition est définie sur la  de vue (voir ci-dessous).
