---
description: Prise en charge des zones réactives et des zones cliquables
solution: Experience Manager
title: Prise en charge des zones réactives et des zones cliquables
feature: Dynamic Media Classic, Visionneuses, SDK/API, Bannières de carrousel
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---


# Prise en charge des zones réactives et des zones cliquables{#hotspot-and-image-maps-support}

Le lecteur prend en charge le rendu des icônes de zones réactives et des zones de zone cliquable au-dessus de la vue principale. L’aspect des icônes et des zones réactives est contrôlé par le biais de CSS, comme décrit dans la section Personnaliser les zones réactives et les zones cliquables.

Voir [Zones réactives et zones cliquables](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Les zones réactives et les régions peuvent soit activer une fonction de Vue rapide sur la page Web d’hébergement en déclenchant un rappel JavaScript, soit rediriger un utilisateur vers une page Web externe.

## Zones réactives de Vue rapide {#section-cda48fc9730142d0bb3326bac7df3271}

Ces types de zones réactives ou de zones cliquables doivent être créés à l’aide du type d’action &quot;Vue rapide&quot; dans Dynamic Media, de l’AEM. Lorsqu’un utilisateur active une zone réactive ou une zone cliquable, le lecteur exécute le rappel JavaScript `quickViewActivate` et lui transmet les données de zone réactive ou de zone cliquable. Il est prévu que la page Web incorporée écoute ce rappel. Lorsqu’elle déclenche la page, elle ouvre sa propre mise en oeuvre de Vue rapide.

## Rediriger vers une page Web externe {#section-ef820c71251e4215800bb99c0c9ebe16}

Les zones réactives ou les zones cliquables créées pour le type d’action &quot;Vue rapide&quot; dans Dynamic Media of AEM redirige l’utilisateur vers une URL externe. Selon les paramètres définis lors de la création, l’URL s’ouvre dans un nouvel onglet de navigateur, dans la même fenêtre ou dans la fenêtre de navigateur nommée.
