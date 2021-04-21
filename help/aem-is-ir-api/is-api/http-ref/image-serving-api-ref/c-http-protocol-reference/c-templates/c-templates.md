---
description: Les modèles peuvent être utilisés pour réduire la longueur et la complexité des requêtes composées de plusieurs calques d’image ou contenant du texte au format rtf.
solution: Experience Manager
title: Modèles
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---


# Modèles{#templates}

Les modèles peuvent être utilisés pour réduire la longueur et la complexité des requêtes composées de plusieurs calques d’image ou contenant du texte au format rtf.

Vous pouvez utiliser des variables personnalisées pour simplifier davantage l’utilisation des modèles. Les modèles sont souvent configurés pour faciliter la permutation d’images ou de texte ou la définition d’autres options au moment de l’exécution.

Les modèles sont stockés en tant qu’enregistrements dans les catalogues d’images, avec le corps du modèle dans le champ `catalog::Modifier` et le champ `catalog::Path` vide ou en spécifiant une image d’arrière-plan statique qui ne peut pas être modifiée dynamiquement.

Les modèles sont spécifiés avec la commande `template=` ou dans le composant path de l’URL de requête. Pour la plupart des applications, il est recommandé d&#39;utiliser la commande `template=` pour spécifier des modèles. La commande `template=`ne doit pas se produire dans le champ `catalog::PostModifier` et ne peut se produire que dans le champ `catalog::Modifier` d&#39;une requête IS imbriquée (c&#39;est-à-dire dans un concept `src=is{...}`). Les enregistrements de modèle ne peuvent pas être référencés dans les commandes `src=` ou `mask=`.

Toute commande `src=` ou `mask=`incorporée dans le modèle peut être résolue dans le catalogue principal de la demande ou dans un autre catalogue d’images. Si aucun `rootId` n&#39;est spécifié explicitement, le catalogue principal est supposé. Le modèle spécifié avec `template=` peut également se trouver dans le catalogue principal ou dans un autre catalogue d’images.

Il est vivement recommandé d’inclure toujours des définitions par défaut pour toutes les variables utilisées dans un modèle. Ainsi, la sortie d’image du modèle peut toujours être vue en spécifiant simplement ses `attribute::RootId` et `catalog::Id`, sans avoir à connaître les variables utilisées dans le modèle.

La variable de substitution de chemin prédéfinie `$object$` peut être utilisée pour appliquer l’objet image spécifié dans le chemin d’URL à toute source ou masque de calque ( `src=` ou `mask=`), même dans les requêtes imbriquées ou incorporées.

* [Exemple A](r-example-a.md)
* [Exemple B](r-example-b.md)
* [Exemple C](r-example-c.md)
