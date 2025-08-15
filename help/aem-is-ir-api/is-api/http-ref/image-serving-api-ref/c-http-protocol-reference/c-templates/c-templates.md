---
title: Modèles
description: Les modèles peuvent être utilisés pour réduire la longueur et la complexité des requêtes qui composent plusieurs calques d’image ou qui incluent du texte au format RTF.
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

Les modèles peuvent être utilisés pour réduire la longueur et la complexité des requêtes qui composent plusieurs calques d’image ou qui incluent du texte au format RTF.

Les variables personnalisées peuvent être utilisées pour simplifier davantage l’utilisation des modèles. Les modèles sont souvent configurés pour permettre de permuter facilement des images ou du texte ou de définir d’autres options au moment de l’exécution.

Les modèles sont stockés en tant qu’enregistrements dans les catalogues d’images, avec le corps du modèle dans le champ `catalog::Modifier` et le champ `catalog::Path` vide ou spécifiant une image d’arrière-plan statique qui ne peut pas être modifiée dynamiquement.

Les modèles sont spécifiés à l’aide de la commande `template=` ou dans le composant de chemin de l’URL de requête. Pour la plupart des applications, il est recommandé d’utiliser la commande `template=` pour spécifier des modèles. La `template=`commande ne doit pas se produire dans le champ `catalog::PostModifier` et peut uniquement se produire dans le champ `catalog::Modifier` dans une requête IS imbriquée (c’est-à-dire, dans un concept `src=is{...}`). Les enregistrements de modèle ne peuvent pas être référencés dans les commandes `src=` ou `mask=`.

Toute `src=` ou `mask=` commande incorporée dans le modèle peut être résolue sur le catalogue principal de la requête ou sur un autre catalogue d’images. Si aucun `rootId` n’est spécifié explicitement, le catalogue principal est pris en compte. Le modèle spécifié par `template=` peut également se trouver dans le catalogue principal ou dans un autre catalogue d’images.

Il est vivement recommandé de toujours inclure des définitions par défaut pour toutes les variables utilisées dans un modèle. De cette façon, la sortie d’image du modèle peut toujours être affichée simplement en spécifiant ses `attribute::RootId` et `catalog::Id`, sans avoir à connaître les variables utilisées dans le modèle.

La variable de substitution de chemin prédéfinie `$object$` peut être utilisée pour appliquer l’objet image spécifié dans le chemin d’accès de l’URL à n’importe quelle source de calque ou masque de calque ( `src=` ou `mask=`), même dans des requêtes imbriquées ou incorporées.

* [Exemple A](r-example-a.md)
* [Exemple B](r-example-b.md)
* [Exemple C](r-example-c.md)
