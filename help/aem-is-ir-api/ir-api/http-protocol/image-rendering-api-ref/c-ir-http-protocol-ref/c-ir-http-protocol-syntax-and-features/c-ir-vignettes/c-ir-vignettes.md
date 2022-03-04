---
title: Vignettes
description: Les vignettes sont des images créées avec la création d’images Dynamic Media à utiliser avec le rendu d’image.
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

Les vignettes sont des images créées avec la création d’images Dynamic Media à utiliser avec le rendu d’image.

IR prend en charge deux types de vignettes de base : *2D* et *3D*. Les scènes de salle sont généralement des vignettes 3D qui peuvent générer des reflets, tandis que la plupart des autres scènes, telles que les vêtements ou la tapisserie, sont normalement des vignettes 2D qui n’ont pas de capacité de rendu de reflet.

Les vignettes contiennent un *view* et une hiérarchie de *objet*.

La vue est le conteneur de l’image principale, des cartes d’éclairage partagées, des cartes de réflexion partagées et d’autres données associées à l’ensemble de l’image.

La hiérarchie d’objets se compose de *groupes d’objets*, *objet standard*, et *objet de chevauchement*.

Chaque objet standard contrôle une zone de l’image vue, définie avec une échelle de gris. *mask*. Les masques des objets standard ne se chevauchent jamais. Les objets standard ne peuvent pas être masqués directement, mais ils peuvent être entièrement ou partiellement recouverts par des objets de chevauchement. La plupart ou tous les objets d’une vignette sont des objets standard.

Chevauchez le calque des objets au-dessus de l’image d’affichage et les uns des autres. L’ordre de chevauchement est défini par une valeur z affectée à l’objet. Les objets de chevauchement sont utiles lorsque des parties d’une scène doivent être affichées ou masquées dynamiquement.

Plusieurs types d’objets sont pris en charge (standard et chevauchement), chacun ayant son propre objectif :

* **Objets planaires** (dans les vignettes 3D) et **objet plat** (dans les vignettes 2D) acceptent les matériaux de texture répétables. Elles sont généralement utilisées pour les sols, les plans de travail et d’autres surfaces plates qui nécessitent uniquement un mappage de perspective.
* **Objets de contour** mappez des surfaces incurvées aux formes lisses, telles que la tapisserie, et sont parfois utilisées pour les vêtements. Ils peuvent être utilisés dans des vignettes 2D et 3D et, s’ils sont entièrement créés, participer au rendu de la réflexion.
* **Objets non texturables** autorise uniquement les changements de couleurs. Elles sont autorisées dans les vignettes 2D et 3D. Elles sont soit intrinsèquement non texturables, soit elles peuvent être un objet plancaire ou de contour avec un indicateur &quot;Pas de texture&quot; spécial défini. Cette méthode est utile dans les vignettes 3D pour permettre aux objets de participer au rendu du reflet, même si l’objet accepte uniquement des matériaux de couleur solides.
* **Objets d’esquisse** sont mieux utilisés pour les objets en tissu avec plis et rides, tels que les vêtements. Comme les objets de contour, ils peuvent être utilisés dans les vignettes 2D et 3D, bien que leur application dans les vignettes 3D soit limitée.
* **Objets de mur** sont similaires aux objets planaires et ne sont pris en charge que dans les vignettes 3D. Ils disposent d’informations de disposition spéciales qui permettent d’appliquer deux finitions de mur différentes (en haut et en bas) et jusqu’à trois matériaux de bordure du mur. Lorsqu’elles sont correctement créées, les matériaux appliqués aux murs circulent de manière précise et transparente entre les murs adjacents, pour des applications réalistes de papier peint ou de bordure mur. Les objets de mur ne prennent pas en charge la rotation de texture.
* **Objets de Cabinet** sont autorisées uniquement dans les vignettes 3D. Ils sont utilisés pour créer des armoires de cuisine et de bain avec des exigences de disposition complexes. Les objets de Cabinet acceptent les textures répétables et les textures spécialement créées *fichier de style cabinet* contenant des images du panneau de l’armoire redimensionnable.

Outre les types d’objet de base, deux types spéciaux d’objets de chevauchement sont pris en charge :

* **Objets de chevauchement statiques** sont des objets qui n’acceptent pas les matériaux. Elles sont autorisées dans les vignettes 2D et 3D. Elles sont utiles pour les accessoires démontables dans une scène de pièce, pour les ombres portées derrière des objets de chevauchement rendables et des applications similaires.
* **Fenêtre recouvrant les objets de cadre** fournissent des informations de positionnement pour l’application de fichiers de style de calques de fenêtre, qui sont créés indépendamment de la vignette et peuvent être partagés entre les vignettes.

Les objets sont collectés dans *groupes d’objets*, similaire à un système de fichiers. Le groupement est normalement basé sur la structure des objets physiques qu’ils représentent (par exemple, un groupe &quot;Toutes les armoires&quot; peut contenir &quot;Armoires de base&quot; et &quot;Armoires murales&quot;). Tout nombre de niveaux de groupe est autorisé. Le regroupement prend en charge l’application de matériaux à plusieurs objets similaires.

* [Coordonnées de scène](c-ir-scene-coordinates.md)
* [Résolution des matériaux](c-ir-material-resolution.md)
