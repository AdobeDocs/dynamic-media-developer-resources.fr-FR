---
description: L'opacité variable est prise en charge pour les textures et les couleurs unies appliquées aux objets qui se chevauchent, ainsi que pour les décalcomanies et les matériaux de recouvrement de fenêtre.
solution: Experience Manager
title: Opacité variable des matériaux
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# Opacité du matériau variable {#varying-material-opacity}

L&#39;opacité variable est prise en charge pour les textures et les couleurs unies appliquées aux objets qui se chevauchent, ainsi que pour les décalcomanies et les matériaux de recouvrement de fenêtre.

Les informations d’opacité peuvent être fournies simplement en utilisant une image RVB avec un canal alpha. En outre, l&#39;opacité globale peut être variée avec la commande `opacity=` (pour les images RVB et RVB).

Les bordures murales prennent également en charge les images RGBA, principalement pour prendre en charge les bordures découpées.

Les fichiers [!DNL vnw] qui définissent les recouvrements de fenêtre peuvent inclure un canal d&#39;opacité, qui est combiné par le rendu avec le canal alpha de la texture répétable et la valeur `opacity=` pour fournir une gamme complète d&#39;effets d&#39;opacité pour les traitements de fenêtre transparent et transparent.
