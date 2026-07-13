---
title: Opacité de matériau variable
description: L'opacité variable est prise en charge pour la couleur unie et les textures répétables appliquées aux objets qui se chevauchent, ainsi que pour les autocollants et les matériaux de recouvrement de fenêtre.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
TQID: 'https://experienceleague.adobe.com/i4d6vy62vn9BfFrS2W0srO671N9Ad4hCUXR7J4cajJA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 0%

---

# Opacité de matériau variable{#varying-material-opacity}

L&#39;opacité variable est prise en charge pour la couleur unie et les textures répétables appliquées aux objets qui se chevauchent, ainsi que pour les autocollants et les matériaux de recouvrement de fenêtre.

Les informations d’opacité peuvent être fournies simplement en utilisant une image RGB avec une couche alpha. En outre, l’opacité globale peut être modifiée à l’aide de la commande `opacity=` (pour les images RGB et RGBA).

Les bordures de mur prennent également en charge les images RGBA, principalement pour prendre en charge les bordures découpées.

Les fichiers [!DNL vnw] qui définissent les recouvrements de fenêtre peuvent inclure un canal d&#39;opacité. Il est combiné par le moteur de rendu à la couche alpha de la texture répétable et à la valeur `opacity=` pour fournir une gamme complète d&#39;effets d&#39;opacité pour les traitements de fenêtres transparentes et translucides.

