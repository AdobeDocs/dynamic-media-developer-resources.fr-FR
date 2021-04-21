---
description: textPs= implémente un algorithme propriétaire d’ajustement de copie qui ajustera automatiquement la ou les tailles de police pour remplir de façon optimale la zone de texte avec du texte, en minimisant l’espace supplémentaire au bas tout en évitant le débordement.
solution: Experience Manager
title: Ajustement de copie
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%

---


# Copier-raccord{#copy-fitting}

textPs= implémente un algorithme propriétaire d’ajustement de copie qui ajustera automatiquement la ou les tailles de police pour remplir de façon optimale la zone de texte avec du texte, en minimisant l’espace supplémentaire au bas tout en évitant le débordement.

L’ajustement par copie peut être activé et contrôlé collectivement pour l’ensemble du calque de texte, sur la base d’un paragraphe, même pour une plage de texte individuelle.

Spécifiez la taille minimale de police avec `\fs` et la taille maximale de police avec `\copyfit`. Tout nombre de plages est autorisé dans la même chaîne RTF. Les tailles de toutes les plages sont variables proportionnellement, ce qui garantit le maintien des proportions de police souhaitées.

`\copyfit` est considérée comme une commande de formatage de caractères et comporte des règles d’étendue comme  `\fs` et  `\b`.

La fonction Copier-raccord est désactivée en spécifiant `\copyfit` avec une taille égale ou inférieure à la taille spécifiée par `\fs`.

## Limitation du nombre de lignes {#section-e5aee0f039e04842afc3d6884ed681ac}

Outre la spécification de la plage de tailles de police, le comportement de l&#39;algorithme de copier-coller peut être contrôlé avec les commandes `\copyfitlines` ou `\copyfitmaxlines`, qui limitent le nombre de lignes que l&#39;algorithme va générer. Les deux commandes acceptent un paramètre de nombre de lignes ou 0, afin de ne pas limiter le nombre de lignes dans la région recopiée.

`\copyfitlines` permet au texte de déborder sur d’autres lignes lorsqu’il ne tient pas dans le nombre de lignes spécifié. Les sauts de ligne explicites dans le segment de texte à copier sont toujours respectés.

`\copyfitmaxlines` tronque toujours les lignes de sortie supplémentaires qui dépassent la limite spécifiée. Le nombre de lignes spécifié ne sera jamais dépassé, même si des sauts de ligne explicites sont présents. Pour cette version de la diffusion d’images, aucun marqueur N-1 `\line` ne peut être présent dans la plage de texte ajustée en copie. Le comportement n&#39;est pas défini si cette limite est dépassée.

## Exemples {#section-f4ddbbfade444560be30a813d90c2c1b}

Les exemples suivants supposent que des corps de texte sont fournis avec des variables nommées *[!DNL $A$]*, *[!DNL $B$]* et *[!DNL $C$]*.

**Conserver le même rapport entre les tailles de police dans toute la plage :**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* sera toujours rendu deux fois plus grand que le reste du texte. Lorsque la quantité de texte est spécifiée, *[!DNL $A$]* et *[!DNL $C$]* sont rendus avec `\fs10` et *[!DNL $B$]* avec `\fs20`. Avec peu de texte, *[!DNL $A$]* et *[!DNL $C$]* utiliseront `\fs100` et *[!DNL $B$]* `\fs200`.

**Convertissez en une taille de police standard si vous ne dessinez qu’une petite quantité de texte :**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

À la plus petite extrémité de la plage, *[!DNL $B$]* est rendu avec `\fs20`, deux fois plus grand que *[!DNL $A$]* et *[!DNL $C$]* à `\fs10`. Tout le texte sera dessiné à `\fs100` (50 points) à l&#39;extrémité opposée de la plage.

**Convertir en une petite taille de police commune si le texte doit être rendu en grande quantité :**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Tout le texte est dessiné avec \fs10 à l&#39;extrémité inférieure de la plage, alors qu&#39;à l&#39;extrémité la plus grande, *[!DNL $A$]* et *[!DNL $C$]* sont rendus avec `\fs100` et *[!DNL $B$]* avec `\fs200`.

**Désactiver le raccord de copie pour une étendue de texte interne :**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

La taille de la police pour *[!DNL $A$]* et *[!DNL $C$]* peut varier entre 10 et 100, tandis que *[!DNL $B$]* est toujours rendu avec `\fs50`.

**Limitez la sortie à une seule ligne, même si davantage d’espace vertical est disponible, mais autorisez le débordement à des lignes supplémentaires si trop de texte est spécifié pour tenir dans une seule ligne à  `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Limitez la sortie à une seule ligne, même si davantage d’espace vertical est disponible. Si trop de texte est spécifié pour tenir dans une seule ligne à `\fs10`, il sera tronqué :**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
