---
description: Notes de compatibilité pour les systèmes d’exploitation, les navigateurs et les périphériques mobiles.
seo-description: Notes de compatibilité pour les systèmes d’exploitation, les navigateurs et les périphériques mobiles.
seo-title: Notes de compatibilité
solution: Experience Manager
title: Notes de compatibilité
topic: Dynamic media
uuid: cf732a03-bfaa-4838-862f-73343cefbd67
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Notes de compatibilité{#compatibility-notes}

Notes de compatibilité pour les systèmes d’exploitation, les navigateurs et les périphériques mobiles.

## Blackberry {#section-0c465ac3775d47fd838e2695a00abc45}

* Incompatibilité avec les anciennes visionneuses de vidéos adaptatives. Vous devrez peut-être recharger les visionneuses de vidéos adaptatives pour autoriser la lecture.

## Généraux {#section-7b9a9fcba85148d1802b7b3016b48e02}

* La mise à l’échelle côté navigateur peut rendre l’interface utilisateur et les images floues lorsque l’utilisateur effectue un zoom sur la page. Le formatage de l’interface utilisateur peut également s’afficher incorrectement selon le zoom. Cela sera reporté en plein écran.
* En raison de la taille limitée sur les périphériques mobiles, la visionneuse de supports variés utilise le mouvement des diapositives pour permuter des images dans des visionneuses d’images incorporées au lieu d’appuyer sur le composant de nuances incorporées. Le composant est là comme indicateur visuel.
* Dans les navigateurs Internet Explorer et sur certains périphériques tactiles, le mode plein écran n’occupe pas l’intégralité de l’écran du périphérique. Il redimensionne l’application à la taille de la fenêtre du navigateur.
* Le bouton Fermer ne fonctionne pas sous iOS 8.0 et iOS 8.1, mais sous iOS 8.2.

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Fuite de mémoire visible avec les visionneuses de zoom et de catalogue électronique. Une navigation répétée dans les cadres peut entraîner le blocage du navigateur.
* Si l’utilisateur appuie sur un  sur une visionneuse, il se peut que la page entière fasse l’objet d’un zoom au lieu de la seule visionneuse dont la mise à l’échelle côté navigateur est activée.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Périphérique détecté comme tablette en mode portrait avec le mode Plein écran coché dans les paramètres du navigateur.

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Si l’utilisateur appuie  sur une visionneuse, il se peut que la page entière fasse l’objet d’un zoom au lieu de la seule visionneuse, la mise à l’échelle côté navigateur étant activée.

## Galaxy Nexus 10 et tablette Galaxy {#section-ef52bd1249fe4f358c11838f7a557a00}

* Le catalogue électronique affiche une planche de page incorrecte avec des orientations portrait et paysage.

## Périphériques mobiles HTC {#section-dc42c80414c842e488738fc157c55b01}

* L’impossibilité de désactiver le zoom par pincement natif est une &quot;fonctionnalité&quot; de l’enveloppe HTC UI wrapper (HTC Sense). Cette fonctionnalité peut entraîner un zoom sur toute une page lors de l’utilisation du mouvement &quot;Pincer pour zoomer&quot; sur le lecteur. Utilisez plutôt un mouvement de -pression.
* Les icônes de zone cliquable peuvent se chevaucher si les zones cliquables sont petites et rapprochées.

## HTML5 Video Viewer {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` est uniquement pris en charge avec la lecture HLS du logiciel et HDS Flash. Cela ne fonctionne pas lorsque la lecture utilise le lecteur natif.
* La lecture progressive OGG et WebM n’est pas prise en charge.
* La mise à l’échelle du navigateur peut entraîner l’affichage du lecteur vidéo à une taille incorrecte (inclure les paramètres d’affichage du panneau de configuration Windows OS).
* La recherche de vidéos en flux continu HLS sur Safari peut être incohérente.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Le mode Quirks n’est pas pris en charge.
* Le mode de compatibilité n’est pas pris en charge.
* Internet Explorer sur mobile n’est pas pris en charge.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Les catalogues électroniques volumineux peuvent entraîner le blocage du navigateur sur l’iPad 2.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 ou version ultérieure : Les paramètres du module externe Internet peuvent empêcher la lecture vidéo Flash.
* La recherche de vidéos en flux continu HLS sur Safari peut être incohérente.
* Impossible de rechercher la fin de la vidéo sur Safari 6 à l’aide de la diffusion en flux continu HLS.

