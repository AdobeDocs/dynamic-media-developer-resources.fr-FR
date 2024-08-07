---
title: Modèles
description: Les modèles peuvent être utilisés pour réduire la longueur et la complexité des demandes qui composent plusieurs calques d’image ou qui incluent du texte au format rtf.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Modèles{#templates}

Les modèles peuvent être utilisés pour réduire la longueur et la complexité des demandes qui composent plusieurs calques d’image ou qui incluent du texte au format rtf.

Les variables personnalisées peuvent être utilisées pour simplifier davantage l’utilisation des modèles. Les modèles sont souvent configurés pour faciliter la permutation d’images ou de texte ou la définition d’autres options au moment de l’exécution.

Les modèles sont stockés en tant qu’enregistrements dans les catalogues d’images, avec le corps du modèle dans le champ `catalog::Modifier` et le champ `catalog::Path` vide ou spécifiant une image d’arrière-plan statique qui ne peut pas être modifiée dynamiquement.

Les modèles sont spécifiés avec la commande `template=` ou dans le composant de chemin d’accès de l’URL de requête. Pour la plupart des applications, il est recommandé d&#39;utiliser la commande `template=` pour spécifier des modèles. La commande `template=`ne doit pas se produire dans le champ `catalog::PostModifier` et ne peut se produire que dans le champ `catalog::Modifier` d’une requête IS imbriquée (c’est-à-dire dans un concept `src=is{...}`). Les enregistrements de modèle ne peuvent pas être référencés dans les commandes `src=` ou `mask=`.

Toutes les commandes `src=` ou `mask=` incorporées dans le modèle peuvent se résoudre par le catalogue principal de la demande ou par un catalogue d’images différent. Si aucun `rootId` n’est spécifié explicitement, le catalogue principal est supposé. Le modèle spécifié avec `template=` peut également se trouver dans le catalogue principal ou dans un catalogue d’images différent.

Il est vivement recommandé de toujours inclure des définitions par défaut pour toutes les variables utilisées dans un modèle. Ainsi, la sortie de l’image du modèle peut toujours être visualisée en spécifiant simplement ses `attribute::RootId` et `catalog::Id`, sans avoir à connaître les variables utilisées dans le modèle.

La variable de substitution de chemin prédéfinie `$object$` peut être utilisée pour appliquer l’objet image spécifié dans le chemin d’URL à n’importe quelle source ou masque de calque ( `src=` ou `mask=`), même dans les requêtes imbriquées ou incorporées.

* [Exemple A](r-example-a.md)
* [Exemple B](r-example-b.md)
* [Exemple C](r-example-c.md)
