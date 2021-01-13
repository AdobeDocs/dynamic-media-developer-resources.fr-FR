---
description: Prise en charge des zones réactives
solution: Experience Manager
title: Prise en charge des zones réactives
topic: Dynamic media
uuid: 62e0e55a-55a3-417d-ad51-ec77a7c16ac3
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---


# Prise en charge des zones réactives{#hotspot-support}

Le lecteur prend en charge le rendu des icônes de zones réactives au-dessus de la vue principale. L’aspect des icônes de zones réactives est contrôlé via CSS, comme décrit dans la section Zones réactives.

Voir [Zones sensibles](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Les zones réactives peuvent activer une fonction de Vue rapide sur la page Web d’hébergement en déclenchant un rappel JavaScript ou en redirigeant un utilisateur vers une page Web externe.

## Zones réactives de Vue rapide {#section-cda48fc9730142d0bb3326bac7df3271}

Ces types de zones réactives doivent être créés à l’aide du type d’action &quot;Vue rapide&quot; dans Dynamic Media, de AEM Assets - sur demande. Lorsqu’un utilisateur active une telle zone réactive, le lecteur exécute le rappel JavaScript `quickViewActivate` et lui transmet les données de la zone réactive. Il est prévu que la page Web incorporée écoute ce rappel. Lorsqu’elle déclenche la page, elle ouvre sa propre mise en oeuvre de Vue rapide.

## Rediriger vers une page Web externe {#section-ef820c71251e4215800bb99c0c9ebe16}

Les zones réactives créées pour le type d’action &quot;Vue rapide&quot; dans Dynamic Media of AEM Assets - à la demande redirigent l’utilisateur vers une URL externe. Selon les paramètres définis lors de la création, l’URL s’ouvre dans un nouvel onglet de navigateur, dans la même fenêtre ou dans la fenêtre de navigateur nommée.
