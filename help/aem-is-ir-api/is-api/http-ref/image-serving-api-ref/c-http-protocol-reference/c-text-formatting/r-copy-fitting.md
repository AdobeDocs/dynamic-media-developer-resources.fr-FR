---
description: textPs= met en oeuvre un algorithme d’ajustement de copie propriétaire qui ajustera automatiquement la ou les tailles de police pour remplir de manière optimale la zone de texte avec du texte, en minimisant l’espace supplémentaire en bas tout en évitant le débordement.
solution: Experience Manager
title: Correspondance
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1a560f3-f92c-4143-b80a-e1674c8a4207
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Correspondance{#copy-fitting}

textPs= met en oeuvre un algorithme d’ajustement de copie propriétaire qui ajustera automatiquement la ou les tailles de police pour remplir de manière optimale la zone de texte avec du texte, en minimisant l’espace supplémentaire en bas tout en évitant le débordement.

L’ajustement de la copie peut être activé et contrôlé collectivement pour l’ensemble du calque de texte, sur la base d’un paragraphe, même pour une plage de texte individuelle.

Définissez la taille de police minimale avec `\fs` et la taille de police maximale avec `\copyfit`. Un nombre illimité de plages est autorisé dans la même chaîne RTF. Les tailles de toutes les plages sont variables proportionnellement, ce qui permet de conserver les proportions souhaitées.

`\copyfit` est considérée comme une commande de formatage de caractères et possède des règles d’étendue telles que `\fs` et `\b`.

Le correctif de copie est désactivé en spécifiant `\copyfit` avec une taille égale ou inférieure à la taille spécifiée avec `\fs`.

## Limiter le nombre de lignes {#section-e5aee0f039e04842afc3d6884ed681ac}

Outre la définition de la plage de tailles de police, le comportement de l’algorithme d’ajustement de copie peut être contrôlé avec la variable `\copyfitlines` ou `\copyfitmaxlines` , qui limite le nombre de lignes générées par l’algorithme. Les deux commandes acceptent un paramètre de comptage de ligne ou 0, afin de ne pas limiter le nombre de lignes dans la région ajustée à la copie.

`\copyfitlines` permet au texte de déborder sur des lignes supplémentaires lorsqu’il ne correspond pas au nombre spécifié de lignes. Les sauts de ligne explicites dans le segment de texte à copier sont toujours honorés.

`\copyfitmaxlines` tronque toujours les lignes de sortie supplémentaires qui dépassent la limite spécifiée. Le nombre spécifié de lignes ne sera jamais dépassé, même en présence de sauts de ligne explicites. Pour cette version de Image Serving, pas plus que N-1 `\line` les marqueurs peuvent être présents dans la plage de texte ajustée à la copie. Le comportement n’est pas défini si cette limite est dépassée.

## Exemples {#section-f4ddbbfade444560be30a813d90c2c1b}

Les exemples suivants supposent que des corps de texte sont fournis avec des variables nommées *[!DNL $A$]*, *[!DNL $B$]*, et *[!DNL $C$]*.

**Maintenir le même rapport entre les tailles de police dans l’ensemble de la plage :**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* est toujours rendu deux fois plus grand que le reste du texte. Lorsque beaucoup de texte est spécifié, *[!DNL $A$]* et *[!DNL $C$]* est rendu avec `\fs10` et *[!DNL $B$]* avec `\fs20`. Avec peu de texte, *[!DNL $A$]* et *[!DNL $C$]* utilisera `\fs100` et *[!DNL $B$]* `\fs200`.

**Effectuez une conversion vers une grande taille de police commune si seule une petite quantité de texte est dessinée :**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

À l’extrémité la plus petite de la plage, *[!DNL $B$]* est rendu avec `\fs20`, deux fois plus grande que *[!DNL $A$]* et *[!DNL $C$]* at `\fs10`. Tout le texte est dessiné dans `\fs100` (50 points) à l’extrémité opposée de la plage.

**Effectuez une conversion vers une petite taille de police commune si vous souhaitez générer beaucoup de texte :**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Tout le texte est tracé avec \fs10 à l’extrémité inférieure de la plage, tandis qu’à sa plus grande, *[!DNL $A$]* et *[!DNL $C$]* sont rendus avec `\fs100` et *[!DNL $B$]* avec `\fs200`.

**Désactiver le correctif pour une plage de texte interne :**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

La taille de police de *[!DNL $A$]* et *[!DNL $C$]* peut varier entre 10 et 100, tandis que *[!DNL $B$]* est toujours rendu avec `\fs50`.

**Limitez la sortie à une seule ligne, même si davantage d’espace vertical est disponible, tout en lui permettant de déborder sur d’autres lignes si trop de texte est spécifié pour tenir sur une seule ligne à l’adresse `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Limitez la sortie à une seule ligne, même si davantage d’espace vertical est disponible. Si trop de texte est spécifié pour tenir sur une seule ligne à l’adresse `\fs10` il est tronqué :**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
