---
description: textPs= implémente un algorithme de copie propriétaire qui ajuste automatiquement les tailles de police pour remplir de manière optimale la zone de texte avec du texte, réduisant ainsi l’espace supplémentaire en bas tout en évitant le débordement.
solution: Experience Manager
title: Ajustement par copie
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1a560f3-f92c-4143-b80a-e1674c8a4207
TQID: 'https://experienceleague.adobe.com/9SthkANFoXF9ANPH2-3Yk9P--7VBJoZy-zscJ0rkTnE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 527
ht-degree: 0%

---

# Ajustement par copie{#copy-fitting}

textPs= implémente un algorithme de copie propriétaire qui ajuste automatiquement les tailles de police pour remplir de manière optimale la zone de texte avec du texte, réduisant ainsi l’espace supplémentaire en bas tout en évitant le débordement.

L’ajustement de copie peut être activé et contrôlé collectivement pour l’ensemble du calque de texte, sur une base de paragraphe, même pour une étendue de texte individuelle.

Indiquez la taille de police minimale avec `\fs` et la taille maximale avec `\copyfit`. Un nombre illimité de plages est autorisé dans la même chaîne RTF. Les tailles de toutes les plages varient proportionnellement, ce qui permet de conserver les proportions de police souhaitées.

`\copyfit` est considérée comme une commande de formatage de caractères et possède des règles d’étendue telles que `\fs` et `\b`.

La fonction de copie est désactivée en spécifiant des `\copyfit` d’une taille inférieure ou égale à la taille spécifiée par `\fs`.

## Limiter le nombre de lignes {#section-e5aee0f039e04842afc3d6884ed681ac}

Outre la spécification de la plage de tailles de police, le comportement de l’algorithme de recopie peut être contrôlé à l’aide des commandes `\copyfitlines` ou `\copyfitmaxlines`, qui limitent le nombre de lignes générées par l’algorithme. Les deux commandes acceptent un paramètre de nombre de lignes ou 0 pour ne pas limiter le nombre de lignes dans la zone recopiée.

`\copyfitlines` permet au texte de déborder sur des lignes supplémentaires lorsqu’il ne tient pas dans le nombre de lignes spécifié. Les sauts de ligne explicites dans le segment de texte à copier sont toujours respectés.

`\copyfitmaxlines` tronque toujours les lignes de sortie supplémentaires qui dépassent la limite spécifiée. Le nombre de lignes spécifié n’est jamais dépassé, même en présence de sauts de ligne explicites. Pour cette version de la diffusion d’images, N-1 marqueurs de `\line` au maximum peuvent être présents dans la plage de texte adaptée à la copie. Le comportement est indéfini si cette limite est dépassée.

## Exemples {#section-f4ddbbfade444560be30a813d90c2c1b}

Les exemples suivants supposent que les corps de texte sont fournis avec des variables nommées *[!DNL $A$]*, *[!DNL $B$]* et *[!DNL $C$]*.

**Conservez le même rapport entre les tailles de police dans toute la plage :**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* est toujours rendu deux fois plus grand que le reste du texte. Lorsqu’une grande quantité de texte est spécifiée, *[!DNL $A$]* et *[!DNL $C$]* sont rendus avec `\fs10` et *[!DNL $B$]* avec `\fs20`. Avec peu de texte, *[!DNL $A$]* et *[!DNL $C$]* utilisent `\fs100` et *[!DNL $B$]* `\fs200`.

**Convertissez vers une grande taille de police commune si une petite quantité de texte est dessinée :**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

À l’extrémité la plus petite de la plage, *[!DNL $B$]* est rendu avec `\fs20`, deux fois plus grand que *[!DNL $A$]* et *[!DNL $C$]* à `\fs10`. Tout le texte est dessiné à `\fs100` (50 points) à l’extrémité opposée de la plage.

**Convertissez vers une taille de police réduite commune si le rendu d’une grande quantité de texte doit être effectué :**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Tout le texte est dessiné avec \fs10 à la petite extrémité de la plage, tandis qu&#39;à sa plus grande, *[!DNL $A$]* et *[!DNL $C$]* sont rendus avec `\fs100` et *[!DNL $B$]* avec `\fs200`.

**Désactiver l’ajustement de copie pour une plage de texte interne :**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

La taille de police de *[!DNL $A$]* et *[!DNL $C$]* peut varier entre 10 et 100, tandis que *[!DNL $B$]* est toujours rendue avec `\fs50`.

**Limiter la sortie à une seule ligne, même si plus d&#39;espace vertical est disponible, mais permettre qu&#39;elle déborde sur des lignes supplémentaires si trop de texte est spécifié pour tenir sur une seule ligne à `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Limitez la sortie à une seule ligne, même si un espace vertical supplémentaire est disponible. Si une trop grande quantité de texte est spécifiée pour tenir sur une seule ligne à `\fs10`, elle est tronquée :**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
