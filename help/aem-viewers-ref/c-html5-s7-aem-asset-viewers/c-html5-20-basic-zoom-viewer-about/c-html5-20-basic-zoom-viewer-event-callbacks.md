---
description: 'null'
seo-description: 'null'
seo-title: Rappels de événement
solution: Experience Manager
title: Rappels de événement
topic: Dynamic media
uuid: 1b9af9e4-463a-4982-9e81-681ebebfd6d7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 1%

---


# Rappels de événement{#event-callbacks}

Le lecteur prend en charge les rappels de événement JavaScript que la page Web utilise pour suivre le processus d’initialisation ou le comportement d’exécution de la visionneuse.

Les gestionnaires de rappel sont affectés en transmettant des noms de événement et des fonctions de gestionnaire correspondantes avec la propriété `handlers` à l’objet JSON `config` dans le constructeur de la visionneuse. Vous pouvez également utiliser la méthode API `setHandlers()`.

Les événements de lecteur pris en charge sont les suivants :

* `initComplete` - se déclenche lorsque l’initialisation de la visionneuse est terminée et que tous les composants internes sont créés, afin qu’il soit possible d’utiliser  `getComponent()` l’API. Le gestionnaire de rappel ne prend aucun argument.

* `trackEvent` - se déclenche chaque fois qu’un événement se produit dans la visionneuse et peut être géré par un système de suivi de événement, tel que Adobe Analytics. Le gestionnaire de rappel prend les arguments suivants :

   * `objID {String}` n’est pas actuellement utilisé.
   * `compClass {String}` n’est pas actuellement utilisé.
   * `instName {String}` nom d’instance du composant SDK de visionneuse qui a déclenché le événement.
   * `timeStamp {Number}` Horodatage événement.
   * `eventInfo {String}` Charge utile du événement.

Voir aussi [BasicZoomViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-basiczoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) et [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-b748b29eaafa463a9d1723cb7b86f0d9).
