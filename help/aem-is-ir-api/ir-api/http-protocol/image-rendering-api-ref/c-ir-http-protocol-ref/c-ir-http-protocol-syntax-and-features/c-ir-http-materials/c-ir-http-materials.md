---
title: Documents
description: Le rendu d’image applique les matériaux aux groupes ou aux objets dans les vignettes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Documents{#materials}

Le rendu d’image applique les matériaux aux groupes ou aux objets dans les vignettes.

Un matériau se compose d’un ensemble d’ *attributs*. Certains attributs sont requis pour certains matériaux, d’autres sont facultatifs et certains sont ignorés s’ils sont présents. De nombreux attributs ont des valeurs par défaut. Tous les matériaux ne peuvent pas être appliqués à tous les objets (par exemple, un matériau de vitrine ne peut pas être appliqué à un canapé).

Tous les attributs qui se produisent dans un segment de spécification de matière (MSS) mais qui ne sont pas répertoriés ci-dessus ou dans les tableaux de matières spécifiques ci-dessous sont ignorés par le serveur.

Les tableaux suivants répertorient les attributs de matière de base. IR prend en charge des attributs supplémentaires pour le contrôle des [effets de rendu avancés](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

Sauf indication contraire, tous les attributs de matériau sont facultatifs, avec des valeurs par défaut appropriées.

* [Couleurs solides](r-ir-solid-colors.md)
* [Textures répétables](r-ir-repeatable-textures.md)
* [Bordures de mur](r-ir-wall-borders.md)
* [Décals](r-ir-decals.md)
* [Armoires](r-ir-cabinets.md)
* [Recouvrements de fenêtres](r-ir-window-coverings.md)
