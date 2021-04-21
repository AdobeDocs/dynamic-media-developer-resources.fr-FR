---
description: Si req=img, la taille de la trame de composition est entièrement déterminée par la taille du calque 0.
solution: Experience Manager
title: La trame de composition
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---


# Canevas de composition {#the-compositing-canvas}

Si req=img, la taille de la trame de composition est entièrement déterminée par la taille du calque 0.

Si `size=` pour le calque 0 n’est pas spécifié explicitement, les transformations de calque sont utilisées pour calculer la taille de la trame de composition (voir ci-dessous).

Si `req=tmb`, la taille du canevas de composition est déterminée par le `size=` spécifié pour le calque 0 ou, si la taille n&#39;est pas spécifiée, la taille du canevas de composition est définie sur la  de vue (voir ci-dessous).
