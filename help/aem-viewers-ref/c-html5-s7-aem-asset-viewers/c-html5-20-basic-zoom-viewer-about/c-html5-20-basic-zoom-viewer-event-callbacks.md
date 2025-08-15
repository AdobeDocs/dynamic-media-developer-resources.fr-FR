---
title: Rappels d’événement
description: Rappels d’événement
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 14b317ab-82fb-4f55-babe-72c24e6afc2c
source-git-commit: d5f1f05c36c1cb8a57b5a4bb8a9d066c20e32e75
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

Voir aussi [BasicZoomViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-basiczoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) et [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-b748b29eaafa463a9d1723cb7b86f0d9).
