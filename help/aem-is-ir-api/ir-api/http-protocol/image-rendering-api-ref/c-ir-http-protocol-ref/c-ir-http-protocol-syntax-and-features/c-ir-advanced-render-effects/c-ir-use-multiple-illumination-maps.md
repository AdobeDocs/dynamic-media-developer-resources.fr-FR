---
description: Certaines applications peuvent nécessiter une carte d'éclairage différente pour différents types de matériaux.
solution: Experience Manager
title: Utilisation de plusieurs cartes d’éclairage
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Utilisation de plusieurs cartes d’éclairage{#using-multiple-illumination-maps}

Certaines applications peuvent nécessiter une carte d&#39;éclairage différente pour différents types de matériaux.

Vous pouvez créer jusqu’à trois cartes d’éclairage pour chaque vignette. La carte d’éclairage pour une opération de rendu est sélectionnée avec les commandes `illum=` et ou `gloss=` .

**** Sélection par défaut : si ni  `illum=` ni  `gloss=` ne sont spécifiés, le moteur de rendu utilise la première carte d’éclairage créée (généralement la carte A, ou carte d’éclairage &quot;plate&quot;).

**Sélection automatique avec`gloss=`** Si  `illum=` n’est pas spécifié ou est défini sur -1, le moteur de rendu compare la  `gloss=` valeur spécifiée avec les valeurs de brillance associées à chaque carte d’éclairage de la vignette, puis sélectionnez la carte d’éclairage dont la valeur de brillance est la plus proche de celle spécifiée  `gloss=`.

**Sélection explicite avec`illum=`** Si  `illum=` est spécifié et défini sur 0, 1 ou 2, le moteur de rendu utilisera la carte d’éclairage correspondante.  `gloss=` est ignorée dans le but de sélectionner la carte d’éclairage.

Si la vignette ne contient qu’une seule carte d’éclairage, le moteur de rendu utilisera cette carte et ignorera les commandes `illum=` et `gloss=`.
