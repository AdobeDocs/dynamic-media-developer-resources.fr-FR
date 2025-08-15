---
title: Notes de compatibilité
description: Notes de compatibilité pour les systèmes d’exploitation, les navigateurs et les appareils mobiles
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7ad499b1-7da6-483b-ab11-cff2eb9271da
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# Notes de compatibilité{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Notes de compatibilité pour les systèmes d’exploitation, les navigateurs et les appareils mobiles

## BlackBerry® {#section-0c465ac3775d47fd838e2695a00abc45}

* Incompatibilité avec les visionneuses de vidéos adaptatives plus anciennes. Chargez à nouveau les visionneuses de vidéos adaptatives pour permettre la lecture.

## Généraux {#section-7b9a9fcba85148d1802b7b3016b48e02}

* La mise à l’échelle côté navigateur rend l’interface utilisateur et les images floues lorsque l’utilisateur effectue un zoom avant sur la page. Le formatage de l’interface utilisateur ne s’affiche pas correctement non plus selon le zoom et est reporté en plein écran.
* En raison de la limitation de la taille sur les appareils mobiles, la visionneuse de médias mixtes utilise des mouvements de diapositive pour permuter les images dans les visionneuses d’images intégrées au lieu d’appuyer sur le composant d’échantillons intégrés. Le composant sert d’indicateur visuel.
* Dans les navigateurs Internet Explorer et certains appareils tactiles, le mode plein écran n’occupe pas l’écran entier de l’appareil. Au lieu de cela, il redimensionne l’application à la taille de la fenêtre du navigateur.
* Le bouton Fermer ne fonctionne pas sous iOS 8.0 et iOS 8.1, mais fonctionne sous iOS 8.2.

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Fuite de mémoire vue avec les visionneuses Zoom et Catalogue électronique. La navigation répétée dans les cadres provoque le blocage du navigateur.
* Lorsque vous appuyez deux fois sur une visionneuse, elle effectue un zoom sur l’ensemble de la page au lieu de la seule visionneuse dont la mise à l’échelle côté navigateur est activée.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Appareil détecté comme tablette en mode portrait avec plein écran activé dans les paramètres du navigateur.

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Lorsque vous appuyez deux fois sur une visionneuse, le zoom de l’ensemble de la page est effectué au lieu de celui de la seule visionneuse, avec la mise à l’échelle côté navigateur activée.

## Galaxy Nexus 10 et Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* Le catalogue électronique affiche une page mal répartie avec des orientations portrait et paysage.

## Appareils mobiles HTC {#section-dc42c80414c842e488738fc157c55b01}

* L’impossibilité de désactiver le pincement-zoom natif est une « fonctionnalité » du wrapper de l’interface utilisateur de HTC (HTC Sense). Cette fonction peut entraîner le zoom d’une page entière lors de l’utilisation d’un mouvement « pincer pour zoomer » sur la visionneuse. Utilisez plutôt un double appui.
* Les icônes des zones cliquables se chevauchent si elles sont petites et proches les unes des autres.

## Visionneuse de vidéos HTML5 {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` modificateur n’est pris en charge qu’avec la lecture logicielle HLS et Flash HDS. Cela ne fonctionne pas lorsque la lecture utilise le lecteur natif.
* Lecture progressive OGG et WebM non prise en charge.
* La mise à l’échelle du navigateur entraîne l’affichage du lecteur vidéo à une taille incorrecte (y compris les paramètres d’affichage du Panneau de Contrôle Windows®).
* Les recherches de vidéos à l’aide de la diffusion en continu HLS sur Safari sont incohérentes.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Le mode Quirks n’est pas pris en charge.
* Mode de compatibilité non pris en charge.
* Internet Explorer sur mobile n’est pas pris en charge.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Les catalogues électroniques volumineux entraînent le blocage du navigateur sur iPad 2.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 ou version ultérieure : les paramètres du plug-in Internet empêchent la lecture de la vidéo Flash.
* Les recherches de vidéos à l’aide de la diffusion en continu HLS sur Safari sont incohérentes.
* Impossible de rechercher la fin de la vidéo sur Safari 6 à l’aide de la diffusion en continu HLS.
