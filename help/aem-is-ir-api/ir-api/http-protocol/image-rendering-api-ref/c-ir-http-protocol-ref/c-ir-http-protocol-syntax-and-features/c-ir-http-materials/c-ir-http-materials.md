---
title: Matériaux
description: Image Rendering applique des matériaux à des groupes ou à des objets dans des vignettes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Matériaux{#materials}

Image Rendering applique des matériaux à des groupes ou à des objets dans des vignettes.

Un matériau est constitué d’un ensemble d’attributs **. Certains attributs sont requis pour certains matériaux, d’autres sont facultatifs et certains sont ignorés s’ils sont présents. De nombreux attributs ont des valeurs par défaut. Tous les matériaux ne peuvent pas être appliqués à tous les objets (par exemple, un matériau d’armoire ne peut pas être appliqué à un canapé).

Tous les attributs qui apparaissent dans un segment MSS (Material Specification Segment) mais qui ne sont pas répertoriés ci-dessus ou dans les tableaux de matériaux spécifiques ci-dessous sont ignorés par le serveur.

Les tableaux suivants répertorient les attributs matériels de base. IR prend en charge des attributs supplémentaires pour contrôler [les effets](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281) de rendu avancés.

Sauf indication contraire, tous les attributs de matériau sont facultatifs, avec des valeurs par défaut appropriées.

* [Couleurs unies](r-ir-solid-colors.md)
* [Textures reproductibles](r-ir-repeatable-textures.md)
* [Bordures murales](r-ir-wall-borders.md)
* [Décalcomanies](r-ir-decals.md)
* [Armoires](r-ir-cabinets.md)
* [Garnitures de fenêtre](r-ir-window-coverings.md)
