---
description: Certaines applications peuvent nécessiter une carte d'éclairage différente pour différents types de matériaux.
seo-description: Certaines applications peuvent nécessiter une carte d'éclairage différente pour différents types de matériaux.
seo-title: Utilisation de plusieurs cartes d’éclairage
solution: Experience Manager
title: Utilisation de plusieurs cartes d’éclairage
topic: Scene7 Image Serving - Image Rendering API
uuid: 24d86229-6e88-4fe2-80ef-30461aee3db5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Utilisation de plusieurs cartes d’éclairage{#using-multiple-illumination-maps}

Certaines applications peuvent nécessiter une carte d&#39;éclairage différente pour différents types de matériaux.

Jusqu&#39;à trois cartes d&#39;éclairage peuvent être créées pour chaque vignette. La carte d’éclairage d’une opération de rendu est sélectionnée avec les commandes `illum=` et ou `gloss=` .

**Sélection** par défaut Si ni `illum=` ni `gloss=` ne sont spécifiés, le rendu utilisera la première carte d’éclairage créée (généralement la carte A, ou carte d’éclairage &quot;plat&quot;).

**Sélection automatique avec`gloss=`**Si`illum=`n’est pas spécifié ou est défini sur -1, le rendu compare la`gloss=`valeur spécifiée avec les valeurs d’éclat associées à chaque mappage d’éclairage dans la vignette, puis choisit la carte d’éclairage dont la valeur d’éclat est la plus proche de la valeur spécifiée`gloss=`.

**Sélection explicite avec`illum=`**Si`illum=`est spécifié et défini sur 0, 1 ou 2, le rendu utilisera le mappage d’éclairage correspondant ; n’`gloss=`est pas prise en compte lors de la sélection de la carte d’éclairage.

Si la vignette ne contient qu’un seul mappage d’éclairage, le rendu utilise ce mappage et ignore les commandes `illum=` et `gloss=` .
