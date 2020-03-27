---
description: Le rendu d’image applique les matériaux aux groupes ou aux objets dans les vignettes.
seo-description: Le rendu d’image applique les matériaux aux groupes ou aux objets dans les vignettes.
seo-title: Matériaux
solution: Experience Manager
title: Matériaux
topic: Scene7 Image Serving - Image Rendering API
uuid: 82284e25-cfe0-4cf8-b410-b49196cc721c
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0

---


# Matériaux{#materials}

Le rendu d’image applique les matériaux aux groupes ou aux objets dans les vignettes.

Un matériau est constitué d&#39;un ensemble d&#39; *attributs*. Certains attributs sont obligatoires pour certains matériaux, d’autres sont facultatifs et certains sont ignorés s’ils sont présents. De nombreux attributs ont des valeurs par défaut. Tous les matériaux ne peuvent pas être appliqués à tous les objets (par exemple, un matériau d&#39;armoire ne peut pas être appliqué à un canapé).

Les attributs qui se trouvent dans un segment de spécification de matière (MSS) mais qui ne sont ni répertoriés ci-dessus ni dans les tableaux de matières spécifiques ci-dessous sont ignorés par le serveur.

Les tableaux suivants  les attributs matériels de base. IR prend en charge des attributs supplémentaires pour contrôler les effets [de rendu](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281)avancés.

Sauf indication contraire, tous les attributs de matière sont facultatifs, avec des valeurs par défaut appropriées.

* [Couleurs unies](r-ir-solid-colors.md)
* [textures répétables](r-ir-repeatable-textures.md)
* [Bordures de mur](r-ir-wall-borders.md)
* [Décles](r-ir-decals.md)
* [Meubles](r-ir-cabinets.md)
* [Recouvrements de fenêtre](r-ir-window-coverings.md)
