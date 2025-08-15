---
title: Utilisation de plusieurs textures d'illumination
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

# Utilisation de plusieurs textures d&#39;illumination{#using-multiple-illumination-maps}

Certaines applications peuvent nécessiter une carte d&#39;éclairage différente pour différents types de matériaux.

Vous pouvez créer jusqu&#39;à trois cartes d&#39;illumination pour chaque vignette. La carte d&#39;illumination d&#39;une opération de rendu est sélectionnée avec les commandes `illum=` et/ou `gloss=`.

**Sélection par défaut** - Si `illum=` ou `gloss=` ne sont pas spécifiés, le moteur de rendu utilise la première carte d&#39;illumination créée (généralement la carte A, soit la carte d&#39;illumination &#39;Plat&#39;).

**Sélection automatique avec`gloss=`** - Si `illum=` n&#39;est pas spécifié ou est défini sur `-1`, le moteur de rendu compare la valeur `gloss=` spécifiée aux valeurs de brillance associées à chaque texture d&#39;éclairage dans la vignette. Il sélectionne la texture d&#39;illumination dont la valeur de brillance est la plus proche de la `gloss=` spécifiée.

**Sélection explicite avec`illum=`** - Si `illum=` est spécifié et défini sur `0`, `1` ou `2`, le rendu utilise la map d&#39;illumination correspondante ; `gloss=` est ignoré pour sélectionner la map d&#39;illumination.

Si la vignette ne contient qu&#39;une seule carte d&#39;illumination, le moteur de rendu l&#39;utilise et ignore les commandes `illum=` et `gloss=`.
