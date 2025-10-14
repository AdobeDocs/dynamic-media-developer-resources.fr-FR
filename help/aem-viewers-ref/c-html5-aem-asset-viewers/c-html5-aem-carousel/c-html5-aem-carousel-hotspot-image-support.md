---
title: Prise en charge des zones réactives et cliquables
description: Prise en charge des zones réactives et cliquables
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: 8d5dbc2d2b5e228f8496fd71633bf1cb96218226
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Prise en charge des zones réactives et cliquables{#hotspot-and-image-maps-support}

La visionneuse prend en charge le rendu des icônes de zone réactive et des zones cliquables en haut de la vue principale. L’aspect des icônes et des zones réactives est contrôlé par CSS, comme décrit dans la section Personnaliser les zones réactives et cliquables .

Voir [&#x200B; Zone réactive et Zone cliquable](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Les zones réactives et les régions peuvent activer une fonctionnalité d’aperçu rapide sur la page web d’hébergement en déclenchant un rappel JavaScript ou en redirigeant un utilisateur vers une page web externe.

## Zones réactives d’aperçu rapide {#section-cda48fc9730142d0bb3326bac7df3271}

Ces types de zones réactives ou cliquables doivent être créés à l’aide du type d’action « Aperçu rapide » dans Dynamic Media de Adobe Experience Manager. Lorsqu’un utilisateur active une zone réactive ou une zone cliquable, la visionneuse exécute le rappel JavaScript `quickViewActivate` et lui transmet les données de la zone réactive ou de la zone cliquable. Il est prévu que la page web d’incorporation écoute ce rappel. Lorsqu’il déclenche la page, il ouvre sa propre mise en œuvre d’aperçu rapide.

## Rediriger vers une page web externe {#section-ef820c71251e4215800bb99c0c9ebe16}

Les zones réactives ou cliquables créées pour le type d’action « Aperçu rapide » dans Dynamic Media d’Experience Manager redirigent l’utilisateur vers une URL externe. Selon les paramètres définis lors de la création, l’URL s’ouvre dans un nouvel onglet du navigateur, dans la même fenêtre ou dans la fenêtre du navigateur nommé.
