---
description: Notes de compatibilité pour les systèmes d’exploitation, les navigateurs et les périphériques mobiles.
seo-description: Notes de compatibilité pour les systèmes d’exploitation, les navigateurs et les périphériques mobiles.
seo-title: Notes de compatibilité
solution: Experience Manager
title: Notes de compatibilité
uuid: cf732a03-bfaa-4838-862f-73343cefbd67
feature: Dynamic Media Classic, Visionneuses, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 0%

---


# Notes de compatibilité{#compatibility-notes}

<!-- Updated January 13,2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Notes de compatibilité pour les systèmes d’exploitation, les navigateurs et les périphériques mobiles.

## Blackberry {#section-0c465ac3775d47fd838e2695a00abc45}

* Incompatibilité avec les anciennes visionneuses de vidéos adaptatives. Vous devrez peut-être recharger les visionneuses de vidéos adaptatives pour autoriser la lecture.

## Généraux {#section-7b9a9fcba85148d1802b7b3016b48e02}

* La mise à l’échelle côté navigateur peut rendre l’interface utilisateur et les images floues lorsque l’utilisateur effectue un zoom sur la page. La mise en forme de l’interface utilisateur peut également s’afficher incorrectement en fonction du zoom. Cette opération sera reportée en plein écran.
* En raison de la limitation de taille sur les périphériques mobiles, la visionneuse de supports variés utilise le mouvement des diapositives pour permuter des images dans des visionneuses d’images incorporées au lieu d’appuyer sur le composant de nuances incorporées. Le composant est présent en tant qu&#39;indicateur visuel.
* Dans les navigateurs Internet Explorer et certains périphériques tactiles, le mode plein écran n’occupe pas l’ensemble de l’écran du périphérique. Il redimensionne l’application à la taille de la fenêtre du navigateur.
* Le bouton Fermer ne fonctionne pas sous iOS 8.0 et iOS 8.1 mais fonctionne sous iOS 8.2.

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* Fuite de mémoire visible avec les visionneuses de zoom et de catalogue électronique. Une navigation répétée dans les cadres peut provoquer un blocage du navigateur.
* Si l’utilisateur appuie sur un doublon sur une visionneuse, il se peut que la page entière fasse l’objet d’un zoom plutôt que simplement sur la visionneuse avec la mise à l’échelle côté navigateur activée.

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* Périphérique détecté comme tablette en mode portrait avec le mode Plein écran coché dans les paramètres du navigateur.

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* Si l’utilisateur appuie sur un doublon sur une visionneuse, il se peut que la page entière fasse l’objet d’un zoom au lieu de la seule visionneuse, la mise à l’échelle côté navigateur étant activée.

## Galaxy Nexus 10 et Galaxy Tablet {#section-ef52bd1249fe4f358c11838f7a557a00}

* Le catalogue électronique affiche des planches incorrectes avec des orientations portrait et paysage.

## Périphériques mobiles HTC {#section-dc42c80414c842e488738fc157c55b01}

* L&#39;impossibilité de désactiver le zoom par pincement natif est une &quot;fonctionnalité&quot; de HTC UI wrapper (HTC Sense). Cette fonction peut entraîner un zoom sur une page entière lors de l’utilisation du mouvement &quot;pincer pour zoomer&quot; sur la visionneuse. Utilisez plutôt un mouvement doublon-appui.
* Les icônes de zone cliquable peuvent se chevaucher si les zones cliquables sont petites et rapprochées les unes des autres.

## Visionneuse vidéo HTML5 {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` est uniquement pris en charge avec la lecture HLS du logiciel et HDS Flash. Il ne fonctionne pas lorsque la lecture utilise le lecteur natif.
* La lecture progressive OGG et WebM n’est pas prise en charge.
* La mise à l’échelle du navigateur peut entraîner l’affichage d’une taille incorrecte du lecteur vidéo (y compris les paramètres d’affichage du panneau de configuration Windows).
* La recherche de vidéos en flux continu HLS sur Safari peut être incohérente.

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* Le mode Quirks n&#39;est pas pris en charge.
* Le mode de compatibilité n&#39;est pas pris en charge.
* Internet Explorer sur mobile n’est pas pris en charge.

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* Les catalogues électroniques volumineux peuvent entraîner le blocage du navigateur sur l’iPad 2.

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1 ou version ultérieure : Les paramètres du module externe Internet peuvent empêcher la lecture vidéo par Flash.
* La recherche de vidéos en flux continu HLS sur Safari peut être incohérente.
* Impossible de rechercher la fin de la vidéo sur Safari 6 à l’aide de la diffusion en flux continu HLS.
