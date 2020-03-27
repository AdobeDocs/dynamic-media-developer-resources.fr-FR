---
description: 'null'
seo-description: 'null'
seo-title: Prise en charge des zones réactives et des zones cliquables
solution: Experience Manager
title: Prise en charge des zones réactives et des zones cliquables
topic: Dynamic media
uuid: 839b6a7f-4f6f-43ad-8eb8-254959c7fbac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Prise en charge des zones réactives et des zones cliquables{#hotspot-and-image-maps-support}

Le lecteur prend en charge le rendu des icônes des zones réactives et des zones de zone cliquable par-dessus le  principal du. L’aspect des icônes et des zones réactives est contrôlé via CSS, comme décrit dans la section Personnaliser les zones réactives et les zones cliquables.

Voir [Zones réactives et zones cliquables](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Les zones réactives et les régions peuvent soit activer une fonction de  rapide sur la page Web d’hébergement en déclenchant un rappel JavaScript, soit rediriger un utilisateur vers une page Web externe.

##  rapides des zones réactives {#section-cda48fc9730142d0bb3326bac7df3271}

Ces types de zones réactives ou de zones cliquables doivent être créés à l’aide du type d’action &quot; rapide&quot; dans Contenu multimédia dynamique d’AEM. Lorsqu’un utilisateur active une zone réactive ou une zone cliquable de ce type, le lecteur exécute le rappel `quickViewActivate` JavaScript et lui transmet les données de zone réactive ou de zone cliquable. Il est prévu que la page Web d’incorporation écoute ce rappel. Lorsqu’il déclenche la page, il ouvre sa propre mise en oeuvre de  rapide.

## Redirection vers une page Web externe {#section-ef820c71251e4215800bb99c0c9ebe16}

Les zones réactives ou les zones cliquables créées pour le type d’action &quot; rapide&quot; dans Contenu multimédia dynamique d’AEM redirigent l’utilisateur vers une URL externe. Selon les paramètres définis lors de la création, l’URL s’ouvre dans un nouvel onglet du navigateur, dans la même fenêtre ou dans la fenêtre du navigateur nommé.
