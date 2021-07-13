---
description: Les vignettes sont des images créées avec la création d’images Dynamic Media à utiliser avec le rendu d’image.
solution: Experience Manager
title: Vignettes
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 5e1be99c-58c0-4e3c-bc57-7be5fa25ccef
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 0%

---

# Vignettes{#vignettes}

Les vignettes sont des images créées avec la création d’images Dynamic Media à utiliser avec le rendu d’image.

IR prend en charge deux types de vignettes de base, *2D* et *3D*. Les scènes de salle sont généralement des vignettes 3D qui peuvent générer des reflets, tandis que la plupart des autres scènes, telles que les vêtements ou la tapisserie, sont normalement des vignettes 2D qui n’ont pas de capacité de rendu de reflet.

Les vignettes contiennent une *vue* et une hiérarchie *objets*.

La vue est le conteneur de l’image principale, des cartes d’éclairage partagées, des cartes de réflexion partagées et d’autres données associées à l’ensemble de l’image.

La hiérarchie d’objets se compose de *groupes d’objets*, *objets standard* et *objets de chevauchement*.

Chaque objet standard contrôle une zone de l’image vue, définie avec une échelle de gris *mask*. Les masques des objets standard ne se chevauchent jamais. Les objets standard ne peuvent pas être masqués directement, mais ils peuvent être entièrement ou partiellement recouverts par des objets de chevauchement. La plupart ou tous les objets d’une vignette sont des objets standard.

Chevauchez le calque des objets au-dessus de l’image d’affichage et les uns des autres. L’ordre de chevauchement est défini par une valeur z affectée à l’objet. Les objets de chevauchement sont utiles lorsque des parties d’une scène doivent être affichées ou masquées dynamiquement.

Plusieurs types d’objets sont pris en charge (standard et chevauchement), chacun ayant son propre objectif :

* **Les objets**  planaires (dans les vignettes 3D) et les objets  **plats**  (dans les vignettes 2D) acceptent les matériaux de texture répétables. Elles sont généralement utilisées pour les sols, les plans de travail et d’autres surfaces plates qui nécessitent uniquement un mappage de perspective.

* **Les** objets de type Flowline s’enchaînent sur des surfaces incurvées aux formes lisses, telles que la tapisserie, et sont parfois utilisés pour les objets de vêtements. Ils peuvent être utilisés dans les vignettes 2D et 3D et, s’ils sont entièrement créés, participeront au rendu de la réflexion.
* **Les** objets non texturables ne permettent que des changements de couleur. Elles sont autorisées dans les vignettes 2D et 3D. Elles sont soit intrinsèquement non texturables, soit elles peuvent être un objet plancaire ou de contour avec un indicateur &quot;Pas de texture&quot; spécial défini. Cela s’avère utile dans les vignettes 3D pour permettre aux objets de participer au rendu du reflet, même si l’objet accepte uniquement les matériaux de couleur solides.
* **Les** objets d’esquisse sont mieux utilisés pour les objets de tissu avec plis et rides, tels que les vêtements. Comme les objets de contour, ils peuvent être utilisés dans les vignettes 2D et 3D, bien que leur application dans les vignettes 3D soit limitée.
* **Les** objets de mur sont similaires aux objets planaires et ne sont pris en charge que dans les vignettes 3D. Ils disposent d’informations de disposition spéciales qui permettent d’appliquer deux finitions de mur différentes (en haut et en bas) et jusqu’à trois matériaux de bordure du mur. Lorsqu’elles sont correctement créées, les matériaux appliqués aux murs s’enchaîneront de manière précise et transparente entre les murs adjacents, pour des applications réalistes de papier peint ou de bordure mur. Les objets de mur ne prennent pas en charge la rotation de texture.
* **Les** objets Cabinet ne sont autorisés que dans les vignettes 3D. Ils sont utilisés pour créer des armoires de cuisine et de bain avec des exigences de disposition complexes. Les objets Cabinet acceptent les textures répétables ainsi que les *fichiers de style Cabinet* spécialement créés contenant des images de panneau d’armoire redimensionnable.

Outre les types d’objet de base, deux types spéciaux d’objets de chevauchement sont pris en charge :

* **Les** objets de chevauchement statiques sont des objets qui n’acceptent pas les matériaux. Elles sont autorisées dans les vignettes 2D et 3D. Elles sont utiles pour les accessoires démontables dans une scène de pièce, pour les ombres portées derrière des objets de chevauchement rendables et des applications similaires.
* **Les** objets de cadre de recouvrement de fenêtre fournissent des informations de placement pour appliquer des fichiers de style de recouvrement de fenêtre, qui sont créés indépendamment de la vignette et peuvent être partagés entre les vignettes.

Les objets sont collectés dans des *groupes d’objets*, semblables à un système de fichiers. Le groupement est normalement basé sur la structure des objets physiques qu’ils représentent (par exemple, un groupe &quot;Toutes les armoires&quot; peut contenir &quot;Armoires de base&quot; et &quot;Armoires murales&quot;). Tout nombre de niveaux de groupe est autorisé. Le regroupement prend en charge l’application de matériaux à plusieurs objets similaires.

* [Coordonnées de scène](c-ir-scene-coordinates.md)
* [Résolution des matériaux](c-ir-material-resolution.md)
