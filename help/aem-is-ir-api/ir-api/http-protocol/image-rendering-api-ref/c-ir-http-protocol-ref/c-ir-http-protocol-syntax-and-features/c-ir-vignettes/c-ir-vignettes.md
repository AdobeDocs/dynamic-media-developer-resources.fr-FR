---
description: Les vignettes sont des images créées avec Dynamic Media Image Authoring pour être utilisées avec le rendu d’images.
solution: Experience Manager
title: Vignettes
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 0%

---


# Vignettes{#vignettes}

Les vignettes sont des images créées avec Dynamic Media Image Authoring pour être utilisées avec le rendu d’images.

IR prend en charge deux types de vignettes de base, *2D* et *3D*. Les scènes en chambre sont généralement des vignettes en 3D qui peuvent rendre des reflets, tandis que la plupart des autres scènes, telles que les vêtements ou les tissus d’ameublement, sont normalement des vignettes en 2D qui n’ont pas de capacité de rendu des reflets.

Les vignettes contiennent une *vue* et une hiérarchie d&#39;objets **.

La vue est le conteneur de l’image principale, des cartes d’éclairage partagées, des cartes de réflexion partagées et d’autres données associées à l’ensemble de l’image.

La hiérarchie d&#39;objets est composée de *groupes d&#39;objets*, *objets standard* et *objets de chevauchement*.

Chaque objet standard contrôle une zone de l’image de la vue, définie avec un masque *en niveaux de gris*. Les masques des objets standard ne se chevauchent jamais. Les objets standard ne peuvent pas être masqués directement, mais ils peuvent être recouverts partiellement ou entièrement par des objets de chevauchement. La plupart ou tous les objets d’une vignette sont des objets standard.

Recouvrement du calque d’objets au-dessus de l’image de vue et les uns des autres. L’ordre de chevauchement est défini par une valeur z affectée à l’objet. Les objets de chevauchement sont utiles lorsque des parties d’une scène doivent être affichées ou masquées dynamiquement.

Plusieurs types d’objets sont pris en charge (standard et chevauchement), chacun ayant son propre objectif :

* **Les objets**  planaires (dans les vignettes 3D) et les objets **** plats (dans les vignettes 2D) acceptent les matériaux de texture répétables. Elles sont généralement utilisées pour les planchers, les comptoirs et les autres surfaces plates qui nécessitent uniquement un mappage de perspective.

* **Les** objets à fleurs sautent sur des surfaces courbes en forme lisse, comme les tissus d&#39;ameublement, et sont parfois utilisés pour les objets de vêtements. Ils peuvent être utilisés dans les vignettes 2D et 3D et, s’ils sont entièrement créés, participeront au rendu de la réflexion.
* **Les** objets non texturables ne permettent que les changements de couleur. Ils sont autorisés dans les vignettes 2D et 3D. Elles sont soit intrinsèquement non texturables, soit elles peuvent être un objet plane ou à flux avec un indicateur spécial &quot;Aucune texture&quot; défini. Cela s’avère utile dans les vignettes 3D pour permettre aux objets de participer au rendu de la réflexion, même si l’objet accepte uniquement les matériaux de couleur unie.
* **Les** objets d’esquisse sont mieux utilisés pour les objets de tissu avec des plis et des rides, tels que les vêtements. Comme les objets de trait de flux, ils peuvent être utilisés dans les vignettes 2D et 3D, bien que leur application dans les vignettes 3D soit limitée.
* **Les** objets de mur sont similaires aux objets planaires et ne sont pris en charge que dans les vignettes 3D. Ils ont des informations de disposition spéciales qui permettent l&#39;application de deux finitions de paroi différentes (supérieure et inférieure) et jusqu&#39;à trois matériaux de bordure de paroi. Une fois correctement rédigées, les matériaux appliqués aux murs circuleront de façon précise et transparente entre les murs adjacents, pour des applications réalistes de papier peint et de bordure des murs. Les objets de mur ne prennent pas en charge la rotation de la texture.
* **Les** objets Cabinet ne sont autorisés que dans les vignettes 3D. Ils sont utilisés pour créer des armoires de cuisine et de bain avec des exigences d&#39;aménagement complexes. Les objets Cabinet acceptent les textures répétables ainsi que les *fichiers de style Cabinet* spécialement créés contenant des images redimensionnables du panneau de l&#39;armoire.

Outre les types d’objet de base, deux types spéciaux d’objets de chevauchement sont pris en charge :

* **Les** objets de chevauchement statique sont des objets qui n&#39;acceptent pas les matériaux. Ils sont autorisés dans les vignettes 2D et 3D. Elles sont utiles pour les accessoires amovibles dans une scène de chambre, pour les ombres portées derrière des objets de chevauchement rendables et des applications similaires.
* **Les** objets de cadre recouverts de fenêtre fournissent des informations de placement pour l’application de fichiers de style de garnitures de fenêtre, qui sont créés indépendamment de la vignette et peuvent être partagés entre les vignettes.

Les objets sont collectés dans des groupes d&#39;objets **, semblables à un système de fichiers. Le regroupement est normalement basé sur la structure des objets physiques qu’ils représentent (par exemple, un groupe &quot;Toutes les armoires&quot; peut contenir &quot;Armoires de base&quot; et &quot;Armoires murales&quot;). Tout nombre de niveaux de groupe est autorisé. Le regroupement prend en charge l&#39;application de matériaux à plusieurs objets similaires.

* [Coordonnées de scène](c-ir-scene-coordinates.md)
* [Résolution du matériau](c-ir-material-resolution.md)
