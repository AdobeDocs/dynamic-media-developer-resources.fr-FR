---
title: Prise en charge des zones réactives
description: Prise en charge des zones réactives
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# Prise en charge des zones réactives{#hotspot-support}

La visionneuse prend en charge le rendu des icônes de zone réactive au-dessus de la vue principale. L’aspect des icônes de zone réactive est contrôlé via CSS, comme décrit dans la section Zones réactives .

Voir [Zones réactives](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Les zones réactives peuvent activer une fonction d’aperçu rapide sur la page web d’hébergement en déclenchant un rappel JavaScript ou en redirigeant un utilisateur vers une page web externe.

## Zones réactives d’aperçu rapide {#section-cda48fc9730142d0bb3326bac7df3271}

Ces types de zones réactives doivent être créés à l’aide du type d’action &quot;Aperçu rapide&quot; dans Dynamic Media, dans Adobe Experience Manager Assets - On-demand. Lorsqu’un utilisateur active une telle zone réactive, la visionneuse exécute le rappel JavaScript `quickViewActivate` et lui transmet les données de zone réactive. Il est prévu que la page web d’incorporation écoute ce rappel. Lorsqu’il déclenche la page, il ouvre sa propre mise en oeuvre d’aperçu rapide.

## Redirection vers une page web externe {#section-ef820c71251e4215800bb99c0c9ebe16}

Zones réactives créées pour le type d’action &quot;Aperçu rapide&quot; dans Dynamic Media of Experience Manager Assets : l’utilisateur est redirigé vers une URL externe. Selon les paramètres définis lors de la création, l’URL s’ouvre dans un nouvel onglet du navigateur, dans la même fenêtre ou dans la fenêtre du navigateur nommé.
