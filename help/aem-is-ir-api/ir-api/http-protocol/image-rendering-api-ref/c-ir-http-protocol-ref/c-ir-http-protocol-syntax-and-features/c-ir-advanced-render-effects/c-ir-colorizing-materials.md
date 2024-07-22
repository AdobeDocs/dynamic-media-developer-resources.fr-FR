---
title: Colorisation des matériaux
description: La plupart des matériaux peuvent être colorés dynamiquement.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# Colorisation des matériaux{#colorizing-materials}

La plupart des matériaux peuvent être colorés dynamiquement.

L&#39;algorithme de colorisation est simpliste et fonctionne le mieux pour les images de matériaux dont la gamme de nuances est limitée. Pour colorer un matériau, le moteur de rendu soustrait simplement la valeur `bgc=` et ajoute la valeur `color=` à chaque valeur de pixel.

La coloration est désactivée si `color=` n’est pas spécifié. L’attribut `bgc=` est ignoré par les matériaux de l’armoire ; la valeur de couleur de base incorporée dans le fichier [!DNL vnc] est utilisée à la place.
