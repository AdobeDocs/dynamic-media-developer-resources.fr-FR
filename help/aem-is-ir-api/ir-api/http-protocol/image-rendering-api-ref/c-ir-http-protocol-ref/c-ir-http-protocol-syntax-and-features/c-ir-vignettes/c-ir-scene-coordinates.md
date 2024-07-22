---
title: Coordonnées de scène
description: L’espace de coordonnées de la scène est utilisé pour spécifier les tailles et les distances sur les surfaces d’objet texturables.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: de7f088e-3825-4d2e-924e-001a44db62a0
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Coordonnées de scène{#scene-coordinates}

L’espace de coordonnées de la scène est utilisé pour spécifier les tailles et les distances sur les surfaces d’objet texturables.

Comme la plupart des vignettes sont des scènes du monde réel représentant des objets physiques, la plupart des vignettes sont créées à l’aide de pouces comme unités pour l’espace de coordonnées de la scène. D&#39;autres unités, telles que mm ou cm, peuvent également être utilisées. Le rendu d’image ne prend pas en charge la conversion d’unité.

Les commandes suivantes acceptent des valeurs dans l’espace de coordonnées de la scène :

* [grout=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
* [pos=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8)
* [size=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988)
