---
description: textPs= implémente un algorithme propriétaire d’ajustement de la copie qui ajustera automatiquement la ou les tailles de police pour remplir de manière optimale la zone de texte avec du texte, en minimisant l’espace supplémentaire au bas tout en évitant le débordement.
seo-description: textPs= implémente un algorithme propriétaire d’ajustement de la copie qui ajustera automatiquement la ou les tailles de police pour remplir de manière optimale la zone de texte avec du texte, en minimisant l’espace supplémentaire au bas tout en évitant le débordement.
seo-title: Copier-ajuster
solution: Experience Manager
title: Copier-ajuster
topic: Scene7 Image Serving - Image Rendering API
uuid: c3ddbf1f-c724-4436-96ff-2c616dfd355d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Copier-ajuster{#copy-fitting}

textPs= implémente un algorithme propriétaire d’ajustement de la copie qui ajustera automatiquement la ou les tailles de police pour remplir de manière optimale la zone de texte avec du texte, en minimisant l’espace supplémentaire au bas tout en évitant le débordement.

L’ajustement par copie peut être activé et contrôlé collectivement pour l’ensemble du calque de texte, sur la base d’un paragraphe, même pour une plage de texte individuelle.

Spécifiez la taille minimale de police avec `\fs` et la taille maximale de police avec `\copyfit`. Tout nombre de plages est autorisé dans la même chaîne RTF. Les tailles de toutes les plages sont variables proportionnellement, ce qui garantit le maintien des proportions de police souhaitées.

`\copyfit` est considérée comme une commande de formatage de caractères et comporte des règles d’étendue telles que `\fs` et `\b`.

L’ajustement par copie est désactivé en spécifiant `\copyfit` une taille égale ou inférieure à la taille spécifiée par `\fs`.

## Limitation du nombre de lignes {#section-e5aee0f039e04842afc3d6884ed681ac}

Outre la spécification de la plage de tailles de police, le comportement de l’algorithme de calibrage peut être davantage contrôlé avec les commandes `\copyfitlines` ou `\copyfitmaxlines` , qui limitent le nombre de lignes générées par l’algorithme. Les deux commandes acceptent un paramètre de nombre de lignes ou 0, afin de ne pas limiter le nombre de lignes dans la zone copiée-ajustée.

`\copyfitlines` permet au texte de déborder sur des lignes supplémentaires lorsqu’il ne tient pas dans le nombre de lignes spécifié. Les sauts de ligne explicites dans le segment de texte à copier sont toujours respectés.

`\copyfitmaxlines` tronque toujours les lignes de sortie supplémentaires qui dépassent la limite spécifiée. Le nombre de lignes spécifié ne sera jamais dépassé, même en présence de sauts de ligne explicites. Pour cette version de la diffusion d’images, la plage de texte recopiée ne peut pas contenir plus de `\line` marqueurs N-1. Le comportement n’est pas défini si cette limite est dépassée.

## Exemples {#section-f4ddbbfade444560be30a813d90c2c1b}

Les exemples suivants supposent que des corps de texte sont fournis avec des variables nommées *[!DNL $A$]*, *[!DNL $B$]* et *[!DNL $C$]*.

**Conserver le même rapport entre les tailles de police dans toute la plage :**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* sera toujours rendu deux fois plus grand que le reste du texte. Lorsque la quantité de texte est spécifiée, *[!DNL $A$]* et *[!DNL $C$]* est générée avec `\fs10` et *[!DNL $B$]* avec `\fs20`. Avec peu de texte, *[!DNL $A$]* et *[!DNL $C$]* utilisera `\fs100` et *[!DNL $B$]* `\fs200`.

**Convertir en une taille de police importante commune si seul un petit nombre de texte est dessiné :**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

A la plus petite extrémité de la plage, *[!DNL $B$]* le rendu sera effectué avec `\fs20`, deux fois plus grand *[!DNL $A$]* que *[!DNL $C$]* et `\fs10`à. Tout le texte sera dessiné à `\fs100` (50 points) à l’extrémité opposée de la plage.

**Convertir en une petite taille de police commune si le texte doit être rendu :**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Tout le texte est tracé avec \fs10 à la petite extrémité de la plage, alors qu’il est le plus grand, *[!DNL $A$]* et *[!DNL $C$]* est rendu avec `\fs100` et *[!DNL $B$]* avec `\fs200`.

**Désactivation de l’ajustement de copie pour une plage de texte interne :**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

La taille de la police *[!DNL $A$]* et *[!DNL $C$]* peut varier entre 10 et 100, alors *[!DNL $B$]* qu’elle est toujours générée avec `\fs50`.

**Limitez la sortie à une seule ligne, même si davantage d’espace vertical est disponible, mais autorisez le débordement à des lignes supplémentaires si trop de texte est spécifié pour tenir dans une seule ligne à`\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Limitez la sortie à une seule ligne, même si davantage d’espace vertical est disponible. Si trop de texte est spécifié pour tenir sur une seule ligne,`\fs10`il sera tronqué :**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
