---
description: Les modèles peuvent être utilisés pour réduire la longueur et la complexité des requêtes composées de plusieurs calques d’image ou contenant du texte au format rtf.
seo-description: Les modèles peuvent être utilisés pour réduire la longueur et la complexité des requêtes composées de plusieurs calques d’image ou contenant du texte au format rtf.
seo-title: Modèles
solution: Experience Manager
title: Modèles
topic: Scene7 Image Serving - Image Rendering API
uuid: 54830d1f-40ad-4bf2-8e3d-d3e4d4ab57b9
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# Modèles{#templates}

Les modèles peuvent être utilisés pour réduire la longueur et la complexité des requêtes composées de plusieurs calques d’image ou contenant du texte au format rtf.

Vous pouvez utiliser des variables personnalisées pour simplifier davantage l’utilisation des modèles. Les modèles sont souvent configurés pour faciliter la permutation d’images ou de texte ou la définition d’autres options au moment de l’exécution.

Les modèles sont stockés sous forme d’enregistrements dans les catalogues d’images, avec le corps du modèle dans le `catalog::Modifier` champ et le `catalog::Path` champ vide ou en spécifiant une image d’arrière-plan statique qui ne peut pas être modifiée dynamiquement.

Les modèles sont spécifiés avec la `template=` commande ou dans le composant de chemin de l’URL de requête. Pour la plupart des applications, il est recommandé d’utiliser la `template=` commande pour spécifier des modèles. La `template=`commande ne doit pas se produire dans le `catalog::PostModifier` champ et ne peut se produire que dans le `catalog::Modifier` champ d’une requête IS imbriquée (c’est-à-dire dans un `src=is{...}` concept). Les enregistrements de modèle ne peuvent pas être référencés dans `src=` ou `mask=`les commandes.

Toute `src=` commande ou `mask=`commande incorporée dans le modèle peut être résolue dans le catalogue principal de la demande ou dans un catalogue d’images différent. Si aucun `rootId` n’est spécifié explicitement, le catalogue principal est pris en compte. Le modèle spécifié avec `template=` peut également se trouver dans le catalogue principal ou dans un autre catalogue d’images.

Il est vivement recommandé d’inclure toujours des définitions par défaut pour toutes les variables utilisées dans un modèle. De cette façon, la sortie d’image du modèle peut toujours être vue en spécifiant simplement son `attribute::RootId` et `catalog::Id`, sans avoir à connaître les variables utilisées dans le modèle.

La variable de substitution de chemin prédéfinie `$object$` peut être utilisée pour appliquer l’objet image spécifié dans le chemin d’URL à n’importe quelle source de calque ou masque ( `src=` ou `mask=`), même dans les requêtes imbriquées ou incorporées.

* [Exemple A](r-example-a.md)
* [Exemple B](r-example-b.md)
* [Exemple C](r-example-c.md)
