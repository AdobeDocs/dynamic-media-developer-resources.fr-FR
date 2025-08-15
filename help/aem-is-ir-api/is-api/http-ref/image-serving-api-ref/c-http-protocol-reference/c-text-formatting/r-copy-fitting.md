---
description: textPs= implémente un algorithme propriétaire d’ajustement de copie qui ajuste automatiquement les tailles de police pour remplir de manière optimale la zone de texte avec du texte, minimisant ainsi l’espace supplémentaire en bas tout en évitant le débordement.
solution: Experience Manager
title: Ajustement de copie
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1a560f3-f92c-4143-b80a-e1674c8a4207
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# Ajustement de copie{#copy-fitting}

textPs= implémente un algorithme propriétaire d’ajustement de copie qui ajuste automatiquement les tailles de police pour remplir de manière optimale la zone de texte avec du texte, minimisant ainsi l’espace supplémentaire en bas tout en évitant le débordement.

L’ajustement peut être activé et contrôlé collectivement pour l’ensemble du calque de texte, sur la base d’un paragraphe, même pour une période de texte individuelle.

Spécifiez la taille de police minimale avec `\fs` et la taille de police maximale avec `\copyfit`. Un nombre illimité de plages est autorisé dans une même chaîne RTF. Les tailles de toutes les gammes varient proportionnellement, ce qui garantit que les rapports de taille de police souhaités sont maintenus.

`\copyfit` est considérée comme une commande de formatage de caractères et possède des règles d’étendue telles que `\fs` et `\b`.

L’ajustement est désactivé en spécifiant `\copyfit` une taille égale ou inférieure à la taille spécifiée avec `\fs`.

## Limiter le nombre de lignes {#section-e5aee0f039e04842afc3d6884ed681ac}

En plus de spécifier la plage de tailles de police, le comportement de l’algorithme d’ajustement de copie peut être contrôlé davantage avec les `\copyfitlines` commandes ou `\copyfitmaxlines` , qui limitent le nombre de lignes générées par l’algorithme. Les deux commandes acceptent un paramètre de comptage de lignes ou 0, pour ne pas limiter le nombre de lignes dans la zone ajustée à copier.

`\copyfitlines` Permet au texte de dépasser des lignes supplémentaires lorsqu’il ne rentre pas dans le nombre de lignes spécifié. Les sauts de ligne explicites dans le segment de texte à ajuster sont toujours respectés.

`\copyfitmaxlines` Tronque toujours les lignes de sortie supplémentaires qui dépassent la limite spécifiée. Le nombre de lignes spécifié n’est jamais dépassé, même si des sauts de ligne explicites sont présents. Pour cette version du service d’images, pas plus de N-1 `\line` marqueurs ne peuvent être présents dans l’étendue de texte ajustée. Le comportement est indéfini si cette limite est dépassée.

## Exemples {#section-f4ddbbfade444560be30a813d90c2c1b}

Les exemples suivants supposent que les corps de texte sont fournis avec les variables nommées *[!DNL $A$]*, *[!DNL $B$]* et *[!DNL $C$]*.

**Conservez le même rapport entre les tailles de police sur toute la plage :**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* est toujours rendu deux fois plus volumineux que le reste du texte. Lorsque beaucoup de texte est spécifié *[!DNL $A$]* et *[!DNL $C$]* qu’il est rendu avec `\fs10` et avec *[!DNL $B$]*.`\fs20` Avec peu de texte, *[!DNL $A$]* et *[!DNL $C$]* utilisez `\fs100` et *[!DNL $B$]* `\fs200`.

**Convergez vers une grande taille de police si vous ne dessinez qu’une petite quantité de texte :**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

À la plus petite extrémité de la plage, *[!DNL $B$]* est rendu avec `\fs20`, deux fois plus grand que *[!DNL $A$]* et *[!DNL $C$]* à `\fs10`. Tout le texte est dessiné à `\fs100` (50 pts) à l’extrémité opposée de la plage.

**Convergez vers une petite taille de police courante si une grande partie du texte doit être rendue :**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Tout le texte est dessiné avec \fs10 à la petite extrémité de la plage, tandis qu’il est au plus grand, *[!DNL $A$]* et *[!DNL $C$]* est rendu avec `\fs100` et avec *[!DNL $B$]*.`\fs200`

**Désactiver l’ajustement d’une partie de texte interne :**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

La taille de police pour *[!DNL $A$]* et *[!DNL $C$]* peut varier entre 10 et 100, tandis que *[!DNL $B$]* est toujours rendue avec `\fs50`.

**Limitez la sortie à une seule ligne, même si plus d’espace vertical est disponible, mais laissez-la déborder sur des lignes supplémentaires si trop de texte est spécifié pour tenir dans une seule ligne à `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Limitez la sortie à une seule ligne, même si l’espace vertical disponible est plus important. Si trop de texte est spécifié pour tenir dans une seule ligne `\fs10` , il est tronqué :**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
