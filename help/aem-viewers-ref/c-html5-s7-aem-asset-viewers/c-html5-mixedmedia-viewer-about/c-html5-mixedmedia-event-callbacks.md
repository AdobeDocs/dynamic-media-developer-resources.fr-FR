---
description: Rappels d’événement
solution: Experience Manager
title: Rappels d’événement
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,User
exl-id: 1a7b51c1-baa7-4ae3-b6b7-17478055a605
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---

# Rappels d’événement{#event-callbacks}

La visionneuse prend en charge les rappels d’événement JavaScript que la page web utilise pour suivre le processus d’initialisation de la visionneuse ou le comportement d’exécution.

Les gestionnaires de rappel sont affectés en transmettant des noms d’événement et les fonctions de gestionnaire correspondantes avec la propriété `handlers` à l’objet JSON `config` dans le constructeur de la visionneuse. Vous pouvez également utiliser la méthode de l’API `setHandlers()`.

Les événements de visionneuse pris en charge sont les suivants :

* `initComplete` : se déclenche lorsque l’initialisation de la visionneuse est terminée et que tous les composants internes sont créés, de sorte qu’il est possible d’utiliser  `getComponent()` l’API. Le gestionnaire de rappel ne prend aucun argument.

* `trackEvent` : se déclenche chaque fois qu’un événement se produit dans la visionneuse et qu’il peut être géré par un système de suivi des événements, tel qu’Adobe Analytics. Le gestionnaire de rappel utilise les arguments suivants :

   * `objID {String}` n’est actuellement pas utilisé.
   * `compClass {String}` n’est actuellement pas utilisé.
   * `instName {String}` nom d’instance du composant SDK de la visionneuse qui a déclenché l’événement.
   * `timeStamp {Number}` horodatage de l’événement.
   * `eventInfo {String}` payload d’événement.

Voir aussi [MixedMediaViewer](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-mixedmediaviewer.md#reference-59b70dd7b58c43059bd85e3295441195) et [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-sethandlers.md#reference-09523cf4f448400b83f7906688368bf3).
