---
description: Le rendu d’image applique des matériaux aux groupes ou aux objets des vignettes.
solution: Experience Manager
title: Matériaux
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# Matériaux{#materials}

Le rendu d’image applique des matériaux aux groupes ou aux objets des vignettes.

Un matériau est constitué d&#39;un ensemble d&#39;attributs **. Certains attributs sont requis pour certains matériaux, d&#39;autres sont facultatifs et certains sont ignorés s&#39;ils sont présents. De nombreux attributs ont des valeurs par défaut. Tous les matériaux ne peuvent pas être appliqués à tous les objets (par exemple, un matériau d&#39;armoire ne peut pas être appliqué à un canapé).

Tous les attributs qui se trouvent dans un MSS (Material Specification Segment) mais qui ne sont ni répertoriés ci-dessus ni dans les tableaux de matières spécifiques ci-dessous sont ignorés par le serveur.

Les tableaux suivants liste les attributs matériels de base. IR prend en charge des attributs supplémentaires pour contrôler les effets de rendu [avancés](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

Sauf indication contraire, tous les attributs de matériau sont facultatifs, avec des valeurs par défaut appropriées.

* [Couleurs unies](r-ir-solid-colors.md)
* [textures répétables](r-ir-repeatable-textures.md)
* [Bordures de mur](r-ir-wall-borders.md)
* [Décles](r-ir-decals.md)
* [Meubles](r-ir-cabinets.md)
* [Revêtements de fenêtre](r-ir-window-coverings.md)
