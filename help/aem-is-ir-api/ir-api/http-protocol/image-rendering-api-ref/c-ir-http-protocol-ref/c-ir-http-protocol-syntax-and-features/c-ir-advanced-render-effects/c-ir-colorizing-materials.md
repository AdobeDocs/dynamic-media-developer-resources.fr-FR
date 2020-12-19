---
description: La plupart des matériaux peuvent être colorés dynamiquement.
seo-description: La plupart des matériaux peuvent être colorés dynamiquement.
seo-title: Coloriser les matériaux
solution: Experience Manager
title: Coloriser les matériaux
topic: Scene7 Image Serving - Image Rendering API
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Colorisation des matériaux{#colorizing-materials}

La plupart des matériaux peuvent être colorés dynamiquement.

L&#39;algorithme de coloration est assez simpliste et fonctionne mieux pour les images de matériaux dont la gamme de teintes est limitée. Pour coloriser un matériau, le rendu soustrait simplement la valeur `bgc=` et ajoute la valeur `color=` à chaque valeur de pixel.

La coloration est désactivée si `color=` n&#39;est pas spécifié. `bgc=` est ignoré par les documents du Cabinet; la valeur de couleur de base incorporée dans le  [!DNL vnc] fichier est utilisée à la place.
