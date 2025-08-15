---
title: Vignettes
description: Les vignettes sont des images créées avec Dynamic Media Image Authoring pour une utilisation avec Image Rendering.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5e1be99c-58c0-4e3c-bc57-7be5fa25ccef
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# Vignettes{#vignettes}

Les vignettes sont des images créées avec Dynamic Media Image Authoring pour une utilisation avec Image Rendering.

L’IR prend en charge deux types de vignettes de base : *2D* et *3D*. Les scènes de pièce sont généralement des vignettes 3D qui peuvent rendre des reflets, tandis que la plupart des autres scènes, telles que les vêtements ou les tissus d’ameublement, sont normalement des vignettes 2D qui n’ont pas de capacité de rendu de reflet.

Les vignettes contiennent une *vue* et une hiérarchie d’objets **.

La vue est le conteneur de l’image principale, des cartes d’éclairage partagées, des cartes de réflexion partagées et d’autres données associées à l’image entière.

La hiérarchie d’objets se compose de groupes d’objets, *d’objets* standard et *d’objets**de chevauchement.*

Chaque objet standard contrôle une zone de l’image visuelle, définie par un masque *en niveau* de gris. Les masques des objets standard ne se chevauchent jamais. Les objets standard ne peuvent pas être masqués directement, mais ils peuvent être couverts partiellement ou entièrement par des objets de chevauchement. La plupart ou la totalité des objets d’une vignette type sont des objets standard.

Chevauchement d’objets sur le dessus de l’image de vue et les uns sur les autres. L’ordre de chevauchement est défini par une valeur z affectée à l’objet. Les objets de chevauchement sont utiles lorsque des parties d’une scène doivent être affichées ou masquées dynamiquement.

Plusieurs types d’objets sont pris en charge (standard et superposé), chacun ayant son propre objectif :

* **Les objets** planaires (dans les vignettes 3D) et **les objets** plats (dans les vignettes 2D) acceptent des matériaux de texture reproductibles. Ils sont généralement utilisés pour les planchers, les comptoirs et autres surfaces planes qui ne nécessitent que la cartographie en perspective.
* **Les objets** Flowline cartographient des surfaces courbes de forme lisse telles que des tissus d’ameublement et sont parfois utilisés pour des objets vestimentaires. Ils peuvent être utilisés dans des vignettes 2D et 3D et, s’ils sont entièrement créés, participer au rendu de réflexion.
* **Les objets** non texturables autorisent uniquement les changements de couleur. Elles sont autorisées dans les vignettes 2D et 3D. Ils sont soit intrinsèquement non texturables, soit ils peuvent être un objet planaire ou de liaison avec un indicateur spécial « Aucune texture ». Cette méthode est utile dans les vignettes 3D pour permettre aux objets de participer au rendu de réflexion, même si l’objet n’accepte que des matériaux de couleur unie.
* **Sketch objets** sont mieux utilisés pour les objets en tissu avec des plis et des rides, tels que les vêtements. Comme les objets flowline, ils peuvent être utilisés dans des vignettes 2D et 3D, bien que l’application dans les vignettes 3D soit limitée.
* **Les objets** muraux sont similaires aux objets planaires et ne sont pris en charge que dans les vignettes 3D. Ils ont des informations de disposition spéciales qui permettent l’application de deux finitions murales différentes (supérieure et inférieure) et jusqu’à trois matériaux de bordure murale. Lorsqu’ils sont correctement créés, les matériaux appliqués aux murs s’écoulent avec précision et de manière transparente entre les murs adjacents, pour des applications réalistes de papier peint / bordure de mur. Les objets muraux ne prennent pas en charge la rotation de la texture.
* **Les objets** meubles sont autorisés dans les vignettes 3D uniquement. Ils sont utilisés pour créer des armoires de cuisine et de salle de bain avec des exigences de mise en page complexes. Les objets de meuble acceptent des textures reproductibles et des fichiers *de style d’armoire spécialement créés* contenant des images de panneau d’armoire redimensionnables.

Outre les types d’objet de base, deux types spéciaux d’objets de chevauchement sont pris en charge :

* **Les objets** de chevauchement statique sont des objets qui n’acceptent pas de matériaux. Elles sont autorisées dans les vignettes 2D et 3D. Ils sont utiles pour les accessoires amovibles dans une scène de pièce, pour les ombres portées derrière des objets de chevauchement pouvant être rendus et pour des applications similaires.
* **Les objets** de cadre de garniture de fenêtre fournissent des informations de placement pour l’application de fichiers de style de garnitures de fenêtre, qui sont créés indépendamment de la vignette et peuvent être partagés entre les vignettes.

Les objets sont rassemblés dans des *groupes* d’objets, semblables à un système de fichiers. Le regroupement est normalement basé sur la structure des objets physiques qu’ils représentent (par exemple, un groupe « Toutes les armoires » peut contenir des « armoires de base » et des « armoires murales »). N’importe quel nombre de niveaux de groupe est autorisé. Le regroupement prend en charge l’application de matériaux à plusieurs objets similaires.

* [Coordonnées de scène](c-ir-scene-coordinates.md)
* [Résolution de la matière](c-ir-material-resolution.md)
