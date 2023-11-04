---
title: Remarques sur la compatibilité
description: Notes de compatibilité pour les systèmes d’exploitation, les navigateurs et les appareils mobiles.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7ad499b1-7da6-483b-ab11-cff2eb9271da
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Remarques sur la compatibilité{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Notes de compatibilité pour les systèmes d’exploitation, les navigateurs et les appareils mobiles.

## BlackBerry® {#section-0c465ac3775d47fd838e2695a00abc45}

* Incompatibilité avec les visionneuses de vidéos adaptatives plus anciennes. Chargez à nouveau des visionneuses de vidéos adaptatives pour permettre la lecture.

## Généraux {#section-7b9a9fcba85148d1802b7b3016b48e02}

* La mise à l’échelle côté navigateur rend l’interface utilisateur et les images floues lorsque l’utilisateur effectue un zoom sur la page. La mise en forme de l’interface utilisateur s’affiche également de manière incorrecte en fonction du zoom et s’affiche en mode plein écran.
* En raison de la taille limitée sur les appareils mobiles, la visionneuse de supports variés utilise le mouvement des diapositives pour permuter des images dans des visionneuses d’images incorporées au lieu d’appuyer sur le composant d’échantillons incorporés. Le composant est présent en tant qu’indicateur visuel.
* Dans les navigateurs Internet Explorer et certains périphériques tactiles, le mode plein écran n’occupe pas tout l’écran du périphérique. Il redimensionne l’application à la taille de la fenêtre du navigateur.
* Le bouton Fermer ne fonctionne pas sous iOS 8.0 et iOS 8.1, mais fonctionne sous iOS 8.2.

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Fuite de mémoire observée avec les visionneuses Zoom et eCatalog. La navigation répétée dans les images provoque le blocage du navigateur.
* Si vous appuyez deux fois sur une visionneuse, la page entière est agrandie au lieu de la visionneuse uniquement avec la mise à l’échelle côté navigateur activée.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Appareil détecté comme tablette en mode portrait avec le mode Plein écran vérifié dans les paramètres du navigateur.

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Si vous appuyez deux fois sur une visionneuse, la page entière est agrandie au lieu de la visionneuse uniquement, avec la mise à l’échelle côté navigateur activée.

## Galaxy Nexus 10 et tablette Galaxy {#section-ef52bd1249fe4f358c11838f7a557a00}

* Le catalogue électronique affiche des pages incorrectes avec des orientations portrait et paysage.

## Périphériques mobiles HTC {#section-dc42c80414c842e488738fc157c55b01}

* L’impossibilité de désactiver le zoom par pincement natif est une &quot;fonctionnalité&quot; du wrapper HTC UI (HTC Sense). Cette fonction peut entraîner un zoom sur une page entière lors de l’utilisation du mouvement &quot;Pincer pour zoomer&quot; sur la visionneuse. Utilisez plutôt un double-appui.
* Les icônes de zone cliquable se chevauchent si les zones cliquables sont petites et rapprochées.

## Visionneuse vidéo HTML5 {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` est uniquement pris en charge avec la lecture HLS du logiciel et HDS par Flash. Cela ne fonctionne pas lorsque la lecture utilise le lecteur natif.
* Lecture progressive OGG et WebM non prise en charge.
* La mise à l’échelle du navigateur entraîne l’affichage du lecteur vidéo à une taille incorrecte (inclut les paramètres d’affichage de Panneau de Contrôle Windows®).
* La recherche de vidéos à l’aide de la diffusion HLS en continu sur Safari est incohérente.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Le mode Quirks n’est pas pris en charge.
* Le mode de compatibilité n’est pas pris en charge.
* Internet Explorer sur mobile n’est pas pris en charge.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Les catalogues électroniques volumineux entraînent le blocage du navigateur sur iPad 2.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 ou version ultérieure : les paramètres du module externe Internet empêchent la lecture vidéo par Flash.
* La recherche de vidéos à l’aide de la diffusion HLS en continu sur Safari est incohérente.
* Impossible de rechercher la fin de la vidéo sur Safari 6 à l’aide de la diffusion HLS en continu.
