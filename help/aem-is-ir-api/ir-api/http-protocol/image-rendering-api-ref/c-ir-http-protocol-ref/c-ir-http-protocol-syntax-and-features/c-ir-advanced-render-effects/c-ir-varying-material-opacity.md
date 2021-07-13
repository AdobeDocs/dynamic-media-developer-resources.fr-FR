---
description: L’opacité variable est prise en charge pour les couleurs solides et les textures répétables appliquées aux objets se chevauchant, ainsi que pour les décals et les matériaux de recouvrement de fenêtre.
solution: Experience Manager
title: Opacité des matériaux variable
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Opacité des matériaux variable{#varying-material-opacity}

L’opacité variable est prise en charge pour les couleurs solides et les textures répétables appliquées aux objets se chevauchant, ainsi que pour les décals et les matériaux de recouvrement de fenêtre.

Les informations d’opacité peuvent être fournies simplement en utilisant une image RVB avec un canal alpha. En outre, l’opacité globale peut être différente avec la commande `opacity=` (tant pour les images RVB que RVBA).

Les bordures de mur prennent également en charge les images RGBA, principalement pour les bordures découpées.

Les fichiers [!DNL vnw] qui définissent les recouvrements de fenêtre peuvent inclure un canal d’opacité, qui est combiné par le moteur de rendu avec le canal alpha de la texture répétable et la valeur `opacity=` pour fournir une gamme complète d’effets d’opacité pour les traitements de fenêtre transparent et transparent.
