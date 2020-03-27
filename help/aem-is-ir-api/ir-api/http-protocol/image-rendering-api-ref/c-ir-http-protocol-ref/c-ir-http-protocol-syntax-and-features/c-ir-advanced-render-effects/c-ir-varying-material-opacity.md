---
description: L’opacité variable est prise en charge pour les textures en couleur unie et répétables appliquées aux objets qui se chevauchent, ainsi que pour les décalages et les matériaux de recouvrement de fenêtre.
seo-description: L’opacité variable est prise en charge pour les textures en couleur unie et répétables appliquées aux objets qui se chevauchent, ainsi que pour les décalages et les matériaux de recouvrement de fenêtre.
seo-title: Opacité du matériau variable
solution: Experience Manager
title: Opacité du matériau variable
topic: Scene7 Image Serving - Image Rendering API
uuid: 6af07ea8-44ba-4253-8a26-614725af2f46
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Opacité du matériau variable{#varying-material-opacity}

L’opacité variable est prise en charge pour les textures en couleur unie et répétables appliquées aux objets qui se chevauchent, ainsi que pour les décalages et les matériaux de recouvrement de fenêtre.

Les informations d’opacité peuvent être fournies simplement en utilisant une image RVB avec un alpha. En outre, l’opacité globale peut être variée avec la `opacity=` commande (pour les images RVB et RVB).

Les bordures des murs prennent également en charge les images RGBA, principalement pour prendre en charge les bordures découpées.

Les [!DNL vnw] fichiers qui définissent les recouvrements de fenêtre peuvent inclure un d&#39;opacité, qui est combiné par le rendu avec le alpha de la texture répétable et la `opacity=` valeur pour fournir une gamme complète d&#39;effets d&#39;opacité pour les traitements de fenêtre transparent et transparent.
