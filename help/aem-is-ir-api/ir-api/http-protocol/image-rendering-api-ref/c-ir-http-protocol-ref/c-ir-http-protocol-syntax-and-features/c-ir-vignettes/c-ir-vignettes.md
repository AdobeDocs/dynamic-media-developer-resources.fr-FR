---
title: Vignettes
description: Les vignettes sont des images créées avec la création d’images Dynamic Media en vue d’être utilisées avec le rendu d’image.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5e1be99c-58c0-4e3c-bc57-7be5fa25ccef
TQID: 'https://experienceleague.adobe.com/g8AE9F8CEmXYwPtG5pWdKeLKQCCzjUdKOgkbLoy1bgE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 628
ht-degree: 0%

---

# Vignettes{#vignettes}

Les vignettes sont des images créées avec la création d’images Dynamic Media en vue d’être utilisées avec le rendu d’image.

IR prend en charge deux types de vignettes : *2D* et *3D*. Les scènes de pièce sont généralement des vignettes 3D qui peuvent rendre des réflexions, tandis que la plupart des autres scènes, telles que les vêtements ou les tissus d&#39;ameublement, sont normalement des vignettes 2D qui n&#39;ont pas de capacité de rendu de réflexion.

Les vignettes contiennent une *vue* et une hiérarchie d’*objets*.

La vue est le conteneur de l&#39;image principale, des cartes d&#39;illumination partagées, des cartes de réflexion partagées et d&#39;autres données associées à l&#39;image entière.

La hiérarchie d’objets se compose de *groupes d’objets*, *objets standard* et *objets de chevauchement*.

Chaque objet standard contrôle une zone de l’image d’affichage, définie avec un *masque* en niveaux de gris. Les masques des objets standards ne se chevauchent jamais. Les objets standard ne peuvent pas être masqués directement, mais ils peuvent être recouverts partiellement ou entièrement par des objets de chevauchement. La plupart ou la totalité des objets d&#39;une vignette type sont des objets standard.

Superposez les objets en haut de l’image d’affichage et les uns sur les autres. L’ordre de chevauchement est défini par une valeur z affectée à l’objet . Les objets de chevauchement sont utiles lorsque des parties d&#39;une scène doivent être affichées ou masquées dynamiquement.

Plusieurs types d’objets sont pris en charge (à la fois standard et de chevauchement), chacun ayant sa propre fonction :

* **Objets planaires** (dans les vignettes 3D) et **objets plats** (dans les vignettes 2D) acceptent les matériaux de texture répétables. Ils sont généralement utilisés pour les sols, les comptoirs et d&#39;autres surfaces plates qui ne nécessitent qu&#39;une cartographie en perspective.
* **Objets Flowline** cartographiez les surfaces courbes de forme lisse telles que les tissus d&#39;ameublement et sont parfois utilisées pour les objets de vêtement également. Ils peuvent être utilisés dans des vignettes 2D et 3D et, s’ils sont entièrement créés, ils participent au rendu par réflexion.
* **Les objets non texturables** autorisent uniquement les changements de couleur. Elles sont autorisées dans les vignettes 2D et 3D. Soit ils sont intrinsèquement non texturables, soit il peut s&#39;agir d&#39;un objet plan ou de ligne de flux avec un indicateur spécial « Aucune texture » défini. Cette méthode est utile dans les vignettes 3D pour permettre aux objets de participer au rendu par réflexion, même si l&#39;objet accepte uniquement les matériaux de couleur unie.
* **Les objets d&#39;esquisse** sont mieux utilisés pour les objets en tissu avec des plis et des rides, tels que les vêtements. Comme les objets de ligne de flux, ils peuvent être utilisés dans les vignettes 2D et 3D, bien que leur application dans les vignettes 3D soit limitée.
* Les **objets de mur** sont similaires aux objets planaires et ne sont pris en charge que dans les vignettes 3D. Ils ont des informations de mise en page spéciales qui permettent l&#39;application de deux finitions de mur différentes (supérieure et inférieure) et jusqu&#39;à trois matériaux de bordure de mur. Lorsqu&#39;ils sont correctement créés, les matériaux appliqués aux murs s&#39;écoulent avec précision et de manière transparente entre les murs adjacents, pour des applications réalistes de papier peint/bordure de mur. Les objets de mur ne prennent pas en charge la rotation de texture.
* Les **objets d’armoire** sont autorisés uniquement dans les vignettes 3D. Ils sont utilisés pour créer des armoires de cuisine et de salle de bain avec des exigences de disposition complexes. Les objets d’armoire acceptent les textures répétables et les *fichiers de style armoire* spécialement créés, contenant des images de panneau armoire redimensionnables.

Outre les types d’objet de base, deux types spéciaux d’objets de chevauchement sont pris en charge :

* **Les objets de chevauchement statiques** sont des objets qui n&#39;acceptent pas de matériaux. Elles sont autorisées dans les vignettes 2D et 3D. Ils sont utiles pour les accessoires amovibles dans une scène de pièce, pour les ombres portées derrière des objets de chevauchement rendus, et des applications similaires.
* **Objets de cadre de recouvrement de fenêtre** fournissent des informations d’emplacement pour l’application de fichiers de style de recouvrement de fenêtre, qui sont créés indépendamment de la vignette et peuvent être partagés entre les vignettes.

Les objets sont collectés en *groupes d’objets*, comme dans un système de fichiers. Le regroupement est normalement basé sur la structure des objets physiques qu&#39;ils représentent (par exemple, un groupe &#39;Toutes les armoires&#39; peut contenir &#39;Armoires de base&#39; et &#39;Armoires murales&#39;). Un nombre illimité de niveaux de groupe est autorisé. Le regroupement prend en charge l’application de matériaux à plusieurs objets similaires.

* [Coordonnées de la scène](c-ir-scene-coordinates.md)
* [Résolution matérielle](c-ir-material-resolution.md)

