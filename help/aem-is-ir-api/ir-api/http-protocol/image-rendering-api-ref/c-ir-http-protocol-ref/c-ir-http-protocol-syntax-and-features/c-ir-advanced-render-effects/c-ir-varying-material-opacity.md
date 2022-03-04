---
title: Opacité des matériaux variable
description: L’opacité variable est prise en charge pour les couleurs solides et les textures répétables appliquées aux objets qui se chevauchent, ainsi que pour les décalages et les matériaux qui recouvrent les fenêtres.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Opacité des matériaux variable{#varying-material-opacity}

L’opacité variable est prise en charge pour les couleurs solides et les textures répétables appliquées aux objets qui se chevauchent, ainsi que pour les décalages et les matériaux qui recouvrent les fenêtres.

Les informations d’opacité peuvent être fournies simplement en utilisant une image de RGB avec un canal alpha. En outre, l’opacité globale peut être variable avec la variable `opacity=` (pour les images RGB et RGBA).

Les bordures de mur prennent également en charge les images RGBA, principalement pour les bordures découpées.

Le [!DNL vnw] Les fichiers qui définissent les recouvrements de fenêtre peuvent inclure un canal d’opacité. Il est combiné par le moteur de rendu avec le canal alpha de la texture répétable et le `opacity=` afin de fournir une gamme complète d’effets d’opacité pour les traitements de vitres simples et translucides.
