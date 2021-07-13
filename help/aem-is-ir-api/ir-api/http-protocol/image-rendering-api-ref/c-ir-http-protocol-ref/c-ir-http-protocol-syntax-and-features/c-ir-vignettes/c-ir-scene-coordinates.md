---
description: L’espace de coordonnées de la scène est utilisé pour spécifier les tailles et les distances sur les surfaces d’objet texturables.
solution: Experience Manager
title: Coordonnées de scène
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: de7f088e-3825-4d2e-924e-001a44db62a0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 1%

---

# Coordonnées de scène{#scene-coordinates}

L’espace de coordonnées de la scène est utilisé pour spécifier les tailles et les distances sur les surfaces d’objet texturables.

Comme la plupart des vignettes sont des scènes du monde réel représentant des objets physiques, la plupart des vignettes sont créées à l’aide de pouces comme unités pour l’espace de coordonnées de la scène. D&#39;autres unités, telles que mm ou cm, peuvent également être utilisées. Le rendu d’image ne prend pas en charge la conversion d’unité.

Les commandes suivantes acceptent des valeurs dans l’espace de coordonnées de la scène :

* [grout=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
* [pos=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8)
* [taille=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988)
