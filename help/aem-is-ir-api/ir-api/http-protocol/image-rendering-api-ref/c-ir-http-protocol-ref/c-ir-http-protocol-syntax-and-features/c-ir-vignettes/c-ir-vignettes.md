---
description: Les vignettes sont des images créées avec Scene7 Image Authoring pour une utilisation avec le rendu d’image.
seo-description: Les vignettes sont des images créées avec Scene7 Image Authoring pour une utilisation avec le rendu d’image.
seo-title: Vignettes
solution: Experience Manager
title: Vignettes
topic: Scene7 Image Serving - Image Rendering API
uuid: 31d6b2b7-57c4-4fef-a498-c357c3724356
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0

---


# Vignettes{#vignettes}

Les vignettes sont des images créées avec Scene7 Image Authoring pour une utilisation avec le rendu d’image.

IR prend en charge deux types de vignettes de base : *2D* et *3D*. Les scènes d’une pièce sont généralement des vignettes en 3D qui peuvent rendre des reflets, tandis que la plupart des autres scènes, comme les vêtements ou les tissus d’ameublement, sont normalement des vignettes en 2D qui n’ont pas de fonctionnalité de rendu de reflet.

Les vignettes contiennent un ** et une hiérarchie d’ *objets*.

Le  est le  de l’image principale, des cartes d’éclairage partagées, des cartes de réflexion partagées et d’autres données associées à l’image entière.

La hiérarchie des objets est constituée de groupes *d’* objets, d’objets ** standard et d’objets *de* chevauchement.

Chaque objet standard contrôle une zone de l’image , définie avec un *masque* en niveaux de gris. Les masques des objets standard ne se chevauchent jamais. Les objets standard ne peuvent pas être masqués directement, mais ils peuvent être entièrement ou partiellement recouverts par des objets de chevauchement. La plupart ou tous les objets d’une vignette standard sont des objets standard.

Recouvrement du calque d’objets au-dessus de l’image  du et les uns des autres. L’ordre de chevauchement est défini par une valeur z affectée à l’objet. Les objets de chevauchement sont utiles lorsque des parties d’une scène doivent être affichées ou masquées dynamiquement.

Plusieurs types d’objets sont pris en charge (standard et chevauchement), chacun ayant son propre objectif :

* **Les objets** planaires (dans les vignettes 3D) et les objets **** plats (dans les vignettes 2D) acceptent les matériaux de texture répétables. Elles sont généralement utilisées pour les planchers, les plans de travail et d’autres surfaces plates qui nécessitent uniquement un mappage de perspective.

* **Les objets** à trait d’écoulement correspondent à des surfaces incurvées en forme lisse, comme les tissus d’ameublement, et sont parfois utilisés pour les objets d’habillement. Ils peuvent être utilisés dans les vignettes 2D et 3D et, s’ils sont entièrement créés, ils participent au rendu de la réflexion.
* **Les objets** non texturables ne permettent que des changements de couleur. Elles sont autorisées dans les vignettes 2D et 3D. Elles sont soit intrinsèquement non texturables, soit elles peuvent être un objet plane ou à flux avec un indicateur &quot;Aucune texture&quot; spécial défini. Cela s’avère utile dans les vignettes 3D pour permettre aux objets de participer au rendu de la réflexion, même si l’objet accepte uniquement les matériaux de couleur unie.
* **Les objets** d’esquisse sont mieux utilisés pour les objets de tissu avec des plis et des rides, tels que les articles d’habillement. Comme les objets de flux, ils peuvent être utilisés dans les vignettes 2D et 3D, bien que l’application dans les vignettes 3D soit limitée.
* **Les objets** de mur sont similaires aux objets planaires et ne sont pris en charge que dans les vignettes 3D. Ils ont des informations de mise en page spéciales qui permettent l&#39;application de deux finitions murales différentes (supérieure et inférieure) et jusqu&#39;à trois matériaux de bordure murale. Une fois correctement rédigées, les matériaux appliqués aux murs circulent avec précision et fluidité entre les murs adjacents, pour des applications réalistes de papier peint et de bordures murales. Les objets de mur ne prennent pas en charge la rotation de la texture.
* **Les objets** d’armoire sont autorisés dans les vignettes 3D uniquement. Ils sont utilisés pour créer des armoires de cuisine et de bain avec des exigences de disposition complexes. Les objets Cabinet acceptent les textures répétables ainsi que les fichiers *de style* CAB spécialement créés contenant des images de panneau CAB redimensionnables.

Outre les types d’objet de base, deux types spéciaux d’objets de chevauchement sont pris en charge :

* **Les objets** de chevauchement statique sont des objets qui n’acceptent pas les matériaux. Elles sont autorisées dans les vignettes 2D et 3D. Elles sont utiles pour les accessoires amovibles dans une scène de salle, pour les ombres portées derrière des objets de chevauchement rendables et des applications similaires.
* **Les objets** de cadre de recouvrement de fenêtre fournissent des informations de placement pour appliquer des fichiers de style de garniture de fenêtre, qui sont créés indépendamment de la vignette et peuvent être partagés entre les vignettes.

Les objets sont collectés dans des groupes *d’* objets, à l’instar d’un système de fichiers. Le regroupement est normalement basé sur la structure des objets physiques qu’ils représentent (par exemple, un groupe &quot;Toutes les armoires&quot; peut contenir &quot;Armoires de base&quot; et &quot;Armoires murales&quot;). Tout nombre de niveaux de groupe est autorisé. Le regroupement prend en charge l’application de matériaux à plusieurs objets similaires.

* [Coordonnées de scène](c-ir-scene-coordinates.md)
* [Résolution du matériau](c-ir-material-resolution.md)
