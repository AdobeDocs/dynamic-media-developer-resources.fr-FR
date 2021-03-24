---
description: La plupart des matériaux peuvent être colorés dynamiquement.
solution: Experience Manager
title: Coloriser les matériaux
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Colorisation des matériaux{#colorizing-materials}

La plupart des matériaux peuvent être colorés dynamiquement.

L&#39;algorithme de coloration est assez simpliste et fonctionne mieux pour les images de matériaux dont la gamme de teintes est limitée. Pour coloriser un matériau, le rendu soustrait simplement la valeur `bgc=` et ajoute la valeur `color=` à chaque valeur de pixel.

La coloration est désactivée si `color=` n&#39;est pas spécifié. `bgc=` est ignoré par les documents du Cabinet; la valeur de couleur de base incorporée dans le  [!DNL vnc] fichier est utilisée à la place.
