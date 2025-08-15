---
title: Rappels d’événement
description: Rappels d’événement
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2493208b-9030-49fa-b1fd-2f2bd524bce6
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# Rappels d’événement{#event-callbacks}

La visionneuse prend en charge JavaScript rappels d’événement que la page Web utilise pour suivre le processus d’initialisation de la visionneuse ou le comportement d’exécution.

Les gestionnaires de rappel sont affectés en transmettant les noms d’événement et les fonctions de gestionnaire correspondantes avec la propriété à `handlers` l’objet `config` JSON dans le constructeur de la visionneuse. Il est également possible d’utiliser `setHandlers()` la méthode API.

Les événements de visionneuse pris en charge sont les suivants :

* `initComplete` - se déclenche lorsque l’initialisation de la visionneuse est terminée et que tous les composants internes sont créés, de sorte qu’il est possible d’utiliser `getComponent()` l’API. Le gestionnaire de rappel n’accepte aucun argument.

* `trackEvent` - se déclenche chaque fois qu’un événement se produit à l’intérieur de la visionneuse et peut être géré par un système de suivi d’événement, tel que Adobe Analytics. Le gestionnaire de rappel accepte les arguments suivants :

   * `objID {String}` Non utilisée actuellement.
   * `compClass {String}` Non utilisée actuellement.
   * `instName {String}` Nom d’occurrence du composant SDK de visionneuse qui a déclenché l’événement.
   * `timeStamp {Number}` Horodatage de l’événement.
   * `eventInfo {String}` Charge utile de l’événement.

Voir aussi [VideoViewer](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-videoviewer.md#reference-bfad5aa071c74a66a23c39a9b48dedb0) et [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-sethandlers.md#reference-22b373b37e8943a7be5c4d4cc21ed926).
