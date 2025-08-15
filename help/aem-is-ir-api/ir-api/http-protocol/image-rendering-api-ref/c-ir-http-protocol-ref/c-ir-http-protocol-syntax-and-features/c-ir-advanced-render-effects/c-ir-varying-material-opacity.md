---
title: Opacité de matériau variable
description: L'opacité variable est prise en charge pour la couleur unie et les textures répétables appliquées aux objets qui se chevauchent, ainsi que pour les autocollants et les matériaux de recouvrement de fenêtre.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Opacité de matériau variable{#varying-material-opacity}

L&#39;opacité variable est prise en charge pour la couleur unie et les textures répétables appliquées aux objets qui se chevauchent, ainsi que pour les autocollants et les matériaux de recouvrement de fenêtre.

Les informations d’opacité peuvent être fournies simplement en utilisant une image RGB avec une couche alpha. En outre, l’opacité globale peut être modifiée à l’aide de la commande `opacity=` (pour les images RGB et RGBA).

Les bordures de mur prennent également en charge les images RGBA, principalement pour prendre en charge les bordures découpées.

Les fichiers [!DNL vnw] qui définissent les recouvrements de fenêtre peuvent inclure un canal d&#39;opacité. Il est combiné par le moteur de rendu à la couche alpha de la texture répétable et à la valeur `opacity=` pour fournir une gamme complète d&#39;effets d&#39;opacité pour les traitements de fenêtres transparentes et translucides.
