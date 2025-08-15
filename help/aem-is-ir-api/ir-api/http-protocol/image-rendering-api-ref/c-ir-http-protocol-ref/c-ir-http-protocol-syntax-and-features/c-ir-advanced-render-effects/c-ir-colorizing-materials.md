---
title: Matériaux colorants
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

# Matériaux colorants{#colorizing-materials}

La plupart des matériaux peuvent être colorés dynamiquement.

L’algorithme de colorisation est simpliste et fonctionne mieux pour les images matérielles qui ont une plage de teintes limitée. Pour colorer un matériau, le moteur de rendu soustrait simplement la valeur `bgc=` et ajoute la valeur `color=` à chaque valeur en pixels.

La colorisation est désactivée si `color=` n’est pas spécifié. L&#39;attribut `bgc=` est ignoré par les matériaux de l&#39;armoire ; la valeur de couleur de base incorporée dans le fichier [!DNL vnc] est utilisée à la place.
