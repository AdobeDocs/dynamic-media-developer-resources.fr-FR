---
description: Prise en charge des zones réactives
solution: Experience Manager
title: Prise en charge des zones réactives
feature: Dynamic Media Classic,Visionneuses,SDK/API,Images interactives
role: Developer,User
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Prise en charge des zones réactives{#hotspot-support}

La visionneuse prend en charge le rendu des icônes de zone réactive au-dessus de la vue principale. L’aspect des icônes de zone réactive est contrôlé via CSS, comme décrit dans la section Zones réactives .

Voir [Zones réactives](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Les zones réactives peuvent activer une fonction d’aperçu rapide sur la page web d’hébergement en déclenchant un rappel JavaScript ou en redirigeant un utilisateur vers une page web externe.

## Zones réactives de l’aperçu rapide {#section-cda48fc9730142d0bb3326bac7df3271}

Ces types de zones réactives doivent être créés à l’aide du type d’action &quot;Aperçu rapide&quot; dans Dynamic Media, d’AEM Assets - on Demand. Lorsqu’un utilisateur active une telle zone réactive, la visionneuse exécute le rappel JavaScript `quickViewActivate` et lui transmet les données de zone réactive. Il est prévu que la page web d’incorporation écoute ce rappel. Lorsqu’il déclenche la page, il ouvre sa propre mise en oeuvre d’aperçu rapide.

## Redirection vers une page web externe {#section-ef820c71251e4215800bb99c0c9ebe16}

Les zones réactives créées pour le type d’action &quot;Aperçu rapide&quot; dans Dynamic Media d’AEM Assets - sur demande redirige l’utilisateur vers une URL externe. Selon les paramètres définis lors de la création, l’URL s’ouvre dans un nouvel onglet du navigateur, dans la même fenêtre ou dans la fenêtre du navigateur nommé.
