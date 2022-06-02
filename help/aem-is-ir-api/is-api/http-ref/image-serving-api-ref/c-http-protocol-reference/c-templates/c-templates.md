---
title: Modèles
description: Les modèles peuvent être utilisés pour réduire la longueur et la complexité des demandes qui composent plusieurs calques d’image ou qui incluent du texte au format rtf.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Modèles{#templates}

Les modèles peuvent être utilisés pour réduire la longueur et la complexité des demandes qui composent plusieurs calques d’image ou qui incluent du texte au format rtf.

Les variables personnalisées peuvent être utilisées pour simplifier davantage l’utilisation des modèles. Les modèles sont souvent configurés pour faciliter la permutation d’images ou de texte ou la définition d’autres options au moment de l’exécution.

Les modèles sont stockés en tant qu’enregistrements dans les catalogues d’images, avec le corps du modèle dans la variable `catalog::Modifier` et la variable `catalog::Path` champ vide ou spécification d’une image d’arrière-plan statique qui ne peut pas être modifiée dynamiquement.

Les modèles sont spécifiés avec la variable `template=` ou dans le composant de chemin d’accès de l’URL de requête. Pour la plupart des applications, il est recommandé d’utiliser la variable `template=` pour spécifier des modèles. Le `template=`ne doit pas se produire dans la fonction `catalog::PostModifier` et ne peut se produire que dans le champ `catalog::Modifier` dans une requête IS imbriquée (c’est-à-dire dans une `src=is{...}` ). Les enregistrements de modèle ne peuvent pas être référencés dans `src=` ou `mask=`des commandes.

Quelconque `src=` ou `mask=`les commandes incorporées dans le modèle peuvent se résoudre par le catalogue principal de la requête ou par un catalogue d’images différent. Si non `rootId` est spécifiée explicitement, le catalogue principal est supposé. Le modèle spécifié avec `template=` peut également se trouver dans le catalogue principal ou dans un catalogue d’images différent.

Il est vivement recommandé de toujours inclure des définitions par défaut pour toutes les variables utilisées dans un modèle. Ainsi, la sortie de l’image du modèle peut toujours être visualisée en spécifiant simplement sa `attribute::RootId` et `catalog::Id`, sans avoir à connaître les variables utilisées dans le modèle.

Variable de substitution de chemin prédéfinie `$object$` peut être utilisé pour appliquer l’objet image spécifié dans le chemin d’URL à n’importe quelle source de calque ou masque ( `src=` ou `mask=`), même dans les requêtes imbriquées ou incorporées.

* [Exemple A](r-example-a.md)
* [Exemple B](r-example-b.md)
* [Exemple C](r-example-c.md)
