---
title: Utilisation de plusieurs cartes d’éclairage
description: Certaines applications peuvent nécessiter une carte d'éclairage différente pour différents types de matériaux.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# Utilisation de plusieurs cartes d’éclairage{#using-multiple-illumination-maps}

Certaines applications peuvent nécessiter une carte d&#39;éclairage différente pour différents types de matériaux.

Vous pouvez créer jusqu’à trois cartes d’éclairage pour chaque vignette. La carte d’éclairage pour une opération de rendu est sélectionnée avec les commandes `illum=` et `gloss=` .

**Sélection par défaut** - Si `illum=` ou `gloss=` ne sont pas spécifiés, le moteur de rendu utilise la première carte d’éclairage créée (généralement la carte A, ou carte d’éclairage &quot;plate&quot;).

**Sélection automatique avec`gloss=`** - Si `illum=` n’est pas spécifié ou est défini sur `-1`, le moteur de rendu compare la valeur `gloss=` spécifiée aux valeurs d’éclat associées à chaque carte d’éclairage dans la vignette. Il sélectionne la carte d’éclairage dont la valeur d’éclat est la plus proche du `gloss=` spécifié.

**Sélection explicite avec`illum=`** - Si `illum=` est spécifié et défini sur `0`, `1` ou `2`, le moteur de rendu utilise la carte d’éclairage correspondante ; `gloss=` est ignoré pour la sélection de la carte d’éclairage.

Si la vignette ne contient qu’une seule carte d’éclairage, le moteur de rendu utilise cette carte et ignore les commandes `illum=` et `gloss=`.
