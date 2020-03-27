---
description: 'null'
seo-description: 'null'
seo-title: Prise en charge des zones réactives
solution: Experience Manager
title: Prise en charge des zones réactives
topic: Dynamic media
uuid: 62e0e55a-55a3-417d-ad51-ec77a7c16ac3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Prise en charge des zones réactives{#hotspot-support}

Le lecteur prend en charge le rendu des icônes des zones réactives au-dessus du principal. L’aspect des icônes des zones réactives est contrôlé via CSS, comme décrit dans la section Zones réactives.

Voir [Zones réactives](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Les zones réactives peuvent soit activer une fonction de  rapide sur la page Web d’hébergement en déclenchant un rappel JavaScript, soit rediriger un utilisateur vers une page Web externe.

##  rapides des zones réactives {#section-cda48fc9730142d0bb3326bac7df3271}

Ces types de zones réactives doivent être créés à l’aide du type d’action &quot; rapide&quot; dans Contenu multimédia dynamique, dans Ressources AEM - à la demande. Lorsqu’un utilisateur active une telle zone réactive, le lecteur exécute le rappel `quickViewActivate` JavaScript et lui transmet les données de cette zone réactive. Il est prévu que la page Web d’incorporation écoute ce rappel. Lorsqu’il déclenche la page, il ouvre sa propre mise en oeuvre de  rapide.

## Redirection vers une page Web externe {#section-ef820c71251e4215800bb99c0c9ebe16}

Les zones réactives créées pour le type d’action &quot; rapide&quot; dans Contenu multimédia dynamique des ressources AEM - à la demande redirige l’utilisateur vers une URL externe. Selon les paramètres définis lors de la création, l’URL s’ouvre dans un nouvel onglet du navigateur, dans la même fenêtre ou dans la fenêtre du navigateur nommé.
