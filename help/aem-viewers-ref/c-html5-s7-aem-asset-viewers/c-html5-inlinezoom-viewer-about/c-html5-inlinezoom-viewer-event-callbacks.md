---
title: Rappels d’événement
description: Rappels d’événement
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: c54c54ae-f98f-4cd4-8c36-c7e2a9f3c6df
source-git-commit: f970421ccc482b698343aa18e7dfde7bea4c2a89
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

Voir aussi [FlyoutViewer](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-flyoutviewer.md#reference-b99bb25606444f46b27529ff3e960b1e) et [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-sethandlers.md#reference-74e9acb1cd0047d5bd60eea5fa5c8692).
