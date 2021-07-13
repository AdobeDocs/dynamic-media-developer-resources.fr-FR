---
description: Prise en charge des zones réactives et des zones cliquables
solution: Experience Manager
title: Prise en charge des zones réactives et des zones cliquables
feature: Dynamic Media Classic,Visionneuses,SDK/API,Bannières de carrousel
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Prise en charge des zones réactives et des zones cliquables{#hotspot-and-image-maps-support}

La visionneuse prend en charge le rendu des icônes de zone réactive et des zones cliquables au-dessus de la vue principale. L’aspect des icônes et des zones réactives est contrôlé par le biais de CSS, comme décrit dans la section Personnalisation des zones réactives et des zones cliquables .

Voir [Zones réactives et zones cliquables](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Les zones réactives et les régions peuvent activer une fonction d’aperçu rapide sur la page web d’hébergement en déclenchant un rappel JavaScript ou en redirigeant un utilisateur vers une page web externe.

## Zones réactives de l’aperçu rapide {#section-cda48fc9730142d0bb3326bac7df3271}

Ces types de zones réactives ou de zones cliquables doivent être créés à l’aide du type d’action &quot;Aperçu rapide&quot; dans Dynamic Media, d’AEM. Lorsqu’un utilisateur active une zone réactive ou une zone cliquable de ce type, la visionneuse exécute le rappel JavaScript `quickViewActivate` et lui transmet les données de zone réactive ou de zone cliquable. Il est prévu que la page web d’incorporation écoute ce rappel. Lorsqu’il déclenche la page, il ouvre sa propre mise en oeuvre d’aperçu rapide.

## Redirection vers une page web externe {#section-ef820c71251e4215800bb99c0c9ebe16}

Les zones réactives ou cliquables créées pour le type d’action &quot;Aperçu rapide&quot; dans Dynamic Media d’AEM redirige l’utilisateur vers une URL externe. Selon les paramètres définis lors de la création, l’URL s’ouvre dans un nouvel onglet du navigateur, dans la même fenêtre ou dans la fenêtre du navigateur nommé.
