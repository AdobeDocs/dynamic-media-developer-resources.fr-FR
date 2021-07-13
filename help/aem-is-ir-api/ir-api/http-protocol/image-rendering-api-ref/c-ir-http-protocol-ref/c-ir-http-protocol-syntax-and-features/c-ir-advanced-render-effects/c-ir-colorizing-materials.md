---
description: La plupart des matériaux peuvent être colorés dynamiquement.
solution: Experience Manager
title: Colorisation des matériaux
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# Colorisation des matériaux{#colorizing-materials}

La plupart des matériaux peuvent être colorés dynamiquement.

L&#39;algorithme de colorisation est assez simpliste et fonctionne le mieux pour les images de matériaux qui ont une gamme limitée de nuances. Pour coloriser une matière, le moteur de rendu soustrait simplement la valeur `bgc=` et ajoute la valeur `color=` à chaque valeur de pixel.

La coloration est désactivée si `color=` n’est pas spécifié. `bgc=` est ignoré par les documents du Cabinet; la valeur de couleur de base incorporée dans le  [!DNL vnc] fichier est utilisée à la place.
