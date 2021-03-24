---
description: Certaines applications peuvent nécessiter une carte d'éclairage différente pour différents types de matériaux.
solution: Experience Manager
title: Utilisation de plusieurs cartes d’éclairage
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# Utilisation de plusieurs cartes d’éclairage{#using-multiple-illumination-maps}

Certaines applications peuvent nécessiter une carte d&#39;éclairage différente pour différents types de matériaux.

Jusqu&#39;à trois cartes d&#39;éclairage peuvent être créées pour chaque vignette. Le mappage d’éclairage pour une opération de rendu est sélectionné avec les commandes `illum=` et ou `gloss=`.

**** Sélection par défautSi ni  `illum=` ni  `gloss=` n’est spécifié, le rendu utilise la première carte d’éclairage créée (généralement la carte A, ou carte d’éclairage &quot;plate&quot;).

**Sélection automatique avec`gloss=`** Si  `illum=` n’est pas spécifié ou est défini sur -1, le rendu compare la  `gloss=` valeur spécifiée avec les valeurs d’éclat associées à chaque mappage d’éclairage de la vignette, puis choisit la carte d’éclairage dont la valeur d’éclat est la plus proche de celle  `gloss=`indiquée.

**Sélection explicite avec`illum=`** Si  `illum=` est spécifié et défini sur 0, 1 ou 2, le rendu utilise la carte d’éclairage correspondante ;  `gloss=` est ignorée dans le but de sélectionner la carte d’éclairage.

Si la vignette ne contient qu’un seul mappage d’éclairage, le rendu utilisera ce mappage et ignorera les commandes `illum=` et `gloss=`.
